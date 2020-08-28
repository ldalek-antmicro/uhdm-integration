all:
	../../../image/bin/surelog -parse -sverilog ibex_register_file_fpga.sv
	../../../image/bin/verilator --cc --trace --exe --Mdir build --uhdm-ast slpp_all/surelog.uhdm sim.cpp
	make -C build -f Vsurelog.mk -j`nproc`
	./build/Vsurelog

clean:
	rm -rf build slpp_all surelog.log
