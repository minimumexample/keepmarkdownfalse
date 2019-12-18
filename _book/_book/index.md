--- 
title: "Can't get rid of .md files"
---

# new_session: yes example

The contents of `_bookdown.yml` are:


```
new_session: yes
```

and the contents of `_output.yml` are:


```
bookdown::gitbook:
  keep_md: false
```

yet `_book/index.md` remains after rendering.

The same is the case with

`bookdown::render_book("index.Rmd", new_session = TRUE, keep_md = FALSE)`
