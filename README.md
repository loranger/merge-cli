# merge360
Combine and crossfade 360 videos into a single spherical tagged mp4 file

## Requirements

This scripts uses `ffmpeg` and the depreacted package `exiftool`.  
They should be installed on your system in order to make merge360 works, plus some unix extra such as `bc` or `awk`.

## Usage

```
merge360 [-d duration] [-t transition] [-o output] file1.mov file2.mp4 file3.mp4
```

- `duration` of the transition, in seconds (default: 3)
- `transition` is one of the [builtin ffmpeg effects](https://trac.ffmpeg.org/wiki/Xfade#Gallery) (default: fade)
- `output` is the name of the output file (default: merged.mp4)

## Installation

### From build

Download binary and store it somewhere in your `$PATH`

```bash
wget -O /usr/local/sbin/merge360 https://raw.githubusercontent.com/loranger/merge-cli/main/merge360
chmod a+x /usr/local/sbin/merge360
```

### From source

Clone this repository, install dependencies then install binary system-wide :

```bash
git clone git@github.com:loranger/merge-cli.git
cd merge360-cli
```

Move the freshly built `merge360` cli somewhere in your `$PATH`

```bash
mv merge360 /usr/local/sbin/merge360
```

or symlink it

```bash
ln -s $PWD/merge360 /usr/local/bin/merge360
```