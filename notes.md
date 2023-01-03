Python libraries topics covered:
```
 =============== DAY 1 ===============
```
1. Python_list vs Numpy_array
    * Square the elements in a python list using list comprehension
    * Square the elements in a numpy_array using simple x**2
2. Python lists are __heterogeneous__
    * Value stored in one block and it's address gets stored in another block. (retriving values makes it as 2-step process)
3. Numpy array are __homogeneous__
    * Value store in only one block, hence indexing is faster.
4. Benefits of using Numpy array:
    * Element wise operation.
    * Faster than python list.
        * Proved it, by comparing the runs between range(100000) & arange (100000) and squaring it.
        * using %timeit (magic function), the respected results were _25.2millisec_ for python list & _29.2microsec_ for numpy array.
5. Heirarchy follows: **Bool --> int --> float --> string** 
    ~~~~
    np.array([1,2,3,True]) ==> int dtype (True get converted to 1)
    np.array([1,2,3.0,True]) ==> float dtype (True get converted to 1.0, 1&2 get converted to float)
    np.array([1,2,3,4.0]) ==> float dtype (all values get converted to float values)
    np.array([1,2,3,"Scaler"]) ==> <U21 dtype (all values get converted to string type. "U" means unicode, 21 bits)
    np.array([1,2,3.0,"Scaler"]) ==> <U32 dtype (all values get converted to string type. "U" means unicode, 32 bits)
    ~~~~
6. Range vs Arange:

    * Range:
        ```
            range(100) ==> from 0 to 99
            range(1,100) ==> from 1 to 99
            range(1,100,2) ==> from 1,3,5,7 to 99
            range(100,1,-1) ==> from 100 till 2 (reverse)
        ```
    * Arange
        ```
            np.arange(100)
            np.arange(1,100)
            np.arange(1,100,2)
            np.arange(100,1,-1)
        ```
    * Everything above is same, but numpy array supports float step size and also it is faster.
        ```
            np.arange(1,100,0.5) ==> from 1, 1.5, 2, 2.5 till 99.5
        ```
