## <a href="#_basic_editing" class="link">Chapter 6. Basic Editing</a>

Armed with the navigation keybindings you’ve already learned and the ability to enter and leave Insert mode at will, your Vim editing experience is getting pretty close to on par with what you might be used to in non-modal editors.

However, moving around and inserting text is a very small part of the life of a software developer. More often, you need to *edit* text. Deleting code, changing code, refactoring code, moving code around. It’s the majority of what we do.

Yes, you can do all of these things by navigating to where you want to, and entering Insert mode. The delete and backspace keys do the same thing in Insert mode that they do in other editors. But there are far more efficient tools available.

The best part is that you already know most of what you need to take advantage of very powerful editing commands!

### <a href="#_the_vim_command_mental_model" class="link">6.1. The Vim Command Mental Model</a>

The navigation commands such as `s` and `f` and `hjkl` and `web` that you already know are collectively known as *motion* commands. They move the cursor from its current location to a new location.

Most motion commands can be prefixed with a count, so the navigation model is always `<count><motion>`. A count usually repeats the motion a certain number of times, although some commands such as `Shift-G` for “Go to line” will use the count as an absolute value instead. If the count is blank, the “default” count is typically `1`. Even a Seek command which uses labels is allowed to be prefixed with a count…​ although the count will be ignored!

The `<count><motion>` commands are great for navigation, which is all we’ve used them for so far, but they can also be combined with a *verb* to do something to the text between the cursor and the location the motion would move you to.

Verbs come first, so the structure is always `<verb><count><motion>`. Navigation is the “default” verb, so if you leave the verb blank (i.e. skip it), your cursor moves to the location indicated by the motion. We’ll discuss various important verbs in this chapter.

But the model keeps growing! It turns out, verbs can *also* be counted. The syntax becomes `<count><verb><count><motion>`. I have never in my life used all four of those in one command, however. Typically you would either do `<count><verb><motion>` **or** `<verb><count><motion>`.

This model is nice because it allows you to divide and conquer your learning strategy, and reuse knowledge as you study. First you learned motion commands. Then you learned counts. Now you will learn verbs. If you learn new motion commands or new verbs in the future, you can mix them with all the verbs and motions you already know and they should behave in a predictable way.

<table>
<tbody>
<tr>
<td class="icon"></td>
<td class="content">Various plugins try to mimic this strategy to help keep your learning model small. In fact, my main complaint with the explorer is that it doesn’t operate with the <code>&lt;verb&gt;&lt;motion&gt;</code> mental model, while mini.files does. Similarly, some folks argue that Seek mode violates the Vim mental model because counts don’t make sense with it. My opinion is that Seek mode simply transcends counts, but it still combines cleanly with verbs so it is a valid Vim model.</td>
</tr>
</tbody>
</table>

#### <a href="#_a_note_on_insert_mode" class="link">6.1.1. A Note on Insert Mode</a>

Like all models, this one is not perfect. For example, you can use counts with the `i`, `I`, `a`, and `A` commands, but it’s clear that “enter Insert mode” is neither a motion nor a verb.

For example, if you type `5ifoo<Escape>`, Neovim will insert `foofoofoofoofoo` for you. That may not seem very useful, but if you ever want an 80 character `*` ruler to underline a heading, `80i*<Escape>` is pretty nifty!

But the `<count>i` “not-motion” commands *cannot* be combined with verbs like the navigation commands you’ve learned. So it’s important to know the limits of the model. In fact, as we’ll see later, Vim uses this effect to its advantage, borrowing the `a`, `i`, and `o` keys to create object motions when combined with a verb.

So now that you understand how the motions you already know can combine with verbs to perform actions other than navigation, you just need to learn some verbs.

### <a href="#_deleting_text" class="link">6.2. Deleting Text</a>

I’ve previewed this a couple times already, and even if I hadn’t, you can probably guess that the verb for deleting text is `d`.

