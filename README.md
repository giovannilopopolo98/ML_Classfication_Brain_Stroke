# ML_Classfication_Brain_Stroke

## Dask
Dask is popularly known as a ‘parallel computing’ python library that has been designed to run across multiple systems. 
What is parallel computing?
Parallel computation is performing multiple tasks (or computations) simultaneously, using more than one resource.
Dask can efficiently perform parallel computations on a single machine using multi-core CPUs. 
In order to use lesser memory during computations, Dask stores the complete data on the disk, and uses chunks of data (smaller parts, rather than the whole data) from the disk for processing. 
During the processing, the intermediate values generated (if any) are discarded as soon as possible, to save the memory consumption.
Dask can run on a cluster of machines to process data efficiently as it uses all the cores of the connected machines. One interesting fact here is that it is not necessary that all machines should have the same number of cores. If one system has 2 cores while the other has 4 cores, Dask can handle these variations internally.
Dask supports the Pandas dataframe and Numpy array data structures to analyze large datasets. Basically, Dask lets you scale pandas and numpy with minimum changes in your code format.
