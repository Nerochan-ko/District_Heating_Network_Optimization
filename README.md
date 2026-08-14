# District Heating Network Optimization

This repository is based off of a university project focused on district heating network optimization. The project explores the use of **DHNx** and **oemof.solph**, starting with a small heating network and evolving it before connecting the physical network optimization with an energy system model.

The project is divided into five steps:

1. **Base heating network** – A small DHNx network with five consumers, two heat producers and two pipe types is created.
2. **Network expansion** – The network is expanded to ten consumers, five producers and a larger selection of pipe diameters to better see later on how the optimisation takes place.
3. **Energy system optimization** – The heat producers are modeled and their dispatch is optimized with `oemof.solph` to meet the aggregated heat demand.
4. **Integration of DHNx and oemof** – Heat losses from the district heating network are added to the demand of the energy system model to study their effect on generation and costs.
5. **Environmental optimization** – CO₂ emissin costs are added to investigate how this changes optimal dispatch of the different heat-generation technologies.

Each step has its own folder containing the relevant **input files, Python code and generated output files**, making it possible to follow the development of the model step by step.

One thing to keep in mind when looking at the results from the first network-optimization steps is the relatively small physical size of the network. Because the pipe lengths are short, the **fixed investment costs** have a stronger influence on the optimization than the cost per meter of pipe. This affects how the optimizer chooses between the available pipe types.

The parameters can be changed in in the network.csv 02_inputs/Input_data_S1/invest_data/network. the network creation is sensitive however to drastic changes and might crash if there are unreasonable values listed

To know more about DHNC and what parametesr and codes they use here is the documentation which I thought was pretty goodd  so you will manage to find everything thre that I am using in this repository and thoruout the steps.
https://dhnx.readthedocs.io/en/latest/network.html

