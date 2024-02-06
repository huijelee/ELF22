## Dataset Overview

The ELF22 2.0 dataset is the expanded version of the original ELF22 dataset added the responses to abusive comments from <a rel="reference" href="https://aclanthology.org/2021.conll-1.43.pdf">CADD dataset</a>.
The responses to the abusive comments in CADD datasets is augmented via OPENAI GPT-4 API, specifically gpt-4-1106-preview version.
The dataset aims to provide a comprehensive toolkit with enabling more effetive strategies to countering internet trolls.

## Augmentation Prompt

The augmentation prompt is structured into three main components:

1. **Description of the Counter-Response Task**: This part outlines the specific task at hand, detailed in `instruction_prompt.txt`, .

2. **Backgrounds of Counter-Response Strategies**: This section provides backgrounds of the counter response strategies required for the task, detailed in `strategy_descriptions.json`.

3. **Few-Shot Examples with Generated Responses**: This segment includes examples that demonstrate how the strategies can be applied to generate responses, detailed in `strategy_examples.json`.


## Dataset Description
The dataset consists of 8,253 pairs, divided into the three JSON files: train, validation, and test.
Each post contains a subreddit name, a title, a body text, a troll comment, the following response and the strategy of the response. 

| Type         | Train | Validation | Test | Total |
|--------------|-------|------------|------|-------|
| Engage       | 2,386 | 377        | 369  | 3,132 |
| Ignore       | 216   | 10         | 35   | 261   |
| Expose       | 1,383 | 102        | 181  | 1,666 |
| Challenge    | 1,069 | 78         | 107  | 1,254 |
| Critique     | 587   | 68         | 79   | 734   |
| Mock         | 843   | 77         | 136  | 1,056 |
| Reciprocate  | 120   | 18         | 12   | 150   |
| **Total**    | **6,604** | **730**    | **919** | **8,253** |


### Data Structure

| Column         | Description                                             |
|----------------|---------------------------------------------------------|
| Subreddit      | The name of the subreddit, prefixed with 'r/'          |
| Context        | Background information including post title and body text |
| Troll          | The identified troll comment   |
| Flag           | An additional phrase corresponding to the Response Label (7 strategies) |
| Response       | The counter-response to the troll comment.              |

