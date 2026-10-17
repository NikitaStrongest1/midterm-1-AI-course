# Midterm 1: answers

GitHub username: nikitastrongest1
Session code: zebra-28
Fingerprint: 32b65508

> Fill in the three lines above from `my_data/DATA.md`. Do not rename headings or table columns: a script reads the numbers.
> Write only in the empty cells and lines. Percentages as 0.78 or 78 %, money as plain numbers.

## AI-use declaration

(About half a page: which assistants or tools you used and for what. If you used none, say so.)

## Part 1: Retrieval and cost decision

### 1a. Metrics (all 60 questions)

| config | recall@1 | recall@3 | recall@5 | MRR@10 |
|---|---|---|---|---|
| A |0.5333|0.6833|0.7667|0.6175|
| B |0.3500|0.6000|0.8333|0.5123|

### 1b. Recall and 95 % Wilson interval of each candidate (recall at its own k)

| candidate | recall@k | lower | upper |
|---|---|---|---|
| A, k=3 |0.6833|0.5577|0.7869|
| A, k=5 |0.7667|0.6456|0.8556|
| B, k=3 |0.6|0.4737|0.7143|
| B, k=5 |0.8333|0.7197|0.9069|

### 1c. Annual model cost in USD

| candidate | annual cost |
|---|---|
| A, k=3 |$25,631.71|
| A, k=5 |$34,775.34|
| B, k=3 |$15,454.20|
| B, k=5 |$17,812.83|

### 1d. Decision (at most 150 words)

Chosen candidate: Candidate B with k = 5

I choose Candidate B with k = 5 because it gives the best recall while staying within the budget. Its recall is 0.8333 (83.33%), which is the highest result among the four configurations. This means that it can find relevant documents for most of the test questions.

The 95% Wilson confidence interval is from 0.7197 to 0.9069. This shows that the recall estimate has some uncertainty, but the overall result is still promising.

The annual cost of Candidate B with k = 5 is $17,812.83, which is below the budget of $21,700. This leaves $3,887.17 available. Candidate B with k = 3 is cheaper, costing $15,454.20, but its recall is only 60%. Candidate A with k = 3 and k = 5 has recall values of 68.33% and 76.67%, respectively, but both options exceed the budget.

For these reasons, I think Candidate B with k = 5 is the best choice because it provides the highest recall among the options that fit the budget.

### 1e. Next measurement (at most 60 words)

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H | | | | | | |
| L | | | | | | |

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)

## Part 3: Explain your own numbers

### Q1

Number:
Why (at most 40 words):

### Q2

Number:
Why (at most 40 words):

### Q3

Number:
Why (at most 40 words):

### Q4

Number:
Why (at most 40 words):

### Q5

Number:
Why (at most 40 words):
