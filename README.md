# Smart-Queuing-Sytem-Intel-DevCloud
This repo demonstrates how to build custom queuing systems for the retail, manufacturing and transportation sectors. This application uses the Intel® DevCloud for the Edge.

![retail](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/retail.jpg)

## Main Tasks

1. Propose a possible hardware solution
2. Build out your application and test its performance on the DevCloud using multiple hardware types
3. Compare the performance to see which hardware performed best
4. Revise your proposal based on the test results

## Project:

1. [Manufacturing Scenario](./Manufacturing_Scenario.ipynb) 
2. [Retail Scenario](./Retail_Scenario.ipynb)
3. [Transportation Scenario](./Transportation_Scenario.ipynb)

## Steps:

1. Create the Python script
2. Create the Job Submission script
3. Execute all the scenarios for all hardware types (CPU, GPU, VPU & FPGA) and compare the performance.

## Choosing the Right Hardware

### Manufacturing Scenario

Model Loading Time:

![manufacturing](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/manufacturing_model_load.png)

Inference Time:

![manufacturing](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/manufacturing_inference_time.png)

Frames per Second (fps):

![manufacturing](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/manufacturing_fps.png)

As it can be seen on the graphs, FPGA performs better than any other hardware, especially on “FPS” and “Inference Time”. “Model Load Time” is mediocre for FPGA, however it is not so important for this scenario.

Mr. Vishwas would like the system to have a good performance on inference time and frames; and test results show that FPGA will easily meet the client’s requirements. Additionally, FPGA lasts 5 to 10 years and it is reprogrammable just Mr. Vishwas would like to have.

### Retail Scenario

Model Loading Time:

![retail](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/retail_model_load.png)

Inference Time:

![retail](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/retail_inference_time.png)

Frames per Second (fps):

![retail](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/retail_fps.png)

As it can be seen on the graphs, FPGA performs better than any other hardware, especially on “FPS” and “Inference Time”.

However, because Mr. Lin do not want to invest in additional hardware, FPGA is not a good choice for this client. IGPU does perform well enough as it can be seen on the graphs; just slightly lower performance than FPGA.

Therefore, integrated GPUs in the client’s computers, which are with Intel i7 processors, can perform good enough and meet the client’s requirements. Additionally, as GPUs are integrated in Intel i7 processors, they will not consume extra power, so Mr. Lin will not see a big increase in the electric bill.

### Transportation Scenario

Model Loading Time:

![transportation](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/transportation_model_load.png)

Inference Time:

![transportation](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/transportation_inference_time.png)

Frames per Second (fps):

![transportation](https://github.com/tharedor/Smart-Queuing-Sytem-Intel-DevCloud/blob/master/images/transportation_fps.png)

As it can be seen on the graphs, FPGA performs better than any other hardware, especially on “FPS” and “Inference Time”.

CPU and GPU also perform better than VPU (Intel Neural Compute Stick 2).

However, because the computers of the client are already being used to process the CCTV camera footage and no additional power is available to run the inference, all these three hardware are not the choices that can be considered.

Though, Intel NCS2 can meet the client’s requirements since Ms. Leah’s $300 budget per machine allows to invest low-cost hardware. Furthermore, Intel NCS2 is also known as a low-power device, and Ms. Leah wants to save future power requirements, so Intel NCS2 seems to be the best choice for this client.
