Arduino BogoMIPS Calculator
###########################
This program calculates your Arduino's BogoMIPS rating.

It provides a very crude rating for how efficient a processor is. 

Processors execute tasks at different speeds.  Per CPU cycle, some processors are more efficient than others, and BogoMIPS is a way of estimating that efficiency.


Example Output:
===============
On Arduino UNO, this program reports the following:

```
Arduino BogoMips calculator
===========================
Calculates number of times Ardunio can calculate a null instruction.
Emulates Linux 'BogoMips' speed calculation.

Waiting for clock to start...ok
Running loop...done
Time elapsed: 0.06038 seconds

CPU Speed: 16.00MHz
BogoMips: 16.5617752075
Rating: clock * 1.04
i386 rating comparison index: 5.75
===========================
For more information about BogoMIPS, see: https://en.wikipedia.org/wiki/BogoMips
```

Notable Ratings
================

| System  | Speed (MHz)  | BogoMIPS  | Rating  | Index  | 
| ------------- | ------------- |
| Arduino UNO         | 16    | 16.5   | clock * 1.04    | 5.75  |
| nRF51:822           | 16    | 2.24   | clock *  0.14   | 0.78  |
| ESP8266             | 80    | 15.9   | clock * 0.919   | 1.10  |
| _i886 (Reference)_  | _25_  | _4.5_  | _clock * 0.18_  | _1_   |

History and Usage
==================
BogoMIPS (Bogus Millions of Instructions Per Second) is the number of times a processor can execute a null instruction in a second.  They are rated against both the CPU speed (typically in mHz) and a known CPU, the i386.

It was invented by Linus Torvold for Linux to estimate if a CPU was working effectively, or was in turbo mode.  It has become a way for people who overclock their CPUs to win pissing competitions against others in online forums.
