# SVG to JSX 🌓
> Tiny module for transforming SVG to valid JSX

### Install ⚙

```
yarn add svg-to-jsx --dev
```

### Use 🛠

```
const fs = require('fs')
const path = require('path')
const transform = require('svg-to-jsx')

const filepath = path.resolve(__dirname, 'test.svg')

fs.readFile(filepath, 'utf8', (error, data) => {

  if (error) throw new Error('😞 Something went wrong')

  // transform but keep ids
  return transform(data, { cleanupIDs: false })
    .then(transformedSVG => console.log(transformedSVG))
    .catch(error => console.log(error))

})
```

### What it can do ✅

`svg-to-jsx` uses `svgo` and accepts all the config that are available in [`svgo`](https://github.com/svg/svgo#what-it-can-do)

```
tansform(someSVG, { cleanupIDs: false, convertPathData: true, ... })
```

### TODO 📝

- [ ] GUI