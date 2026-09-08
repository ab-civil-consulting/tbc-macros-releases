# AB Civil TBC Macros

Free command pack for **Trimble Business Center**, built by [AB Civil Consulting](https://ab-civil.com) for our own 3D modeling work and shared as-is.

Sixteen commands for drawing and cleaning linework, elevating 2D lines, labeling surfaces, exporting machine-control packages, and moving objects between projects.

## Download

**[Download the latest installer (Setup .exe)](https://github.com/ab-civil-consulting/tbc-macros-releases/releases/latest/download/ABCivil-TBC-Macros-Setup.exe)**

Prefer a ZIP? Every release on the [Releases page](https://github.com/ab-civil-consulting/tbc-macros-releases/releases) also has one with a batch installer inside.

## Install

1. Close Trimble Business Center.
2. Run the Setup .exe and click through the wizard (Windows will ask for admin permission).
3. Open TBC and type an underscore ( `_` ) or `ABC` in the command search box.

The installer puts the macros in `C:\ProgramData\Trimble\MacroCommands3\ABCivil`. To update, run the newer installer; it replaces the old versions in place. Uninstall from Windows Settings > Apps.

> **SmartScreen note:** the installer is not yet code-signed, so Windows may show "Windows protected your PC" once. Click **More info > Run anyway**.

## Commands

Select your objects first, then run the command. Most of them work on whatever is selected.

### Drawing and editing lines

| Command | What it does |
|---|---|
| `_Quick Line Advanced` | Draws linestrings fast with a 2D mode and add-to-surface as you draw. Spacebar starts a new line, D toggles 2D/3D, A toggles add-to-surface, S cycles the target surface. |
| `_Join Selected Lines` | Joins separate lines into one continuous line. Bridges small gaps, cleans overlaps, flips backwards lines. |
| `_Break at Offset` | Breaks lines where they would cross an offset of a reference line, even though nothing is drawn there. |
| `_Name Lines by Layer` | Names lines from the layer they sit on, with case, prefix/suffix and numbering options. |
| `_Trim Line Ends` | Shaves a small distance off both ends of the selected lines. |
| `_Trim Intersecting Lines` | Trims away the parts of lines inside or outside an area you define, with offsets and a preview. |
| `_ABC Relayer` | Moves objects to a target layer and remembers it, so you can keep tossing objects onto the same layer (Ctrl+R companion). |
| `ABC Convert To Linestring` | Converts CAD lines, polylines and arcs into TBC linestrings with by-layer properties. |

### Elevation and surfaces

| Command | What it does |
|---|---|
| `_Elevate From 3D Lines` | Gives elevations to 2D lines wherever they cross 3D reference lines. |
| `_ABC Surface Elevation Label` | Drops a live surface elevation label with a leader, still linked to the surface. |
| `_ABC Surface Slope Label` | Draws a line draped on a surface and labels the slope percent of every segment. |

### Export and file sharing

| Command | What it does |
|---|---|
| `_ABC Design Exporter` | One-button machine-control export: freezes the surface, converts linework, exports DXF, LandXML, VCL and more into a clean folder structure. |
| `_ABC Capture Background Image` | Exports georeferenced background images with world files, named after the image in TBC. |
| `_Quick Export VCL` / `_Quick Import VCL` | Move objects (and their georeferenced PDFs) from one TBC project to another, like copy and paste between files. |

### View helpers

| Command | What it does |
|---|---|
| `_Sync Plan Views` | Locks two plan views together so panning or zooming one moves the other. |

## Source

The macros are plain IronPython and XAML. Every release ZIP contains the full source in its `macros` folder. Some commands started from the public Trimble TBC macro SDK samples.

## Support

Questions or problems: adam@ab-civil.com. Bug reports are welcome on the [Issues](https://github.com/ab-civil-consulting/tbc-macros-releases/issues) tab.

MIT licensed. Trimble Business Center is a trademark of Trimble Inc.; this project is not affiliated with or endorsed by Trimble.
