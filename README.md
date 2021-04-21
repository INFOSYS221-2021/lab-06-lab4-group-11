Group 11: Henry Chen, Malachi Blair, Renee Braddock, Steven Cao

1.What is the type of collection used in the exercise?

(List, queue)

2.What are the different ways of iterating through a collection?

(Use While/while() & For/for() )

3.How do you find out the size of a collection?

return queue.length

4.How do you add an item to a collection? What happens if you try to add an item to a collection that is already full?

queue.push(item);

5.How do you remove an item to a collection? What happens if you try to remove an item that does not exist in the collection?

queue.shift(item);

6.Change the implementation of a FIFO queue to a LIFO queue in 5.6.1.

# // use python queue
from queue import Queue

# Initialise a queue
miqVoucherQ = Queue(maxsize = 100)

# NB: Assume we do not know about objects in python, so create functions insteand

# define a function to add to end of queue
def fifoEnqueue(queue,item):
  return queue.put(item)
  
# define a functiion to remove from front of queue
def fifoDequeue(queue):
  return queue.get();
  
# define a function to find queue length
def fifoLength(queue):
    return queue.qsize()
    
# define a function to find if queue is empty
def fifoIsEmpty(queue):
    return queue.empty()
    
print(fifoLength(miqVoucherQ))
print(fifoIsEmpty(miqVoucherQ))

# Add some travellers
fifoEnqueue(miqVoucherQ,["Jones, E","10","10-01-2021","20-01-2021"])
fifoEnqueue(miqVoucherQ,["Amed, J","1","11-02-2021,20-02-2021"])
fifoEnqueue(miqVoucherQ,["Vine, M","8","9-01-2021,21-09-2021"])

# Show queue length, isEmpty
print(miqVoucherQ);
print(fifoLength(miqVoucherQ));
print(fifoIsEmpty(miqVoucherQ));

# remove from the queue and make sure FIFO
fifoDequeue(miqVoucherQ) 
print(fifoLength(miqVoucherQ));
