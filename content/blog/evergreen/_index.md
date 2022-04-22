---
author: Bastián Aballay
categories:
- r
date: "2021-01-20"
draft: false
excerpt: "Puntos a considerar para escribir código reproducible. Persona escribiendo kanji en Hanami, Jardín Botánico, Viña del Mar, V región de Chile (2019) [@joseidg9](https://www.instagram.com/joseidg9/)"
layout: single
subtitle: Puntos a considerar para escribir código reproducible
title: Buenas prácticas de escritura de código R
---

## Rendering mathematical equations

Examples from the [mathjax demo](https://www.mathjax.org/#demo).
But they work with `katex` as well.

### Rmarkdown

In `.Rmarkdown` documents, you can use either

```
$a \ne 0$
```

to get inline math: `\(a \ne 0\)`.
There is no conflict with using dollar symbols regularly, because `knitr` automatically escapes freestanding dollar symbols.

And you can use

```
$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
```

to get a math paragraph:

$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$

### md

In `.md` documents, you can **not** use the single dollar syntax.
The double dollar syntax still gives you a math paragraph.

```
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
```

$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$

In order to get inline equations, use:

```
`\(a \ne 0\)`
or
\\(a \ne 0\\)
```

to get: `\(a \ne 0\)`.



