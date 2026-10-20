---
title: Component Selection
---

## Motor Power Control System

1. H-Bridge PWM[cite: 3]

    * $0.89/each[cite: 3]
    * Amazon Link H-Bridge[cite: 3]

    | Pros | Cons |
    | --- | --- |
    | Inexpensive[cite: 3] | Heat[cite: 3] |
    | Can be run with PWM[cite: 3] | Motor wear[cite: 3] |

2. Low Pass Filter PWM with H-Bridge[cite: 3]

    * $0.99/each[cite: 3]
    * Amazon Link H-Bridge[cite: 3]

    | Pros | Cons |
    | --- | --- |
    | Cheap[cite: 3] | Heat[cite: 3] |
    | Changes PWM to constant lower voltage[cite: 3] | Higher power drain for battery[cite: 3] |

3. MOSFET[cite: 3]

    * $0.99/each[cite: 3]
    * Amazon MOSFET[cite: 3]

    | Pros | Cons |
    | --- | --- |
    | Simple[cite: 3] | Unidirectional[cite: 3] |
    | Cheap[cite: 3] | No brake for motor[cite: 3] |

**Choice:** Option 2: Low Pass Filter PWM with H-Bridge[cite: 3]

**Rationale:** The low pass filter with an h-bridge is simple to implement while also being cost effective and meeting all the requirements for controlling the motor speed and precision. While it does suffer from the greater heat and wasted power it does not put extra wear on the motor like just PWM with an h-bridge and it can fully control the motor unlike only a single MOSFET.[cite: 3]

---

## LED Error Code System

1. Single RGB LED[cite: 3]

    * $0.09/each[cite: 3]
    * Amazon RGB LED[cite: 3]

    | Pros | Cons |
    | --- | --- |
    | Simple[cite: 3] | Potential issues for colorblind users[cite: 3] |
    | Easy to implement with each color representing an error[cite: 3] | Additional wiring[cite: 3] |

2. 3 Single Color LEDs[cite: 3]

    * $0.18/set of 3[cite: 3]
    * Amazon LED[cite: 3]

    | Pros | Cons |
    | --- | --- |
    | Many possible states with on, off, or flashing[cite: 3] | Additional wiring and pins used[cite: 3] |
    | Clear to user[cite: 3] | More space[cite: 3] |

3. Single Flashing LED[cite: 3]

    * $0.06/each[cite: 3]
    * Amazon LED[cite: 3]

    | Pros | Cons |
    | --- | --- |
    | Simplest design[cite: 3] | Harder to tell specific codes with flashes[cite: 3] |
    | Cheapest[cite: 3] | |

**Choice:** Option 2: 3 Single Color LEDs[cite: 3]

**Rationale:** The 3 single color LEDs are simple to implement and have 27 different possible combinations. The 3 LEDs are the most expensive and use the most pins on the microcontroller, but despite this, the additional information provided to the user will be far more valuable than the potential lost uses for those pins and space.[cite: 3]

---

## Watchdog Timer

1. Internal Watchdog Timer[cite: 4]

    * No cost already on Curiosity Nano[cite: 4]

    | Pros | Cons |
    | --- | --- |
    | Simple[cite: 4] | Vulnerable to system wide failure[cite: 4] |
    | Cheap[cite: 4] | Potential debugging issues[cite: 4] |

2. External Watchdog Timer[cite: 4]

    * $1.77/each[cite: 4]
    * Digikey Watchdog Timer[cite: 4]

    | Pros | Cons |
    | --- | --- |
    | Independent from microcontroller[cite: 4] | More expensive[cite: 4] |
    | Hardware shutdown capability[cite: 4] | Additional board space[cite: 4] |

3. Windowed Watchdog Timer[cite: 4]

    * Already on Curiosity Nano[cite: 4]

    | Pros | Cons |
    | --- | --- |
    | Strict timing[cite: 4] | Higher complexity[cite: 4] |
    | Catches loops[cite: 4] | Possible debugging issues[cite: 4] |

**Choice:** Option 3: Windowed Watchdog Timer[cite: 4]

**Rationale:** The windowed watchdog timer will not take up additional board space and will allow for more accurate catching of issues. Despite the higher software complexity the additional functionality will help users to detect issues before they cause permanent problems.[cite: 4]