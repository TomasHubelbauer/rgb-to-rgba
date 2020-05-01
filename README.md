# RGB to RGBA

```js
/** @type {Uint8ClampedArray} */
const rgb = …;
const rgba = new Uint8ClampedArray((rgb.length / 3) * 4);
for (let index = 0; index < rgba.length; index++) {
  // Set alpha channel to full
  if (index % 4 === 3) {
    rgba[index] = 255;
  }
  // Copy RGB channel components from the RGB array
  else {
    rgba[index] = rgb[~~(index / 4) * 3 + (index % 4)];
  }
}
```
