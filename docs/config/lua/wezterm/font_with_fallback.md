# `wezterm.font_with_fallback(families [, attributes])`

This function constructs a lua table that configures a font with fallback processing.
Glyphs are looked up in the first font in the list but if missing the next font is
checked and so on.

The first parameter is a table listing the fonts in their preferred order:

```lua
local wezterm = require 'wezterm';

return {
  font = wezterm.font_with_fallback({"JetBrains Mono", "Noto Color Emoji"}),
}
```

The second parameter behaves the same as that of `wezterm.font`.


