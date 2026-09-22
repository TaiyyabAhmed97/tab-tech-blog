+++
title = "Intermediate concepts in Kotlin"
date = "2026-09-22"
[taxonomies]
tags=["Software Engineering", "Intermediate Kotlin"]
+++

This series will go through intermediate concepts in Kotlin in my own words. I have learned all these from the [official kotlin docs](https://kotlinlang.org/docs/kotlin-tour-intermediate-extension-functions.html)

### Scope functions
These are little niceties that are included in the language that make your code a bit more consise and nicer to read. (`let`, `apply`, `run`, `also`, `with`)

### let
the let keyword *lets* you check a field or value before using it in case its null. lets take a look at some examples
lets say you have an `Item` and you need to retrieve data about it from a function or method `retrieveItem` this could represent a db lookup or http call or some interaction with code whose implementation you dont control.
```
data class Item(val name: String, val height: Number?, val weight: Number?)
val item = retrieveItem(name)
// at this point, we can only use item if its not null, otherwise we cant use it further in our code
val item = retrieveItem("fdasf")
val someCalculation = item?.let {
    applyFurtherAction(it)
}
```

So in essence, the `let` function allowed us to create a mini scope where the value of `item` could not be null and then apply actions to it there.

### apply
very typically we want to apply many actions to an class/model at the time of its creation. for example an `order` could never be created empty, there must be certain requirements at its createion, like a customer attached to it, the set of products that they wish to purchase, any other discounts or other data that must be present at the time of the creation of an order.
using `apply` we could do something like
```
    val order = Order().apply {
        setCustomer()
        setProducts(listOf(Prodcut("fds", 1)))
        retrieveDiscounts()
        attachProductMetadata()
    }
```