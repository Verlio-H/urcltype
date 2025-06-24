# urcltype

A text renderer and shaper written in 16 bit IRIS URCL.

Renders glyphs as defined by linear and quadratic bezier curves. A ttf importer exists but is not included within this repository. Some pre-imported TrueType fonts are available in the fonts directory. CFF tables are not supported, so many/most .otf fonts cannot be used without conversion to .ttf.

The shaper supports a number of text layout options (configurable in config.urcl). The shaper also supports kerning and ligatures based on the information contained in the original font's GPOS and GSUB tables (no contextual substitution is supported).

Limited unicode support is available, but no shaping features exist for languages that rely on those beyond what is necessary for english text (such as right-to-left languages). Due to the limitations of a 16 bit address space, few glyphs can be imported simultaneously.

Use urcl-ld to link the source files into a usable file. Ensure to link layout.urcl, main.urcl, config.urcl, rendering.urcl, and one .urcl file from the font directory. A pre-linked example is available in output.urcl.