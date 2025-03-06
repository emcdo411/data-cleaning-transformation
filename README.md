Data/Example:
Script Title: Data Preprocessing for Retail CRM Analysis

Data Cleaning Steps:

Handling Missing Values:
python
Copy
Edit
data.fillna(method='ffill', inplace=True)  # Forward fill missing values
Removing Duplicates:
python
Copy
Edit
data.drop_duplicates(subset=['customer_id'], inplace=True)
Data Transformation:

Normalization:
python
Copy
Edit
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
data['purchase_amount'] = scaler.fit_transform(data[['purchase_amount']])
