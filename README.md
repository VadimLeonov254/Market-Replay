# Market Replay Engine

[![C++](https://img.shields.io/badge/C++-17-blue)](https://isocpp.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Simulate historical trades from CSV files in real-time with adjustable replay speed.

---

## Features

- Replay trades from CSV at custom speed (`1x`, `2x`, `10x`, etc.)  
- Preserves inter-trade latency for realistic timing  
- Console-based trade output  
- Ready for multi-threaded or multi-symbol extensions  
- Lightweight — no external dependencies  

## How It Works
- Load trades from CSV into memory.
- Calculate latency between consecutive trades.
- Loop through trades:
- Sleep for latency / speed milliseconds
- Print trade details into console

---

## Usage


### From market_replay folder:


	cd build         # go to your existing build folder
	cmake ..         # generate build system (if not already done)
	cmake --build .  # compile the project

### Run

	./main

Enter inputs when prompted:

- Enter the filename: trades.csv
- Enter the speed you want to replay the market at (ex. 1, 2, 10, etc.): 5
---
## CSV Format

### Each line should be:

	id,price,quantity,quote_quantity,timestamp,is_buyer

# Example:
	12345,101.5,0.01,1.015,1675123456789,True
	12346,101.6,0.02,2.032,1675123456792,False

