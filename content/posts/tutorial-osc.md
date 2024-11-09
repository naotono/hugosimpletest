+++
date = '2024-11-09T13:11:01+09:00'
draft = false
title = 'Tutorial Osc'
ShowToc = true
TocOpen = true
+++

## Phasor Wave

### genを使ったPhasor Wave
![alt](/images/phasor.png)

---

### Codeboxを使ったPhasor Wave
```
History h;
sr = samplerate;
freq = in1;
delta = freq / sr;

y = h + delta;
y = y % 1;
h = y;

out1 = y;
```
---

## Sin Wave

### genを使ったSin Wave

---

### Codeboxを使ったSin Wave
```
History h;
sr = samplerate;
freq = in1;
delta = freq / sr;

y = h + delta;
y = y % 1;
h = y;

y = sin(y * twopi);

out1 = y;
```

---

## Rectangle
### genを使ったRectangle Wave

---

### Codeboxを使ったRectangle Wave
```
History h;
sr = samplerate;
freq = in1;
delta = freq / sr;

y = h + delta;
y = y % 1;
h = y;

y = (y > 0.5) ? 1 : -1;

out1 = y;