# MariaDB on Power8

**MariaDB - 64% faster on POWER8 than on Intel**

**MariaDB 1 0.1 can process 1 .2 million queries per second**

Settings for configuring and benchmarking MariaDB on Power8 architecture servers

Please read the white paper concerning the benchmarking run of MariaDB on Power8, achieving 1.2 million queries per second, available from [quru.com](https://quru.com/whitepapers/mariadbonpower8)

### Other details:

The benchmark was run on an IBM S822L Power8 server with 2 sockets, 20 cores and 8-way SMT (160 hardware threads), and 128GB RAM. The machine runs PowerKVM 3.1 and inside KVM a Red Hat Enterprise Linux 7.1 (ppc64le) guest

Virtual machine details:
* RAM: 128GB
* CPU Configuration: 2 sockets, 10 cores per socket, 2 threads per core
* CPU DSCR: on

MariaDB was built from source using the IBM Advance Toolchain version 8.0. Binaries were built unstripped. IBM's FDPR tool (Feedback Directed Program Restructuring) was then run against the MariaDB server binary produced to optimize against the sysbench workload, and the benchmarks were repeated.
