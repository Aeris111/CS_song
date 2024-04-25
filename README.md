
# Code-switching features of cantonese songs in the recent 20 years

## Overview

This repository contains lyrics for total 100 songs from Ultimate Song Chart Awards Presentation Top5 between 2004-2023. All lyrics utilize texts posted on KKBOX, which contains more than 90 million songs with lyrics. The text corpus is munually annotated with code-switching information. 

The default for code-switching is to alternate between Cantonese and non-Cantonese languages.

## Description

All files are in the Tab-separated values (TSV) format.
- Some columns exist in both files.
- Spoken words refer to Cantonese.

### __data/(sheet1).tsv__
Data in this files is for marking annotation and counting words, from each line of lyric(the basic unit) to the whole lyric.

| Column | Explanation | 
| ---    | --- | 
| song ID | Lyric lines within a song have the same song ID  | 
| lyric ID | Number in the lyric ID represents the line number |
| Lyrics | Lyric in one line, marked with tags (if applicable)  |
| Word count in sentence |  Number of words in this line, all languages ​​are counted |
| Total word count | Number of words in the whole song, all languages ​​are counted |
| English exist in sentence | The presence or absence of English word in this line is indicated by True/False |
| Eng word count in sentence | Number of English words in this line |
| Total Eng word count | Number of English words in the whole song  |
| Eng % in sentence | Ratio of English words exists in this line |
| Eng % in whole | Ratio of English words exists in the whole song |
| Spoken exist in sentence | The presence or absence of Spoken word is indicated by True/False |
| Spoken word count in sentence | Number of Spoken words in this line |
| Total Spoken word count | Number of spoken words in the whole song |
| Spoke % in sentence | Ratio of spoken words exists in this line |
| Spoken % in whole| Ratio of spoken words exists in the whole song |
| Putonghua exist in sentence| The presence or absence of Putonghua is indicated by True/False |
																																
### __data/metadata.tsv__
Data in this files is for analysation and counting ratio of code-switching features existed. Explanation of columns which are also existed in `data/(sheet1).tsv` will be omitted.  

| Column  | Explanation | 
| ---    | --- | 
| song ID | - |
| song title | the title of song |
| lyricist | name(s) of lyricist |
| Total word count | - |
| English exist in whole | The presence or absence of English word in the whole lyric is indicated by True/False |
| Total Eng word count | - |
| Eng % in whole | - |
| Total Spoken word count | - |
| Spoken % in whole | - |
| Putonghua exist in whole | The presence or absence of Putonghua in the song is indicated by True/False  |
| both eng and spoken | The presence or absence in both Chinese and English is indicated by True/False |
										

## Annotation Tags

| tag | mark for | example | 
| ---   | --- | ---    |
| (((text))) | English | ``蔑視一棟一劃一捺 (((sorry)))一律不值得`` |
| {{text}} | Spoken language | ``忘掉有{{幾多}}虧欠 只想有些歡笑嘴臉``|
| [[[text]]] | Putonghua | ``[[[那些年錯過的愛情]]]`` |

## Notes on annotation guidelines

- definition of spoken language
- In casual and informal expressions, tends to be more dynamic.
- definition of English
- As some lyris maybe is onomatopoeia, like 'ha', 'oh'. And some are whole sentences and words.
  

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
