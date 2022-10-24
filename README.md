# DOSP_Project3



## Team Members:
Uma Sai Sree Avula - UFID : 38554667<br/>
Bhanu Rekha Musuluri - UFID : 98477459<br/>

## Description
In this project, chord protocol is implemented to prove the usefulness of the services provided in the overlay networks using Erlang. It is a simple application that associates a key to a string using chord protocol and a object access service.   

## Execution Steps - 

1. Create a node for the server using the command -

      erl -name uavula@192.168.0.105

2. Compile the modules using the command -

      c(project3).

3. To start the compiled program and enable the main module, use the command - 

      project3:main(20,2).

      Here the first argument represents the number of peers that has to be created in peer-to-peer system. The second argument represents the number of requests that each peer has to make.


## Report Questions

1. What is working ? -

* Network join and routing is implemented successfully as per the requirement.</br>
* This implementation uses consistent hashing so that each node maintains information about only O(log N) nodes and lookup requires O(log N) messages.</br>
* AKKA actor framework is carried out i.e. every peer has an actor modelled.

2. What is the largest network you managed to deal with ?

The largest network for which the current implementation worked is 25000 number of nodes and 5 requests per node.



<img width="734" alt="Screen Shot 2022-10-23 at 11 52 38 PM" src="https://user-images.githubusercontent.com/57837608/197445499-de3e8213-3c67-4bb1-8d4e-58f372213935.png">


The below table depicts the number of hops and average hops for different number of peers and no. of requests

<img width="491" alt="Screen Shot 2022-10-23 at 11 42 11 PM" src="https://user-images.githubusercontent.com/57837608/197444487-a2e1087e-6982-4189-b43f-084dc639986a.png">

The below line graph represents the relation between average of hops and number of nodes for 5 no. of requests

![chart](https://user-images.githubusercontent.com/57837608/197444496-3957e479-b6fd-4d2e-a05b-8cfe71e35a77.png)


#Observations:
* As no. of nodes increase, average hops increase for the same no. of requests.
* As no. of requests increase, average hops decrease for the same no. of nodes.
