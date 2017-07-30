CHANGELOG
================================================================================
This project is using [Semantic Versioning 2.0.0](http://semver.org/)

## v1.0.0

### New Features
  - Added 6 new fonts:
    - Code New Roman (enhancement #85)
    - Gohu (enhancement #90)
    - Hasklig (enhancement PR #103) (@jrolfs)
    - Mononoki (enhancement #89)
    - Share Tech Mono (enhancement #105)
    - Space Mono (enhancement #93)
  - Added new Glyph Sets:
    - [Font Awesome Extension](http://andrelzgava.github.io/font-awesome-extension/) (Over 170 glyphs) (enhancement #96)
    - [IEC Power Symbols](http://unicodepowersymbol.com/) (enhancement #94)
  - Added additional methods to download the fonts:
    - Support for [Home Brew fonts](https://github.com/caskroom/homebrew-fonts) (enhancement #72)
    - Archive downloads via releases with scripts to generate archive downloads for patched fonts (enhancement #32)
  - Added single Nerd Fonts glyphs only fonts for Fontconfig aliasing (enhancement #84)
  - Added TTF version of Terminess (Terminus) font (fixes #23)
  - Added support for custom symbol fonts (with `--custom` flag) (PR #107 @sharkusk)
  - Added progress bars options: `--progressbars` & `--no-progressbars` to patcher script
  - Added `--postprocess` flag to allow additional scripts to run after patching (related to #70)

### Updates / Improvements
  - Improved repository size greatly (partially fixes #73)
    - Provides only `complete` version of patched fonts by default (others are still possible via patcher script)
  - Removed `minimal` version of patched fonts (not particularly useful)
  - Removed `variation` versions of patched fonts and instead provides generated list of commands for each combination
  - Updated Font Awesome to the latest version v4.7.0:
    - https://github.com/FortAwesome/Font-Awesome/releases/tag/v4.7.0
    - https://github.com/FortAwesome/Font-Awesome/issues?q=milestone%3A4.7.0
  - Updated Octicons font from [v3.2.0](https://github.com/github/octicons/releases/tag/v3.2.0) to [v4.4.0](https://github.com/github/octicons/releases/tag/v4.4.0)
    - Last version with [font support](https://github.com/primer/octicons/issues/108)
    - Adds glyphs: `verified`, `smiley`, `unverified`, `ellipses`, `file`, `grabber`, `plus-small`, `reply`
    - Various glyph modifications and fixes
  - Updated [DejaVu Sans Mono](http://dejavu-fonts.org/wiki/Changelog) from version 2.33 to 2.37
  - Updated readme with information on shallow cloning (enhancement #102)
  - Updated readme with better readability, prose, and removes some passive voice issues
  - Updated sankey diagram in readme with a more visual representation of the glyphs combined
  - Updated readability and format of changelog (even past versions)
  - Removed redundant flag `--limit-font-name-length`

### Fixes
  - Added missing glyphs in range `2630` through `2637` (trigrams) to DejaVu Sans Mono (fixes #100)
  - Fixed various missing glyphs such as `heart`, `zap`, `desktop` (fixes #87)
  - Fixed several long standing issues (fix & enhancement PR #107) (@sharkusk)
    - glyphs (scaling and positioning) (fixes #74, #37)
    - Monospaced font issues
    - Windows and macOS issues (fixes #111)
  - Fixed font name for glyph font 'PowerlineExtraSymbols.otf' (fixes #109)
  - Fixed and tweaked various powerline gaps (PR #107 @sharkusk)
  - Fixed Hack hints being removed in patched versions (Knack) (fixes #70, with help from @chrissimpkins)
  - Fixed various issues with '--careful' flag (PR #107 @sharkusk)
  - Fixed missing codepoint conflict information for Octicons & Font Awesome (fixes #116) (image from @kaymmm)
  - Fixed and refactored various code logic and style
  - Fixed missing Powerline glyphs in `MPlus` font (fixes #40)

## v0.8.0
  - Added 2 new fonts:
    - [Fantasque Sans Mono](https://github.com/belluzj/fantasque-sans) (enhancement #80)
    - [Iosevka](https://github.com/be5invis/Iosevka) (enhancement #81)
  - Added new Glyph set: [Font Linux](https://github.com/Lukas-W/font-linux) (enhancement #75)
  - Updated font install script to limit to a single font family (more typical use case) (enhancement PR #82) (@rawkode)
  - Updated readme: Misc readability tweaks and clean-up
  - Fixed Powerline Symbols not correctly rendering (if font already has the symbols) (fixes #78)
  - Fixed AttributeError with Python 3 version of font patcher script (fixes #79)
  - Fixed certain Hack/Knack font style sets by updating version of Hack to [v2.020](https://github.com/chrissimpkins/Hack/releases/tag/v2.020) (fixes #63)

## v0.7.0
  - Added 3 new fonts:
    - Monoid (enhancement #54)
    - Roboto Mono (enhancement #55)
    - Fira Code (enhancement PR #62, fixes #59) (@jrolfs)
  - Added 1 new font variant:
    - Proggy Clean (Slashed Zero) (fixes #69)
  - Added contributing and issue PR templates (enhancement #66)
  - Added Python 3 version of the font-patcher script (fixes #49)
  - Improved explanation of font choices (complete vs alternative vs minimal choices) with bash script to maintain (fixes #52)
  - Updated Hack to v2.019 (fixes #53)
  - Updated Font Awesome to the latest version v4.5.0 (20 new icons) (fixes #48):
    - https://github.com/FortAwesome/Font-Awesome/releases/tag/v4.5.0
    - https://github.com/FortAwesome/Font-Awesome/issues?q=milestone%3A4.5.0
  - Fixed fonts showing as duplicates in OS X Font Book (fixes #56, enhancement PR #61) (@jrolfs)
  - Fixed Powerline Symbols not being applied correctly to patched fonts since v0.5.0 (fixes #68, fix PR #71) (@F1LT3R)

## v0.6.1
  - Added 'font installation' section from [vim-devicons](https://github.com/ryanoasis/vim-devicons) with changes (enhancement PR #47) (@her)
  - Improved various readme updates and fixes: Improved section headers, gitter badge, misc
  - Fixed possible error with '--careful' flag (fixes #45)
  - Fixed default font directory on linux install script to `~/.local/share/fonts` as the previous was deprecated (fix PR #51) (@shaief)
  - Fixed broken curl download example (fixes #50)
- v0.6.0
  - Updated Font naming conventions and directory paths that are more manageable (partially fixes #32, #42)
  - Updated Font variations to use same Font Family (partially fixes #25, #42)
  - Updated Hack/Knack font to [v2.018](https://github.com/chrissimpkins/Hack/releases/tag/v2.018) (enhancement #39)
  - Updated Source Code Pro (Sauce Code Pro) font to [v2.010/v1.030](https://github.com/adobe-fonts/source-code-pro/releases/tag/2.010R-ro%2F1.030R-it) (enhancement #33)
  - Updated Octicons font to [v3.2.0](https://github.com/github/octicons/releases/tag/v3.2.0) plus latest master commits
  - Updated readme with alternate OSX install and execution options (enhancement #38)
  - Improved performance of 'Multiple Fonts Patcher (Gotta Patch 'em All Font Patcher!) by using parallelization (background processes) (enhancement #44)
  - Added new flag/option to font patcher (--outputdir) to allow specifying where to save patched font instead of current directory (enhancement #44)
  - Added 'Powerline Extra' symbols (enhancement #30, #35)
  - Added more Glyphs from Vim-devicons glyph set (various folders, Go, Windows logo, Vim logo, etc)
  - Fixed patched fonts not retaining glyph names (fixes #41)
  - Fixed Ligatures being lost/overwritten when patching (fixes #43)
  - Regenerated all patched fonts

## v0.5.1
  - Added Gitter chat badge
  - Updated readme with badges

## v0.5.0
  - Added Hack font (as 'Knack' for now) (enhancement PR #28) (@cheba)
  - Updated and improved all fonts patcher script (enhancement PR #27) (@cheba)
  - Updated Font Awesome to the latest version v4.4.0
    - for more details see https://github.com/FortAwesome/Font-Awesome/releases/tag/v4.4.0
  - Updated readme with Reserved Font Name info, Hack font, and various version updates
  - Updated the directory structures to make it easier to find font styles
  - Updated all patch fonts to use latest changes and fixes
  - Fixed unicode codepoints for Font Awesome glyphs (fixes #31)
  - Fixed potential SIL Open Font License (OFL) issue with 'Fira Mono' (patched as 'Fura')

## v0.4.1
  - Fixed wrong em sizes on some glyphs (particularly Font Awesome) (fixes #24)
    - Regenerated all patched fonts
  - Added version, comment and fontlog (with changelog notes) to fonts
  - Added image: non text version of patcher logo
  - Removed misc unnecessary code (clean-up)
  - Updated changelog: added missing release details and updated other releases

## v0.4.0
 - Added support for 'octicons', 'font-awesome' font glyphs
 - Added missing font combinations
 - Added Hermit (as 'Hurmit' to comply with SIL Open Font License (OFL)) font
 - Added more sample fonts (Hermit and SourceCodePro variants)
 - Added logos
 - Added 'Code of Conduct'
 - Added missing Pomicons.otf source file and update .gitignore (fixes #19)
 - Added 'all fonts patcher script' pattern parameter support (fuzzy matching)
 - Updated readme: python-fontforge minimum version & link to FontForge install docs (enhancement PR #18) (@blueyed)
 - Updated readme: various misc improvements and fixes
 - Fixed font-patcher to only load Pomicons.otf with '--pomicons' flag (enhancement PR #20) (fixes #19) (@blueyed)
 - Fixed other misc issues
 - Added font files versioning

## v0.3.1
 - Updated readme
 - Fixed font patcher output name for Mono fonts
 - Fixed patcher overwriting fonts with 'Mono' versions preventing all combinations from being generated (only 220 instead of 352)
 - Fixed more possible license issues by completely removed 'Input Mono' font related files
 - Fixed all patched fonts: Re-patched all the fonts due to issue with font patcher and all fonts

## v0.3.0
 - Added new fonts, set up unpatched sources, and set up patched version folders (enhancement #10)
   - Fonts: 3270, Aurulent Sans Mono, Bitstream Vera Sans Mono, Heavy Data, Lekton, MPlus (M+), ProFont
 - Added script to re-patch all of the fonts (work in progress) for enhancement (enhancement #11)
 - Added pomicon glyphs (enhancement #14)
 - Updated devicons font source to latest version 1.8.0 release
 - Updated the range to include new glyphs from latest devicons 1.8.0 (work toward but NOT does not fix #12)
 - Updated scripts and files: various clean-up and refactoring tasks
 - Updated readme

## v0.2.1
 - Added fonts install script for Linux and Mac OS (enhancement PR #5) (@srijanshetty)
 - Added detection and warnings when using unsupported (old) fontforge versions (fixes #6)
 - Added missing patched fonts
 - Fixed Licensing compliance issues (#7)
   - includes removing PragmataPro (@abl)
 - Updated readme: misc updates and tweaks

## v0.2.0
 - True mono support
   - Script can now build single and double width glyphs!
 - Added details of cli parameters and updated fonts list with the true mono spaced fonts (#4)
 - Added/fixed mono fonts single width glyphs support
 - Updated readme

## v0.1.2
 - Updated readme with better description and explanation of the options available
 - Added new unpatched font PragmataPro for Powerline
 - Added new patched font PragmataPro for Powerline Plus Nerd File Types

## v0.1.1
 - Fixes scaling issues in first set of glyphs in certain fonts (fixes issue #1)

## v0.1.0
 - Release
 - Inital port from 'features/1-script-patch-fonts' branch on vim-webdevicons repo
