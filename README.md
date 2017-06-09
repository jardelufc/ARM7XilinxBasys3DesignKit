# ARM7XilinxBasys3DesignKit

Jesus Cristo é o Senhor.

Jesus Christ is the Lord.

This a kind of Educational Kit for Computer Engineering Students .


Its an Very Simple ARM7 Single Cycle  (same architecture) open source processor with only seven main instructions: add,sub,and,orr,ldr,str and b . It too supports ands,orrs,adds and subs, besides the usefuk arm conditions like beq or addeq for example.

For more information about this arm7 like micro architecture, please read chapter 7 of harris and harris or look at the slides at http://pages.hmc.edu/harris/class/e85/DDCAarm_Ch7.pptx .

The System Verilog sources cames from the book Computer Design Arm Edition of Harris and Harris . Essentialy, its everything in https://github.com/jardelufc/ARM7XilinxBasys3DesignKit/blob/master/ARM7-DesignKit/EXAMPLE_SoC/ARMSOC_1/arm_single.sv .

Before starting, you are supposed to install, in RWindo$ OS, the free version of  Vivado (webpack) , MDK Keil and Mdk Keil Legacy Support form ARM7 

After the installation, you are ready to go:

1. Open the myarm7code.uvproj mdk keil project in folder Software . Remember using only the seven implemented instructions and its derivations . Type F7 for compiling and automatically generating (it calls fromelf and hex2sv programs) the system verilog ready for synthesis code memory imem.sv . Type ctrl+f5 for simulation.

2. Open ARMSOC_1.xpr vivado project in Xilinx folder. You can Simulate or generate bit stream and download it to Basys 3 Artix 7 based board from digilent inc .

You have a few code examples in software folder ( .S files) . Creative solutions are needed , because you dont have mov or BL instructions. Look at the examples .

If you want to learn how to add more instructions, please, look lab 9 at https://booksite.elsevier.com/9780128000564/content/labs_companion.zip .

Vivavdo design is configured for running at 10mhz. You can easily increase or decrease it by reconfiguring the clock manager .

There are two peripherals: GPIO and Timer .

GPIO reg for defining direction is at 0x804 
GPIO reg for reading or writing pins is at 0x800

At his time, there is at least one bug: You need use str two times for writing at GPIO .

I've never tested the timers . Enjoy it :) 
