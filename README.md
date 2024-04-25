
# Code-switching features of cantonese songs in the recent 20 years

## Overview

This repository contains lyrics for total 100 songs from Ultimate Song Chart Awards Presentation Top5 between 2004-2023. All lyrics utilize texts posted on KKBOX, which contains more than 90 million songs with lyrics. The text corpus is munually annotated with code-switching information. 

The default for code-switching is to alternate 
between Cantonese and non-Cantonese languages.

## Decision of the scope of collection

Due to the representation of public preferences, we have decided to collect the lyrics of the top 5 songs from each year. We specifically chose popular songs from the past 20 years because there have been significant shifts in pop music trends during this period. By focusing on these recent years, we expect to identifying more obvious change that will assist in the further analysis.


## Description

All files are in the Tab-separated values (TSV) format.
- Some columns exist in both files.
> ⚠️ if you find the data/sheet1.tsv is unreadable, please open the Google Sheet link for further information: https://docs.google.com/spreadsheets/d/1y_eLNm7-UIKgZxkuh_jCYRUEbTs9os2CQSA62DQrIh4/edit?usp=sharing

### __data/sheet1.tsv__
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
Data in this files is for analysation and counting ratio of code-switching features existed. Explanation of columns which are also existed in `data/sheet1.tsv` will be omitted.  

| Column  | Explanation | 
| ---    | --- | 
| song ID | - |
| song title | the title of song |
| singer | name of singer(s) |
| lyricist | name of lyricist(s) |
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

#### definition of spoken language:
>Spoken language refer to Cantonese words. However, especially in the lyric, there are sometime ambiguous that distinguish whatever they are written or spoken language is difficult, we set up guidelines that only words or sentence not generally used in Putonghua are counted as spoken language.

#### definition of English words:

> There are some English characters written in the lyrics that do not have lexical meaning. we have differentiated them into two class in our collection: Some of them are defined as onomatopoeia, as they are clearly pronunced as a single sound, and these are counted as English words in our guidelines; while some are defined as snort or grunt, which are pronunced relatively slower and longer, and these are not counted as English word.




## Organization of the data

- basic unit: a single line of lyric
- we add song ID and lyric ID for each row of data to convenient searching: 
    - song ID is Composed from: 'S' + 'yy' + #(a number representing rank of the song)
        > e.g. S10-1 represent the song which is the first place in 2010
    - lyric ID is Composed from: 'L' + #(a number)
        > e.g. L11 represent the 11th line of lyric
- we remove symbols which are represent of repeated parts of lyric, instead those parts will be filled up with the lyric which is actually sung in the song


### Organisation of Metadata 

- when there are multiple participants in the '*singer*' and '*lyricist*' column, participants are separated by a comma.
    > e.g. 李克勤 (Hacken Lee),容祖兒 (Joey Yung)

### Reason of Metadata choices
- Names of singers and lyricists included in our metadata file to distinguish song from others which have the same title

## Source

- The ranking: `Ultimate Song Chart Awards Presentation` from [LemonMusic](https://www.lemonmusic.com.hk/awards.htm)
- Lyric, metadata: [KKbox](https://www.kkbox.com/tw/tc/search/lyrics)
 

### Reason of source choice
1. **LemonMusic**
> The ranking of Top5 songs from each year is listed in a clear way which helps us to built up the beginning organisation of data effectively.
2. **KKbox**
> All lyrics, along with the corresponding singers and lyricists, are collected from the same source. The format of the singers' names, including both the Chinese and English names, follows their respective origins and ensures consistency in our metadata file.

## Significance and further applications
- Cultural Preservation and Transmission
- Reproduction/Recreation (manual, AI)
