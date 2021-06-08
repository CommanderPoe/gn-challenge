# Glassnode: Data Science Challenge

The Blockchain Data Science Code Challenge is an opportunity to demonstrate proficiency with problem solving, coding and data science skills we would expect you to use.

The challenge creates a foundation for further onsite collaboration during your interview. Additionally, we want you to get a feel for some of the challenges you'll encounter here at Glassnode.

## How to Complete a Challenge

Simply organize your code in a folder containing your jupyter notebooks, modules, scripts, READMEs -- anything you'd like to provide.
We love Python, and appreciate if you use it as well. Once you're done, archive it and [send it to us](mailto:rafael@glassnode.com).

## Time

We respect your time and the challenge is designed in such a way as not to take more than 3-4 hours.
We just want to get a sense of your thought process and the way you do the work.
If there are things you don't have time to implement, feel free to describe the intended approach to
implementation in the README. 

## The Challenge

The challenge consists of two parts.

### 1 - Blockchain Data Insights

The goal of this task is to query data from the Bitcoin blockchain in order extract a few on-chain insights.
To do so, you will be using [Google's BigQuery Bitcoin Database](https://console.cloud.google.com/marketplace/product/bitcoin/crypto-bitcoin).

There are different ways in which you can interact with Bitcoin's BigQuery DB.

1. If you have a Google Cloud Platform account, or you set one up, you can interact with the
   database directly via [your Browser](https://console.cloud.google.com/bigquery?p=bigquery-public-data&d=crypto_bitcoin&page=dataset).
   
2. Instead, if you prefer to perform queries via the BigQuery API in your favorite programming language,
   you can follow [this guide](https://cloud.google.com/bigquery/docs/quickstarts/quickstart-client-libraries) to
   set up the authentication.

Here are three questions we would like you to solve you in this task:

- What is currently the total amount of BTC recorded on the blockchain?
- What is currently the amount of **unspent** BTC that were created in coinbase transactions?
  In other words, we are interested in knowing the amount of mining rewards that have never left the mining address.
- Create a time series that shows the amount of unspent mining rewards (see previous question) over Bitcoin's entire history.

For all three questions, we expect the query you used in addition to the actual result.

*ATTENTION:* Interacting with BigQuery in the free tier comes with restrictions - only the first terabyte of data processed per month is free.
If you apply queries to the full blockchain, you might quickly run into this limit. To circumvent this issue, you can
exploit the partitioning of the table `transactions` and restrict the processed data via a filter, e.g., `block_timestamp_month <= '2010-01-01'`.
It's ok if your query and your results don't cover the full blockchain, just make sure to document which limit you chose.

### 2 - Blockchain Archaeology

In this part your task is to dive into the Bitcoin blockchain, poke around, find patterns or other
interesting insights related to Bitcoin addresses.  For this, you can use a blockchain explorer of
your choice (or multiple ones), such as
[blockchain.com](https://www.blockchain.com/explorer?view=btc),
[btc.com](https://explorer.btc.com/),
[blockchair.com](https://blockchair.com/bitcoin), or
[bitinfocharts.com](https://bitinfocharts.com/bitcoin/explorer/).
You may also again use the BigQuery dataset.

The address we are interested in is `3M219KR5vEneNb47ewrPfWyb5jQ2DjxRP6`. What
can you find out about it?

The task is deliberately held general. Here are a couple of things to consider:

 - Over which time periods does to address hold funds?
 - How does its balance increase or decrease?
 - What are common trading partners, i.e. addresses it is interacting with?
 - Which transactions would you rate as interesting and why?
 - What are typical transferred values?
 - Are there outliers with respect to the transferred values? If yes, what could they indicate?
 - If you know some "best practices" for Bitcoin addresses, how would you rate the general behavior?
 - Can the owner of the address be identified?
 - Can you spot any interesting patterns which might help you to identify addresses that are somehow similar or belong to the same owner?
 - Here's a second address to investigate: `3BMEXYAk2tXXG5dS21fz2v7G7cBsZyUuUr`. What is different?

Note: Code is not necessarily required in this task – but you can of course code for the
computation/aggregation/visualization of anything you think could be of interest. If you decide to
use BigQuery, you may of course attach your queries.



## What we care about

Make sure you include:

- A description of the problem and solution.
- The reasoning behind your technical choices: trade-offs you might have made, anything you left out, or what you might do differently if you had additional time.
- What you'd do next and why.

Reviewing your submission we'll rather look at the following aspects:

* *Documentaion and Clarity*: Does the README/Jupyter notebook clearly explain the problem and solution? Do you use visualisations in order to clearly communicate you results?
* *Correctness*: Does the submission accomplish what was asked? If there is anything missing, does the README explain why it is missing?
* *Quality Assurance*: Have there been attempts to verify the correctness of results? Were the approach meaningful? Do they seem over-engineered?
* *Code Quality*: Is the code simple, easy to understand, well documented? Is it aligned with the community-accepted way of solving similar problems?
* *Technical choices and creativity*: What was your approach to tackle the problems? What algorithms and evaluation metric did you choose? What is the level of creativity / ingenuity of your solution?

# Questions?

Feel free to [email us](mailto:rafae@glassnode.com) with any questions you might have about the challenge.

Looking forward to your submission!
