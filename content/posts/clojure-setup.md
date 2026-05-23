+++
title = "Setup Clojure"
date = "2026-05-23"
[taxonomies]
tags=["Software Engineering"]
+++

Let's set up clojure and run our first clojure program.

### Download Clojure

Follow this official guide to install the `clj` and `clojure` binaries. For now we just need those 2. Once you're all done, come back and lets move on to the next section.

### Running our first program

Let's create an empty directory to hold all our clojure source code

```
mkdir hello-world
cd hello-world
mkdir src
touch hello.clj
```

`hello.clj`

```
(ns hello)

(defn run [opts]
  (print "Hello from Clojure!"))
```

Finally run this command from the root of the `hello-world` directory `clj -X hello/run`

You should see the output:
`Hello from Clojure!`

Congratulations on running your first Clojure program!
