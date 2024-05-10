## Usage

`camera-support [-libraw <path>] [-rawspeed <path>] [-wbpresets <path>] [-noiseprofiles <path>] [-stats <stdout|table|all|none>] [-format <md|html|tsv|none>] [-headers <h1|h2|h3|h4|h5|h6>] [-fields <...|no-maker|all|all-debug>] [-bools <...,...>] [-unsupported] [<output path>]`

All options that take a file path accept either a URL (starting with `https://`) or a relative local path.

### -libraw
  
`imageio_libraw.c` location. If empty, LibRaw cameras will not be included.
Default: `https://raw.githubusercontent.com/darktable-org/darktable/master/src/imageio/imageio_libraw.c`
  
### -rawspeed

`cameras.xml` location.
Default: `https://raw.githubusercontent.com/darktable-org/rawspeed/develop/data/cameras.xml`

### -wbpresets

`wb_presets.json` location.
Default: `https://raw.githubusercontent.com/darktable-org/darktable/master/data/wb_presets.json`

### -noiseprofiles

`noiseprofiles.json` location.
Default: `https://raw.githubusercontent.com/darktable-org/darktable/master/data/noiseprofiles.json`
  
### -stats

Print statistics.
`stdout` prints at the end of normal output to the terminal. Default.
`table` adds stats to table headers.
`all` does both.
`none` prints nothing.

### -format

Output format.
`md`, the default, is Markdown table.
`html` is HTML table.
`tsv` is tab separated values.
`none` creates no output. Useful if only interested in statistics.
  
### -headers
  
Segments tables by maker, adding a header using the specified level (h1-h6).
  
### -fields

Comma delimited list of fields to print. Default is `Maker,Model,Aliases,WBPresets,NoiseProfiles,Decoder`.
See the `camera` struct in `camera-support.go` for valid fields.
Presets: no-maker|all|all-debug

### -bools

Text to use for boolean fields. Format is "true,false" with a comma delimiter.

### -unsupported

Include unsupported cameras. Also affects statistics.

### \<output path\>

Output file. Defaults to stdout.

### -h / -help

Prints a short version of this help.
