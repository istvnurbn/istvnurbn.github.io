+++
title = "{{ replace .File.ContentBaseName "-" " " | title }}"
summary = "Summary goes here"
date = {{ .Date }}
lastmod = [":git", "lastmod", "date", "publishDate"]
thumbnailAlt = "The alternative text description for the thumbnail image."
[params]
  images = ["thumb.jpg"]
draft = true
+++

Text of the actual post.
