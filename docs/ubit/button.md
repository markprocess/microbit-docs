#Buttons

##Overview

The micro:bit has two forward facing buttons either side of the display, `buttonA`
and `buttonB`. These are intuitively exposed on the [`MicroBit`](../ubit.md) object as `uBit.buttonA`
and `uBit.buttonB`. A third button, `uBit.buttonAB` is used to detect the combined
input of `buttonA` and `buttonB`, and is an instance of the class [`MicroBitMultiButton`](multibutton.md).

Hardware buttons are notoriously renowned for generating multiple open/close transitions
for what a user perceives as a single press, which can make depending on the raw input
of a button unreliable. To combat this, a technique called 'debouncing' is used, which
periodically polls the state of the button, when a transition from open to close
(and vice versa) is detected. Through periodically polling the button, we get a
more accurate representation of the state of a button.

`MicroBitButton`s and [`MicroBitMultiButton`](multibutton.md)s are debounced in
software and provide a number of events that can be used to detect different
variations of presses.

The `MicroBitButton` debouncing mechanism is used to provide resistive touch sensing on [`MicroBitPin`](io.md)s
and could also be used on external 'button-like' input if required.

##Message Bus ID
| Constant | Value |
| ------------- |-------------|
| MICROBIT_ID_BUTTON_A | 1 |
| MICROBIT_ID_BUTTON_B | 2 |

##Message Bus Events

| Constant | Value |
| ------------- |-------------|
| MICROBIT_BUTTON_EVT_DOWN | 1 |
| MICROBIT_BUTTON_EVT_UP | 2 |
| MICROBIT_BUTTON_EVT_CLICK | 3 |
| MICROBIT_BUTTON_EVT_LONG_CLICK | 4 |
| MICROBIT_BUTTON_EVT_HOLD | 5 |
| MICROBIT_BUTTON_EVT_DOUBLE_CLICK | 6 |

##API
[comment]: <> ({"className":"MicroBitButton"})
[comment]: <> ({"end":"MicroBitButton"})