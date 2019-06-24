# Report Parts

- Title

- Dedicating to *

- Declaration with Name undersigned

- Acknowledgements

- Abstract

- Table of Contents 

- List of figures

- AJIT's HPC FPGA Model

	- Introduction to general embedded processor space
	- Introduction to AJIT and SPARC
	- Need for a System
	- Introduction to FPGA Systems
	- Design of the System
	- Setup specifications
	- System level description
	- Interface level description
		- AXI Interface
		- PCIe Interface
		- AFB Interface
		- HLS Stream Interface
		- Req and Ack protocol
	- Block level description
		- AJIT Core
		- DRAM Controller
		- PCIe-AXI IP
		- AFB-AXI Bridge
		- FIFO Controllers
		- FIFOs 
	- Software Interface
		- pcimem reference
		- Driver Interface discussion
		- Driver development discussion

	- Performance of the system
		- Writing speed of PCIe
		- Reading speed of PCIe

	- Tests conducted
		- March test on memory
		- Filling up whole memory through MAT

	- Alternate designs tried
		- Single bar of 4GB
		- Multiple bars of smaller size i.e. 4K, 32MB etc until we arrived at 128MB limit.
		- Memory Address Translator block
		- Memory Copier Block

	- Current shortcomings
		- Read speed over PCIe is lesser than expected and could be a bottleneck in future.
	- Problems faced
		- Motherboard memory space limit for PCIe bars
		- Vivado putting random errors and resolving it by redundant actions.

- Neural Engine as a peripheral

	- Introduction
	- Need for a Neural Engine
	- Specifications
	- Design of the Engine
		- Storage design for image data
		- Fetch policy for the engine
		- Number of coprocessors
	- Implementation
		- Vivado HLS
		- Aa HLS
	- Testing setup
		- Hardware Test
		- Software Test
	- Performance comparison between software and hardware and results

- References
	- http://www.fpgadeveloper.com
	- https://github.com/billfarrow/pcimem

