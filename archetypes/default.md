+++
title = "{{ replace .File.ContentBaseName "-" " " | title }}"
summary = "Summary goes here"
tags = [ "tags", "go", "here"]
date = {{ .Date }}
lastmod = [":git", "lastmod", "date", "publishDate"]
thumbnailAlt = "The alternative text description for the thumbnail image."
[params]
  images = ["thumb_XXX.jpg"]
draft = true
+++

Text of the actual post.
