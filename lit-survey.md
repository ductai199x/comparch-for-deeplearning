- [Eyeriss v1: A Spatial Architecture for Energy-Efficient Dataflow for Convolutional Neural Networks](#eyeriss-v1-a-spatial-architecture-for-energy-efficient-dataflow-for-convolutional-neural-networks)
- [Eyeriss v2: A Flexible Accelerator for Emerging Deep Neural Networks on Mobile Devices](#eyeriss-v2-a-flexible-accelerator-for-emerging-deep-neural-networks-on-mobile-devices)
- [A New MRAM-based Process In-Memory Accelerator for Efficient Neural Network Training with Floating Point Precision](#a-new-mram-based-process-in-memory-accelerator-for-efficient-neural-network-training-with-floating-point-precision)
- [RNNFast: An Accelerator for Recurrent Neural Networks Using Domain Wall Memory](#rnnfast-an-accelerator-for-recurrent-neural-networks-using-domain-wall-memory)
- [An Efficient Accelerator Design Methodology for Deformable Convolutional Networks](#an-efficient-accelerator-design-methodology-for-deformable-convolutional-networks)
- [Lupulus: A Flexible Hardware Accelerator for Neural Networks](#lupulus-a-flexible-hardware-accelerator-for-neural-networks)
- [Hardware for Machine Learning: Challenges and Opportunities](#hardware-for-machine-learning-challenges-and-opportunities)

# Eyeriss v1: A Spatial Architecture for Energy-Efficient Dataflow for Convolutional Neural Networks

Author: Yu-Hsin Chen, Vivienne Sze (MIT RLE lab)

Abstract: Eyeriss v1 is a Deep CNN accelerator architecture that leverages a
novel dataflow called row-stationary (RS), which minimizes data movement energy
consumption of a spatial architecture. This is realized by exploiting local data
reuse of filter weights and activations in the high-dimensional convolutions,
and minimizing data movement of partial sum accumulations. Eyeriss v1 can adapt
to different CNN shape configurations and reduce all types of data movement
through maximally utilizing the process engine's (PE) local storage, direct
inter-PE communication, and spatial parallelism. Experiments shows Eyeriss v1
has 1.4x and 2.5x less energy consumption for conv and fc, respectively, running
AlexNet.

# Eyeriss v2: A Flexible Accelerator for Emerging Deep Neural Networks on Mobile Devices

Author: Yu-Hsin Chen, Vivienne Sze (MIT RLE lab)

Abstract: Eyeriss v2 is a DNN accelerator architecture designed for running
compact and sparse DNNs. It has a highly flexible on-chip network - a
hierachical mesh - that can adapt to the different amount of data
reuse/bandwidth. In addition, Eyeriss v2 can process sparse data directly in the
compressed domain for both weights and activations. Eyeriss v2 is ~12.6x faster
and ~2.5x more energy efficient than Eyeriss v1 running MobileNet.

# A New MRAM-based Process In-Memory Accelerator for Efficient Neural Network Training with Floating Point Precision

Author: Hongjie Wang (ECE Rice University)

Abstract: State-of-the-art PIM DNN training accelerators employs either
analog/mixed signal computing which has limited precision or digital computing
based on a memory technology that supports limited logic functions and thus
require more clock cycles to do floating-point arithmetics. This paper
introduces SOT-MRAM - Spin Orbit Torque Magnetic Random Access Memory - based
digital PIM that addresses this problem. Experiments show that SOT-MRAM is 3.3x,
1.8x, and 2.5x improvement in term of energy, latency, and area, respectively.

# RNNFast: An Accelerator for Recurrent Neural Networks Using Domain Wall Memory

Author: Mohammad H. Samavatian (Ohio State University, University of Michigan)

Abstract: RNNFast is a hardware accelerator for RNN that leverages a class of
NVMs called Domain-Wall Memory (DWM). The researchers show that DWM is suited
for RNN acceleration due to its very high density and low read/write energy. At
the same time, the sequential nature of input/weight processing of RNNs
mitigates one of the downsides of DWM, which is the linear (rather than
constant) data access time. RNNFast is designed to have 1) flexible mapping of
logical neurons to RNN hardware blocks, 2) custom DWM-based cells for floating
point arithmetics and activation functions, 3) minimized data movement by
closely interleaving DWM storage and computation. Experiments show that RNNFast
is 21.8x and 70x improvement in term of performance and energy, respectively.

# An Efficient Accelerator Design Methodology for Deformable Convolutional Networks

Author: Saehyun Ahn (EE Sogang University, LG Uplus)

Abstract: Unlike standard CNN, deformable CNN decides the receptive field size
(kernel size) using dynamically generated offsets, which leads to an irregular
memory access. Especially, the memory access pattern varies both spatially and
temporally, making static optimization ineffective. The researchers propose: 1)
a novel training method to reduce the size of the receptive field without
compromising accuracy, 2) an efficient systolic architecture to maximize its
efficiency, 3) an optimized dataflow design on FPGA.

# Lupulus: A Flexible Hardware Accelerator for Neural Networks

Author: Andreas T. Kristensen (TCL Lausanne Polytech, EE Eindhoven University of
Technology)

Abstract: The high rate of innovation in ma-chine learning makes it important
that hardware implemen-tations provide a high level of programmability to
supportcurrent and future requirements of neural networks. In thiswork, we
present a flexible hardware accelerator for neuralnetworks, calledLupulus,
supporting various methods forscheduling and mapping of operations onto the
accelerator.Lupulus was implemented in a28 nmFD-SOI technologyand demonstrates a
peak performance of380 GOPS/GHzwith latencies of21.4 msand183.6 msfor the
convolutionallayers of AlexNet and VGG-16, respectively.

# Hardware for Machine Learning: Challenges and Opportunities

Author: Vivienne Sze (MIT)

Abstract: Machine learning plays a critical role in extracting meaningful
information out of the zetabytes of sensor data collected every day. For some
applications, the goal is to analyze and understand the data to identify trends
(e.g., surveillance,portable/wearable electronics); in other applications, the
goal is to take immediate action based the data (e.g., robotics/drones,
self-driving cars, smart Internet of Things). For many of these applications,
local embedded processing near the sensor is preferredover the cloud due to
privacy or latency concerns, or limitations in the communication bandwidth.
However, at the sensor thereare often stringent constraints on energy
consumption and cost in addition to throughput and accuracy requirements.
Furthermore, flexibility is often required such that the processing can be
adapted for different applications or environments (e.g., update the weights and
model in the classifier). In many applications, machine learning often involves
transforming the input data intoa higher dimensional space, which, along with
programmable weights, increases data movement and consequently energy
consumption. In this paper, we will discuss how these challenges can be
addressed at various levels of hardware design ranging from architecture,
hardware-friendly algorithms, mixed-signal circuits, and advanced technologies
(including memories and sensors)
