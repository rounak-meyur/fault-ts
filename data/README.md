## Data Description

This directory contains time series dataset for fault simulation in the IEEE 68 bus power system. The description of each csv files are provided here.

- _ieee68-coordinates.csv_: This file contains the (x,y) coordinates of each node in the 68 bus power grid. The coordinates are useful in displaying image of the power grid, if required. The columns are:
    - node: ID of the node in the power grid
    - x: x-coordinate of the node in the 2-D plane
    - y: y-coordinate of the node in the 2-D plane

- _ieee68-edgelist.csv_: This file contains the edgelist for the network.
    - fbus: node ID of the from bus
    - tbus: node ID of the to bus
    - id: edge identifier between the node pairs (parallel lines exist)
    - r: resistance of the edge (in pu)
    - x: reactance of the edge (in pu)
    - flow: power flowing through the edge (in pu)

- _ieee68-faults.csv_: This file contains the list of three phase faults considered in the simulation.
    - index: fault identifier which is used in refering files for a particular fault
    - type: type of fault ("edge": three phase line fault at to bus)
    - fbus: node ID of the from bus
    - tbus: node ID of the to bus
    - eid: edge identifier between the node pairs