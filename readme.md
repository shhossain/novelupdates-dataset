---
license: mit
task_categories:
- text-classification
- zero-shot-classification
- feature-extraction
language:
- en
pretty_name: 'Novelupdates Dataset'
size_categories:
- 10K<n<100K
dataset_info:
  features:
  - name: novel_id
    dtype: int64
  - name: url
    dtype: string
  - name: title
    dtype: string
  - name: associated_names
    sequence: string
  - name: img_url
    dtype: string
  - name: showtype
    dtype: string
  - name: genres
    sequence: string
  - name: tags
    sequence: string
  - name: description
    dtype: string
  - name: related_series
    struct:
    - name: related_series
      list:
      - name: title
        dtype: string
      - name: url
        dtype: string
    - name: total
      dtype: int64
  - name: recommendations
    struct:
    - name: recomendations
      list:
      - name: recommended_user_count
        dtype: int64
      - name: title
        dtype: string
      - name: url
        dtype: string
    - name: total
      dtype: int64
  - name: recommendation_lists
    struct:
    - name: list
      list:
      - name: title
        dtype: string
      - name: url
        dtype: string
    - name: total
      dtype: int64
  - name: rating
    dtype: string
  - name: language
    dtype: string
  - name: authors
    sequence: string
  - name: artists
    sequence: string
  - name: year
    dtype: string
  - name: status_coo
    dtype: string
  - name: licensed
    dtype: string
  - name: translated
    dtype: string
  - name: publishers
    sequence: string
  - name: en_pubs
    sequence: string
  - name: release_frequency
    dtype: string
  - name: weekly_rank
    dtype: string
  - name: monthly_rank
    dtype: string
  - name: all_time_rank
    dtype: string
  - name: monthly_rank_reading_list
    dtype: string
  - name: all_time_rank_reading_list
    dtype: string
  - name: total_reading_list_rank
    dtype: string
  - name: chapters
    struct:
    - name: chapters
      list:
      - name: title
        dtype: string
      - name: url
        dtype: string
    - name: total
      dtype: int64
  splits:
  - name: train
    num_bytes: 58948539.85115204
    num_examples: 11770
  - name: test
    num_bytes: 14739639.148847958
    num_examples: 2943
  download_size: 22367283
  dataset_size: 73688179.0
---

# Dataset Card for Novelupdates Webnovels


### Dataset Summary

This dataset contains information about webnovels from Novelupdates, a popular webnovel platform. It includes details such as novel ID, URL, title, associated names, cover image URL, show type, genres, tags, description, related series, recommendations, recommendation lists, rating, language, authors, artists, year, status, licensing information, translation status, publishers, release frequency, rankings, total reading list rank, and chapters.

### Supported Tasks and Leaderboards

The dataset can be used for various tasks such as text classification, zero-shot classification, and feature extraction. It currently does not have an established leaderboard.

### Languages

The dataset is primarily in English.

## Dataset Structure

### Data Instances

The dataset contains 14,713 data instances.

### Data Fields

The dataset includes the following fields:

- novel_id: integer
- url: string
- title: string
- associated_names: list of strings
- img_url: string
- showtype: string
- genres: list of strings
- tags: list of strings
- description: string
- related_series: struct
  - related_series: list of structs
    - title: string
    - url: string
  - total: integer
- recommendations: struct
  - recommendations: list of structs
    - recommended_user_count: integer
    - title: string
    - url: string
  - total: integer
- recommendation_lists: struct
  - list: list of structs
    - title: string
    - url: string
  - total: integer
- rating: string
- language: string
- authors: list of strings
- artists: list of strings
- year: string
- status_coo: string
- licensed: string
- translated: string
- publishers: list of strings
- en_pubs: list of strings
- release_frequency: string
- weekly_rank: string
- monthly_rank: string
- all_time_rank: string
- monthly_rank_reading_list: string
- all_time_rank_reading_list: string
- total_reading_list_rank: string
- chapters: struct
  - chapters: list of structs
    - title: string
    - url: string
  - total: integer


## Dataset Creation

### Curation Rationale

The dataset was curated to provide a comprehensive collection of webnovel information from Novelupdates for various text analysis tasks.

### Source Data

### Annotations

#### Annotation process

The dataset does not contain explicit annotations. It consists of the information available on the Novelupdates website.

#### Who are the annotators?

N/A

### Personal and Sensitive Information

The dataset does not include any personal or sensitive information.
