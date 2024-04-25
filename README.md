
# Code-switching features of cantonese songs in the recent 20 years

## Overview

This repository contains lyrics for total 100 songs from Ultimate Song Chart Awards Presentation Top5 between 2004-2023. All lyrics utilize texts posted on KKBOX, which contains more than 90 million songs with lyrics. The text corpus is munually annotated with code-switching information. 

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
| (((text))) | English | ``蔑視一棟一劃一捺 (((sorry)))一律不值得`` |
| {{text}} | Spoken language | ``忘掉有{{幾多}}虧欠 只想有些歡笑嘴臉``|
| [[[text]]] | Putonghua | ``[[[那些年錯過的愛情]]]`` |

## Notes on annotation guidelines

- definition of spoken language
  In casual and informal expressions, tends to be more dynamic
- definition of English
  

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

the rank source choice, is unified list of award-winners over the years has been planned.

## Significance and further applications
- Cultural Preservation and Transmission
- Reproduction/Recreation (manual, AI)
