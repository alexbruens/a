---
title: Pride R Palettes
author: R package build
profile: true
date: '2022-06-13'
slug: pride-r-palette
categories:
  - R
tags:
  - R
subtitle: ''
summary: ''
authors:
  - admin
lastmod: '2022-06-13T13:01:33-07:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
links:
  - icon_pack: fab
    icon: github
    name: Originally Published to Github
    url: 'https://github.com/alexbruens/PrideR'
---

Ever need a fun color palette for your graphs, plots, or... for anything else in {{< icon name="r-project" pack="fab" >}}. I have created a list of palettes based on a number of pride flags, encompassing the original Baker flag created in 1977 to the non-binary flag created in 2014.

Thanks, Matt <a href="https://github.com/mattreyes13" target="_blank" rel="noopener">{{< icon name="github" pack="fab" >}}</a> for the fun idea!

Colors drawn from flags at <a href="https://www.pride.com/pride/2018/6/13/complete-guide-queer-pride-flags-0" target="_blank" rel="noopener">this article.</a>

## Palette: Flag, color, history
- `bakerpride`: Original/Baker pride flag, 8 colors, designed by Gilbert Baker in 1977.[^1]

[^1]: Click<a href="https://en.wikipedia.org/wiki/Gilbert_Baker_(artist)" target="_blank" rel="noopener">here</a> for more information.

- `traditionalpride`: Traditional/Popular pride flag, 6 colors, 1979 San Francisco flag.[^2]

[^2]: Click <a href="https://www.sftravel.com/article/brief-history-rainbow-flag" target="_blank" rel="noopener">here</a> for more information.

- `phillypride`: Philadelphia pride flag, 8 colors, recognizing that queerness is intersectional.[^3]

[^3]: Click <a href="https://en.wikipedia.org/wiki/Rainbow_flag_(LGBT)#Variations" target="_blank" rel="noopener">here</a> for more information.

- `bipride`: Bisexual pride flag, 3 colors, designed by Michael Page in 1998.[^4] 

[^4]: Click <a href="https://www.thisisbiscuit.co.uk/hoisting-our-colours-a-brief-history-of-the-bisexual-pride-flag/" target="_blank" rel="noopener">here</a> for more information.

- `panpride`: Pansexual pride flag, 3 colors, popular online since early 2010s.[^5]

[^5]: Click <a href="https://en.wikipedia.org/wiki/Pansexual_pride_flag" target="_blank" rel="noopener">here</a> for more information.

- `apride`: Asexual pride flag, 4 colors, created by AVEN user _standup_ in 2010.[^6]

[^6]: Click <a href="http://www.asexualityarchive.com/the-asexuality-flag/" target="_blank" rel="noopener">here</a> for more information.

- `labryspride`: Labrys lesbian flag, 3 colors, created by lesbian feminists in the 1970s.[^7]

[^7]: Click <a href="http://findinglesbians.blogspot.com/2013/08/labrys-tool-of-lesbian-feminism.html" target="_blank" rel="noopener">here</a> for more information.

- `intersexpride`: Intersex pride flag, 2 colors, created in 2013 by Morgan Carpenter.[^8]

[^8]: Click <a href="https://en.wikipedia.org/wiki/Morgan_Carpenter" target="_blank" rel="noopener">here</a> for more information.

- `transpride`: Transgender pride flag, 3 colors, created in 1999 by Monica Helmes.[^9]

[^9]: Click <a href="http://point5cc.com/the-history-of-the-transgender-flag/" target="_blank" rel="noopener">here</a> for more information.

- `gfluidpride`: Genderfluid pride flag, 5 colors, creted in 2012 by _genderfluidity_ on Tumblr.[^10]

[^10]: Click <a href="https://genderfluidity.tumblr.com/post/28614422659/so-i-couldnt-find-a-flag-that" target="_blank" rel="noopener">here</a> for more information.

- `gqueerpride`: Genderqueer pride flag, 3 colors, created in 2011 by Marilyn Roxie.[^11]

[^11]: Click <a href="https://genderqueerid.com/about-flag" target="_blank" rel="noopener">here</a> for more information.

- `lesbianpride`: Lesbian pride flag, 7 colors, adapted from a 2010 post on the blog _This Lesbian Life_.[^12]

[^12]: Click <a href="https://en.wikipedia.org/wiki/Lesbian_flag" target="_blank" rel="noopener">here</a> for more information.

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
