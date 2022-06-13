---
title: Pride R Palettes
author: R package build
date: '2022-06-13'
slug: pride-r-palette
categories: []
tags: []
subtitle: ''
summary: ''
authors: []
lastmod: '2022-06-13T13:01:33-07:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

Simple, easy to access R palettes based on pride flags.
Thanks, Matt <a href="https://github.com/mattreyes13">{{< icon name="github" pack="fab" >}}</a> for the idea!

Colors drawn from flags at <a href="https://www.pride.com/pride/2018/6/13/complete-guide-queer-pride-flags-0">this article.</a>

## Palette: Flag, color, history
- `bakerpride`: Original/Baker pride flag, 8 colors, designed by Gilbert Baker in 1977. (<a href="https://en.wikipedia.org/wiki/Gilbert_Baker_(artist)">more</a>)

- `traditionalpride`: Traditional/Popular pride flag, 6 colors, 1979 San Francisco flag. (<a href="https://www.sftravel.com/article/brief-history-rainbow-flag">more</a>)

- `phillypride`: Philadelphia pride flag, 8 colors, recognizing that queerness is intersectional. (<a href="https://en.wikipedia.org/wiki/Rainbow_flag_(LGBT)#Variations">more</a>)

- `bipride`: Bisexual pride flag, 3 colors, designed by Michael Page in 1998. (<a href="https://www.thisisbiscuit.co.uk/hoisting-our-colours-a-brief-history-of-the-bisexual-pride-flag/">more</a>)

- `panpride`: Pansexual pride flag, 3 colors, popular online since early 2010s. (<a href="https://en.wikipedia.org/wiki/Pansexual_pride_flag">more</a>)

- `apride`: Asexual pride flag, 4 colors, created by AVEN user _standup_ in 2010. (<a href="http://www.asexualityarchive.com/the-asexuality-flag/">more</a>)

- `labryspride`: Labrys lesbian flag, 3 colors, created by lesbian feminists in the 1970s. (<a href="http://findinglesbians.blogspot.com/2013/08/labrys-tool-of-lesbian-feminism.html">more</a>)

- `intersexpride`: Intersex pride flag, 2 colors, created in 2013 by Morgan Carpenter. (<a href="https://en.wikipedia.org/wiki/Morgan_Carpenter">more</a>)

- `transpride`: Transgender pride flag, 3 colors, created in 1999 by Monica Helmes. (<a href="http://point5cc.com/the-history-of-the-transgender-flag/">more</a>)

- `gfluidpride`: Genderfluid pride flag, 5 colors, creted in 2012 by _genderfluidity_ on Tumblr. (<a href="https://genderfluidity.tumblr.com/post/28614422659/so-i-couldnt-find-a-flag-that">more</a>)

- `gqueerpride`: Genderqueer pride flag, 3 colors, created in 2011 by Marilyn Roxie. (<a href="https://genderqueerid.com/about-flag">more</a>)

- `lesbianpride`: Lesbian pride flag, 7 colors, adapted from a 2010 post on the blog _This Lesbian Life_. (<a href="https://en.wikipedia.org/wiki/Lesbian_flag">more</a>)

- `nonbinarypride`: Nonbinary pride flag, 4 colors, created by Kye Rowan in 2014.

## Examples
`bakerpride` is 8 colors, which can be displayed using;

`image(1:8,1,as.matrix(1:8),col=pridepalettes$bakerpride,xlab="",
      ylab="",xaxt="n",yaxt="n",bty="n")`

Output: <img src="images/bakerpride.png" width="400" height="200" align=center>

Using `OrchardSprays`, I created two boxplots, `decrease ~ treatment` with `transpride` and `nonbinarypride` palettes using;

`plot(decrease ~ treatment, OrchardSprays, col=pridepalettes$transpride)`

Output:

<img src="images/transorchard.png" width="400" align=center>

`plot(decrease ~ treatment, OrchardSprays, col=pridepalettes$nonbinarypride)`

Output:

<img src="images/nonbinaryorchard.png" width="400" align=center>

To use: run the below code.

```r
pridepalettes <- list(
  bakerpride = c("#fe6ab4", "#fe0000", "#fe8d01", "#ffff01", "#008d00", "#00c1c0", "#42009b", "#8f008e"),
  traditionalpride = c("#e40203","#ff8b00", "#feed01", "#007f24", "#004dff", "#760789"),
  phillypride = c("#010101", "#785016", "#fe0000", "#fd8c00", "#ffe500", "#109e0a", "#0644b3", "#c22edc"),
  bipride = c("#d6006f", "#724e94", "#0038a7"),
  panpride = c("#ff228c", "#ffd801", "#20b2ff"),
  apride = c("#000000","#7f7f7f","#ffffff","#660066"),
  labryspride = c("#782591", "#000000", "#ffffff"),
  intersexpride = c("#ffd800", "#7902aa"),
  transpride = c("#5bcefa", "#f5a8b8", "#ffffff"),
  gfluidpride = c("#fe75a1", "#ffffff", "#bd16d6", "#000000", "#323dbb"),
  gqueerpride = c("#b57edc", "#ffffff", "#4A8123"),
  lesbianpride = c("#a40061", "#b75592", "#d063a6", "#ededeb", "#e3abce", "#c54e54", "#8a1e04"),
  nonbinarypride = c("#fef433", "#ffffff", "#9a59cf", "#2d2d2d")
)
```

Please use these palettes as you wish, and tag me in a tweet if you do!
