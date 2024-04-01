# Digital Circuit Design Project
# Overview
This GitHub repository contains a comprehensive project on digital circuit design. The main focus of this project is to understand and design circuits, particularly Up and Down Counter Circuits, alongside in-depth research on Seven Segment Displays and Counters.

## Objective

The main objective of this report is to understand and design circuits with designing
steps. Additionally, research about the seven-segment display and counters.

## Introduction

This project is about designing an Up and Down Counter Circuit presented on the complete
logic diagram with Design steps. Also, research on seven-segment displays and two different
types of seven-segment displays. And lastly, counters and their application and types.

## Seven Segment Display

Each of the decimal numbers (from 0 to 9) is represented by its equivalent binary pattern
in the Binary Coded Decimal (BCD) encoding technique (which is generally of 4-bits).

As opposed to this, a Seven-segment display is an electrical gadget that uses seven Light
Emitting Diodes (LEDs) organized in a certain pattern (common cathode or common anode
type) to show Hexadecimal numbers (in this case decimal numbers, as input is BCD i.e., 0-9).

Two different seven-section LED display types:


* Common Cathode type: In this type of display, each of the seven LEDs cathodes is
connected to the ground or -Vcc (thus, common cathode), and when a "HIGH" signal is
applied to each individual anode, the LEDs show numbers.


* Common Anode type: In this type of display, all seven of the LEDs' anodes are
connected to a battery or +Vcc, and the LEDs display numbers when the individual
cathodes get a "LOW" signal.

However, the seven-segment display does not function by directly applying power to the various
LED segment segments. Our decimal number is converted to its BCD equivalent signal first, and
that signal is then transformed by a BCD to seven-segment decoder into the form that is sent to
the seven segment display.

This BCD to seven-segment decoder includes four input lines (A, B, C, and D) and seven output
lines (a, b, c, d, e, f, and g). This output is provided to a seven-segment LED display that shows
the decimal number based on inputs.

