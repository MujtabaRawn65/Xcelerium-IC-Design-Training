# _*_ Makefile _*_

# Tools
IVER = iverilog -g2012 -o
VVP = vvp
PROG = cache_mem_axi4

# Default target
all: $(PROG)_tb.vvp

# Rule to compile Verilog/SystemVerilog files
$(PROG)_tb.vvp: *.sv $(PROG)_tb.sv
	@$(IVER) $@ $^

# Rule to run simulation
run: $(PROG)_tb.vvp
	@$(VVP) $(prog)

# Clean up
clean:
	@rm -f *.vvp *.vcd

.PHONY: all clean run

