# ArchiTag

---

## Description

ArchiTag is a very small utility based on **[Python 3](https://www.python.org/)** and **[Mutagen](https://mutagen.readthedocs.org)** to provide missing functionality in `opusenc` of writing specific **[Opus](http://opus-codec.org/)** metadata, such as total number of tracks or track number.

---

## Installaton

Ensure you have Python 3 and Mutagen (for python 3) installed. On Debian and Ubuntu this is as easy as `apt-get install python3-mutagen`. Check out the docs for other OSes instructions.

You can put `architag` file for example in your `/bin` directory to have it in your `PATH`.

---

## Usage

After encoding a song file using `opusenc`, for example with:

```
opusenc --bitrate 128 --artist "MyArtist" --album "MyAlbum" --title "MyTitle" song.flac song.opus
```

Simply call `architag` with desired arguments, for example:

```
architag -p "MyPerformer" -tn 1 -tt 9 song.opus
```

Review `architag --help` for further help.

---

## Features

Currently ArchiTag can write following Opus metadata blocks into opus-encoded audio file:

- Comment
- Performer
- Track number
- Track total

You can very easily extend it for other metadata blocks.

---

## Contributions

All contributions are welcome. I coded this small script for myself in order to add missing `opusenc` metadata functionality. You can easily extend it for your own needs and send a pull request back if appropriate!
