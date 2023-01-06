---
title: "system upgrade"
date: 2022-04-06T09:37:54+02:00
draft: false
tags: ["hardware"]
cover:
  image: "/images/cover/001.png"
  caption: "M1 chip design originally by John Siracusa."
  alt: "M1 chip design originally by John Siracusa."
  hidden: true
---

# prelude :scroll:

<!--more-->

It was 2015 when I purchased my first Apple machine in form of a MacBook Pro and said farewell to Windows in my private life for good. This platform — macOS — is a good place for me to have a UNIX system. I can play around with the terminal, use as much open-source software as I can, and still have the convenience that the Cupertino company provides.

Fast forward seven years and the honeymoon with my beloved MacBook Pro is well over. I started to notice that it is slower than it used to be. I wanted to switch to a new machine earlier, but the omission of ports, the presence of the touch bar, and the infamous butterfly keyboard held me back. Meanwhile, Apple started to transition to ARM with their M-series of chips, and with the 2021 MacBook Pro line, they returned to the form that I like.

# the upgrade :rocket:

After waiting nearly four months to see the reaction from the community I decided that it is time for me to upgrade. Speccing it was no easy feat for me, as I like to overthink. Finally, I landed on a 14" MacBook Pro with M1 Pro chip (10 core CPU, 16 core GPU, and 16 GB RAM) with 1TB of storage. Luckily for me, a local retailer run a sale where I was able to purchase the silver one with about a USD 200 discount compared to the Space Grey model.

|         | **MacBook Pro (13-inch Retina Early 2015)** |    **MacBook Pro (14-inch, 2021)**     |
|---------|:-------------------------------------------:|:--------------------------------------:|
| Model   | [MacBookPro12,1](https://is.gd/nKJHiV)      | [MacBookPro18,3](https://is.gd/VKPu8V) |
| CPU     | Intel Core i5-5257U                         | Apple M1 Pro (10 core)                 |
| RAM     | 8 GB                                        | 16 GB                                  |
| GPU     | Intel Iris Graphics 6100                    | Apple M1 Pro (16 core)                 |
| Storage | 256 GB                                      | 1 TB                                   |

# some figures :chart_with_upwards_trend:

From the feel of it, this thing is a beast. But I wanted to be *objective* so I ran 3 tests 5 times — yes, you read it correctly FIVE times — and compared the averaged results.

The most demanding stuff I do is working with huge files in the Affinity suite of apps. Affinity Photo has a built-in benchmarking tool. They state that the test performance can be translated to real-life workloads and the results are linearly comparable (double the score means twice as fast). I've omitted the Raster (Multi GPU) and the Combined (Multi GPU) tests, as these machines do not have multiple GPUs.

|                       | **Intel MacBook** | **M1 MacBook** | **Gain** |
|-----------------------|:-----------------:|:--------------:|:--------:|
| Vector (Single CPU)   |               169 |            527 |    +212% |
| Vector (Multi CPU)    |               447 |          3 275 |    +633% |
| Raster (Multi CPU)    |               120 |            914 |    +661% |
| Raster (Single GPU)   |             2 373 |         16 852 |    +610% |
| Combined (Multi CPU)  |               144 |            944 |    +555% |
| Combined (Single GPU) |             1 760 |         15 843 |    +800% |

I also help with the distribution of podcasts on YouTube. For that, I use `ffmpeg` to combine WAV files with PNG files into a video. This is just a simple one-liner that I run in the terminal. Depending on the length of the given episode it can take some time to finish.

|        | **Intel MacBook** | **M1 MacBook** | **Gain** |
|--------|:-----------------:|:--------------:|:--------:|
| ffmpeg |           5:36,75 |        1:16,20 |    +342% |

Recently I learned about [Blender Open Data](https://opendata.blender.org/about/) so for a synthetic test, it was a good pick. They have a command-line version which made my life easier. I did it for the fun of it but the results are interesting. I might have to learn 3D modeling after this!

|           | **Intel MacBook** | **M1 MacBook** | **Gain** |
|-----------|:-----------------:|:--------------:|:--------:|
| monster   |         16,413701 |      98,231952 |    +498% |
| junkshop  |          5,568315 |      53,057263 |    +853% |
| classroom |          7,267270 |      41,592097 |    +472% |

The gains are **insane** and my old Intel-based MacBook Pro was left in the dust.

# conclusion :fire:

I'm very happy with my purchase so far. The port selection is as good as it gets in 2022, the keyboard feels good, and the screen is phenomenal. I have no complaint about performance. I only have had this laptop since yesterday, so I had no time to test the battery life. I think it is a good investment but we will see whether it has the longevity as my past one.