# Safety Standards

## SCS Signals Compliance

- Detection of disconnection of signal
- Short-circuit of signal to VCC
- Short-circuit of signal to Ground

Assuming the signal is carried in a cable harness, where if a signal is:

- Shorted to VCC
- Shorted to Ground
- Disconnected

the same will be applied to all signals in this cable harness.he proposed solution to this issue is to run the signal through a NOT gate, carrying both the inverted and normal signal in the same cable harness. Using the following non-programmable circuit, we can detect if the signal is implausible. Thus raising a connection fault flag, which can be dispalyed via a LED or a programmable display via a Microcontroller.

![img]()

## Appendix 2

Assuming there is more than 1 set of SCS data signals (ie. CANBUS), detection of wrong connection is also a potential issue.
The potential solution to this issue is to have a programmable circuit, sending a PWM signal from 1 end of the circular network, and detecting the same signal at the other end of the network. Each network will have its own assigned signal, varying based on freqency and pulse width.
This solution is able to detect:

- Short-circuit of signal to VCC
- Short-circuit of signal to Ground
- Disconnection of signal
- Connection of cable harness to the wrong network.
