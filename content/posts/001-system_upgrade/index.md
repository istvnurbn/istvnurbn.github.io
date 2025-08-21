---
title: system upgrade
description: Seven years later, my MacBook Pro was starting to feel slow.
tags: ["hardware", "mac"]
date: 2022-04-06T09:37:54+02:00
cover:
  image: thumb_001.jpg
  alt: M1 chip logo originally designed by John Siracusa.
  relative: true
---

## prelude :scroll:

It was 2015 when I bought my first Apple machine in the form of a MacBook Pro and said goodbye to Windows in my personal life forever. This platform - macOS - is a good place for me to have a UNIX system. I can play around with the terminal, use as much open source software as I can, and still have the convenience that Cupertino provides.

Fast forward seven years, and the honeymoon with my beloved MacBook Pro is well over. I began to notice that it was slower than it used to be. I wanted to upgrade sooner, but the loss of ports, the presence of the touch bar, and the infamous butterfly keyboard held me back. Meanwhile, Apple started moving to ARM with their M-series of chips, and with the 2021 MacBook Pro line, they have returned to the form that I like.

## the upgrade :rocket:

After waiting almost four months to see the reaction from the community, I decided it was time for me to upgrade. Specifying was not easy for me as I like to overthink. In the end, I settled on a 14-inch MacBook Pro with an M1 Pro chip (10-core CPU, 16-core GPU, and 16GB RAM) and 1TB of storage. Luckily, a local retailer was having a sale and I was able to get the silver one for about $200 less than the space gray model.

|         | **MacBook Pro (13-inch Retina Early 2015)** |    **MacBook Pro (14-inch, 2021)**     |
|---------|:-------------------------------------------:|:--------------------------------------:|
| Model   | [MacBookPro12,1](https://is.gd/nKJHiV)      | [MacBookPro18,3](https://is.gd/VKPu8V) |
| CPU     | Intel Core i5-5257U                         | Apple M1 Pro (10 core)                 |
| RAM     | 8 GB                                        | 16 GB                                  |
| GPU     | Intel Iris Graphics 6100                    | Apple M1 Pro (16 core)                 |
| Storage | 256 GB                                      | 1 TB                                   |

## some figures :chart_with_upwards_trend:

From the feel of it, this thing is a beast. But I wanted to be *objective*, so I ran 3 tests 5 times - yes, you read that correctly, FIVE times - and compared the averaged results.

The most demanding thing I do is work with large files in the Affinity suite of applications. Affinity Photo has a built-in benchmarking tool. They claim that the test performance can be translated to real-world workloads and that the results are linearly comparable (double the score means twice as fast). I omitted the Raster (multi-GPU) and Combined (multi-GPU) tests because these machines don't have multiple GPUs.

|                       | **Intel MacBook** | **M1 MacBook** | **Gain** |
|-----------------------|:-----------------:|:--------------:|:--------:|
| Vector (Single CPU)   |               169 |            527 |    +212% |
| Vector (Multi CPU)    |               447 |          3 275 |    +633% |
| Raster (Multi CPU)    |               120 |            914 |    +661% |
| Raster (Single GPU)   |             2 373 |         16 852 |    +610% |
| Combined (Multi CPU)  |               144 |            944 |    +555% |
| Combined (Single GPU) |             1 760 |         15 843 |    +800% |

I also help distribute podcasts on YouTube. I use `ffmpeg` to combine WAV files with PNG files into one video. This is just a simple one-liner that I run in the terminal. Depending on the length of the episode, it may take some time to finish.

|        | **Intel MacBook** | **M1 MacBook** | **Gain** |
|--------|:-----------------:|:--------------:|:--------:|
| ffmpeg |           5:36,75 |        1:16,20 |    +342% |

I recently learned about [Blender Open Data](https://opendata.blender.org/about/), so it was a good choice for a synthetic test. They have a command line version which made my life easier. I did it for fun, but the results are interesting. I may have to learn 3D modeling after this!

|           | **Intel MacBook** | **M1 MacBook** | **Gain** |
|-----------|:-----------------:|:--------------:|:--------:|
| monster   |         16,413701 |      98,231952 |    +498% |
| junkshop  |          5,568315 |      53,057263 |    +853% |
| classroom |          7,267270 |      41,592097 |    +472% |

The gains are **insane** and my old Intel based MacBook Pro has been left in the dust.

## conclusion :fire:

I'm very happy with my purchase so far. The port selection is as good as it gets in 2022, the keyboard feels good, and the screen is phenomenal. I have no complaints about the performance. I have only had this laptop since yesterday, so I have not had time to test the battery life. I think it is a good investment, but we will see if it has the longevity of my previous one.
