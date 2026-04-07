Project Documentation: LinkedIn Compatibility Dataset Analysis
1. Project Overview
Objective:
Analyze a dataset of 50,000 LinkedIn profiles to perform data operations and compare sequential vs parallel execution times.
Key Goals:
Filter profiles with high compatibility (>70)
Compute average compatibility score
Sort profiles by compatibility score
Compare sequential vs parallel execution performance
Dataset Source:
Kaggle dataset: likithagedipudi/linkedin-compatibility-dataset-50k-profiles
2. Tools and Technologies Used
Tool / Technology
Purpose
Python 3.12
Programming language for data analysis and parallelization
Pandas
Data manipulation, filtering, aggregation, sorting
Threading
Parallel execution of independent tasks
Multiprocessing (optional)
For CPU-bound tasks and true parallel execution
KaggleHub
Download datasets from Kaggle
Google Colab / Jupyter Notebook
Execution environment and interactive analysis
Time
Measuring execution performance


3. Project Timeline / Work Log
Date
Task / Activity
Status / Notes
2026-02-07
Project kickoff, dataset exploration
Completed
2026-02-17
Implement sequential data operations
Completed
2026-02-17
Implement threading for parallel execution
Completed
2026-03-19
Measure execution times and compare performance
Completed
2026-03-19
Draft midterm report and performance tables
Completed
2026-03-20
Prepare README.md and documentation
Completed

4. Project Implementation Steps
Dataset Download and Loading
Download dataset via KaggleHub.
Load CSV file into Pandas DataFrame.
Inspect columns, check for missing values, and count rows.
Sequential Execution
Filter profiles with compatibility_score > 70.
Compute average compatibility_score.
Sort dataset by compatibility_score descending.
Measure total execution time.
Parallel Execution (Threading)
Define three functions for filter, average, and sort.
Run them concurrently using Python threading.
Store results in a shared dictionary.
Measure execution time.
Parallel Execution (Multiprocessing)
Split the dataset into chunks for each process.
Use multiprocessing Pool to run operations concurrently.
Measure execution time.
Compare overhead vs threading.
Results and Performance Comparison
Number of filtered rows.
Average compatibility score.
Top 5 profiles sorted by compatibility.
Execution times for sequential vs parallel.
Summary Table
Display all results and performance metrics in a clear, readable table.

5. Performance Analysis
Threading vs Sequential
- Sequential execution took 2.611 seconds for the dataset.
- Parallel execution using threading took 2.856 seconds, slightly slower than sequential.
- The operations (filtering, computing mean, sorting) are CPU-bound, and Python’s Global Interpreter Lock (GIL) allows only one thread to execute Python bytecode at a time. Thread creation and synchronization overhead   caused the parallel version to run slower than the sequential version for this dataset.
Multiprocessing (optional)
- Using multiprocessing without chunking incurs high overhead due to copying the DataFrame to separate processes.
- Proper chunking of the dataset and aggregating results is required to achieve performance gains for CPU-heavy operations.

Observations
- Threading is efficient for I/O-bound tasks or light operations on small datasets.
- Sequential execution can outperform threading for CPU-bound operations on small to medium datasets due to thread overhead and the GIL.
- Multiprocessing can show real parallel speedup for CPU-heavy tasks if the dataset is large and properly split into chunks

7. Team Members and Roles
Name
Role
Jullie Anne Temporosa - Project Lead  
Paule Kenneth Dela Rosa
Raxell Louis I. Constantino - Data Analysis 
Liz Samantha De Rojas - Documentation / Report Preparation
David Jeremy Contreras - Documentation / Report Preparation
Miguel Laxamana - Testing & Validation

8. Instructions for Running the Project
Install required libraries:
pip install pandas kagglehub
Open the Jupyter Notebook or Google Colab file.
Run the notebook sequentially:
  - Dataset download & loading
  - Sequential execution
  - Parallel execution (threading)
  - Display results & comparison tables
Inspect tables for filtered rows, average score, top 5 profiles, and execution times.


