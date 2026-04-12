# AGENTS.md

## Repository Structure

This is a markdown-based book about LazyVim. 20 chapters + associated media images.

- **Chapters**: `chapter-1.md` through `chapter-20.md` (5915 lines total)
- **Media**: Organized as `media/chapter-N/` directories containing PNG images referenced in markdown
- **Naming convention**: Image files use hash-based names or `info.png`; referenced in markdown as `./media/chapter-N/<filename.png>`

## Key Tasks

### Adding or Modifying Content

When editing chapters:
- Each chapter is a standalone markdown file
- Media images are stored in `media/chapter-N/` matching the chapter number
- Images are referenced as relative paths: `./media/chapter-N/filename.png`
- **Important**: Each `media/chapter-N/` directory contains a standard `info.png` file that should not be deleted

### Media Management

- Never remove `info.png` files from any chapter media directory—they are required for consistency
- New images should be placed in the corresponding chapter's `media/chapter-N/` directory
- Use relative paths when referencing images in markdown

## Git Workflow

- Early-stage repo: only 3 commits so far, initial setup phase
- Commit style: conventional commits (`chore:`, `init:`, etc.)
- Author: Celal Karakoç (c.karakoc@live.nl)
- Editor config: `core.editor=nvim`

## No Build, Test, or Lint Steps

This is a documentation repository with no automated build, test, or lint pipeline. Focus on content accuracy and markdown correctness by inspection.
