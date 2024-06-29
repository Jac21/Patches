# mg-convert

This simple script converts all audio files in a provided directory into [MakeNoise Morphagene](http://www.makenoisemusic.com/modules/morphagene) compatible files (48KHz, floating-point, 32-bit, stereo WAV). It auotmatically names the files in the proper format too.

## Requirements

You must be comfortable with the comand-line, and have [sox](http://sox.sourceforge.net) installed.

Copy this script to somewhere in your PATH, and make it executable (`chmod +x mg-convert`).



## Example

```
ls /some/direcotry/of/sounds

├── foo.wav
├── bar.wav
└── baz.wav
```

```
mg-convert /some/directory/of/sounds
```

will produce:

```
├── foo.wav
├── bar.wav
├── baz.wav
└── converted
    ├── mg1.wav
    ├── mg2.wav
    └── mg3.wav
```

Everything in the `converted` subdirectory will be in Morphagene compatible format. All original input files are preserved. Subsequent runs will override anything in the `converted` directory.

## NOTE

I've only tried this with a handful of input file formats, but in theory should work with any file format sox can process.

Use at your own risk, I'm not able to provide support for this.