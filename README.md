# ELF22: A Context-based Counter Trolling Dataset to Combat Internet Trolls

ELF22 is a troll-response pairwise dataset along with contextual text from posts in the Reddit community.

## Dataset description
The dataset consists of 5,535 pairs, together with 1,151 'your response', divided into the three JSON files: train, validation, and test.

Each post contains a subreddit name, a title, a body text, and two target sentences: a troll comment and the following response. Each post includes two labels: Type of Trolls (2 labels) and Counter Response Strategies (7 labels).

We note that the dataset may contain offensive, sexual, or hateful language. The dataset can be remixed, transformed, and built upon its contents, except for tracking and re-identifying authors.

|     Type    |  Train | Validation |  Test |  Total |
|-------------|--------|------------|-------|--------|
| Overt |  2,331 |        166 |   340 |  2,837 |
|  Covert |  3,020 |        407 |   422 |  3,849 |
|              |      |       |  |     |
|  Engage |  2,331 |        631 | 1,339 |  2,817 |
|  Ignore |  216 |      10 | 35 | 261 |
|  Expose|  1,131 |      75 | 135 | 1,359 |
|  Challenge |  818 |      48 | 71 | 937 |
|  Critique |  340 |      31 | 52 | 423 |
|  Mock |  592 |      51 | 96 | 739 |
|  Reciprocate |  120 |      18 | 12 | 150 |
|              |      |       |  |     |
|     All     | 5,351 |      573| 762 | 6,686 |

The fields of post in json files are as follows:

|     Field    |          Description|
|---------|--------|
| Subreddit| a subreddit name, usually after 'r/' |
| Title        | a title text | 
| Post       |  a body text         | 
| Troll        | the root comment with thumbs-down |        
| TrollL       |  a type of Trolls {1: 'overt', 2: 'covert'}       |       
| Response |  the following comment with thumbs-up         |        
| ResponseL |  a counter response strategy {1: 'engage', 2: 'ignore', 3: 'expose', 4:'challenge', 5:'critique', 6: 'mock', 7:'reciprocate'}         |        
|                 |           |        
| Flag        |  an additional phrase corresponding to its ResponseL for task C. counter response generaetion task       |        |
| Input       |  an input text (Title + Post + Troll + Response + Flag)  for task C.       |        |
| Output     |  an output text (Response)  for task C.        |        |

## Reference

```
@inproceedings{lee2021elf22,
      title={ELF22: A Context-based Counter Trolling Dataset to Combat Internet Trolls},
      author={Huije Lee and Young Ju NA and Hoyun Song and Jisu Shin and Jong C. Park},
      year={2022},
      booktitle = {Proceedings of the 13th Language Resources and Evaluation Conference}
}
```

## License

These resources are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />
