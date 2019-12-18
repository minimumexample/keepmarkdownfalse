--- 
title: "Can't get rid of .md files"
---

# `new_session: yes` example

The contents of `_bookdown.yml` are:


```
output_dir: docs
new_session: yes
delete_merged_file: true
```

and the contents of `_output.yml` are:


```
bookdown::gitbook:
  keep_md: false
```

yet [`docs/index.md`](https://github.com/minimumexample/keepmarkdownfalse/blob/master/docs/index.md) remains after rendering.

The same is the case with

`bookdown::render_book("index.Rmd", new_session = TRUE, clean = TRUE)`
