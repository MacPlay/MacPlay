# re-vim
                         _
     _ __ ___     __   _(_)_ __ ___
    | '__/ _ \____\ \ / / | '_ ` _ \
    | | |  __/_____\ V /| | | | | | |
    |_|  \___|      \_/ |_|_| |_| |_|

re-vim - Reasonable, Readable, Reliable vimrc (Ever for ordinary people)

- Well polished, documented, should work on Mac, Linux and Windows.

- Single file, just download the [.vimrc][vimrc] file. Ready to rock in 5 secs.

- Extend easily, make it fulfill your need.

Best with "huge" Vim 7.4 +lua +python.

## How to begin?

- *nix & Mac

    `curl -Lo ~/.vimrc http://jump.im/re`

    *If the link is broken, use this in stead:*

    *`curl -Lo ~/.vimrc https://raw.githubusercontent.com/ashfinal/vimrc-config/master/.vimrc`*

- Windows

    Download [.vimrc][vimrc] and put it in your home directory.

**Run vim as usual, it can handle itself quite well.**

## Plugins

re-vim uses [vim-plug](https://github.com/junegunn/vim-plug) (`+python` required) as plugin manager. ★ Single file. Super-fast parallel installation/update.

You can install plugins by running `PlugInstall` in vim to acquire more power. This should be completed in 30 secs.

### Plugins list

- [delimitMate][delimitMate] - provides insert mode auto-completion for quotes, parens, brackets, etc.
- [neocomplete][neocomplete] - Next generation completion framework after neocomplcache(`+lua` required)
- [vim-unimpaired][vim-unimpaired] - pairs of handy bracket mappings
- [vim-align][vim-align] - Clone of the Align.vba file, since I think VBA files are a freaking abomination.
- [YankRing.vim][YankRing.vim] - Maintains a history of previous yanks, changes and deletes
- [goyo.vim][goyo.vim] - Distraction-free writing in Vim
    - [limelight.vim][limelight.vim] - Best served with [goyo.vim][goyo.vim]
- [ultisnips][ultisnips] - The ultimate snippet solution for Vim. Send pull requests to SirVer/ultisnips!(`+python` required)
    - [vim-snippets][vim-snippets] - Source of [ultisnips][ultisnips]
- [emmet-vim][emmet-vim] - emmet for vim: http://emmet.io/
- [vim-surround][vim-surround] - surround.vim: quoting/parenthesizing made simple
- [vim-signature][vim-signature] - Plugin to toggle, display and navigate marks
- [vim-gitgutter][vim-gitgutter] - A Vim plugin which shows a git diff in the gutter (sign column) and stages/undoes hunks.
- [nerdcommenter][nerdcommenter] - Vim plugin for intensely orgasmic commenting
- [vim-airline][vim-airline] - lean & mean status/tabline for vim that's light as air
- [vim-jsbeautify][vim-jsbeautify] - vim plugin which formated javascript files by js-beautify(`node.js` required)
- [undotree][undotree] - The ultimate undo history visualizer for VIM
- [vim-easymotion][vim-easymotion] - Vim motions on speed!
- [ctrlp.vim][ctrlp.vim] - Active fork of kien/ctrlp.vim—Fuzzy file, buffer, mru, tag, etc finder.
- [vim-colors-pencil][vim-colors-pencil] - Light (& dark) color scheme inspired by iA Writer

## Key bindings

### Primary key bindings.

    map ; : " remap `;` to `:` in Normal/Visual Mode
    imap jj <Esc> " remap `jj` to `<Esc>` in Insert Mode
    mapleader = "," " map `,` to `<Leader>` in Normal Mode

### Commands

use `W` for sudo writing on Mac & *nix.

### Move around & Edit

| Key                  |      Mode      | Action                                    |
|:---------------------|:--------------:|:------------------------------------------|
| `<CR>`               |     Normal     | unhighlight the search result             |
| `<Tab>`              |     Normal     | switch to next buffer                     |
| `<Shift>` + `<Tab>`  |     Normal     | switch to previous buffer                 |
| `<Ctrl>` + `a`       | Command/Insert | move the cursor to the begining of line   |
| `<Ctrl>` + `c`       |     Normal     | show highlight group under current cursor |
| `<Ctrl>` + `e`       | Command/Insert | move the cursor to the end of line        |
| `<Ctrl>` + `h`       | Command/Insert | move the cursor left by word              |
| `<Ctrl>` + `l`       | Command/Insert | move the cursor right by word             |
| `<Ctrl>` + `b`       |     Insert     | move the cursor left by char              |
| `<Ctrl>` + `f`       |     Insert     | move the cursor right by char             |
| `<Ctrl>` + `j`       |     Insert     | move the cursor down by line              |
| `<Ctrl>` + `k`       |     Insert     | move the cursor up by line                |
| `<Ctrl>` + `j`       |     Visual     | move the current line downward            |
| `<Ctrl>` + `k`       |     Visual     | move the current line upward              |
| `<Ctrl>` + `h`       |     Normal     | resize the current split window           |
| `<Ctrl>` + `l`       |     Normal     | resize the current split window           |
| `<Ctrl>` + `j`       |     Normal     | resize the current split window           |
| `<Ctrl>` + `k`       |     Normal     | resize the current split window           |
| `<Ctrl>` + `w` + `=` |     Normal     | resize split windows to equal             |
| `<Ctrl>` + `w` + `m` |     Normal     | maximize the current split window         |

### `<Leader>` key related

| Key                    |  Mode  | Action                                                   |
|:-----------------------|:------:|:---------------------------------------------------------|
| `<Leader>` + `r`       | Normal | Restore last session                                     |
| `<Leader>` + `e`       | Normal | Use Netrw file explorer                                  |
| `<Leader>` + `b`       | Normal | Toggle background(need colorscheme support)              |
| `<Leader>` + `c`       | Normal | Toggle showing colorcolumn(highlight 80 column etc.)     |
| `<Leader>` + `d`       | Normal | Toggle expandtab(automatically expand tab to space?)     |
| `<Leader>` + `f`       | Normal | Toggle fileformat(unix/mac/dos)                          |
| `<Leader>` + `k`       | Normal | Toggle showing linebreak(add '+++' before wrapped line)  |
| `<Leader>` + `l`       | Normal | Toggle showing non-print char                            |
| `<Leader>` + `m`       | Normal | Toggle showing foldnumber margin                         |
| `<Leader>` + `n`       | Normal | Toggle showing linenumber                                |
| `<Leader>` + `s`       | Normal | Strip whitespace & blankline EOF                         |
| `<Leader>` + `t`       | Normal | Toggle tab & space(also can be used as indent guideline) |
| `<Leader>` + `w`       | Normal | Toggle linewrap                                          |
| `<Leader>` + `x`       | Normal | Toggle modifiable(readonly mode)                         |
| `<Leader>` + `z`       | Normal | Toggle SearchFold(also can be used as outliner)          |
| `<Leader>` + `<Space>` | Normal | Toggle FoldMethod                                        |

### Plugins key bindings

| Plugin                           | Key                      |      Mode     | Action                              |
|:---------------------------------|:-------------------------|:-------------:|:------------------------------------|
| [ctrlp.vim][ctrlp.vim]           | `<Leader>` + `o`         |     Normal    | Open CtrlP window                   |
| [undotree][undotree]             | `U`                      |     Normal    | Toggle undotree window              |
| [YankRing.vim][YankRing.vim]     | `<Leader>` + `y`         |     Normal    | Open YankRing window                |
| [YankRing.vim][YankRing.vim]     | `<Ctrl>` + `p`           |     Normal    | Replace with previous YankRing item |
| [YankRing.vim][YankRing.vim]     | `<Ctrl>` + `n`           |     Normal    | Replace with next YankRing item     |
| [nerdcommenter][nerdcommenter]   | `\`                      | Normal/Visual | Toggle comment                      |
| [nerdcommenter][nerdcommenter]   | `Ctrl` + `\`             | Normal/Visual | CommentSexy                         |
| [emmet-vim][emmet-vim]           | `<Leader>` + `,`         | Insert/Visual | Expand abbr                         |
| [vim-easymotion][vim-easymotion] | `<Space>`                |     Normal    | Search for single char              |
| [vim-align][vim-align]           | `<Leader>` + `g`         |     Normal    | Config AlignCtrl                    |
| [vim-align][vim-align]           | `g` + `l`                |     Visual    | align with                          |
| [goyo.vim][goyo.vim]             | `Ctrl` + `w` + `<Space>` |     Normal    | Toggle distraction-free mode        |
| [ultisnips][ultisnips]           | `ii`                     |     Insert    | Expand snips                        |
| [ultisnips][ultisnips]           | `<Tab>`                  |     Insert    | Jumpforward                         |
| [ultisnips][ultisnips]           | `<Shift> + <Tab>`        |     Insert    | Jumpbackward                        |
| [vim-jsbeautify][vim-jsbeautify] | `<Leader>` +  `j` + `s`  |     Normal    | JsBeauty                            |

For more key bindings please refer to the plugin's manual.

## Customization

re-vim uses `~/.vimrc.before` and `~/.vimrc.after` for your customization.

For example, to override the default colorscheme:

    echo "colorscheme solarized" >> ~/.vimrc.after

To add new plugins, you should create `~/.vimrc.plug`:

    echo "Plug 'altercation/vim-colors-solarized'" >> ~/.vimrc.plug

## Read online

Read the [.vimrc](http://macplay.github.io/attachment/vimrc.html) file online and copy what you need.

## Screenshots

#### Netrw, iTerm, Mac

![screenshot-mac](./screenshot-mac.png)

#### Autocomletion, NeoComplete, Windows 10

![screenshot-win](./screenshot-win.png)

#### Distraction-free, Goyo & Limelight, OpenSUSE Leap

![screenshot-opensuse](./screenshot-opensuse.png)

## Learn more

Read [the article](http://macplay.github.io/cool-software/share-my-dot-vimrc-config/) to learn more about re-vim.


[vimrc]:https://raw.githubusercontent.com/ashfinal/vimrc-config/master/.vimrc "https://raw.githubusercontent.com/ashfinal/vimrc-config/master/.vimrc"
[delimitMate]:https://github.com/Raimondi/delimitMate "https://github.com/Raimondi/delimitMate"
[neocomplete]:https://github.com/Shougo/neocomplete.vim "https://github.com/Shougo/neocomplete.vim"
[vim-unimpaired]:https://github.com/tpope/vim-unimpaired "https://github.com/tpope/vim-unimpaired"
[vim-align]:https://github.com/tsaleh/vim-align "https://github.com/tsaleh/vim-align"
[YankRing.vim]:https://github.com/vim-scripts/YankRing.vim "https://github.com/vim-scripts/YankRing.vim"
[goyo.vim]:https://github.com/junegunn/goyo.vim "https://github.com/junegunn/goyo.vim"
[limelight.vim]:https://github.com/junegunn/limelight.vim "https://github.com/junegunn/limelight.vim"
[ultisnips]:https://github.com/SirVer/ultisnips "https://github.com/SirVer/ultisnips"
[vim-snippets]:https://github.com/honza/vim-snippets "https://github.com/honza/vim-snippets"
[emmet-vim]:https://github.com/mattn/emmet-vim "https://github.com/mattn/emmet-vim"
[vim-surround]:https://github.com/tpope/vim-surround "https://github.com/tpope/vim-surround"
[vim-signature]:https://github.com/kshenoy/vim-signature "https://github.com/kshenoy/vim-signature"
[vim-gitgutter]:https://github.com/airblade/vim-gitgutter "https://github.com/airblade/vim-gitgutter"
[nerdcommenter]:https://github.com/scrooloose/nerdcommenter "https://github.com/scrooloose/nerdcommenter"
[vim-airline]:https://github.com/bling/vim-airline "https://github.com/bling/vim-airline"
[vim-jsbeautify]:https://github.com/maksimr/vim-jsbeautify "https://github.com/maksimr/vim-jsbeautify"
[undotree]:https://github.com/mbbill/undotree "https://github.com/mbbill/undotree"
[vim-easymotion]:https://github.com/Lokaltog/vim-easymotion "https://github.com/Lokaltog/vim-easymotion"
[ctrlp.vim]:https://github.com/ctrlpvim/ctrlp.vim "https://github.com/ctrlpvim/ctrlp.vim"
[vim-colors-pencil]:https://github.com/reedes/vim-colors-pencil "https://github.com/reedes/vim-colors-pencil"
