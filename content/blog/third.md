+++
title = "Arabic font setup for html/css"
date = 2026-02-03
+++

## Add Arabic font setting in yout html/css

I ran into the issue of setting my specific arabic font on my blog. Here are some steps you can use to setup arabic for your html/css page.
1. you need to add this line inside your `<head>` tag so that the browser will know how to render those characters  
  `<meta charset="utf-8">`  
  
2. go to https://fonts.google.com/ and find the font you want then just embed that into your css
3. you can use it in your css as you would any english font:  
```
.arabic {
  font-size: 1.5rem;
  font-family: 'Scheherazade New', sans-serif;
  font-weight: 600;;
}
```