# BlockChainValidation by Hamza Baniata

This program initiates a simple blockchain with two classes

The first class is the Block class:
8-14:  we initiate the parameters of the code
16-18: a function that generates a random number between 1-1000000 \\we can change the random number generator with an input function that allows the user to provide their own data.
19-29: a function that performs the hashing of a combination of (block nonce, block data, pervious block's hash, current timestamp, and the block number)
30-32: a function that returns the information of the block.


The second class is the BlockChain class:
35-38: defining the difficulty of the puzzle. \\ the higher the 'diff', the harder the proof of work needed, hence the more time the node will take to solve the puzzle.
39-41: defining the first block in the chain, and sitting the pointer of the head.
42-49: a function that allows the addition of a new block while maintaining the property of linking the blocks togethe (linked list)
50-72: a function where the mining of block is done:
     - check if the current hash satisfies the required condition
       if it does, start counting time,
                   check if the data is in the chain already, \\ I used a 'set' to                      hold data because the set does not support duplication of data,                      while a 'list' does. Usually the validation is to insure that the sender has sufficient amount of money to transfer, however it will take the same amount of time.
                   if it was in the chain already, stop counting time, print an                        apology to the user and print how much time the validation                          process took, then add the elapsed time to a list of elapsed                        times made to calculate the average validation time later.
                   if the data is not in the chain already, add the whole block to the chain, print all the information of the block, add only the data of the block to the valid loclly saved chain, stop counting time, print the updated blockchain, print the elapsed time for validation and the addition, add the elapsed time to the list of elapsed times to calculate the average validation time later.
                   
       if the hash doesn't satisfy the required condition then try a different hash.
       
       
       
 73-87: run the blockchain class
        declare the set of valid data in the chain
        declare a list of validation times
        declare two variables for computing the average time of validation
        
        start adding blocks to the chain... we can change the range to as many blocks as we want to test
        mine the blocks
        compute the total elapse time to calculate the average required time for validation.
        compute the average validation time for all blocks by THIS node.\
        print the validation times list and the average time needed for validation.\
        
        print all the blocks in the chain.

                   
