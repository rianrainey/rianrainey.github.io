---
layout: post
title: "How To Find A File Using Unix\'s Find"
date: 2013-10-03 09:39
comments: true
tags: Unix
summary: I can never remember. If I post it, then I will, right?
---

Whenever I need to find text within a file, I use
[Ack](http://www.beyondgrep.com). However, when I need to find where a
particular file is and I know the name of the file, there is nothing
better than using `find`. What the below command is doing is finding, in
the current directory, by name, the file, `deploy.yml`.

```
find . -name deploy.yml
```

For information, check out `man find`. I'm still making a more conserted
effort to read and more easily interpret Man pages.
