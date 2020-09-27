# QOSF-Mentorship-Prgram---Task-3-solution
This repository contains QOSF Mentorship Program's solution to Task 3. I have also uploaded the file of the tasks given so that you can refer to the tasks easily.

The task was to Define quantum circuits given by the gates H,I,X,Y,Z,Cnot,Rx,Ry,Rz,Cz only in terms of Rx,Rz, and cz gates. So basically compile them to these gates. 
The task is pretty simple and so is my solution.
First of all, the task is possible because these gates are universal so we can define any circuit in terms of these gates (and by these gates I mean  Rx,Rz,Cz gates) 

The other part of the problem is to analyse the overhead and suggest how the solution can be made better, now this is the part where we will need alot of thinking. If we talk about IBM quantum computer, there is only one type of 2-qubit gate possible to apply on it which is Cnot Gate, so other 2 qubit gates are all applied using Cnot in some combination with itself and other gates to implement in circuits, but if u look at the Task we are supposed to implement only cz gate as a 2 qubit gate. I think we found our first overhead. Let me explain, if you are running my solution on a
IBM Quantum Computer then we are supposed to implement Cnot gate in terms of Cz gate , But these Cz gates are again being coverted to Cnot internally on the IBM Quantum Computer. You can see this as a time complexity overhead for sure and also the number of gates required increases, more on this in the document "How it works and the overhead analysis" that i have uploaded in this repo.

So to understad the solution,I Suggest you to go through the "Final solution to Task 3.ipynb" file first. Note that this file is designed to convey how the solution works, This file has comments along the lines of codes inorder to present the reader the approach used to solve this problem. The actual solution is in the folder "Compile" which is the same as in the "task3solution.ipynb" file.The only difference is it is a modular approach which means the funtions used in the program are stored in different file inorder to make the code look clean and can be reused. Also to do the second part of the Task which is to analyse the overhead and to make the compiling task better is present in the doc "How it works and the overhead analysis" which also has a breif explaination of the current approach.



 
