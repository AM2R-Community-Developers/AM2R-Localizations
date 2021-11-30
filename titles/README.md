# Title Images

## Naming Format
- General format: `/AM2R/lang/titles/*languageName*x###*y###*.png` (see [FAQ](https://am2r-community-developers.github.io/DistributionCenter/faq#how-do-i-use-custom-title-images))
- Title image filenames use the string defined in `[Header] Language =` (not the filename of the ini file)
- <span title="parenthesis filtering requires 1.5.2+">Parentheses in language names are ignored. `Deutsch (16:9)` will match `deutsch.png`</span>
- Filenames can match multiple languages/variants. <span title="incomplete reverse sort order: SPACE ()-.0123456789abcdefghijklmnopqrstuvwxyz[]_{}">The last alphabetical match will be loaded.</span>
- If invalid coordinates are specified, they will be set to `x000` or `y000`. This includes languages with an "x" or "y" in the name.
  - For non-zero coordinates, languages with an &quot;x&quot; or &quot;y&quot; in the name require coordinates to be specified before the language name
- If omitted from the filename, the default coordinates are `x057 y022`
- Left border alignment is at <span title="negative coordinates require 1.5.2+">`-x053`</span> for widescreen, `x000` for standard


## Legacy Notes

### 1.5-1.5.1
- <span title="this can prevent loading title image for germanwide.ini due to invalid filename characters">Language matching includes parentheses</span>
- Negative pixel coordinates are not supported

### 1.5
- If omitted from the filename, the default coordinates are `x000 y000`

### 1.4.1-1.4.3
- Single image `/AM2R/mods/titles/title.png`
- Coordinates are set in `/AM2R/mods/titles/config.ini`

### 1.2.8-1.4
- Single image `/AM2R/title.png`

