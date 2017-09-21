# multithreaded-Bank
creating a producer and consumer

Your assignment is to write a multithreaded program incorporating a producer-consumer algorithm. 
You will write a producer-consumer program with a single producer and multiple consumers. 
Your producer and your consumers will run as separate threads, 
so you will use mutexes to protect and manage shared data structures.

Your program will spawn a single data input thread (the producer). 
The input thread will read in lines of data where each line specifies a color and a number. T
he producer will sort (i.e. categorize) the different input lines by color and feed the data for a single color to a single consumer. 
There will be multiple colors, so there will be multiple consumers. 
For example, the producer would feed red data to one consumer, the green data to a second consumer and the blue data to a third consumer.
You have (at least) two choices for where the producer thread puts the categorized data. 
First, you may opt to put the data into separate queues, one for each category. 
Each consumer thread will have exclusive access to a specialized queue. 
Second, you may choose to put all data into a single shared buffer that will be used by all the consumer threads. 
The data queues (or buffer) are initially empty.

Your program will also spawn multiple data extraction threads (the consumers), one consumer thread for each category. 
The data extraction threads will extract all data for their category from the data structure shared with the producer and print the individual data items.
You should write a red, green and blue consumer. 
The red consumer will extract prime numbers, the green consumer will extract Fibonacci numbers and the blue server will extract multiples of 3 and 5 (in memory of an old drinking game). 
Each server extracts and prints the required numbers and ignores the others. 
The individual consumers would not get all of the primes or Fibonacci or multiples, but it would produce interesting output nonetheless.
Requirement 1: there should be a minimum of BUSYWAITING in your code.
Requirement 2: there should be NO DEADLOCKS and NO RACE CONDITIONS in your code.
