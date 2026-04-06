---
title: from dotfiles to dendrites
description: How I turned a simple dotfile backup into a three-week existential crisis involving functional programming.
tags: ["mac", "linux", "nix", "geek"]
date: '2026-04-06T21:42:52+02:00'
cover:
  image: thumb_011.jpg
  alt: My Saviour, Nix — Screenshot from @notthebee@tilde.zone's YouTube video
  relative: true
---

I told myself I just wanted to make sense of my dotfile management; I didn't expect to accidentally become a Nix cultist.

I don't switch or reinstall systems that often, but when I do, I always end up setting everything up from scratch. Going through each setting in the apps I use and checking every system setting box is tedious. I have been using dotfiles ever since I switched to a UNIX-like system. However, that doesn't exempt me from having to deal with various `defaults write` commands on macOS.

## failing fast, and often :bomb:

As you can imagine, doing things the way I described above has a lot of pitfalls. Apart from proper backups, I was concerned about making things interoperable between my systems. To add insult to injury, I like to experiment with different settings that often break things, so the ability to roll back would be a benefit as well. 

Initially, I tried to back up all my dotfiles manually, but I often missed some of them. Also, some apps do not expose their settings transparently or portably, not to mention the hassle of macOS system settings. For the latter, I found a solution: I wrote a shell script containing all my desired settings that I can set up with one command. This made my life significantly easier; I just needed a tool to wrap everything up. At first, I found [`chezmoi`](https://www.chezmoi.io/), which was okay, but it did more gymnastics with dotfiles and `git` than I could wrap my head around at that time. So, I settled on using `stow` and `git` together. After taking care of backup and file management, I still felt that something was missing.

These days, people are sharing their configurations online. I'd even say they're showing off their "rice" in every way possible whether it's a Reddit post or even a full-blown YouTube video. I think everyone can learn something from looking at other people's code, so I'm all for it. One day, I came across a video by [Elliott Minns](https://www.youtube.com/watch?v=Z8BL8mdzWHI) on how he manages his macOS machine with Nix. I felt like my invisible itch had been scratched, so I immediately jumped headfirst into the seemingly magical world of Nix. I quickly realized, though, that the water was about 30 cm (a foot) deep.

Initially, I thought Nix was just a glorified configuration file, so YouTube videos helped me set up a basic system configuration with `nix-darwin`. However, as I dug deeper and extended my configuration, I realized I was wrong. Nix is a purely functional, declarative, and lazily evaluated programming language, and the last time I touched code was when I wanted to learn Python about ten years ago. I learned the hard way that Nix is nothing like that at all. I hit a roadblock because I didn't understand the concepts well. There was less documentation than I needed. The evaluation error messages weren't helpful. And I was doing all of this on macOS instead of a proper Linux box. Anyway, I continued with my patchwork configuration, trying to learn from my mistakes because I believed I could turn things around.

## melting the flake :snowflake:

As time went on, I read more and more people's Nix config and watched a ton of videos on NixOS setups and how to do things. This made me feel a bit embarrassed because I felt like I couldn't move forward, but at the same time, I got more comfortable reading and understanding Nix code. I got inspired to look into this more after seeing [Wolfgang](https://tilde.zone/@notthebee) from the homelab/self-hosting space switch from purpose-built solutions like TrueNAS or Proxmox to NixOS. It made me think more about the potential of declarative multi-host system management. I was also a subscriber to [vimjoyer](https://www.youtube.com/@vimjoyer), which is where I learned about nix concepts and picked up new ideas like the [Dendritic pattern](https://github.com/mightyiam/dendritic).

This approach promised to simplify the maintenance of complex, multi-system setups by reducing code duplication and centralizing the logic for each feature. It provides a unified configuration that organizes code by feature rather than by host, eliminating the need for complex glue code. It sounded like the Holy Grail I was looking for, but wrapping my head around its inner workings felt like learning Chinese, even though I had seen a lot of Nix code by that time. I thought to myself that the only way out was through, or, as we said back then, "git gud" -- gamer speak for "get better" or the core philosophy of overcoming challenges through practice.

I'm not sure how, but I was determined to spend the next two or three weeks converting my `nix-darwin` configuration to the Dendritic pattern. I used the [excellent guide](https://github.com/Doc-Steve/dendritic-design-with-flake-parts) by Doc Steve and the well-documented personal configuration by [Victor Borja](https://github.com/vic/vix/tree/449572c34bda13b3828ea04c03f0fa202f78a763?tab=readme-ov-file). I eventually gained enough understanding of the topic to make my configuration work the way I wanted. I was very happy with my achievement -- and my stubbornness -- but I had to postpone the celebration until the next day, as the breakthrough happened around 2–3 a.m.

Since gaining an understanding, I have managed to expand my configuration to levels that were unimaginable to me when I first started. Growing more confident in my abilities, I began to feel that Nix would be the hammer in the law of the instrument for me. [Despite the warnings](https://jade.fyi/blog/use-nix-less/), I implemented `home-manager` for dotfile management, and I set my sights on the next target: migrating my NAS to NixOS from Ubuntu. Unrelated to my newfound obsession with Nix, I had some overdue tasks and new ideas to implement, so I went for it.

Before committing to the switch to NixOS, I decided to keep the services running in Docker. The reasons behind it are simple: I don't want to rely too heavily on NixOS, and I'm already comfortable with containers. NixOS with Flakes can provide a solid foundation thanks to version locking, and Docker allows for experimentation with its ephemeral nature. After some troubleshooting thanks to ZFS, `disko`, and `systemd`, I managed to make my configuration truly cross-platform. At the same time, I updated my compose files, eliminated unused services, and set up remote access through Tailscale. Seeing that everything works as I wanted is more than rewarding.

## i use nix, btw :wink:

In short, it was an incredible journey. I learned a lot about Linux in general, programming concepts, and Git. Most surprising of all was what I learned about myself. I knew that once I set my mind on something, I would see it through to the end, but experiencing the drive I had during this endeavor was something else entirely. I also realized that I only use code to create and manage structure, which is probably why my previous attempts at learning programming failed. There was no practical reason behind it besides doing it for its own sake. I need a more tangible goal.

For me, it started with the simple problem of managing dotfiles, which quickly escalated to managing multiple systems. In the future, I plan to stay up to date with Nix and try to write more elegant code, most likely with the help of the [`den`](https://github.com/vic/den) framework.

Of course, this is where I do the shameless plug: check out my [dotfiles repository](https://github.com/istvnurbn/dotfiles) on GitHub. Feel free to study and modify it. If you think there are ways I can improve, a pull request is very welcome.
