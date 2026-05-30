+++
title = "clojure Overview"
date = "2026-05-23"
[taxonomies]
tags=["Software Engineering"]
+++

This is my own overview of the language and its related tools for my own reference and for anyone. I was heavily inspired by the amazing [overview](https://odin-lang.org/docs/overview/) provided by the authors of the Odin programming language.

### Overview

- When `doc` and `apropos` and `source` are not loading in the repl, then its almost always because you did not load in those functions in the repl instance. To do that run `use 'clojure.repl`

- When `(-main)` is throwing an error, just select the whole file and run the vs code calva command to 'evaluate current selected form'

- using a `case` statement to compare against characters, you need to do backslash the character in the condition part of the form, eg:

```
(case passed-in
    \( (println "LEFT_PAREN ( null")
    \) (println "RIGHT_PAREN ) null")
)
```

- Use `doseq` to loop through any kind of sequence

- Caveat on the above `doseq` tip, it would be more functionally apropritate to instead use `map` in many cases. As all we are doing is taking a list of things, evaluating each item to do something(modify, print, whatever) and then collect those results of those evaluations into an equivalently sized list.
