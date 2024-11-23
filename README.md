# Elemental-swordtail
Come to me beautiful sinner

![buh](https://github.com/nicolasbaez/Elemental-swordtail/blob/main/xp043.gif)
```javascript
setup = (_) => createCanvas((w = 500), w);
draw = (_) => {
  a = 255;
  b = 99 * noise(w);
  background(0, 8);
  beginShape();
  fill(a, b, b);
  stroke(a, 32 * noise(w), a);
  for (i = -0.03; i < 6.3; i += 0.03) {
    r = w * 0.4;
    curveVertex(
      r * noise(i) * sin(map(i, -0.03, 6.3, 0, PI)) * cos(i + w) + a,
      r * sin(i + w) + a
    );
  }
  endShape();
  if (w == 500) saveGif("xp043.gif", 1256, { delay: 0, units: "frames" });
  w -= noise(w) * 0.01;
};
