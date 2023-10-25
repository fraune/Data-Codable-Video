# Data Codable Video

## Background

### The Plot
This project is a proof of concept for encoding non-video data into videos.
Since all data is represented by bits and bytes, it is theoretically possible to encode the bytes of a zip file into a video.
This is desirable because there are various online platforms that let users upload their videos for free (e.g. YouTube, TikTok, Facebook).
Meanwhile, personal data storage platforms like iCloud and Google Drive have limitations on data that can be stored by a single account for free.

### The Math
Consider an _uncompressed_ video with the resolution of 1920x1080, 24 bit color depth, and a framerate of 30 fps.
* 1,920 x 1,080 = 2,073,600 pixels per frame
* 2,073,600 x 3 = 6,220,800 bytes per frame
* 6,220,800 x 30 = 186,624,000 bytes per second
* 186,624,000 x 60 = 11,197,440,000 bytes per minute, or approximately 10.42 GB/min

### Compression
Uncompressed video requires too much bandwidth to be viewed by users on most devices, and is generally unsupported on streaming platforms.
According to [this calculator](https://toolstud.io/video/filesize.php?width=1920&height=1080&framerate=30&timeduration=60&timeduration_unit=seconds&compression=19290&specificbitrate=100&specificbitrate_unit=1000000), a video with a standard codec such as H.264 has a bandwidth of 72 MB/min for a video of roughly the specifications.
A video encoded with H.264 would need to be roughly 2.5 hours long to have the same _file size_ (10.42 GB) as the video in the last scenario.
The length of the video is not very important, since YouTube will allow very long video uploads, and the video is not meant to be viewed.
YouTube may also allow uploads with 4k resolution and 60 fps, which would increase the data that may be stored.

YouTube does not list their official 

## Goals
This project aims to exploit common video codecs and compression algorithms, so that users can upload videos to common platforms which encode large amounts of data, for free.

### Features

[ ] Store some