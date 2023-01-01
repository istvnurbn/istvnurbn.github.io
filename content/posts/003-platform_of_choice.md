---
title: "platform of choice"
date: 2022-09-27T18:20:22+02:00
draft: false
tags: ["backend"]
cover:
  image: "/images/cover/003.png"
  caption: "GoHugo.io's logo."
  alt: "GoHugo.io's logo."
  hidden: true
---

After deciding to restart blogging, my first task was to look for a simple yet powerful platform.

<!--more-->

# pepperidge farm remembers :older_man:

In prehistoric times, I hand-coded my homepage with a text editor. God, the end product looked horrible, and it wasn't fun. So, I switched to a less labor-intensive publishing tool, WordPress. That had the benefits of being customizable and light yet feature-rich enough for my needs.

Fast forward a decade, and the standard on the internet changed dramatically. The [median page weight](https://is.gd/spTkFX) on desktops climbed from 738,3 Kilobytes to 2 291,6 Kilobytes in ten years. Mobile is even worse as the starting median was nearly half of the desktop's figure while the ending is only 200 Kilobytes lower. The main drivers are reliance on CDNs, embedded content, extensive tracking, general asset size, and lack of optimization.

In short, the web is bloated.

# enter hugo :mouse:

As a minimalist and pragmatic person, I said no to all the nonsense described above. I ended up choosing a "static site generator" that checks the following boxes for me:

- Simple to use and maintain
- Flexible and customizable
- Modern web ready
- Actively developed

The final decision was to use Hugo with the PaperMod theme. It does not just meet my expectations but over-delivers in meaningful ways:

- It's an open-source project with a thriving community and frequent updates.
- Currently, the blog is less than 700 Kilobytes in size.
- Rendering and publishing take less than 2 seconds.
- You can use it with the version control system of your choice, as it's a configuration file in YAML, and the content is in Markdown.
- A GitHub repository and a simple GitHub Action make it portable and CI/CD ready.
- I must research to utilize all of its features.

You might say it is missing essential features like statistics or comments. I'm not interested in statistics and will not implement it at the expense of tracking. Turning on comments would make the experience a bit more interactive. However, I'm not feeling comfortable with the idea right now, but that might change in the future.

# verdict :hammer:

My recent addition of version tracking and automatic deployment via GitHub Actions required me to learn and tinker around. By optimizing the workflow, I have one less excuse to avoid posting more.

So, Hugo is the platform for me to move forward.