+++
title = "Zola blog setup"
date = 2026-02-03
+++

## How to setup a blog with Zola

So I just setup this blog with [zola](https://www.getzola.org/), a fantastic cmd line tool that got everything up very quickly. Honestly, their docs were the best resource so head over there and follow the [overview](https://www.getzola.org/documentation/getting-started/overview/).

The one twist that I needed to do some more googling was applying my scss to my html. The way I did it is you add this line  
`<link rel="stylesheet" href="{{ get_url(path='styles.css') | safe }}" />` to your `base.html`  
and in your sass directory should inclde a styles.scss which should look like  
```
@use "base";

```  
and you would have a `base.scss` file which would have your css rules that you want to apply to your elements:  
`base.scss`
```
$font-stack: Helvetica, sans-serif;
@import url('https://fonts.googleapis.com/css2?family=Noto+Naskh+Arabic:wght@400..700&family=Scheherazade+New:wght@400;500;600;700&display=swap');
body {
  font: 100% $font-stack;
  background-color: #fdf6e3;
}
.container {
  max-width: 65ch;
  margin-inline: auto;
  padding-inline: 1.5rem;
  border-left: 3px dashed #93a1a1;
  border-right: 3px dashed #93a1a1;
  
  p {
    border: 1px solid #eee8d5;
    padding: 1rem;
    border-radius: 4px;
  }
}

.arabic {
  font-size: 1.5rem;
  font-family: 'Scheherazade New', sans-serif;
  font-weight: 600;;
}

```  

That's all for now for my first blog. 👋