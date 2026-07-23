# Unidad 1
## Actividad entregable 1 - arreglo musical en strudel
```javascript
setcpm(80/4)
let beat = stack(
   s("oh").beat("5, 7, 11, 13", 16),
   s("hh").beat("0, 4, 6, 8, 10, 12, 14", 16),
   s("cp").beat("1, 5, 8, 11, 14, 15", 16),
   s("bd").beat("0, 4, 7, 10, 13", 16)
).bank("RolandTr909")

let bass = note("<c2 c2 f2 g2>")
   .sound("sawtooth")
   .lpf(400)
   .sustain(0.3)
   .gain(0.8)

let harmony = chord("<Am7 F G G>")
   .voicing()
   .s("gm_epiano1")
   .room(0.5)
   .gain(0.6)

let melody = note("c4 e4 g4 ~ a3 ~ c4 d4 ~ e4 ~ g4 f4 ~ d4 ~")
   .sound("piano")
   .legato(1)
   .gain(0.9)

let effects = note("<c5 e5 f5 g5>")
   .sound("piano")
   .delay(0.5)
   .delaytime(0.375)
   .delayfeedback(0.4)
   .lpf(slider(1925.4, 300, 3000))
   .gain(0.85)

$: beat
$bass: bass
$harmony: harmony
$melody: melody
$effects: effects
```

# Unidad 2
