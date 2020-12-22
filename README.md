
# Project Title

Final project for the Building AI course

## Summary

Predistortion for the amplifier could be the typical application for AI model.
The code shall calculate the factor to multiplies to the input value to make the output from the amplifier as desired


## Background

Amplifier has non-linear characteristics on the output especially higher input power range.
Also it will get errors across temperature and frequesncies.
Predistortion shall handle input value to adjust it before going into amplifier by considering those non-linearities and errors,
in order to get correct linear output from the amplifier.


## How is it used?

In the wireless communication such as telecommunication, IoT, connected vehicle etc, power of the signal shall be incrased before transmission.
Power amplifier shall take the role, but the signal will not reach correctly to the destination if expected amplified power can't be extracted.
To adjust and guarantee the quarity of the output from the amplifier, the factor for the predistortion to add the input value shall be estimated.
Estimated factor shall be multiplied to the input power value and let going through the amplifier,
and hopefully linearly amplified output power could be extracted.


## Data sources and AI methods
Training data could be extracted by testing actual amplifier input vs. output across the power, temperature, and frequency range.
Also it could be a closed loop to continuously get the output from the amplifier as the input to the next estimation.

| Input power | Frequency   | Temperature | Output power |
| ----------- | ----------- | ----------- | -----------  |
| Pin1        | F1          | T1          | Pout1        |
| Pin2        | F2          | T2          | Pout2        |
| :           | :           | :           | :            |

## Challenges

Different amplifier has different characteristics, but could be the meaningful estimation.
More training datas from variety of amplifers make the estimation more generic, but it might not good to specific device.

## What next?

This is the example just for the amplifier but in the wireless communication there are many linear process.
Propagation channel is the another example, and it has transmission signal as a input and muptiplies by channel matrix,
and added some interference signal and noises, and received signal as the output.
Estimating channel matrix is the important process to transmit/receive data efficiently/fast by adding calculated wieght
at both sender and receiver sides.
AI model could be applied to this kind of process too.


## Acknowledgments

Wireless communication and autonomous driving are the background of the inspiration.
In the both cases, bunch of set of input/output data would be extracted.
Thing is we need to analyse and clarify the blackbox in between input and output data,
so that we will be able to know many phsical characteristics there,
and use them for any applications.
