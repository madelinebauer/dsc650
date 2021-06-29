---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Maddie Bauer
---

## 1.2 

#### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes       |
| 1024x768 PNG image                         | 1.5 MB          |
| 1024x768 RAW image                         | 2.25 MB          | 
| HD (1080p) HEVC Video (15 minutes)         | 2500 MB          |
| HD (1080p) Uncompressed Video (15 minutes) | 156000 MB          |
| 4K UHD HEVC Video (15 minutes)             | 2550 MB          |
| 4k UHD Uncompressed Video (15 minutes)     | 255000 MB          |
| Human Genome (Uncompressed)                | 1.5 GB          |

1. http://extraconversion.com/data-storage/characters/characters-to-bits.html 
2. ((1024 * 768 * 16 bit)/(8 * 1024))/1024=1.5 MB
3. ((1024 * 768 * 24 bit))/(8 * 1024))/1024=2.25 MB
4. http://extraconversion.com/data-storage/characters/characters-to-bits.html
5. https://www.digitalrebellion.com/webapps/videocalc?format=uncompressed_8_1080&frame_rate=f30&length=15&length_type=minutes
6&7.170MB per 60 seconds (1 minute) so 170MB*15minutes = 2550 MB
https://www.imore.com/how-shoot-trim-edit-and-share-4k-video-iphone 
8. https://bitesizebio.com/8378/how-much-information-is-stored-in-the-human-genome/ 



#### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 64 GB       |   1   |
| Daily Twitter Tweets (Snappy Compressed)  | 37.65 GB      |   1   |
| Daily Instagram Photos                    | 112.5 TB       |  12    |
| Daily YouTube Videos                      | 500 TB       |  50    |
| Yearly Twitter Tweets (Uncompressed)      | 23.36 TB       |   3   |
| Yearly Twitter Tweets (Snappy Compressed) | 13.75 TB       |   2   |
| Yearly Instagram Photos                   | 41062.5 TB       | 4107    |
| Yearly YouTube Videos                     | 182500 TB       |  18250    |

1. 500 million * 128 bytes = 64GB
2. 64GB / 1.7 = 37.65 GB
3. 75 Million Instagram Pictures * 1.5 MB PNG Image = 112500000MB = 112.5 TB.  112.5 TB / 10 TB per HD = 11.25 HD. (round up = 12 HD)
4. 500 hours * 60 mins = 30000 mins. 15 min = 2500MB, 30000/15 = 2000, 2000 * 2500 = 5000000MB = 500 TB
5. 64 GB (daily) * 365 = 23360 GB = 23.36 TB, 23.36 / 10 TB per HD = 2.336 (round up = 3 HD)
6. 37.65 GB (daily) * 365 = 13742.25 GB = 13.75 TB, 13.75 / 10 TB per HD = 1.375 (round up = 2 HD)
7. 112.5 TB (daily) * 365 = 41062.5 TB, 41062.5 / 10 TB per HD = 4106.25 (round up = 4107 HD)
8. 500 TB (daily) * 365 = 182500 TB, 182500 / 10 TB per HD = 18250 HD

#### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | 3   |     0.0255       |
| Twitter Tweets (Snappy Compressed) | 2   |     0.017       |
| Instagram Photos                   | 4107   |    34.9095       |
| YouTube Videos                     | 18250   |   155.125         |

1. failure rate = 0.85% (https://www.backblaze.com/b2/hard-drive-test-data.html)
   0.0085 * 3 = 0.0255
   0.0085 * 2 = 0.017
   0.0085 * 4107 = 34.9095
   0.0085 * 18250 = 155.125

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 139.611 ms                 |
| Low Earth Orbit Satellite | 600 ms                 |
| Geostationary Satellite   | 240 ms                 |
| Earth to the Moon         | 2560 ms                 |
| Earth to Mars             | 13 minutes            | 

1. https://wondernetwork.com/pings
2. https://www.omniaccess.com/leo/#:~:text=The%20GEO%20latency%20is%20of,and%20an%20essential%20part%20if
3. https://www.satsig.net/latency.htm
4. https://en.wikipedia.org/wiki/Earth%E2%80%93Moon%E2%80%93Earth_communication#:~:text=Propagation%20time%20to%20the%20Moon,milliseconds%20of%20wave%20travel%20time.
5. https://blogs.esa.int/mex/2012/08/05/time-delay-between-mars-and-earth/
