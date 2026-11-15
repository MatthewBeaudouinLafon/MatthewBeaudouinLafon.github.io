---
title: "Color Field: Professional Vision for Color Grading"
date: 2023-10-30
conference: "UIST 2023"
author: ["Matthew T. Beaudouin-Lafon", "Jane L. E", "Haijun Xia"]
summary: 'An interactive tool to visualize the effect of color filters as a vector field over a color space. We draw inspiration from Goodwin''s Professional Vision to help novices "see" color grading like experts.'
description: 'An interactive tool to visualize the effect of color filters as a vector field over a color space. We draw inspiration from Goodwin''s Professional Vision to help novices "see" color grading like experts.'

thumbnailLink: "/images/thumbnails/ColorFieldThumbnail.png"

# weight: 1
# aliases: ["/first"]
tags: ["publications"]
# author: ["Me", "You"] # multiple authors
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

{{< paper-callout link=https://dl.acm.org/doi/abs/10.1145/3586183.3606828 >}}
Read the full paper here
{{</ paper-callout >}}

## Video Overview

{{< youtube id=yMT4CxSqtWg >}}

## Abstract

Color filters are ubiquitous across visual digital media due to their transformative effect. However, it can be difficult to understand how a color filter will affect an image, especially for novices. In order to become experts, we argue that novices need to develop Goodwin’s notion of Professional Vision [29]. Then, they can "see" and interpret their work in terms of their domain knowledge like experts. Using the theory of Professional Vision, we present two design objectives for systems that aim to help users develop expertise. These goals were used to develop Color Field, an interactive visualization of color filters as a vector field over the Hue-Saturation-Lightness color space. We conducted an exploratory user study in which five color grading novices and four experts were asked to analyze color filters. We found that Color Field enabled multiple strategies to make sense of filters (e.g. reviewing the overall shape of the vector field) and discuss them (e.g. using spatial language). We conclude with other applications of Color Field and future work to leverages Professional Vision in HCI.

## Conference Talk

It seems like the good people who recorded and uploaded this talk determined that it will only be interesting to your left ear. Sorry!
{{< youtube id=PkXHuPkatpk start=10083 end=11076 >}}

## Cite Color Field

```plain
@inproceedings{ColorField2023_BeaudouinLafon,
    author = {Beaudouin-Lafon, Matthew T and E, Jane L and Xia, Haijun},
    title = {Color Field: Developing Professional Vision by Visualizing the Effects of Color Filters},
    year = {2023},
    isbn = {9798400701320},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3586183.3606828},
    doi = {10.1145/3586183.3606828},
    abstract = {Color filters are ubiquitous across visual digital media due to their transformative effect. However, it can be difficult to understand how a color filter will affect an image, especially for novices. In order to become experts, we argue that novices need to develop Goodwin’s notion of Professional Vision [29]. Then, they can "see" and interpret their work in terms of their domain knowledge like experts. Using the theory of Professional Vision, we present two design objectives for systems that aim to help users develop expertise. These goals were used to develop Color Field, an interactive visualization of color filters as a vector field over the Hue-Saturation-Lightness color space. We conducted an exploratory user study in which five color grading novices and four experts were asked to analyze color filters. We found that Color Field enabled multiple strategies to make sense of filters (e.g. reviewing the overall shape of the vector field) and discuss them (e.g. using spatial language). We conclude with other applications of Color Field and future work to leverages Professional Vision in HCI.},
    booktitle = {Proceedings of the 36th Annual ACM Symposium on User Interface Software and Technology},
    articleno = {101},
    numpages = {16},
    keywords = {color filter, color grading, creativity support tool, professional vision, support novice, visualization},
    location = {San Francisco, CA, USA},
    series = {UIST '23}
}
```
