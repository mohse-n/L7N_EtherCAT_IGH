This repository contains example code (orginiated from and similar to the examples in IgH EtherCAT Master library), 
written for motion control of two servomotors connected to LS Mecapion L7N servo drives in CSP mode. The codes are extensively 
commented to facilitate the conversion process to accommodate different setups.  
Additionally, in [Installation guides](https://github.com/mohse-n/L7N_EtherLab/tree/master/Installation%20guides) folder, you will find step-by-step procedures for installing:

* [kernel with RTAI patch](https://github.com/mohse-n/L7N_EtherLab/blob/master/Installation%20guides/RTAI%20Installation%20Guide.md)
* [kernel with PREEMPT_RT patch](https://github.com/mohse-n/L7N_EtherLab/blob/master/Installation%20guides/PREEMPT_RT%20Installation%20Guide.md)
* [Igh EtherCAT master library](https://github.com/mohse-n/L7N_EtherLab/blob/master/Installation%20guides/IgH%20EtherCAT%20Master%20Installation%20Guide.md)   

and a few [suggestions for optimizing the performance of PREEMPT_RT](https://github.com/mohse-n/L7N_EtherLab/blob/master/Installation%20guides/Further%20Improvements%20to%20PREEMPT_RT.md).    
___
To run the programs, after installing the IgH Master library, copy-and-replace each in the `examples` folder, and 
1. For the user example, in `~/stable-1.5/examples/usr`,
   - `make clean`
   - `make` 
   - `./ec_user_example` to run the userspace process. 
2. For the RTAI example, in `/usr/local/src/ethercat/examples/rtai`,
   - `make clean`  
   - `make modules`   
   - `insmod ec_rtai_sample.ko` to load the kernel module (and start the hard real-time task).


