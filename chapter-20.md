## Chapter 20. Where to go Next

We're wrapping up our LazyVim journey together, but if you've made it this far, I'm sure you'll continue to forge new paths with this excellent Neovim distro. This final chapter summarizes some of my favourite places to go for more help, deeper insights, news, and plugins.

### 20.1. Reread This Book

You've definitely forgotten some interesting tidbits that I've covered in this book. I know this because in rereading it myself during each of several editorial passes I have learned things. One of the reasons I love writing is that it forces me to cover topics in far greater detail than I otherwise would.

So I recommend rereading this book, or at least skimming through it. Write out a cheat sheet of every keybinding that fits in the "That's really cool but I don't think I'll memorize it" box. I recommend handwriting it; it'll stick in your memory longer and you can keep annotating it on your desk as you learn new things.

If you are reading a print or E-book copy, it will, sadly, become outdated. For the latest version, have a look at my official website at https://lazyvim-ambitious-devs.phillips.codes, and subscribe to my mailing list if you want to hear about updates.

### 20.2. The Neovim Documentation

Vim was created in 1991 when not everyone had access to the Internet. Back then it was common to ship documentation with software instead of linking to it on the world-wide web (indeed, the web was created the same year). Given that you had the stamina to read this entire book, you might just want to type `:help user-manual<Enter>` and read from beginning to end. Possibly more than once throughout your Vim career. (`:help<Enter>` will give access to even more documentation).

The key to navigating the help files is the keybinding `Control-]`. The documentation is interlinked like a wiki and if you place your cursor over any of the bold text and hit `Control-]`, you'll jump to that section, much like clicking a link.

If you prefer reading documentation in a web browser, the user manual is rendered to html at https://neovim.io/doc/user/usr_toc.html. It's the same content as `:help`, just more clicky.

The manual is extremely comprehensive and covers a lot of commands and keybindings that maybe aren't as relevant as they once were. I believe I've covered everything that is relevant to a modern developer, but I'm sure you'll find additional nuggets of wisdom in there.

### 20.3. The LazyVim Documentation

LazyVim has its own website at https://www.lazyvim.org. It is a little sparse on hand-holding (which is why this book exists), but it is a super valuable resource once you know how to use it. Most importantly, it comprehensively lists the current configuration for every plugin and extra that ships with the distro. You **will** be visiting these from time to time when you want to tweak the configuration to better match your usage. Every plugin is listed with an `Options` and a `Full Spec` tab. The `Options` represent whatever LazyVim passes as `opts` for that plugin spec, while `Full Spec` includes the entire configuration.

### 20.4. LazyVim Discussion Groups

The quickest way to get answers to questions (at least, those questions that can't be accurately answered by AI) is to ask them in the [discussion groups on GitHub](http:///github.com/LazyVim/LazyVim/discussions). I am somewhat active there, but your question will probably be answered by someone far more knowledgeable than me.

If you have found an issue with LazyVim, the first step is to create a minimal repro with as few plugins as possible. The LazyVim issue tracker contains a template for a `repro.lua` that you can use to configure the minimal repro. Add the relevant plugins and run it with `nvim -u repro.lua` to test the issue. Upload this with your issue (or to the Discussion groups) to make it easy for the maintainers to help you.

### 20.5. Finding Interesting Plugins

For the most part, LazyVim contains the best-in-class version of most plugins you'll need. However, if there is a feature you think the editor should have and it isn't available as an extra, you can almost certainly find it in the [Awesome Neovim](https://github.com/rockerBOO/awesome-neovim) repo on Github.

Another terrific resource is the [neovimcraft](https://neovimcraft.com) website. Incidentally, the maintainers of neovimcraft are also responsible for [pgs.sh](https://pgs.sh), the host for this book's website. I appreciate their product so I wanted to throw in some free advertising for them.

### 20.6. Dotfiles

Historically, the easiest way to configure Vim has always been to look at someone else's configuration and copy the interesting bits. Nowadays, the easiest way is to use LazyVim, but you may still want to check out the dotfiles of some prominent Neovim and LazyVim users:

[Folke Lemaitre](https://github.com/folke/dot)  
The creator of LazyVim and a whole host of excellent Neovim plugins (most of which are included with LazyVim).

[Evgeni Chasnovski](https://github.com/echasnovski/nvim/)  
The creator of the mini.nvim group of plugins and a Neovim core contributor.

[Iordanis Petkakis](https://github.com/dpetka2001/dotfiles)  
is the person who is most likely to answer your question if you ask it on the LazyVim GitHub Discussion group.

[Myself](https://github.com/dusty-phillips/dotfiles/)  
I don't really deserve to be mentioned alongside the other names on this list! I push tweaks to my dotfiles regularly and I'm pretty selective about which plugins I use, so if it's in there, it's probably pretty good.

These are also people worth following on various social networks.

### 20.7. Neovim GUIs

I still maintain that LazyVim is best run in a first-rate terminal, but there are some excellent GUIs out there that you can try if you want.

The primary benefit of Neovim GUIs is that they operate at the pixel level instead of the character level. This means that things like smooth scrolling, cursor motion, or animated window resizes can be more nuanced or performant. Some GUIs also optionally ship with their own bufferline, statusline, or file tree, but they are generally inferior to the ones that ship with LazyVim.

There have been a ton of attempts at Neovim GUIs over the years, but most of them are not or poorly maintained. I've actually tried pretty much every GUI out there, and it is my considered opinion that these are the only ones worth testing, at least at the time of writing:

[Vimr](https://github.com/qvacua/vimr)  
is MacOS only, but it provides some nice integrations with MacOS if that is what you use.

[Neovide](https://neovide.dev)  
is the best one if you want to use all your existing Neovim plugins, but want the animations and scrolling to be a little smoother. It's super performant as well.

[Goneovim](https://github.com/akiyosi/goneovim)  
is a solid contender as well.

|||
| -- | -- | 
| ![info](./media/chapter-20/info.png) | If you use any of these, you may well want to look for plugins that make the embedded Neovim integrated terminal experience better since you won't be able to switch to a separate pane in a host terminal. |


### 20.8. Summary

This was a short chapter summarizing various resources you might find valuable as you independently continue your LazyVim and Neovim journey.

I want to thank you for sticking with me to the end. I hope you've enjoyed the book! If you're anything like me, you may be using modal editing concepts for decades to come. Someday Neovim will be "Old Vim", but I'm very confident the principles that guide it will be relevant in future iterations of this editor as well.

Code happily, everyone!
