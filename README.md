
# Code-switching features of cantonese songs in the recent 20 years

## Overview

This repository contains total 100 song lyrics with annotation information

- alternate between cantaonese to non-cantonese language 

```txt
abc
```
## Description

All files are in the Tab-separated values (TSV) format.

### data/(sheet1).tsv
| Column | explanation | 
| ---    | --- | 
| song ID | lyric lines in a song have the same ID  | 
| lyric ID | ID number represents for the line number |
| abc | defghij |
| abc | defghij |
| abc | defghij |
| abc | defghij |
						
### data/metadata.tsv
| Column  | Content | 
| ---    | --- | 
| abc | defghij |
| abc | defghij |
| abc | defghij |

## Annotation Tags

| tag | mark for | example | 
| ---   | --- | ---    |
| (((text))) | English | ``abc`` |
| {{text}} | Spoken language | ``abc``|
| [[[text]]] | Putonghua | ``abc`` |

## Notes on annotation guidelines

- definition of spoken language
- definition of English (words or Onomatopoeia?)

## Organization of the data

- basic unit: a single line of lyric
- columns (e.g.song ID, lyric ID) > easy to search
- song id: 'S' + 'yy' + ranking
    > e.g. S10-1 represent the song which is the first place in 2010
- remove symbols represent to repeated line

### Metadata list

- singer name, lyricist name
- when there are multiple participants...
    > e.g. 李克勤 (Hacken Lee),容祖兒 (Joey Yung)

### (reason of metadata choice?)

- to distinguish song from others which have the same title 

## Source

- [KKbox](https://www.kkbox.com/tw/tc/search/lyrics)
- [rank](https://www.lemonmusic.com.hk/awards.htm) 

### (reason of source choice?)

abcabc

## Significance and further applications
- Cultural Preservation and Transmission
- Reproduction/Recreation (manual, AI)
