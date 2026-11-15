---
title: "Belidor: A Language for User Interface Analogies"
author:
  [
    "Matthew T. Beaudouin-Lafon",
    "Devamardeep Hayatpur",
    "Arvind Satyanarayan",
    "Haijun Xia",
  ]
conference: "CHI 2026"

# Summary for list view, truncates at least after 150 characters
summary: "A specification language for the structure underlying user interfaces. Beldior's semantics can express a wide range of UIs and surface analogies between very different interfaces (eg. a calendar and a video editor)."

# Desc text below post title.
description: "A specification language for the structure underlying user interfaces. Beldior can express a wide range of UIs (simple and complex GUIs, screen readers, and hardware devices). Belidor's semantics help surface analogies between very different interfaces (eg. a calendar and a video editor)."
date: 2026-04-13T15:03:11-07:00

# Thumnail needs to be square. It will be resized to 280x280
thumbnailLink: "images/thumbnails/BelidorThumbnail.png"

# weight: 1
# aliases: ["/first"]
tags: ["publications"]
draft: false
# canonicalURL: "https://canonical.url/to/page"

showToc: false
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: true
ShowReadingTime: false
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: false
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
  image: "<image path/url>" # image path/url
  alt: "<alt text>" # alt text
  caption: "<text>" # display caption under cover
  relative: false # when using page bundles set this to true
  hidden: true # only hide on current single page
---

{{< paper-callout link=https://dl.acm.org/doi/10.1145/3772318.3791613 >}}
Read the full paper here
{{</ paper-callout >}}

## Video Overview

{{< youtube JfdKa_VwHrs >}}

# Abstract

We present Belidor, a text notation that describes the structure underlying user interfaces (UIs). Belidor’s relational model emphasizes how structures, such as the temporal order of text messages, cut across an interactive system’s conceptual model, user-facing presentation, and interactive behavior. We demonstrate Belidor’s expressive power with a gallery of examples spanning GUIs (eg. messaging, video editors), screen readers, and hardware devices.

Belidor serves as an effective representation for structural analogies between user interfaces (eg. between calendars and video-editors). In contrast, prior work relied on visual UI representations and therefore prioritized visual style transfer. In three case studies, we show how Belidor can reveal analogies, help transfer ideas between user interfaces, and describe design patterns as analogies. We discuss the implications of representing the structure of interactive systems for designers and developers, and envision how Belidor might support “structural design moves” for interface designers.

## Conference Talk

{{< youtube T-VMaQs_G-o >}}

## Cite Belidor

```plain
@inproceedings{10.1145/3772318.3791613,
    author = {Beaudouin-Lafon, Matthew T and Hayatpur, Devamardeep and Satyanarayan, Arvind and Xia, Haijun},
    title = {Belidor: A Specification Language for Operationalizing Structural Analogies Between User Interfaces},
    year = {2026},
    isbn = {9798400722783},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3772318.3791613},
    doi = {10.1145/3772318.3791613},
    abstract = {We present Belidor, a text notation that describes the structure underlying user interfaces (UIs). Belidor’s relational model emphasizes how structures, such as the temporal order of text messages, cut across an interactive system’s conceptual model, user-facing presentation, and interactive behavior. We demonstrate Belidor’s expressive power with a gallery of examples spanning GUIs (eg. messaging, video editors), screen readers, and hardware devices. Belidor serves as an effective representation for structural analogies between user interfaces (eg. between calendars and video-editors). In contrast, prior work relied on visual UI representations and therefore prioritized visual style transfer. In three case studies, we show how Belidor can reveal analogies, help transfer ideas between user interfaces, and describe design patterns as analogies We discuss the implications of representing the structure of interactive systems for designers and developers, and envision how Belidor might support “structural design moves” for interface designers.},
    booktitle = {Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems},
    articleno = {381},
    numpages = {21},
    keywords = {User Interface, Specification Language, Analogy, Structural Design},
    location = {},
    series = {CHI '26}
}
```
