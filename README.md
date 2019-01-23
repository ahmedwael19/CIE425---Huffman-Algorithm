# CIE425---Huffman-Algorithm
This program will take a text file as input and encode it using Huffman lossless algorithm.

This code is fully developed by Ahmed Wael for the Information Theory and Coding class in Fall 2018.

## How to use
Run the .m file named Huff as it is the main program where all the functions are called.

For code details and documentation, please take a look at the Documentation folder, where both the details of the algorithm and the code details are explained throughly. 


# Algorithm
1. Convert the stream of symbol into a stream of decimal numbers:
    - Get the ascii code for each symbol
2. Calculate the entropy using Shannon formula.
3. Evaluate the run-length code and calculate its efficiency.
4. Construct the decision tree:
    - Sort the probabilities of the alphabet symbols in a descending order.
    - Sum the least two probabilities.
    - Make a binary tree, with the parent is equal to the sum of the least
two probabilities, and the children equal to the two least
probabilities.
    - Assign weight = 1 for the edge connecting the parent node and the
smallest number node, and weight = 0 for the edge connecting the
parent node and the second smallest node.
    - Repeat the steps from 1 to 4 until there is only one symbol with
probability = 1.
5. Giving weights for each alphabet symbol
    - For each symbol in the alphabet do the following
        - Traverse the tree from the root using the binary search
algorithm, where the half of the tree is ignored each iteration,
and concatenate the weights in each step.
6. Encode the stream of symbols
    - Loop through the stream of symbol and map each symbol to its
corresponding code.
7. Decode the encoded symbols
    - Reverse the process of encoding by looping through the encoded
stream of bits and comparing it with each code and map it back into
the corresponding decimal value and therefore its corresponding
symbol.
8. Calculate the efficiency of the Huffman code and compare it with the runlength code efficiency.


## Decision Tree

For the attached example, the decision tree can be generated in a MATLAB graph as following :
![alt text](https://raw.githubusercontent.com/ahmedwael19/CIE425---Huffman-Algorithm/master/tree.bmp)





## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