So where `<motion>` will take you to a specific location in the code, `d<motion>` will delete all the text between the cursor and that location. Here are some examples:

- `dh` to delete the character to the left of the cursor.

- `d3w` to delete three words.

- `3dw` to delete one word, three separate times.

- `d^` to delete from the cursor to the beginning of the line.

- `d2fe` to delete all text between the cursor location and the second `e` after the cursor, including that second `e`.

- `d2Ta` to delete all text between the cursor and the second `a` *behind* the cursor, *not* including that second `a`.

- `dsfoos` to delete text between the current cursor position and the label `s` that pops up when you use Seek mode to seek to `foo`. Note that Seek mode **always** jumps to the beginning of the word you searched for. This means that if the `foo` you jump to is *after* the current cursor location, the `oo` will not be deleted, but the `f` will. But if the `foo` you jump to is *before* the current cursor location, all three letters of `foo` will be deleted.

If any of those are surprising, ignore the `d` and refer back to chapter 3 to refresh your memory of the motions.

So `d` will work with all the motion commands you know, as well as all the motion commands you don’t know yet, **and** all the motion commands that are defined by plugins you haven’t yet installed.

When the delete command is completed, Neovim will still be in Normal mode, and you can immediately perform any other `<verb><motion>` combination.

### <a href="#_changing_text" class="link">6.3. Changing Text</a>

Sometimes you just want to delete text, but another common task is editing text. Replace a word with another word, change spelling, delete the rest of the paragraph and replace it with something new, etc.

This *could* easily be handled by combining the delete verb with Insert mode (e.g. `dwi` will delete a word and enter Insert mode.) However, you can save a keystroke by using the `c` verb, which means “**c**hange”. If you replace the `d` in each of the examples I outlined above with a `c`, you will effectively get “delete the text and immediately enter Insert mode.”

### <a href="#_operating_to_end_of_the_current_line" class="link">6.4. Operating to End of the Current Line</a>

It is very common to want to delete or change from the cursor position to the end of the current line, leaving the beginning of the line intact. These actions happen more often than you would expect in source code editing, so there is a shortcut for them.

Yes you *could* `d$` and `c$` to delete or change to the end of the line, since `$` is the “jump to end of line” motion. That is the “correct” format for the mental model. However, because this is such a common operation, you can “cheat” with one fewer keystrokes and just use the capitalized `D` or `C` instead.

<table>
<tbody>
<tr>
<td class="icon"></td>
<td class="content">There is no inverse shortcut verb for “delete to the beginning of the line”, so you’ll have to use <code>d^</code> or <code>d0</code> instead, where <code>^</code> is the motion to jump to the first non-blank character and <code>0</code> is the motion to jump to the first column regardless of whether it is blank.</td>
</tr>
</tbody>
</table>

### <a href="#_operating_on_entire_lines" class="link">6.5. Operating on Entire Lines</a>

Another common action is to change or delete an *entire* line of text. So much so, in fact, that there are special motions for “the whole line”. These motions are accessed by duplicating the verb. This is another place where the mental model kind of breaks down; the interpretation of the motion *depends* on the verb.

In practice, this just means that `dd` deletes an entire line and `cc` deletes it and enters Insert mode. These are nice and easy to type, so it makes for a nice shorthand.

You can combine these bespoke motions with counts. `d3d` will delete three lines, and `3dd` will delete one line three times (which is faster to type because you don’t have to move your finger off of `d` to hit it twice). Yes, that has the same outcome either way, but the model is such that you can use either of them. Note that there are situations where the two formats may have subtly different behaviours, although in practice I have never encountered surprises.

### <a href="#_some_shortcuts_for_modifying_individual_characters" class="link">6.6. Some Shortcuts for Modifying Individual Characters</a>

