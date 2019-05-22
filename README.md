# slash_link_check

# example for chrome bookmarkbar
## codes
### change not trailing shashed link background into deep blue
```js
[...document.querySelectorAll("a")]
  .filter(e => e.href && e.href.length > 0)
  .filter(e => !e.href.split("?")[0].match(/\/$/))
  .map(e => {
    console.log(e.style.backgroundColor === "rgb(64, 64, 255)");
    if (e.style.backgroundColor === "rgb(64, 64, 255)") {
      e.style.backgroundColor = "";
    } else {
      e.style.backgroundColor = "rgb(64, 64, 255)";
    }
    return e;
  });
```

### change not trailing shashed link's parentNode background into deep blue
```js
[...document.querySelectorAll("a")]
  .filter(e => e.href && e.href.length > 0)
  .filter(e => !e.href.split("?")[0].match(/\/$/))
  .map(e => {
    console.log(e.style.backgroundColor === "rgb(64, 64, 255)");
    if (e.parentNode.style.backgroundColor === "rgb(64, 64, 255)") {
      e.parentNode.style.backgroundColor = "";
    } else {
      e.parentNode.style.backgroundColor = "rgb(64, 64, 255)";
    }
    return e;
  });
```

### alert not trailing shashed link count
```js
window.alert(
  `I found ${
    [...document.querySelectorAll("a")]
    .filter(e => e.href && e.href.length > 0)
    .filter(
      e => !e.href.split("?")[0].match(/\/$/)
    ).length
  }`
);
```
## how to use
replace some bookmark url to follows.

### change not trailing shashed link background into deep blue
```js
javascript:console.log([...document.querySelectorAll('a')].filter(e => e.href && e.href.length > 0).filter(e => !e.href.split('?')[0].match(/\/$/)).map(e => { console.log(e.style.backgroundColor === "rgb(64, 64, 255)"); if (e.style.backgroundColor === "rgb(64, 64, 255)") { e.style.backgroundColor = ""; } else { e.style.backgroundColor = "rgb(64, 64, 255)"; }; return e }));
```

### change not trailing shashed link's parentNode background into deep blue
```js
javascript:console.log([...document.querySelectorAll('a')].filter(e => e.href && e.href.length > 0).filter(e => !e.href.split('?')[0].match(/\/$/)).map(e => {console.log(e.style.backgroundColor === "rgb(64, 64, 255)");if (e.parentNode.style.backgroundColor === "rgb(64, 64, 255)") {e.parentNode.style.backgroundColor = "";} else {e.parentNode.style.backgroundColor = "rgb(64, 64, 255)";};return e}));
```

### alert not trailing shashed link count
```js
javascript:window.alert(`I found ${[...document.querySelectorAll('a')].filter(e => e.href && e.href.length > 0).filter(e => !e.href.split('?')[0].match(/\/$/)).length}`);
```

and click, click, click,,,
