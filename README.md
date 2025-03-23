# 🛠️ Recyclable and Low Fat Products (LEETCODE PROBLEM)

## 📌 Problem Description
We have a table called `Products` that holds information about different products. It looks like this:

| Column Name | Type          |
|-------------|---------------|
| `product_id` | `int`         |
| `low_fats`   | `enum('Y', 'N')` |
| `recyclable` | `enum('Y', 'N')` |

### 🧾 Explanation of columns:
- **`product_id`**: A unique number for each product.
- **`low_fats`**: 'Y' means the product is low fat, 'N' means it is not.
- **`recyclable`**: 'Y' means the product is recyclable, 'N' means it is not.

---

## 🎯 Goal
We want to **find the product IDs** for products that are **both low fat and recyclable**.

---

## 🔍 Example
Imagine the table looks like this:

| `product_id` | `low_fats` | `recyclable` |
|--------------|------------|--------------|
| 1            | Y          | Y            |
| 2            | N          | Y            |
| 3            | Y          | N            |
| 4            | Y          | Y            |
| 5            | N          | N            |

The products that are **both low fat and recyclable** are **Product 1** and **Product 4**.

✅ Expected output:

| `product_id` |
|--------------|
| 1            |
| 4            |

---

## 🛠️ SQL Query Solution
Here’s a simple SQL query to solve this:

```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y' AND recyclable = 'Y';
```

### 💡 Explanation of the query:
1. **`SELECT product_id`**: This picks the product ID from the table.
2. **`FROM Products`**: This tells SQL we’re working with the `Products` table.
3. **`WHERE low_fats = 'Y' AND recyclable = 'Y'`**: This checks each row to see if the product is low fat **AND** recyclable. Only rows that have 'Y' in both columns will be included.

✅ **Result:** We get the product IDs of products that are both low fat and recyclable.

---

✨ **Now you’re ready to filter out the eco-friendly, healthy products like a SQL pro!** 🌟

