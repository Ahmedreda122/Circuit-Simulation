# Circuit-Simulation
A Simulation of a circuit that does operations on 3-bit signed numbers using Verilog HDL.

---

### 3-Bit Signed Integer Selector

#### Inputs
- Two selection inputs (S1 and S0)
- Two signed integers (A and B) in 2's complement form, each represented using 3 bits.

#### Output
- A signed integer (G) in 2's complement form, with a size of 3 bits.

#### Operation Logic

The output G is determined based on the selection inputs S1 and S0 as follows:

- When Selection Inputs are 00 (S1=0, S0=0):
  - G = A + 1

- When Selection Inputs are 01 (S1=0, S0=1):
  - G = A + B

- When Selection Inputs are 10 (S1=1, S0=0):
  - G = B - A = B + ~A + 1

- When Selection Inputs are 11 (S1=1, S0=1):
  - G = 1 - B = ~B + 1 + 1

#### Explanation
- The selector operates on 3-bit signed integers A and B.
- Different operations (addition, subtraction, complement) are performed based on the selection inputs to derive the output G.
- Each operation corresponds to a specific combination of selection inputs, allowing versatile manipulation of signed 3-bit integers.
