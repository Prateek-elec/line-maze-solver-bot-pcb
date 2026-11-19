<div align="center">

<img src="docs/banner.png" alt="Line & Maze Solver PCB" width="100%"/>

**A plug-in carrier board for competition line-follower and maze-solving robots: Arduino Nano, TB6612FNG dual motor driver, IR sensor array input and start / calibrate buttons on one clean PCB.**

![Arduino](https://img.shields.io/badge/Arduino-Nano-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![Motor driver](https://img.shields.io/badge/TB6612FNG-dual%20H--bridge-ef4444?style=for-the-badge)
![Robotics](https://img.shields.io/badge/robotics-competition-8b5cf6?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge)

</div>

---

## Highlights

- 🏁 **Competition-ready:** built for line-follower and maze-solving events.
- 🔌 **Plug and race:** drop in an Arduino Nano and a TB6612FNG, plug in sensors and motors.
- 🧹 **No jumper-wire nest:** one PCB instead of a breadboard that falls apart mid-run.
- 📘 **Wiring guide included:** battery advice, checklist and common fixes.

## The problem it solves

Breadboard robots fall apart on the track. This board replaces the jumper-wire nest with a single PCB: drop in an Arduino Nano and a TB6612FNG module, plug in the IR array and motors, and you're racing.

## Features

- **Arduino Nano** socket
- **TB6612FNG** dual motor driver module socket (two DC motors, PWM speed + direction)
- **IR sensor array** connector (5 V, GND + 5 analog inputs)
- Motor A / Motor B output headers
- **Battery input** with screw terminal, plus 12 V → 9 V and 12 V → 5 V regulator module headers
- **SW1 / SW2** push buttons (start, mode select or sensor calibration)
- Status LED

## Design

<table>
<tr>
<td width="50%"><img src="docs/images/schematic.png" alt="Schematic"/><br/><sub><b>Schematic</b></sub></td>
<td width="50%"><img src="docs/images/pcb-layout.png" alt="PCB layout"/><br/><sub><b>PCB layout</b></sub></td>
</tr>
</table>

## Wiring

Full connection guide, battery recommendations, a pre-power checklist and common fixes: **[docs/wiring_notes.md](docs/wiring_notes.md)**

## Roadmap

- [x] Schematic + PCB layout
- [ ] Gerbers committed to the repo
- [ ] Example line-following + maze-solving (LSRB) Arduino sketch
- [ ] Photos / video of the bot on a track

## License

[MIT](LICENSE) © Prateek Sarkar

---

<div align="center">

### Found this useful?

**Drop a ⭐ so more builders find it, and share it with someone who'd build one.**

[![Share on X](https://img.shields.io/badge/share%20on-X-000000?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/intent/tweet?text=No%20more%20jumper-wire%20nests%3A%20a%20clean%20PCB%20for%20maze-solving%20robots%20%F0%9F%A4%96&url=https%3A%2F%2Fgithub.com%2FPrateek-elec%2Fline-maze-solver-bot-pcb)
[![Share on LinkedIn](https://img.shields.io/badge/share%20on-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fgithub.com%2FPrateek-elec%2Fline-maze-solver-bot-pcb)
[![Follow](https://img.shields.io/badge/follow-@Prateek--elec-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Prateek-elec)

</div>
