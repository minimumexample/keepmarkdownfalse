--- 
title: "Can't get rid of .md files"
---

# `new_session: yes` example

I am using `new_session: yes` for the [“Knit and Merge” (K-M) approach](https://bookdown.org/yihui/bookdown/new-session.html) to book rendering.  I do not want to keep `.md` files but I can't find a way to get rid of them.

The contents of the [`_bookdown.yml`](https://github.com/minimumexample/keepmarkdownfalse/blob/master/_bookdown.yml) file are:


```
output_dir: docs
new_session: yes
delete_merged_file: true
edit: https://github.com/minimumexample/keepmarkdownfalse/edit/master/%s
view: https://github.com/minimumexample/keepmarkdownfalse/blob/master/%s
```

and the contents of the [`_output.yml`](https://github.com/minimumexample/keepmarkdownfalse/blob/master/_output.yml) file are:


```
bookdown::gitbook:
  keep_md: false
```

yet [`docs/index.md`](https://github.com/minimumexample/keepmarkdownfalse/blob/master/docs/index.md) remains after rendering.

(`keep_md: false` shouldn't be necessary but tried it just in case. It didn't help.)

The same is the case with

`bookdown::render_book("index.Rmd", new_session = TRUE, clean = TRUE)`