![](https://github.com/Raiyan-S/Up-Down-Counter/blob/main/BCD.png)

## Counters

A counter is a device that counts the occurrences of a specific event or process and, on
occasion, displays that information, frequently in relation to a clock signal.

In digital electronics, counters are used for counting purposes. They can count a specific event
that occurs in the circuit.
For instance, in a UP counter, the count rises with each rising edge of the clock. A counter can
follow a specific sequence based on our design, such as any random sequence 0,1,3,2..., in
addition to counting. Flip-flops can also be used in their creation.

## Types of Counters

Counters consist of flip-flop arrangement; counters are useful for digital clocks and timers:

### Asynchronous Counter


* In the Asynchronous Counter, also known as the Ripple Counter, different flip flops are
triggered with different clocks, not simultaneously.

* The number of flip-flops used in a ripple counter depends on the number of counter
positions e.g.(Mod 4, Mod 2, etc.). The number of output states of the counter is called
the "Modulus" or "MOD" of the counter. The maximum number of states a counter can
have is 2n, where n is the number of flip-flops used in the counter.

For example, if we have 2 flip-flops, the maximum number of counter outputs is 4, i.e.22.
So, it is called "MOD-4 counter" or "Modulus 4 counter".

### Synchronous Counter

* Unlike asynchronous counters, in the synchronous counter, all flip-flops are activated
simultaneously with the same clock and the synchronous counter runs faster than the
asynchronous counter.

* The result of this synchronization is that all the individual output bits changing state at
the same time in response to the common clock signal with no ripple effect and therefore,
no propagation delay.

## Application of Counters

### 1 - Asynchronous Counter.

```
Used as frequency dividers.
Used for low noise emission and low power applications.
Used in designing asynchronous decade counter.
```
### 2 - Synchronous Counter.

```
Alarm.
Television.
Air conditioner.
```
### 3 - Asynchronous Decade Counter.

```
Clock circuit.
Frequency dividers.
State machine.
```
### 4 - Synchronous Decade Counter.

```
Count sequence.
Registers.
VCR clock.
```
## Design Steps (Counter-Up/Down)

![](https://github.com/Raiyan-S/Up-Down-Counter/blob/main/Pins%20and%20Functions.png)

```
1 - Implement two 4-bit counting registers.
2 - Implement two 4-bit LED displays.
3 - Implement UP counter toggle switch.
4 - Implement a Down counter toggle switch.
5 - Implement a Pause toggle switch.
6 - Implement a Reset toggle switch.
7 - Connect each of the 4-bit counting register outputs to their 4-bit LED display.
8 - Connect the Reset toggle switch with inverse and all other switches to the NOR gate into 4-bit
counting register reset slot, same for the other register.
9 - Connect UP, Down, and Pause switches to the XOR gate into a 4-bit counting register count enable
slot, same for the other register.
10 - Connect UP, Pause switches to XOR into 4-bit counting register count UP/Down slot,
same for the other register.
11 - Connect the up 4-bit register output 0-2 to AND gate to the down 4-bit register with
NOR gate into Reset slot.
12 - Connect the down 4-bit register output 0-3 to AND gate to the up 4-bit register connected
with NOR gate into the Reset slot.
13 - Connect the down 4-bit register output 0, 1, 2, 3 to NORX gate into the left 4-bit register
leading-edge trigger.
14 - Connect the clock pulse to the down 4-bit register leading-edge trigger.
15 - Set up 4-bit register parameters maximum count 5.
16 - Set down 4-bit register parameters maximum count 9.
```
## Circuit layout and implementation

![](https://github.com/Raiyan-S/Up-Down-Counter/blob/main/Circuit%20layout.png)

## Test

![](https://github.com/Raiyan-S/Up-Down-Counter/blob/main/CedarLogic.gif)

## Conclusion

Seven Segment display:
As an alternative to the more complicated dot matrix displays, a seven-segment display is
a type of electronic display device for displaying decimal numerals.
Digital clocks, electronic meters, simple calculators, and other electronic devices that display
numerical data frequently employ seven-segment displays.

Counter:
A counter is one of the more common flip flops, it is a type of sequential circuit which
uses pulses to generate an output in a given time using a feedback function from previous states.

Difference between synchronous and asynchronous counter:
The following are some distinctions between synchronous and asynchronous counters:

* Synchronous counters are faster than asynchronous counters due to superior clocking.

* In a synchronous counter, each flip-flop is activated simultaneously by the same clock,
whereas in an asynchronous counter, each flip-flop requires a different clock, which
prevents parallel operation.

* An asynchronous counter is straightforward to construct, whereas a synchronous counter
has numerous states and is therefore complex and challenging to create.

* In synchronous counters, propagation delay—the amount of time it takes a signal to
travel from one end to the other of the counter or circuit—is reduced.

* As opposed to an asynchronous counter, a synchronous counter is more adaptable.

Circuit layout and implementation:
The counter circuit layout is functioning as intended from 0 to 60 and vice versa. The same
goes for the toggle switches.

## References

Retrieved from [ELPROCUS](https://www.elprocus.com/different-types-of-digital-logic-circuits/)

Retrieved from [WIKIBOOKS](https://en.wikibooks.org/wiki/Digital_Circuits/Digital_Circuit_Types)

Retrieved from [ELPROCUS](https://www.elprocus.com/what-is-digital-circuit-design-and-its-applications/)

Panigrahi, K. K. Retrieved from [tutorialspoint](https://www.tutorialspoint.com/difference-between-synchronous-and-asynchronous-counter)

rajkumarupadhyay515. Retrieved from [geeksforgeeks](https://www.geeksforgeeks.org/seven-segment-displays/)


## Contributing
Contributions to this project are welcome! If you have suggestions for improvements, additional resources, or corrections, please feel free to submit a pull request or open an issue.

## License
This project is licensed under the MIT License, granting permission for anyone to use, modify, and distribute the code and resources included, provided the original license and copyright notices are retained.

