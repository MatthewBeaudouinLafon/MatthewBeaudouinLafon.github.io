---
title: "Understanding Color Blindness with Color Field"
author: ["Matthew T. Beaudouin-Lafon"]

# Summary for list view, truncates at least after 150 characters
summary: "Visualizing color vision deficiency."
# Desc text below post title.
description: "Visualizing color vision deficiency."
# aliases: ["/first"]
tags: ["blog"] #, "HCI for the Working Designer"]
draft: false
# canonicalURL: "https://canonical.url/to/page"
showToc: false
ShowReadingTime: true
ShowWordCount: false

# Add start date to show range
date: 2025-02-08T18:41:35-07:00

# Thumnail needs to be square. It will be resized to 280x280. It can be empty.
thumbnailLink: ""

# weight: 1

TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
  image: "<image path/url>" # image path/url
  alt: "<alt text>" # alt text
  caption: "<text>" # display caption under cover
  relative: false # when using page bundles set this to true
  hidden: true # only hide on current single page
---

_This blogpost focuses on a specific aspect of our paper on [Color Field](https://dl.acm.org/doi/epdf/10.1145/3586183.3606828). If you find this interesting, check out the full paper for a lot more detail!_

Interface designers often use color for communicative purposes. Of course, not all people perceive colors the same way. For example, 5% of men and 1% of women have deutanomaly, a common form of red-green color blindness.{{< sidenote >}}Kalloniatis M, Luu C. The Perception of Color. 2005 May 1 [Updated 2007 Jul 9]. In: Kolb H, Fernandez E, Jones B, et al., editors. Webvision: The Organization of the Retina and Visual System [Internet]. Salt Lake City (UT): University of Utah Health Sciences Center; 1995-. Table 1, Prevalence of congenital color deficiencies. Available from: https://www.ncbi.nlm.nih.gov/books/NBK11538/table/ch28kallcolor.T1/{{< /sidenote >}} Therefore, designers should be thoughtful about how they use colors in their work. But if you have “normal” trichromatic vision, how should you think about color blindness? There are commonly three ways approaches.

First, there is the version I was taught:

> People who are color blind see fewer colors. It turns out that if you need color contrast, you should stick to blue and orange.

This is good, pragmatic advice, although it doesn’t explain why it happens, or how people actually perceive problematic color pairs, like red and green.

Second, there is the scientific understanding:

> People with color vision deficiencies have reduced sensitivity in one or more cone cells, resulting in a smaller effective perceptual color space.

This is cool for nerds like myself, but it doesn’t actually help me understanding how someone with red-green color-blindness might see an image.

Both have their value, but neither really gives me a sense of how the colors colors I see translate for someone with color blindness. How can I be thoughtful about my choice of colors, if I can’t think about other perceptions of color?

The third approach is to use simulations of color blindness like [Coblis](https://www.color-blindness.com/coblis-color-blindness-simulator/). You can plug in your image, and simulate what it might look like to someone with a specified color vision deficiency.{{< sidenote >}}I should note that these simulations are not without problems. Some are made purely on physical models of visual perception and not validated against people with the condition. Check out this article for more info: https://daltonlens.org/opensource-cvd-simulation/{{< /sidenote >}} Some Figma plugins even let you do this directly in your design file. This is convenient on a case by case basis and I have successfully used them to convince coworkers to avoid using an inaccessible design. However, I have never felt like they helped me develop an intuition for even a single type of color vision deficiencies. Even with a Figma plugin, the round trip to test a design takes just long enough that I don’t do it regularly. What I really want is to be able to look at an image and intuitively gauge how someone with color blindness would perceive it.

In 2023, we primarily designed [Color Field](https://dl.acm.org/doi/epdf/10.1145/3586183.3606828) as a visualization tool for color grading; but color blindness simulations are also color filters! Here is the color filter for protanopia.

{{< figure
  src="protanopia-color-field.png"
  align=center
  caption="Color Field for intense protanopia."
  alt="Two vector fields over the hue-saturation-lightness color space. Left: a saturation-lightness square for a pure red, where vectors move from light and saturated reds to grayscale and darker colors. Right: a hue-lightness rectangle, where reds and greens shift towards oranges, while pinks and purples move towards blues. Pure reds decrease in lightness as well."
  target="_blank" >}}

The visualization might be a bit overwhelming until you get the hang of it.
The key is to think of a color filter (like the colorblindness simulation) as a function that takes a three-dimensional color, and spits out another three-dimensional color. We use the Hue-Saturation-Lightness (HSL) color space, which is similar to what you use in color pickers. Color field shows this function as a vector field! The vector’s start represents the input and its end represents the output color (shown as a diamond ♢). Showing these as straight lines makes them all overlap, so instead Color Field shows the vectors as a curved lines instead. {{< sidenote >}}The curve represents what happens if you incrementally blend in the filter, which has the added benefit of making the lines flow together. Check out the paper for more details!{{< /sidenote >}}

{{< figure
  src="labeled-protanopia-colorfield.png"
  align=center
  caption="Hue-Lightness part of Color Field. The hue of [1] and [2] converge towards orange/brown but [1] becomes much darker. [3] and [4] also converge but keep similar lightness, so they become harder to distinguish."
  alt="A saturation-lightness square for a pure red, where vectors move from light and saturated reds to grayscale and darker colors. Right: a hue-lightness rectangle where reds and greens shift towards oranges, while pinks and purples move towards blues. Pure reds decrease in lightness as well. Label 1 shows a deep red becoming dark brown, label 2 shows a saturated green becoming darkish yellow, label 3 shows a blue become slightly brighter and much more saturated, label 4 shows a purple becoming blue."
  target="_blank" >}}

The “sampler” lets you highlight what happens to a specific color. On the left, you can see that the green at [2] (circle) moves left towards the yellows, only changing hue. The red sampler [1] shows that red moves right BUT it also moves down, making it significantly darker. This is consistent with the scientific explanation of the condition (that red cone-cells are either less sensitive or absent), but I have never heard about that effect in any design class!
A designer could have chosen to mitigate the color contrast issue by making the red lighter, but to someone with protanopia the contrast would have been worse than if they had similar lightness. You can also see that cooler reds and purples shift towards blue, which I had also never heard about before. Notably, Color Field has the same caveat as color simulation. We picked a color filter that is at least partially validated with people who have color vision deficiencies, but we're not color perception experts. {{< sidenote offset="-6em" >}} G. M. Machado, M. M. Oliveira and L. A. F. Fernandes, "A Physiologically-based Model for Simulation of Color Vision Deficiency," in IEEE Transactions on Visualization and Computer Graphics, vol. 15, no. 6, pp. 1291-1298, Nov.-Dec. 2009, doi: 10.1109/TVCG.2009.113.{{< /sidenote >}}

I find Color Field’s visualization much richer than either conceptual models for color blindness I opened this blogpost with. I can hold the field in my head while looking at an image and think about how each color might be affected without having to use a tool.{{< sidenote offset="0em">}}In our user study, we found evidence of participants doing the same thing. [Check out section 6.2.3 for more details!](https://dl.acm.org/doi/epdf/10.1145/3586183.3606828){{< /sidenote >}} In our paper, we argue that this is an example of Goodwin’s _Professional Vision_ — the expert’s ability to “see” their conceptual tools in the artifacts they discuss.

Conceptualizing color vision deficiency with Color Field has helped me with more than interface design. I work with people who are color blind, and I now think more carefully about how I highlight text in my documents and the markers I pick up at the whiteboard.
