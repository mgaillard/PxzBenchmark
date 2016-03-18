# PxzBenchmark
A Docker container to benchmark the CPU. Make use of PXZ to compress a large file in a ramdisk. The benchmark is repeated many times and the result is writen in a CSV file.

Generate the Docker image
-------------------------
	make

Run the Benchmark
----------------
	touch ~/result.csv
	docker run --privileged -v ~/result.csv:/root/result.csv -e NUMBER="10" mgaillard/pxz_benchmark

The variable `NUMBER` is the number of times the benchmark is repeated.  
You can replace `~/result.csv` with the location of the result file on the host.
