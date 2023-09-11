(lesson_2_5)=
# Tips on memory management
Since everyone will be using the same cluster, it is important to be mindful of how to reserve resources in job submission.
This is especially important because this cluster machine is also being used for research purposes for Ph.D. students and faculty members.

## Tracing memory allocation
We will see how much memory some of the basic tasks in Python take by using the `tracemalloc` (trace memory allocation) library.

Let us try to add some numbers and see how much memory it takes.

````{admonition} Adding Numbers
- 1 to 10,000
    ```{figure} ../pictures/lesson_2_5/add_1.png
    ```
- 1 to 1,000,000
    ```{figure} ../pictures/lesson_2_5/add_2.png
    ```
- 1 to 10,000,000
    ```{figure} ../pictures/lesson_2_5/add_3.png
    ```
- 1 to 100,000,000
    ```{figure} ../pictures/lesson_2_5/add_4.png
    ```
````

```{warning}
- While using Jupyter Notebook is convenient, everyone will be running it on the login node (ds01). If the cell runs more than 30 seconds, stop it, and submit it as a job that runs a `.py`  file to the cluster.
- If the memory you reserve is not enough, the job will fail. Try to add 1-2 GB at a time, and if you think you will need more than 20GB, ask the instructors first.
```

## Practice 13
Check the memory usage of your `combining_files.ipynb`. Check also the memory usage of reading the
`test_file.gz` from `/home/practice_data/`. Provide a screenshot of the code with the result.
