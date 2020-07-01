# Computer Architecture For Deep Learning
This repository maintains my research on computer architectures for the acceleration and improvement of deep learning

# Documented Research

## 06-28-2020

- From `Deep Learning for Computer Architect`: 
  - The Minerva framework is composed of 3 main levels: `Software Level`, `Architectural Level`, and `Circuit Level`.
    - `Software Level`: This level needs a software implementation of the neural network that leverages the underlying hardware. It is used to run/compute the output of the network, which allows us to gauge the network's performance. Most "unsafe" optimizations are done in this layer. Unsafe optimizations are those that has the potential to reduces the accuracy of the neural network. However, the framework decides that: if an unsafe optimization has the same effect as the performance variation from random initialization, then it is desired. The performance variation from random initialization is measured by running the network many times, accumulating the run history and compute the performance's mean and standard deviation. This is called the network noise. This noise is decided to lie in between the +/- 1 sigma from the mean.
    - `Architectural Level`: This level allows the designer to explore the accelerator design space quickly. Basically, the trained neural network in the software stack is used to search the accelerator microarchitectural design space for high-performing designs. Evaluating the accelerator design space entails generating and evaluating thousands of unique accelerator implementations, all capable of executing the same neural network. From the frontier, users are free to select whichever design meets their specifications. Note that because Minerva reduces power by around an order of magnitude, a user may want to select a point above their power budget knowing that the optimizations will bring it down to maximize performance. This design is taken as the baseline and is indicative of how neural network accelerators are built today.
    - `Circuit Level`: This level models the actual hardware used down to the individual CMOS transistors, capacitors and resistors. Couple this with a clock of a certain frequency, the designer can have a very accurate estimate of the area and power consumption of the ASIC.


