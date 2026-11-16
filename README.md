Customer Analytics Data Warehouse
Experiment 5: Classification Algorithms Using Python
This experiment implements and compares two supervised classification algorithms:
- Decision Tree
- Gaussian Naive Bayes
The models use the Exited attribute as the target. In the dataset, 0 represents a customer who stayed and 1 represents a customer who exited.
Dataset
The practical uses the customer dataset file named Churn_Modelling.csv. This is the source CSV filename retained by the supplied practical. The project/report title is Customer Analytics Data Warehouse.

The dataset contains 10,000 records and 14 original attributes. Features used by the models include CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, and EstimatedSalary. Identifier columns (RowNumber, CustomerId, and Surname) are removed before training.
Requirements
- Python 3.9 or newer
- pandas
- matplotlib
- seaborn
- scikit-learn
Install dependencies:
pip install pandas matplotlib seaborn scikit-learn
Files
- Customer_Analytics_Data_Warehouse_Experiment_5.docx - editable updated practical document
- Customer_Analytics_Data_Warehouse_Experiment_5.pdf - PDF version of the practical
- customer_analytics_classification.py - complete runnable Python implementation
- README.md - project and execution instructions
How to Run
1. Download Churn_Modelling.csv and place it in the project folder, or note its full path.
2. Open a terminal in the project folder.
3. Install the required Python packages.
4. Run:
python customer_analytics_classification.py Churn_Modelling.csv
To print the confusion matrices without opening heatmap windows:
python customer_analytics_classification.py Churn_Modelling.csv --no-plots
The script performs the same workflow as the practical: removes identifier columns, applies one-hot encoding to Geography and Gender, creates an 80:20 stratified training/testing split using random_state=42, trains both classifiers, and prints accuracy, precision, recall, F1-score, classification reports, confusion matrices, and a model comparison table.
Notes on the Recorded Results
The practical document retains its recorded results and inference. Results may vary if the CSV data, preprocessing, scikit-learn version, or model settings differ. Do not treat the displayed values as guaranteed output from every environment. Since the dataset has imbalanced target classes, review recall and F1-score for class 1 (Exited) alongside overall accuracy.
Result
Decision Tree and Gaussian Naive Bayes classification algorithms are implemented using Python, evaluated on a held-out test dataset, and compared using standard classification metrics.
