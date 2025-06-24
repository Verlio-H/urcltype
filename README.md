# urcltype

A text renderer and shaper written in 16 bit IRIS URCL.

Renders glyphs as defined by linear and quadratic bezier curves. A ttf importer exists but is not included within this repository. Some pre-imported TrueType fonts are available in the fonts directory. CFF tables are not supported, so many/most .otf fonts cannot be used without conversion to .ttf.

The shaper supports a number of text layout options (configurable in config.urcl). The shaper also supports kerning and ligatures based on the information contained in the original font's GPOS and GSUB tables (no contextual substitution is supported).

Limited unicode support is available, but no shaping features exist for languages that rely on those beyond what is necessary for english text (such as languages written right-to-left). Due to the limitations of a 16 bit address space, few glyphs can be imported simultaneously.

Use urcl-ld to link the source files into a usable file. Ensure to link layout.urcl, main.urcl, config.urcl, rendering.urcl, and one .urcl file from the font directory. A pre-linked example is available in output.urcl.

## Examples

![image](https://github.com/user-attachments/assets/08a4afb2-c9c7-448f-9e6a-801cab2352ba)

<img width="512" src="https://github.com/user-attachments/assets/27a668c4-4291-4c0a-acd1-a40b7b843c8a" />

<img width="512" src="https://github.com/user-attachments/assets/a34f7233-8e81-4f6f-bcb1-38b22ca85a90" />
