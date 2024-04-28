# merge360
Combine and crossfade 360 videos into a single spherical tagged mp4 file

## Requirements

This scripts uses `ffmpeg` and the depreacted package `exiftool`.  
They should be installed on your system in order to make merge360 works, plus some unix extra such as `bc` or `awk`.

## Installation

### From build

Download binary and store it somewhere in your `$PATH`

```bash
wget -O /usr/local/sbin/merge360 https://raw.githubusercontent.com/loranger/merge360-cli/master/merge360
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