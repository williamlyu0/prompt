# tree-write-up

Here, we define a write-up format called "tree-write-up". The following is the syntax of such "tree-write-up" format:
```
* {statements X}
  * INTERPRETATION: {quote of part of X or empty for referencing the entirety of X}
    * {statements Y1 that elaborate on the quote}
    * {statements Y2 that elaborate on the quote}
    ...
    * {statements Ym that elaborate on the quote}
  * EXPANSION: {quote of part of X or empty for referencing the entirety of X}
    * {statements Z1 that explain an aspect of the quote}
    * {statements Z2 that explain an aspect of the quote}
    ...
    * {statements Zn that explain an aspect of the quote}
```

The "INTERPRETATION" part means something very general. It can include anything that is remotely related to any interpretation of the quoted content. Think of it like relevant comment. Note that the quoted content should not be presented inside quotation marks.

The "EXPANSION" part is for expanding upon several sub-aspects of the specified quote of statement X.

Note that `{statements Yi}` or `{statements Zj}` can be treated as the new root (`{statements X}`) for recursive expansion. The scopes of `{statements Zi}` should sum up to the scope of the quoted part of X.

# disambiguation notation

We shall define "disambiguation notation" as the notation `[ {phrase} @@ {disambiguator} ]` for disambiguating phrases. Phrases need disambiguation when such phrase has different meanings in a writeup. The `{phrase}` part can be a single word or a short phrase, while the `{disambiguator}` part is a short description providing enough context for differentiating the meaning of this word in a writeup. Consider the word "memory" in the following writeup:
```
I cannot recall how much memory I allocated to this data object from my memory.
```

The first "memory" is referring to the a hardware resource of a computer, while the second "memory" is referring to the my own recollection of events. A single word or phrase can have multiple meanings. When the same word or phrase with different meaning occurs within the same sentence or the same paragraph, we can use the "disambiguation notation" just like the following to rewrite the previous sentence:
```
I cannot recall how much [ memory @@ computer hardware resource ] I allocated to this data object from my [ memory @@ recollection of events ].
```
