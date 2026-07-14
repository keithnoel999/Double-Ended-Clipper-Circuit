## Double-Ended Clipper Circuit

## Overview

This project demonstrates the design and simulation of a **biased double-ended clipper circuit using Multisim**.

The circuit uses two silicon PN junction diodes and DC bias voltage sources to limit both the positive and negative peaks of an AC input signal. The clipping levels are determined by the applied DC bias voltages and the forward voltage drop of the diodes.

The project demonstrates the practical operation of diode clipping circuits and their use in waveform shaping, signal conditioning, and voltage limiting applications.

---

## Objective

To design and simulate a biased double-ended clipper circuit and analyze the clipping of both positive and negative portions of an AC input waveform.

---

## Software Used

- Multisim

---

## Components Used

| Component | Specification |
|-----------|---------------|
| AC Signal Generator | XFG1 |
| Series Resistor R1 | 1 kΩ |
| Diode D1 | 1N4007 |
| Diode D2 | 1N4007 |
| DC Bias Source V1 | 2.5 V |
| DC Bias Source V2 | 2.5 V |
| Load Resistor R2 | 10 kΩ |
| Oscilloscope | XSC1 |

---

## Circuit Description

The circuit consists of an AC signal generator connected to the clipping network through a 1 kΩ series resistor.

Two 1N4007 silicon diodes are connected in opposite directions to clip the positive and negative portions of the input waveform.

Two 2.5 V DC sources provide biasing to the diodes and determine the clipping voltage levels.

A 10 kΩ resistor acts as the load resistor, and the output voltage is measured across it.

An oscilloscope is used to observe and compare the input and output waveforms.

---

## Working Principle

A double-ended clipper circuit limits both the positive and negative peaks of an input signal when the voltage exceeds predefined levels.

The two oppositely connected diodes control the positive and negative clipping action.

### Positive Half Cycle

When the input voltage exceeds the positive clipping level:

```text
+(Vbias + Vdiode)
```

Diode D1 becomes forward biased.

The excess voltage is diverted through D1 and the DC bias source V1 to ground.

As a result, the output voltage is limited at the positive clipping level.

For a silicon diode:

```text
Vclip ≈ Vbias + Vdiode
```

Assuming a diode forward voltage of approximately 0.7 V:

```text
Vclip ≈ 2.5 V + 0.7 V

Vclip ≈ +3.2 V
```

Therefore, the positive peak is approximately clipped at +3.2 V.

### Negative Half Cycle

When the input voltage goes below the negative clipping level:

```text
-(Vbias + Vdiode)
```

Diode D2 becomes forward biased.

The excess negative voltage is diverted through D2 and the DC bias source V2.

The output voltage is limited at the negative clipping level.

Therefore:

```text
Vclip ≈ -(2.5 V + 0.7 V)

Vclip ≈ -3.2 V
```

The negative peak is approximately clipped at -3.2 V.

---

## Output Waveform

The output waveform is limited at both the positive and negative voltage levels.

The waveform appears flattened at the top and bottom when the input voltage exceeds the clipping limits.

Approximate clipping levels:

```text
Positive Clipping Level ≈ +3.2 V

Negative Clipping Level ≈ -3.2 V
```

This confirms the operation of the biased double-ended clipper circuit.

---

## Role of Components

### AC Signal Generator

Generates the sinusoidal input waveform applied to the clipper circuit.

### Resistor R1 – 1 kΩ

The resistor is connected in series with the input signal.

It limits the current flowing through the diodes and protects them from excessive current.

### Diodes D1 and D2 – 1N4007

The silicon PN junction diodes perform the clipping operation.

D1 controls positive clipping, while D2 controls negative clipping.

### DC Bias Sources V1 and V2

The 2.5 V DC sources provide biasing to the diodes.

They determine the positive and negative clipping voltage levels.

### Load Resistor R2 – 10 kΩ

The load resistor provides the output path.

The output voltage is measured across this resistor.

### Oscilloscope

The oscilloscope displays the input and output waveforms and is used to observe the clipping action.

## Conclusion

The biased double-ended clipper circuit was successfully designed and simulated using Multisim.

The circuit limits both the positive and negative peaks of the AC input waveform using two oppositely connected 1N4007 diodes and 2.5 V DC bias sources.

The output waveform demonstrates clipping at both the positive and negative voltage levels, confirming the expected operation of the double-ended clipper circuit.

This project demonstrates the practical use of diode circuits for waveform shaping, signal conditioning, and voltage limiting applications.
