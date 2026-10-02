# Autonomous 3-Wheel Car

An autonomous three-wheeled car built from scratch, developed across three
prototypes under Romania's **Tinerii Cercetatori** (Young Researchers) program.

Everything physical is modelled in OnShape and 3D-printed locally: the chassis,
the servo stand, and the gear sets that turn the steering servo into usable
torque. Control runs on an Arduino Nano alongside an ESP32, with an ESP32-CAM for
vision and an ultrasonic sensor for obstacle detection.

---## Hardware

### Electronics

| Component | Role |
|---|---|
| Arduino Nano | Main control board |
| ESP32 | Secondary controller |
| ESP32-CAM | Vision |
| DC motors + wheels | Drive |
| Servo motor | Steering |
| Ultrasonic sensor | Obstacle detection |
| Driver module | Motor driver (L298N-style) |

Datasheets for the DC motors are included in
[`Hardware/Parts_list/DC motors&wheels`](Hardware/Parts_list).

### 3D-printed parts

Designed in OnShape and printed in parts — the STL sources are all here.

| File | Part |
|---|---|
| `baza.stl` | Chassis / base plate |
| `picioruse.stl` | Legs |
| `servo stand.stl` | Servo mount |
| `shield.stl` | Electronics shield |
| `gears - gear motor.stl` | Gears for the gear motor |
| `gears - gear servo.stl` | Gears for the steering servo |

## The steering mechanism

A plain servo does not have enough torque to turn a wheel on the ground, so
`Mechanism/Direction Mecanism` documents a reduction stage built from printed
gears and a three-plank linkage. `Gears/` holds side-by-side video of the real
gears and a simulation of the ratio, which is how the tooth count was chosen.

The first attempt is kept under `3 planks linkage (first try)` for comparison.

## Repository layout

```
Docs/
  Images/                     photos of each prototype
  Videos/                     build and testing footage
Hardware/
  Parts_list/                 full BOM, datasheets, board choice
  3D printed parts/           STL sources for every printed component
Mechanism/
  Direction Mecanism/
    3 planks linkage (first try)/
    Gears/                    real vs simulated gear ratio
```

## CAD

The full assembly is modelled in OnShape and is publicly viewable:

**[3D module of the car →](https://cad.onshape.com/documents/ff636740be168123f48758d5/w/d57728c19c89ce734805763d/e/8b3c496aefd2b781c6376e6f?renderMode=0&uiState=68da711b1f2368f0e61ee5ec)**

## Resources

Tutorials I worked through while learning the tools:

- [OnShape beginner tutorial](https://www.youtube.com/watch?v=pMWnsHpDlQE&list=PLxmrkna-ixrIQmsPR3MITi4Ru1bnMH4-l)
- [Arduino beginner tutorial](https://www.youtube.com/watch?v=JnJIKX5J0Cc&list=PLwWF-ICTWmB7-b9bsE3UcQzz-7ipI5tbR)
