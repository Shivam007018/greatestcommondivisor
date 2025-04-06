# 🔁 GCD Calculator in Verilog

Hey there! 👋  
This is a fun little hardware project where I built a **GCD (Greatest Common Divisor)** calculator using Verilog. It’s based on the classic subtraction method and implemented using a clean **datapath + controller FSM** structure.

---

## 💡 What It Does

Give it two 16-bit numbers, and it’ll subtract its way down to the GCD.  
All the logic is split into:
- A **datapath** that handles the math
- A **controller FSM** that decides what to do next
- A **testbench** to feed it numbers and watch the magic happen

---

## 🧱 Project Files

- `gcd_datapath.v` – Contains registers, subtractor, muxes, and comparator.
- `gcd_controller.v` – FSM that controls the datapath using flags.
- `gcd_test.v` – Sets up the inputs, starts the process, and dumps the waveforms.

---

## ▶️ How to Run It

Make sure you have **Icarus Verilog** and **GTKWave** installed.

1. **Compile:**
   ```bash
   iverilog -o mysim gcd_datapath.v gcd_controller.v gcd_test.v
TO RUN THIS CODE 
vvp mysim
for wave
gtkwave gcd.vcd




OUTPUT 
 A = 143, B = 78, Done = 0
 A =  65, B = 78, Done = 0
 A =  65, B = 13, Done = 0
 ...
 A =  13, B = 13, Done = 0
 A =   0, B = 13, Done = 1

