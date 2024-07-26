# ML_Classfication_Brain_Stroke
The initial data manipulation is done with a Python tool called Pandas, along with Numpy.

Pandas and Numpy, have certain limitations when efficiently handling large datasets. While these libraries are undeniably powerful, their computational efficiency can be challenged, particularly when manipulating gigabytes of data. 

To overcome this obstacle, one can use Dask Python, a tool that scales data workflows perfectly, providing a flexible, parallel processing framework to address the challenges posed by a large dataset.

In our case, the dataset is not very large, but we will still exploit Dask to study the different efficiencies between the 2 tools

## Dask
Dask is popularly known as a ‘parallel computing’ python library that has been designed to run across multiple systems. 
What is parallel computing?
Parallel computation is performing multiple tasks (or computations) simultaneously, using more than one resource.
Dask can efficiently perform parallel computations on a single machine using multi-core CPUs. 
In order to use lesser memory during computations, Dask stores the complete data on the disk, and uses chunks of data (smaller parts, rather than the whole data) from the disk for processing. 
During the processing, the intermediate values generated (if any) are discarded as soon as possible, to save the memory consumption.
Dask can run on a cluster of machines to process data efficiently as it uses all the cores of the connected machines. One interesting fact here is that it is not necessary that all machines should have the same number of cores. If one system has 2 cores while the other has 4 cores, Dask can handle these variations internally.
Dask supports the Pandas dataframe and Numpy array data structures to analyze large datasets. Basically, Dask lets you scale pandas and numpy with minimum changes in your code format.



![](https://cdn.analyticsvidhya.com/wp-content/uploads/2018/07/dask-1.png)
Dask has a central task scheduler and a set of workers. The scheduler assigns tasks to the workers. Each worker is assigned a number of cores on which it can perform computations. 
The workers provide two functions:
compute tasks as assigned by the scheduler
serve results to other workers on demand
Below is an example that explains how a conversation between a scheduler and workers looks like (this has been given by one of the developers of Dask, Matthew Rocklin):
The central task scheduler sends jobs (python functions) to lots of worker processes, either on the same machine or on a cluster
