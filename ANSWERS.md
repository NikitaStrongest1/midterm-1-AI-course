# Midterm 1: answers

GitHub username: nikitastrongest1
Session code: zebra-28
Fingerprint: 65cf1eaa

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
| A, k=3 |$10,449.84|
| A, k=5 |$13,688.10|
| B, k=3 |$6,942.34|
| B, k=5 |$7,842.26|

### 1d. Decision (at most 150 words)

Chosen candidate: Candidate B with k = 5

I choose Candidate B, k = 5. Its annual cost is $7,842.26, which is below the budget of $9,100. This means the bank can use this configuration and still have $3,887.17 left in the budget.

Candidate B with k = 5 has an overall recall of 83.33%. It performs better than the other options that fit the budget. Candidate B with k = 3 is cheaper, but its recall is only 60%. Candidate A with k = 3 and k = 5 has a higher cost, and both options exceed the budget.

The 95% Wilson confidence interval for Candidate B with k = 5 is 71.97%–90.69%. This interval shows that the estimated recall has some uncertainty because it was measured on a limited test set. However, this candidate still offers a good balance between retrieval quality and cost.

The recall results for Candidate B with k = 5 are 75% for English, 70% for Russian, and 70% for Kazakh. English has the highest recall, while Russian and Kazakh have slightly lower results. The bank should monitor the performance for Russian and Kazakh questions and improve retrieval for these languages if needed.

Overall, I would choose Candidate B with k = 5 because it provides the highest recall among the options within the budget while keeping some money available.

### 1e. Next measurement (at most 60 words)

I would test the retrieval system on a larger set of questions, especially in Russian and Kazakh, because their recall is lower than English. I would also compare the results on real bank documents to check whether Candidate B, k = 5 works well in practice and continues to fit the budget.

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H |91.11%|RU, degraded|86.67%|70.32%|94.69%|$21385.35|
| L |79.44%|KK, degraded|56.67%|39.20%|72.62%|$10800|

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)

I would choose Pipeline H for the bank's document processing.

Pipeline H has an overall accuracy of 91.11%, while Pipeline L has 79.44%. H also has better results for difficult documents. Its weakest result is for degraded Russian documents, with 86.67% accuracy. For Pipeline L, the weakest result is for degraded Kazakh documents, with only 56.67% accuracy. This is important because mistakes when reading invoice numbers, dates, seller IDs, or totals can cause problems for the bank.

However, Pipeline H costs more. Its annual cost is $21,385.35, compared with $10,800 for Pipeline L. By choosing L, the bank could save $10,585.35 per year, but it might also need to spend more time checking documents manually because of its lower accuracy.

Data privacy is another important point. About 22% of the 3,000 daily pages contain a person's name and IIN. This means Pipeline H would send 240,900 pages with personal data abroad every year. This could create privacy concerns. Pipeline L processes documents on a server in Kazakhstan, assuming the data is not sent to external services, so it gives the bank more control over personal information.

Overall, Pipeline H is more accurate, while Pipeline L is cheaper and better for keeping data in Kazakhstan. I would prefer H if accuracy is the main priority and the bank can manage the privacy risks. However, if keeping personal data in Kazakhstan is more important, L could be a better choice, but its accuracy should be improved first.

## Part 3: Explain your own numbers

### Q1

Number: 2.48
Why (at most 40 words): The bill ratio differs from the token ratio because input and output tokens have different prices. Output tokens cost more, so the proportion of input and output tokens affects the final bill.

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
