import pandas as pd
import numpy as np

# Load datasets
orders = pd.read_csv("olist_orders_dataset.csv")
customers = pd.read_csv("olist_customers_dataset.csv")

# Preview data
print("ORDERS DATA")
print(orders.head())
print(orders.shape)

print("\nCUSTOMERS DATA")
print(customers.head())
print(customers.shape)

orders_customers = pd.merge(
    orders,
    customers,
    on="customer_id",
    how="left"
)
print(orders_customers.head())
print(orders_customers.shape)

print(orders_customers.isnull().sum())
orders_customers.to_csv("orders_customers.csv", index=False)
print("Merged dataset saved!")
