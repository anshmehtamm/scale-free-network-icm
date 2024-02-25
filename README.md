# Information Cascade Model on Scale Free Networks using NetLogo

This repository is part of Social Network Project under Dr. Sakthi Balan Muthaiah (LNMIIT), dated: May 2020

## Scale Free Network in NetLogo

For creating a scale free network, we are using **Preferential Attachment Model** (described by Barabasi and Albert – 1999). In this model a new node is created at each time step and connected to existing nodes according to “preferential attachment” principle. 
At a given time step, the probability p of creating an edge between an existing node u and the new node is: p = [(degree(u) + 1)/(|E| + |V| )] where |V| is a set of nodes and |E| is the set of edges.

- Nodes forming the network will be called turtles in NetLogo, and each link created has an
activation-probabilities
- The make-node procedure takes one input – turtle to make links with which is randomly selected from all the links present in the network. This selection takes care of the preferential attachment equation as the node with more links has a higher chance of getting selected to
make another link.

[IMG]

[IMG]


## Information Cascade Model 

**Selection of Starting Nodes**
From the network we randomly select the number of nodes selected in the slider num-of-starting-nodes and set their color yellow - indicating they are infected.

**Setting Activation Probabilities**
Activation probabilities pv,w is the probability of a directed link from v → w to get activated, i.e. if v is infected then pv,w is the probability of infecting w too. Now say a node v has n out − links to other nodes, then the probability of each link
to get activated is pv,i for all i ∶ 0 ≤ i ≤ n

We do this in NetLogo by for every node’s (turtles) out-links, assigning a random weight from 1 to 100 and then dividing the weight by the sum of all weights from
that node. This ensures that equation is satisfied. 

**Cascading Effect**
For cascading the information, we perform the following steps:

1. Start with random set of nodes (2.1)
2. Generate a random number from 0 to 1 for each node’s out links.
3. If the generated number is less than the activation probability (2.2) the other node of that is also infected (yellow). If p < pv,w ∶ w gets infected (eq 2) Ref 1.
4. Make a new set of newly infected nodes and continue from step 2 again till there no new nodes.

## Simulation Results

**Start Nodes - 25**


**Start Nodes - 75**

**Start Nodes - 150**

**Results Overall**




