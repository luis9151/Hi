default:
	iverilog -Wall -o mipstest *.v

test: default
	./mipstest <<< "finish"

display:
	python dvi-display.py display.ppm & ./mipstest <<< "finish"

wave:
	gtkwave mipstest.vcd &

clean:
	killall mipstest & rm -rf mipstest mipstest.vcd display.ppm &
