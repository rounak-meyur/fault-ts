## Data Description

This directory contains time series dataset for fault simulation in the IEEE 68 bus power system. 
The directory also contains relevant information and data regarding the 68 bus system parameters and conditions.
The description of each csv file are provided here.

- _ieee68-coordinates.csv_: This file contains the (x,y) coordinates of each node in the 68 bus power grid. The coordinates are useful in displaying image of the power grid, if required.
    - node: ID of the node in the power grid
    - x: x-coordinate of the node in the 2-D plane
    - y: y-coordinate of the node in the 2-D plane

- _ieee68-edgelist.csv_: This file contains the edgelist for the network.
    - fbus: node ID of the from bus
    - tbus: node ID of the to bus
    - id: edge identifier between the node pairs (parallel lines exist)
    - r: resistance of the edge (in pu)
    - x: reactance of the edge (in pu)
    - flow: power flowing through the edge (in MVA)

- _ieee68-faults.csv_: This file contains the list of three phase faults considered in the simulation.
    - index: fault identifier which is used in refering files for a particular fault
    - type: type of fault ("edge": three phase line fault at to bus)
    - fbus: node ID of the from bus
    - tbus: node ID of the to bus
    - eid: edge identifier between the node pairs

- _ieee68-label.csv_: This file contains the coherent generator group to which each bus belongs. All nodes with the same label are coherent and observe similar voltage phase shapes.

- _ieee-nodelist.csv_: This file contains the node attributes.
    - node: ID of the node in the power grid
    - pgen: real power generation at node (in MW)
    - qgen: reactive power generation at node (in MVAR)
    - pmax: maximum real power capacity (in MW)
    - qmax: maximum reactive power capacity (in MVAR)
    - sload: load consumption at node (in MVA)



The directory _ieee68_ contains the time series dataset for the bus voltage phase angles during different faults. The files are named as follows
> angle-`<fault>`-`<condition>`.csv
- *fault*: this denotes the fault identifier from the _ieee68-faults.csv_ file. Refere to the _ieee68-faults.csv_ file to get the location of the fault.
- *condition*: this denotes the condition of the simulation.
    - _trip_: the faulted bus is tripped after the fault occurs and records are stored only for generator buses.
    - _notrip_: the faulted bus is not tripped after the fault occurs and records are stored only for generator buses.
    - _check_: some dummy simulation run to check the validity of the dataset produced.
    - _allbus-notrip_: the faulted bus is not tripped after the fault occurs and records are stored for all buses.