Another common operation is to perform a delete or change operation on a single character or specific number of characters. You could do this using `dl` to delete the character under the cursor or `4dl` to delete that character and the three characters that come after it. However, because you do this so often, there is a shorthand verb that doesn’t have a motion (or rather, the motion is implied): `x`. For example, you can use `x` to delete an extraneous `u` in words like “behaviour” if you prefer American spelling. The single letter will be deleted, and you’ll be back in Normal mode ready to proceed.

The `x` command can be used with a count, so if you want to delete five characters starting with the one under the cursor, just use `5x`.

If you need to go the other direction and delete characters *before* the cursor, use a capital `X`. This, too, can have a count, and it will basically delete that many characters to the left. I rarely use this, since the shift brings us up to two keystrokes anyway, and `hx` or `d4h` is no harder.

If, instead of deleting, you need to replace a character with a different character, use the `r` command. This command will briefly enter Insert mode while you type one character, then immediately return to Normal mode. Much fewer keystrokes for a common operation (spelling errors are common, right? It’s not just me?) than something like `cle<Escape>`. Using `r` with a count is possible, but the behaviour is kind of unhelpful: it will replace the character under the cursor and the `<count>` number of characters after that character with the same letter. The only example I can imagine this being remotely useful is when you copy-paste a password prompt from somewhere and need to replace all the characters in the password with `*`.

One shortcut I do use frequently can delete the newline at the end of the current line. Use the `J` (“**J**oin Lines”) command from anywhere in the line. I use this one a lot. If you need to merge multiple consecutive lines together, `J` takes a count. It generally does the right thing around whitespace (replacing indentation with a single space), but if you need to do a join without modifying whitespace, use the two-character verb `gJ`.

### <a href="#_manipulating_case" class="link">6.7. Manipulating Case</a>

If you need to convert a character or sequence of characters to uppercase, use the verb `gU` (that’s a shifted `U` for the second character) followed by any standard navigation motion. I find this particular verb frustrating because `g` is normally assigned to the `Go To` motions. In this case, (as with `gJ` above) it is a verb instead.

I guess you can think of it as “Go To and Convert to Uppercase” where `U` is short for `Uppercase`.

The inverse function to convert all text between the current cursor position and the motion destination is to use a lowercase `gu` before the motion. Kind of weird to remember, but it does match the common Vim idiom of `gu` means an action and `gU` means the same action BUT BIGGER.

I don’t find these commands very useful. I more frequently use the `~` command, which inverts the case of the character under the cursor.

The duplicate commands `gUU` and `guu` do the same thing as other duplicate verbs, applying the upper/lower case operation to the entire line.

<table>
<tbody>
<tr>
<td class="icon"></td>
<td class="content">If you find yourself doing a lot of case switching work, see Chapter 13 for a discussion of the <code>text-case</code> plugin.</td>
</tr>
</tbody>
</table>

### <a href="#_repeating_commands" class="link">6.8. Repeating Commands</a>

LazyVim doesn’t have a multiple cursor mode. There *are* plugins to support multiple cursors, but in my experience they don’t work very well. The Neovim developers have multiple cursors on their roadmap, so I am hoping they will come up with a paradigm that integrates nicely with the Vim mental model.

In the meantime, Neovim provides several different tools for performing an action in multiple places in your code. We’ll cover basic repetitions here, and other useful techniques in later chapters.

Once you have performed any verb, you can navigate to another place in the document and repeat that verb with a single keypress: `.` (That’s a period, although you will usually hear it referred to as “dot repeat” in this context).

This highlights why `d` and `c` need to be separate verbs, as opposed to using something like `d<motion>i`. When you use `c`, the delete motion **and** the text you inserted is remembered, so you can repeat the entire change with a `.` command. For example, if you want to replace all instances of a variable named `i` with a much better name of `index`, you could jump to the first instance of `i` and type `clindex<Escape>` to “change one character to index”. Then you can use navigation commands to go to the next use of `i`. Now just type `.` to repeat the change. Then continue to the next instance.

