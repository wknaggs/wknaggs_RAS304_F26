---
title: Component Selection 
---

## Motor Power Control System

1. H-Bridge PWM

    * $0.89/each
    * Amazon Link H-Bridge

    | Pros | Cons |
    | --- | --- |
    | Inexpensive | Heat |
    | Can be run with PWM | Motor wear |

2. Low Pass Filter PWM with H-Bridge

    * $0.99/each
    * Amazon Link H-Bridge

    | Pros | Cons |
    | --- | --- |
    | Cheap | Heat |
    | Changes PWM to constant lower voltage | Higher power drain for battery |

3. MOSFET

    * $0.99/each
    * Amazon MOSFET

    | Pros | Cons |
    | --- | --- |
    | Simple | Unidirectional |
    | Cheap | No brake for motor |

**Choice:** Option 2: Low Pass Filter PWM with H-Bridge

**Rationale:** The low pass filter with an h-bridge is simple to implement while also being cost effective and meeting all the requirements for controlling the motor speed and precision. While it does suffer from the greater heat and wasted power it does not put extra wear on the motor like just PWM with an h-bridge and it can fully control the motor unlike only a single MOSFET.

---

## LED Error Code System

1. Single RGB LED

    * $0.09/each
    * Amazon RGB LED

    | Pros | Cons |
    | --- | --- |
    | Simple | Potential issues for colorblind users |
    | Easy to implement with each color representing an error | Additional wiring |

2. 3 Single Color LEDs

    * $0.18/set of 3
    * Amazon LED

    | Pros | Cons |
    | --- | --- |
    | Many possible states with on, off, or flashing | Additional wiring and pins used |
    | Clear to user | More space |

3. Single Flashing LED

    * $0.06/each
    * Amazon LED

    | Pros | Cons |
    | --- | --- |
    | Simplest design | Harder to tell specific codes with flashes |
    | Cheapest | |

**Choice:** Option 2: 3 Single Color LEDs

**Rationale:** The 3 single color LEDs are simple to implement and have 27 different possible combinations. The 3 LEDs are the most expensive and use the most pins on the microcontroller, but despite this, the additional information provided to the user will be far more valuable than the potential lost uses for those pins and space.

---

## Watchdog Timer

1. Internal Watchdog Timer

    * No cost already on Curiosity Nano

    | Pros | Cons |
    | --- | --- |
    | Simple | Vulnerable to system wide failure |
    | Cheap | Potential debugging issues |

2. External Watchdog Timer

    * $1.77/each
    * Digikey Watchdog Timer

    | Pros | Cons |
    | --- | --- |
    | Independent from microcontroller | More expensive |
    | Hardware shutdown capability | Additional board space |

3. Windowed Watchdog Timer

    * Already on Curiosity Nano

    | Pros | Cons |
    | --- | --- |
    | Strict timing | Higher complexity |
    | Catches loops | Possible debugging issues |

**Choice:** Option 3: Windowed Watchdog Timer

**Rationale:** The windowed watchdog timer will not take up additional board space and will allow for more accurate catching of issues. Despite the higher software complexity the additional functionality will help users to detect issues before they cause permanent problems.