
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

### Columns

word count: to count the words in that sentence 

Total word count: to know how many words in that song
English exist in sentences: Through the formula (=checkFormat()), we can know if there is English word in the sentence 

English word no. : Through the formula (=countEnglishWords()), we can know how many English words in the sentence

Total English word count: Through the formula (sum()), we can know the total English words used in that song

English % in sentence: Through the formula (IF()), we can know that the percentage of the English words used in that sentence 

English % in whole song: Through the formulation (IF()), we can know that the percentage of the English words used in that song 

Spoken exist in sentence: Through the formula (checkFormat2()), we can know that if there is spoken words(Cantonese) in that sentence 

Spoken word no. : Through the formula(countTextInsideDoubleBraces(), we can know how many spoken words(Cantonese) in that sentence

Total Spoken word count: Through the formula(sum()), we can know the total spoken words(Cantonese) in that song

Spoke % in sentence: Through the formula(if()), we can know the percentage of using spoken words(Cantonese) in that sentence 

Spoke % in whole: Through the formula(if()), we can know the percentage of using spoken words(Cantonese) in the whole song

Putonghua exist in sentence: Through the formula(checkFormat3(F2)), we can know if  Putonghua exists in the sentence

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

About the rank source choice, is unified list of award-winners over the years has been planned.

## Significance and further applications
- Cultural Preservation and Transmission
- Reproduction/Recreation (manual, AI)