Like motions and verbs, the `.` command can be given a count. However, counts with `.` are a little bit nuanced. Rather than blindly repeating the command `<count>` number of times, it will instead *replace* the count of the command being repeated.

This means that if you use the verb `3dd` to delete three lines, and the next operation you perform is `2.` (“2 dot”), the second operation will delete *two* lines, rather than six.

### <a href="#_recording_commands" class="link">6.9. Recording Commands</a>

Vim’s command recording and playback system is extremely powerful. You can trivially record an arbitrary sequence of navigation, editing, and insertion commands, then repeat that sequence on demand at any location.

To start a recording, press `qq`. Sorry, but I have no mnemonic to remember `q`. I have a feeling it was just the last available key on the keyboard!

After that, type whatever sequence of navigation, editing, and insertion commands you want to record. Delete words, insert text, change text, search for words (don’t use Seek mode, as the replay mechanism will have no idea what label to jump to). Virtually anything you can do in Vim (even `:` commands) can be recorded and replayed later.

When you are finished recording, just press `q` again. The recording will be stored ready for replay whenever you desire.

#### <a href="#_appending_to_a_recording" class="link">6.9.1. Appending to a Recording</a>

If you partially complete your recording and then realize you need some more information or need to make an edit before completing the recording, you can pause the recording using `q` as usual and do the thing you need to do.

When you are ready to continue recording, use `qQ` to record in *append* mode instead. The main tip here is that you need to make sure your cursor is in a location such that the merged recording will make sense. This usually means the same place it was when you stopped recording, although it may depend on what changes you made in the meantime.

#### <a href="#_playing_back_a_recording" class="link">6.9.2. Playing Back a Recording</a>

The easiest and fastest way to play back your most recently saved recording is with a capital `Q`.

<table>
<tbody>
<tr>
<td class="icon"></td>
<td class="content">It is possible to store and replace multiple recordings at once using <em>registers</em> (a stupid name for a storage location that harkens back to humanity’s dark days of assembly programming). We will go into more detail about registers in chapter 8.</td>
</tr>
</tbody>
</table>

### <a href="#_undo_and_redo" class="link">6.10. Undo and Redo</a>

Obviously, these are the most important operations in the whole book! Use the `u` key to undo your most recent change. Note that “most recent change” can be a pretty big whack of text, especially if you haven’t exited Insert mode for a while. For example, I wrote this entire paragraph in one Insert session. If I press `u` the entire paragraph will be lost.

That’s ok, though, because I can redo using `Control-r`. Like most developers, I use both of these extensively. (Did you know that in the old days of typewriters, secretaries had to get 100% accuracy scores on their typing tests? There was no backspace or delete key, you see).

Neovim actually does an amazing job of keeping track of your entire history, rather than just the most recent suite of changes. So if you make a bunch of changes to get to state B, then undo to state A, and then make a bunch more changes to get to state C, it is still possible to get back to state B (ie: back out of the C changes to state A and go back up the B changes to state B).

It’s kind of the same concept as git branches, except your history is *automatically* tracked for every keystroke you make. Working with branches of undo history using raw Neovim commands can feel pretty clumsy, though (read through `:help undo-branches` if you’re brave). Instead I recommend configuring and installing the [undotree](https://github.com/jiaoshijie/undotree) plugin.

About 99.9% of the time, `u` and `Control-r` will be all you need, but that remaining 0.1% can make `undotree` a godsend when you need it.

### <a href="#_summary_6" class="link">6.11. Summary</a>

In this chapter, we expanded our understanding of the Vim mental model, and then introduced several verbs that can be combined with the navigation motions we were already familiar with.

We discussed an assortment of other editing commands before covering how to repeat motions using `.` and command recordings. Finally, we covered undo and redo.

In the next chapter, we’ll learn about text objects and some additional nuances of the Vim mental model with operator-pending mode. Combined, these allow us to very quickly perform actions on a huge variety of code constructs.
