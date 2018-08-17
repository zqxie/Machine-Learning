# Chapter 1 - Introduction

Tags ： Machine-Learning

---

[TOC]

# The reason why we need machine learning
The method of handcoded rules of "if" and "else" decisions to process data or adjust to user input, to some tasks, such as spam filter function or face detection, are nearly impossible.

 - the logic is specfic, so even a slight change of the task may cause to rewrite the whole system.
 - the rules require a human expert who has a deep understanding of how a decision should be made.

# Problems Machine Learning Can Solve
**Supervised learning**

> Learn from input/output pairs, just like a "teacher" provides supervision to the algorithms in the form of the desired outputs for each example that they learn from.

 - *Identifying the zip code from handwritten digits on an envelope*
 - *Determining whether a tumor is benign based on a medical image*
 - *Detecting fraudulent activity in credit card transactions*

**Unsupervised learning**

> Only the input data is known, no known output data is given to the algorithm.

 - *Identifying topics in a set of blog posts*
 - *Segmenting customers into groups with similar preferences*
 - *Detecting abnormal access patterns to a website*

# Knowing Your Task and Knowing Your Data
 - what questions am I trying to answer? Do I think the data collected can answer that question?
 - What is the best way to phrase my questions as a machine learning problem?
 - Have I collected enough data to represent the problem I want to solve?
 - What features of the data did I extract, and will these enable the right prediction?
 - How will I measure success in my application?
 - How will the machine learning solution interact with other parts of my research or business product?

# Python
## Anaconda
 - scikit-learn, numpy, scipy, matplotlib, pandas, ipython, Jupyter Notebook

## Some Userful Functions
```python
    # numpy
    x = np.array([[1,2,3],[4,5,6]])
    print("x:\n{}".format(x))
    
    # scipy
    from scipy import sparse
    # sparse: CSR format, COO format
    data = np.ones(4)
    row_indices = np.arange(4)
    col_indices = np.arange(4)
    eye_coo = sparse.coo_matrix((data, (row_indices, col_indices)))
    
    # pandas
    import pandas as pd
    data = {'Name': ["John", "Anna", "Peter", "Linda"],
            'Location' : ["New York", "Paris", "Berlin", "London"],
            'Age' : [24, 13, 53, 33]
            }
    data_pandas = pd.DataFrame(data)
    display(data_pandas)
    '''
    This produces the following output:
        Age Location Name
        0 24 New York John
        1 13 Paris Anna
        2 53 Berlin Peter
        3 33 London Linda
    '''
    display(data_pandas[data_pandas.Age > 30])
    '''
        Age Location Name
        2 53 Berlin Peter
        3 33 London Linda
    '''
    
    
}
```

# Classifying Iris Species

![Pair-plot-of-the-Iris-dataset](images/Chapter-1-Pair-plot-of-the-Iris-dataset.png)

View details in scikit-learn Page

 


