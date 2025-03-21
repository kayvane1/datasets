---
annotations_creators: []
language_creators:
- found
languages:
- en
licenses:
- unknown
multilinguality:
- monolingual
size_categories:
  emoji:
  - 100K<n<1M
  emotion:
  - 1K<n<10K
  hate:
  - 10K<n<100K
  irony:
  - 1K<n<10K
  offensive:
  - 10K<n<100K
  sentiment:
  - 10K<n<100K
  stance_abortion:
  - n<1K
  stance_atheism:
  - n<1K
  stance_climate:
  - n<1K
  stance_feminist:
  - n<1K
  stance_hillary:
  - n<1K
source_datasets:
  emoji:
  - extended|other-tweet-datasets
  emotion:
  - extended|other-tweet-datasets
  hate:
  - extended|other-tweet-datasets
  irony:
  - extended|other-tweet-datasets
  offensive:
  - extended|other-tweet-datasets
  sentiment:
  - extended|other-tweet-datasets
  stance_abortion:
  - extended|other-tweet-datasets
  stance_atheism:
  - extended|other-tweet-datasets
  stance_climate:
  - extended|other-tweet-datasets
  stance_feminist:
  - extended|other-tweet-datasets
  stance_hillary:
  - extended|other-tweet-datasets
task_categories:
- text-classification
task_ids:
  emoji:
  - multi-class-classification
  emotion:
  - multi-class-classification
  - sentiment-classification
  hate:
  - intent-classification
  irony:
  - multi-class-classification
  offensive:
  - intent-classification
  sentiment:
  - multi-class-classification
  - sentiment-classification
  stance_abortion:
  - intent-classification
  - multi-class-classification
  stance_atheism:
  - intent-classification
  - multi-class-classification
  stance_climate:
  - intent-classification
  - multi-class-classification
  stance_feminist:
  - intent-classification
  - multi-class-classification
  stance_hillary:
  - intent-classification
  - multi-class-classification
paperswithcode_id: tweeteval
pretty_name: TweetEval
---

# Dataset Card for tweet_eval

