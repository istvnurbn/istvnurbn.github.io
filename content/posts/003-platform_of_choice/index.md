---
title: platform of choice
description: A post about admitting that I tinker with the backbone of my blog far too much.
tags: ["hugo"]
date: 2022-09-27T18:20:22+02:00
cover:
  image: thumb_003.jpg
  alt: Part of the configuration of this site in Zed.
  relative: true
---

After deciding to start blogging again, my first task was to find a simple yet powerful platform.

## pepperidge farm remembers :older_man:

In prehistoric times, I hand-coded my homepage with a text editor. God, the end product looked terrible, and it wasn't fun. So I switched to a less labor-intensive publishing tool, WordPress. It had the advantage of being customizable and lightweight, yet feature-rich enough for my needs.

Fast forward a decade, and the standard on the web has changed dramatically. The [median page weight](https://httparchive.org/reports/page-weight?start=2012_09_01&end=latest&view=list) on desktops has gone from 738.3 kilobytes to 2,291.6 kilobytes in ten years. Mobile is even worse, with a starting median nearly half that of desktops, and a final median only 200 kilobytes lower. The main drivers are reliance on CDNs, embedded content, extensive tracking, overall asset size, and lack of optimization.

In short, the Web is bloated.

## enter hugo :mouse:

Being a minimalist and pragmatic person, I said no to all the nonsense described above. I ended up choosing a "static site generator" that checked the following boxes for me

- Easy to use and maintain
- Flexible and customizable
- Modern web ready
- Actively developed

The final decision was to use Hugo with the PaperMod theme. It not only met my expectations, but exceeded them in meaningful ways:

- It's an open source project with a thriving community and frequent updates.
- The blog is currently less than 700 kilobytes in size.
- Rendering and publishing takes less than 2 seconds.
- You can use it with the version control system of your choice because it's a configuration file in YAML and the content is in Markdown.
- A GitHub repository and a simple GitHub action make it portable and CI/CD ready.
- I have to do some research to use all its features.

You might say that it lacks essential features like statistics or comments. I'm not interested in statistics and won't implement them at the expense of tracking. Enabling comments would make the experience a bit more interactive. However, I'm not comfortable with that idea right now, but that may change in the future.

## verdict :hammer:

My recent addition of version tracking and automatic deployment via GitHub Actions required some learning and tinkering. By streamlining the workflow, I have one less excuse not to post more.

So Hugo is the platform for me to move forward.
