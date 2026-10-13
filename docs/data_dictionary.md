# Data Dictionary

## Dataset Overview
The project uses the Brazilian E-Commerce Public Dataset by Olist.

## Main Tables

### Customers — `olist_customers_dataset`
- `customer_id`: Customer identifier associated with an order.
- `customer_unique_id`: Identifier used to recognize a customer across orders.
- `customer_city`: Customer city.
- `customer_state`: Customer state.

### Orders — `olist_orders_dataset`
- `order_id`: Unique order identifier.
- `customer_id`: Customer identifier associated with the order.
- `order_status`: Order status.
- `order_purchase_timestamp`: Date and time the order was placed.

### Order Items — `olist_order_items_dataset`
- `order_id`: Order identifier.
- `product_id`: Product identifier.
- `price`: Price of the item.
- `freight_value`: Shipping charge associated with the item.

### Products — `olist_products_dataset`
- `product_id`: Product identifier.
- `product_category_name`: Product category.

### Payments — `olist_order_payments_dataset`
- `order_id`: Order identifier.
- `payment_type`: Payment method.
- `payment_value`: Recorded payment amount.

## Important Notes
- `customer_unique_id` is useful for identifying repeat customers across different orders.
- Item revenue can be calculated by summing `price` in the order items table.
- Payment value and item revenue are different measures and should not be treated as interchangeable.
- The dataset records Brazilian e-commerce transactions, so monetary values are in Brazilian reais (BRL).

Column names may differ if they were renamed during Power Query transformations.