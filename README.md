# Quantum_AES_

## Introduction

An attempt at recreating Quantum circuit for Advanced Encryption Standard and its Experimental Realisation" by Subhash Shankar Pandey, Dhrubajyoti Sadhukhan, and Prasanta K. Panigrahi for large data sizes. We attempt to use a similar construction but scaled to be accomodated into the Qiskit Simulator. 
Contains an account of learning done by us from the textbook on qiskit.org in the process of implementing the circuit.

## Learning

### Day 1

The **QuantumCircuit()** Function is used to initialise a circuit in qiskit, and the **x()** function adds a NOT gate. It can be used to set Qubits to zero or 1 when mimicing basic digital gates' operation. __cx()__ gate XORs the inputs, and saves it to the second argument. __ccx()__ gate ANDs the first two arguments and saves it to the third. This gate is called the Toffoli gate.
The above mentioned gates are used to create a half adder in the [Atoms of Computation](https://qiskit.org/textbook/ch-states/atoms-computation.html) page in the qiskit textbook.

The implemented half adder for input 11 is as follows:

![image](https://user-images.githubusercontent.com/66631868/216019432-696fd1ef-2ecb-4f25-bef3-5e973af13dc9.png)

_Half Adder Circuit_

![image](https://user-images.githubusercontent.com/66631868/216019603-cfc74e38-1bd8-4549-9856-43dd6b90f604.png)

_Output. The numbers at the bottom represent the Qubits in the order Carry, Sum._

The implemented Full Adder for input 111 is as follows:

![image](https://user-images.githubusercontent.com/66631868/216019983-78f4028d-bcb9-493a-b9f7-af4335ccd26e.png)

_Full Adder Circuit_

![image](https://user-images.githubusercontent.com/66631868/216020094-832713ad-e854-4498-b64d-d4143c3d1800.png)

_Output. The numbers at the bottom represent the Qubits in the order Carry, Sum._

By Adding or removing NOT gates at the start of each Qubit's processing, the input bit sequence to the adders can be controlled.
