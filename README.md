[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23209952&assignment_repo_type=AssignmentRepo)
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
