# vue3-absurd-product-fix

Consider the following data:
``` js
[
  {
    a1: "Phone",
    b1: "Apple iPhone 13",
    c1: 999,
    d1: "https://example.com/iphone-13.jpg",
  },
  {
    a1: "Laptop",
    b1: "Dell XPS 15",
    c1: 1499,
    d1: "https://example.com/dell-xps-15.jpg",
  }
]
```

By keeping the original data as it is, create a vue3 computed property that fixes the absured keys with proper keys as follows:
```
a1: category
b1: name
c1: price
d1: imageUrl
```

Display list of products how ever you like on the screen by using the proper keys only.
