# What is an "AsyncMachine"?

Just a Computer. And yes, it is possible not even to understand how a Computer works, but also how to construct another one. And it is not only possible to synthesize logic and flash it onto an FPGA, but also to build a physical one.
And no, you dont need Millions to engage a Foundry in that. You can in fact assemble a working computer at home. Thousands of People have done and some of them you can read about at https://www.homebrewcpuring.org/. The mostly recommended and straight forward approach is to build one of "TTL-Logic". Have a look at Ben Eater (https://www.youtube.com/playlist?list=PLowKtXNTBypGqImE405J2565dvjafglHU).

But somehow this was never enough for me. I needed hard mode. Why build just a "working" Computer, if you can build an "awesome" Computer. Something like a new Computing Paradigm... And this is it.
Currently there are some sketches of this computer in this repo. The Goal it to build the real thing. But it is far from finish. 

Nevertheless I will tell you about this machine. It has two uses:
1) To be a Project to learn Computer Architecture beyond the point most lectures end (have a look at https://www.youtube.com/playlist?list=PL5Q2soXY2Zi8tTLVb-9CUHcfKXLWESjOD, i would seriously reccomend it if you have interest in this topic.
2) Be a Proof of Concept of an actually new Paradigm

Some Facts about the Computer:
1. In its final version it is supposed to utilize dual rail 2 phase protocol asynchronous logic.
2. I am still investigating ternary logic. Currently everything is developed with binary Logic.
3. There is an actual Paradigm shift. Look at the ISA (need to translate from German). The difference between todays Computers and the Draft is mainly caused by the program counter.
Have you ever asked when the Program Counter stops? The natural answer would be "If it receives the halt instruction"... But why actually? There is no direct reason to it! Another way is to just tell the Program Counter two things every time: Where to start and how long to count.
This actually has giant implications. It goes as far as even making Branch Prediction (the Bottleneck of todays CPU's) unnecessary to a certain point. The implication: No backwards compatability. Programs have to be fundamentally different.
But as mathematicians say: The remaining implications are trivial and left to the reader.
4. It is going to be 8bits (reducing physical size, but still usable)
5. Maybe RTOS or MINIX can be ported (need to simulate an x86 or modify the compiler)
6. It needs to be pipelined, otherwise because of the "low speed of light" it is not usable for even the simplest things.
7. Currently I have failed to find proper elementary logic elements to implement the asynchronous protocols. Probably I will need to ask a Computer Science Professor to help me out. I noticed a fundamental Error in many Textbooks on this Topic related to the Dual-Rail-And-Gate. As my Logic Synthesis shows
it is probably not possible to build this Gate from two Müller C-Elements. But it should be. Everyone says it. There are two possible scenarios: First I misunderstood the 2 Phase Protocol... or they have just taken for granted it and not tested it. We will find out... 

---

### License & Intellectual Property

This software/hardware is licensed under the GNU General Public License v3.0, allowing you to freely use, modify, and distribute the code provided that you maintain the same license terms.