## Table of Contents
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks and Leaderboards](#supported-tasks-and-leaderboards)
  - [Languages](#languages)
- [Dataset Structure](#dataset-structure)
  - [Data Instances](#data-instances)
  - [Data Fields](#data-fields)
  - [Data Splits](#data-splits)
- [Dataset Creation](#dataset-creation)
  - [Curation Rationale](#curation-rationale)
  - [Source Data](#source-data)
  - [Annotations](#annotations)
  - [Personal and Sensitive Information](#personal-and-sensitive-information)
- [Considerations for Using the Data](#considerations-for-using-the-data)
  - [Social Impact of Dataset](#social-impact-of-dataset)
  - [Discussion of Biases](#discussion-of-biases)
  - [Other Known Limitations](#other-known-limitations)
- [Additional Information](#additional-information)
  - [Dataset Curators](#dataset-curators)
  - [Licensing Information](#licensing-information)
  - [Citation Information](#citation-information)
  - [Contributions](#contributions)

## Dataset Description

- **Homepage:** [Needs More Information]
- **Repository:** [GitHub](https://github.com/cardiffnlp/tweeteval)
- **Paper:** [EMNLP Paper](https://arxiv.org/pdf/2010.12421.pdf)
- **Leaderboard:** [GitHub Leaderboard](https://github.com/cardiffnlp/tweeteval)
- **Point of Contact:** [Needs More Information]

### Dataset Summary

TweetEval consists of seven heterogenous tasks in Twitter, all framed as multi-class tweet classification. The tasks include - irony, hate, offensive, stance, emoji, emotion, and sentiment. All tasks have been unified into the same benchmark, with each dataset presented in the same format and with fixed training, validation and test splits.

### Supported Tasks and Leaderboards

- `text_classification`: The dataset can be trained using a SentenceClassification model from HuggingFace transformers.

### Languages

The text in the dataset is in English, as spoken by Twitter users.

## Dataset Structure

### Data Instances

An instance from `emoji` config:

```
{'label': 12, 'text': 'Sunday afternoon walking through Venice in the sun with @user ️ ️ ️ @ Abbot Kinney, Venice'}
```

An instance from `emotion` config:

```
{'label': 2, 'text': "“Worry is a down payment on a problem you may never have'. \xa0Joyce Meyer.  #motivation #leadership #worry"}
```

An instance from `hate` config:

```
{'label': 0, 'text': '@user nice new signage. Are you not concerned by Beatlemania -style hysterical crowds crongregating on you…'}
```

An instance from `irony` config:

```
{'label': 1, 'text': 'seeing ppl walking w/ crutches makes me really excited for the next 3 weeks of my life'}
```

An instance from `offensive` config:

```
{'label': 0, 'text': '@user Bono... who cares. Soon people will understand that they gain nothing from following a phony celebrity. Become a Leader of your people instead or help and support your fellow countrymen.'}
```

An instance from `sentiment` config:

```
{'label': 2, 'text': '"QT @user In the original draft of the 7th book, Remus Lupin survived the Battle of Hogwarts. #HappyBirthdayRemusLupin"'}
```

An instance from `stance_abortion` config:

```
{'label': 1, 'text': 'we remind ourselves that love means to be willing to give until it hurts - Mother Teresa'}
```

An instance from `stance_atheism` config:

```
{'label': 1, 'text': '@user Bless Almighty God, Almighty Holy Spirit and the Messiah. #SemST'}
```

An instance from `stance_climate` config:

```
{'label': 0, 'text': 'Why Is The Pope Upset?  via @user #UnzippedTruth #PopeFrancis #SemST'}
```

An instance from `stance_feminist` config:

```
{'label': 1, 'text': "@user @user is the UK's answer to @user and @user  #GamerGate #SemST"}
```

An instance from `stance_hillary` config:

```
{'label': 1, 'text': "If a man demanded staff to get him an ice tea he'd be called a sexists elitist pig.. Oink oink #Hillary #SemST"}
```

### Data Fields
For `emoji` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: ❤

    `1`: 😍

    `2`: 😂

    `3`: 💕

    `4`: 🔥

    `5`: 😊

    `6`: 😎

    `7`: ✨

    `8`: 💙

    `9`: 😘

    `10`: 📷

    `11`: 🇺🇸

    `12`: ☀

    `13`: 💜

    `14`: 😉

    `15`: 💯

    `16`: 😁

    `17`: 🎄

    `18`: 📸

    `19`: 😜

For `emotion` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: anger

    `1`: joy

    `2`: optimism

    `3`: sadness

For `hate` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: non-hate

    `1`: hate

For `irony` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: non_irony

    `1`: irony

For `offensive` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: non-offensive

    `1`: offensive

For `sentiment` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: negative

    `1`: neutral

    `2`: positive

For `stance_abortion` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: none

    `1`: against

    `2`: favor

For `stance_atheism` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: none

    `1`: against

    `2`: favor

For `stance_climate` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: none

    `1`: against

    `2`: favor

For `stance_feminist` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: none

    `1`: against

    `2`: favor

For `stance_hillary` config:

- `text`: a `string` feature containing the tweet.

- `label`: an `int` classification label with the following mapping:

    `0`: none

    `1`: against

    `2`: favor



### Data Splits

| name            | train | validation | test  |
| --------------- | ----- | ---------- | ----- |
| emoji           | 45000 | 5000       | 50000 |
| emotion         | 3257  | 374        | 1421  |
| hate            | 9000  | 1000       | 2970  |
| irony           | 2862  | 955        | 784   |
| offensive       | 11916 | 1324       | 860   |
| sentiment       | 45615 | 2000       | 12284 |
| stance_abortion | 587   | 66         | 280   |
| stance_atheism  | 461   | 52         | 220   |
| stance_climate  | 355   | 40         | 169   |
| stance_feminist | 597   | 67         | 285   |
| stance_hillary  | 620   | 69         | 295   |

## Dataset Creation

### Curation Rationale

[Needs More Information]

### Source Data

#### Initial Data Collection and Normalization

[Needs More Information]

#### Who are the source language producers?

[Needs More Information]

### Annotations

#### Annotation process

[Needs More Information]

#### Who are the annotators?

[Needs More Information]

### Personal and Sensitive Information

[Needs More Information]

## Considerations for Using the Data

### Social Impact of Dataset

[Needs More Information]

### Discussion of Biases

[Needs More Information]

### Other Known Limitations

[Needs More Information]

## Additional Information

### Dataset Curators

Francesco Barbieri, Jose Camacho-Collados, Luis Espiinosa-Anke and Leonardo Neves through Cardiff NLP.

### Licensing Information

[Needs More Information]
### Citation Information

```
@inproceedings{barbieri2020tweeteval,
title={{TweetEval:Unified Benchmark and Comparative Evaluation for Tweet Classification}},
author={Barbieri, Francesco and Camacho-Collados, Jose and Espinosa-Anke, Luis and Neves, Leonardo},
booktitle={Proceedings of Findings of EMNLP},
year={2020}
}
```

### Contributions

Thanks to [@gchhablani](https://github.com/gchhablani) and [@abhishekkrthakur](https://github.com/abhishekkrthakur) for adding this dataset.
