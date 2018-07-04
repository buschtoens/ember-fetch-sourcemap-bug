# ember-fetch: source map bug

This demos shows how installing `ember-fetch` will kill source maps for minified
files.

```
# => "sources":["0"]
ember build -prod && head -c 500 ./dist/assets/vendor*.map 

# => "sources":["vendor/ember-cli/vendor-prefix.js", ...
yarn remove ember-fetch && ember build -prod && head -c 500 ./dist/assets/vendor*.map
```
