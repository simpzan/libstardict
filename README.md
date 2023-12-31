# A stardict dictionary parser library

Library implements a subset of stardict dictionary formats as well as a binary
lookup in the dictionary index.

BEWARE this is not well tested beta software.

## how to use
Run `./Runfile setup` to
- compile the source code
- install dictionary data.
- lookup the word `apple`

Run `./Runfile lookup orange` to just lookup word `orange`

## key files to study
- sd-cmd.c
- libstardict.h
- libstardict.c

## support `.dict` file
currently this tool only support `.dict.dz` compressed file, we want it support `.dict` uncompressed file as well. Please implement this feature using standard C file functions `fopen/fread`.

The format information is
https://github.com/huzheng001/stardict-3/blob/81e9f560dd8f704a1fa6b20b0405c0cd80f54ce5/dict/doc/StarDictFileFormat#L319

After implementing this feature, command `./Runfile lookup.dict` should not fail. The output should be exactly like the of command `./Runfile lookup.dz`.
