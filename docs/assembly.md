# Assembly steps

All the boards use the same motor preparation and placement. The following section contains what you will need to assemble each board. Followed by specific assembly for the more complex boards.

## What you need for each board

### Buzz Simple boards a, b, c

For these boards you will only need a vibration motor.

![Simple (a) parts](./imgs/simple-a-parts.jpg)
![Simple (b) parts](./imgs/simple-b-parts.jpg)
![Simple (c) parts](./imgs/simple-c-parts.jpg)

### Buzz Breakout

The breakout board allows for two configurations.
(1) 220 ohm current limiting resistor (cut jumper JP1).
(2) flyback diode only (solder jumper JP1 if previously cut).

![Breakout parts](./imgs/breakout-parts.jpg)

#### BOM

| Qty | Value          | Package | Designator | Part number              |
| :-- | -------------- | ------- | ---------- | ------------------------ |
| 1   | 1N4148         | DO-35   | D1         | onsemi - 1N4148          |
| 1   | 220R, 1/4W, 1% | -       | R1         | YAGEO - MFR-25FBF52-220R |

### Buzz Driver

The driver board is designed to accommodate different sizes of resistors, and capacitors. The BS170 MOSFET could be replaced with other options that share the same pinout. For convenience the pins are marked drain (D), gate (G) and source (S).

![Driver parts](./imgs/driver-parts.jpg)

#### BOM

| Qty | Value                   | Package    | Designator | Part number              |
| :-- | ----------------------- | ---------- | ---------- | ------------------------ |
| 1   | .1uF, ceramic, 50V, 10% | Leaded 5mm | C1         | Vishay - K104K15X7RF5WH5 |
| 1   | 1N4148                  | DO-35      | D1         | onsemi - 1N4148          |
| 1   | 100R, 1/4W, 1%          | -          | R1         | YAGEO - MFR-25FBF52-100R |
| 1   | 10K, 1/4W, 1%           | -          | R2         | YAGEO - MFR-25FBF52-10K  |
| 1   | MOSFET BS170[^1]        | TO-92-3    | Q1         | onsemi - BS170           |

[^1]: Not all BS170 have the same pinout: original vs new have the gate and source flipped. We use the "original" pinout(Drain-Gate-Source). More information [here](https://www.ic-components.com/blog/the-ultimate-guide-to-n-channel-mosfets-key-applications-of-2n7000-and-bs170.jsp).

## Motor Preparation

Depending on the manufacturer of the motor, the motor wires vary in length. Step 2 can be omitted if the wires are already short.

1. Get your vibration motor
   ![Single vibration motor](./imgs/single-motor.jpg)
2. Cut the motor wires to a 1cm (2/5in) length
   ![Cutting wires](./imgs/cut-wires.jpg) ![Short wires](./imgs/short-wires.jpg)
3. Strip the motor wires around 0.4-0.5cm (1/5in) from the bottom
   ![Stripping wires](./imgs/strip-wire.jpg) ![Stripped motor wires](./imgs/stripped-motor-wires.jpg)

## Motor placement

This section shows how to place and solder the vibration motor for all the boards. The process is exactly the same for all of them. Different boards are through the steps in this section.

1. Remove the protective layer from behind the motor
   ![Removing protective layer](./imgs/remove-protection.jpg)
2. Insert the motor wires into the pad holes
   ![Insert motor wires into pad holes](./imgs/insert-motor-wires.jpg)
3. Align the motor to the circle outline on the PCB
   ![Aligning the motor with the circle outline](./imgs/align-motor.jpg)
4. Push the motor to the PCB
   ![Push motor](./imgs/push-motor.jpg)
5. Solder motor wires to the pad
   ![Soldering motor wires](./imgs/solder-motor.jpg)
6. Cut the excess wire
   ![Cut excess wire](./imgs/cut-excess.jpg)

> [!TIP]
> Use as little solder as possible and cut the excess wire flush for best results flat mounting.

## Buzz Breakout assembly

The resistor for the breakout board is optional. If you are going to use the resistor remember to cut the JP1 jumper (step 2).

1. Place the diode (align the indicator lines) and solder it
   ![Place the diode](./imgs/place-diode.jpg)
2. Cut excess diode leads
   ![Cut excess diode leads](./imgs/cut-diode-leads.jpg)
3. (optional) Cut the JP1 jumper if you are using the resistor
   ![Cut the JP1 jumper](./imgs/cut-jumper.jpg)
4. (optional) Placing the resistor
   ![Place R1 resistor](./imgs/resistor-placement.jpg)
5. (optional) Solder Resistor and cut the excess leads
   ![Solder resistor](./imgs/solder-resistor.jpg)

## Buzz Driver assembly

1. Bend the MOSFET leads 90 degrees
   ![Bend MOSFET leads 90 degrees](./imgs/bend-mosfet-leads.jpg)
2. Place the MOSFET (round side up) and solder it
   ![Place MOSFET with the round side up](./imgs/place-mosfet.jpg)
3. Place the diode D1 (align the indicator lines) and capacitor C1
   ![Place the diode D1 and capacitor C1](./imgs/place-c1-d1.jpg)
4. Place the Resistor R1(10K ohm) & R2(100 ohm) and solder
   ![Place the resistors R1 and R2](./imgs/place-r1-r2.jpg)
5. Cut excess leads from all the components
   ![Cut the excess leads from all the components](./imgs/driver-cut.jpg)

### Final result

![Driver final result](./imgs/driver-final.jpg)
