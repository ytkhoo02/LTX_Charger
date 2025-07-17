# LTX_Charger
Uses:
- Python
- LXI over LAN
- SCPI

Requirements 
| Parameter            | Requirement                    |
| -------------------- | ------------------------------ |
| Charging voltage     | **14.4V** max (initial charge) |
| Float voltage        | **13.8V** after full charge    |
| Max charging current | **0.8A**                       |
| Battery type         | 2Ah SLA (sealed lead-acid)     |
| Charge indication    | Current stabilises to 40–80mA  |
| Overcharge risk      | Avoid charging >12h            |

E36200 Keysight PSU script for initial full charge and float charge.

1. Initial charge:
   
  Set voltage to 14.4V

  Set current limit to 0.8A

  Enable output and monitor current

  When current drops to ~50–80mA, battery is full

2. Switch to float:

  Reduce voltage to 13.8V

  Keep current limit at 0.8A

  Leave connected for maintenance charging
