# E-Commerce Dashboard Project

This project visualizes key metrics of an E-Commerce store using **Power BI**.  
It demonstrates data modeling, measure creation, and building interactive dashboards from CSV exports.

---

## 📂 Project Files

- `Ecommerce_Dashboard.pbix` – Power BI file with all visuals and measures  
- CSV files:  
  - `customers.csv`  
  - `products.csv`  
  - `orders.csv`  
  - `order_items.csv`  
  - `payments.csv`  
- `Ecommerce_Dashboard_Screenshot.png` – Screenshot of the full dashboard  
- `README.md` – project documentation  

---

## 🗄 Tables & Relationships

| Table          | Key Columns | Notes |
|----------------|------------|-------|
| `customers`    | customer_id | Stores customer info |
| `products`     | product_id, price, category | Product catalog |
| `orders`       | order_id, customer_id, order_date, status | Customer orders |
| `order_items`  | order_item, order_id, product_id, quantity, price | Items per order |
| `payments`     | payment_id, order_id, amount, payment_method | Payment records |

**Relationships:**  
- `customers[customer_id] → orders[customer_id]`  
- `orders[order_id] → order_items[order_id]`  
- `orders[order_id] → payments[order_id]`  
- `products[product_id] → order_items[product_id]`  

---

## 📊 Measures Created

- **Total Sales** = Sum of `quantity * price` from `order_items`  
- **Total Orders** = Count of rows in `orders`  
- **Average Order Value** = `Total Sales / Total Orders`  
- **Total Customers** = Distinct count of `customers[customer_id]`  
- **Total Payments** = Sum of `payments[amount]`  

---

## 🖼 Dashboard Screenshot

![<img width="970" height="538" alt="Ecommerce_Dashboard_Screenshot" src="https://github.com/user-attachments/assets/2727193a-0733-41bd-bce0-09331925fc50" />
](Ecommerce_Dashboard_Screenshot.png)

> 💡 The screenshot shows KPI cards, charts, and table for the full E-Commerce dashboard.  

---

## 📌 Notes
- Data comes from CSV exports.  
- Dashboard is interactive; users can filter by date, product, or customer.  
- All measures are created in **DAX** within Power BI.  

---

## 📝 How to Use
1. Download the `.pbix` file.  
2. Open in **Power BI Desktop**.  
3. Interact with filters, slicers, and visuals.  
4. Optional: Replace CSV files with your own data to update dashboard.
