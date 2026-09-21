# Spotify Streaming History
Exploratory data analysis of Spotify streaming history to uncover listening patterns, user behavior and music consumption trends using Python

## Table of Contents
- [1. Project Overview]()
- [2. Data Overview](#2-data-overview)
  - [2.1. Dataset Information](#21-dataset-information)
  - [2.2. Data Dictionary](#22-data-dictionary) 
- [3. Data Cleaning](#3-data-cleaning)
  - [3.1. Data type Conversion](#31-data-type-conversion)
  - [3.2. Valid Stream Identification](#32-valid-stream-identification)
  - [3.3. Feature Engineering](#33-feature-engineering)
- [4. Exploratory Data Analysis](#4-exploratory-data-analysis)
  -  [4.1 Streaming Duration](#41-streaming-duration)

## 1. Project Overview

## 2. Data Overview
### 2.1. Data Information
Dataset source: [Spotify Streaming History Dataset](https://www.kaggle.com/datasets/arshmankhalid/shopify-streaming-history-dataset)
- **Total records:** 149,860 listening events
- **Number of attributes:** 11
- **Date range:** 08/07/2013 - 15/12/2024
- **Total listening hours:** 5,341.54 hours
### 2.2. Data Dictionary
| Cột                 | Mô tả                                                                | Kiểu dữ liệu                       |
| ------------------- | -------------------------------------------------------------------- | ---------------------------------- |
| `spotify_track_uri` | Spotify URI that uniquely identifies each track in the form of "spotify:track:<base-62 string>"                                             | `string`                           |
| `ts`                | Timestamp indicating when the track stopped playing in UTC (Coordinated Universal Time)                        | `datetime` (`YYYY-MM-DD HH:MM:SS`) |
| `platform`          | Platform used when streaming the track                                   | `string`                           |
| `ms_played`         | Number of milliseconds the stream was played                                    | `int64`                            |
| `track_name`        | Name of the track                                                          | `string`                           |
| `artist_name`       | Name of the artist                                                          | `string`                           |
| `album_name`        | Name of the album                                                            | `string`                           |
| `reason_start`      | Why the track started                                           | `string`                           |
| `reason_end`        | Why the track ended                                               | `string`                           |
| `shuffle`           | TRUE or FALSE depending on if shuffle mode was used when playing the track                | `boolean`                          |
| `skipped`           | TRUE of FALSE depending on if the user skipped to the next song | `boolean`                          |

## 3. Data Cleaning
### 3.1. Data type Conversion
### 3.2. Valid Stream Identification
For a track to register as a stream on Spotify, you must listen to it for at least 30 seconds.

A new variable called `is_valid_stream` was created:

| `is_valid_stream` | Condition |
|---|---|
| `True` | `ms_played >= 30,000` |
| `False` | `ms_played < 30,000` |
### 3.3. Feature Engineering

## 4. Exploratory Data Analysis
### 4.1 Streaming Duration
