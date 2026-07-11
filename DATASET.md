# Dataset Description — TheLook E-commerce Dataset

This project uses the **TheLook E-commerce Dataset**, a publicly available retail dataset hosted by Google Cloud BigQuery. The dataset was created to simulate the operations of an online fashion retailer and is designed for practising SQL, data analytics, business intelligence, and machine learning workflows.

Unlike many small demonstration datasets, TheLook contains multiple relational tables representing different stages of the customer journey, allowing analysts to perform end-to-end analyses ranging from customer acquisition to purchasing behaviour and revenue forecasting.

The dataset is particularly well suited for portfolio projects because it closely resembles the structure of a real-world transactional database while remaining freely accessible.

## Data Source

The dataset is available through the Google Cloud Public Datasets Program and can be queried directly within Google BigQuery without downloading any data.

**Dataset:**
```
bigquery-public-data.thelook_ecommerce
```

**Official documentation:**
https://console.cloud.google.com/marketplace/product/bigquery-public-data/thelook-ecommerce

Because the dataset is hosted as a public BigQuery dataset, users only need a Google Cloud account to execute SQL queries. The project can be analysed directly in BigQuery or exported to Python, R, Tableau, or Power BI for further analysis.

## Database Structure

The dataset consists of multiple relational tables linked primarily through user, order, and product identifiers.

| Table | Description |
|---|---|
| `users` | Customer demographic information including age, gender, location and acquisition channel |
| `events` | Clickstream data capturing customer browsing behaviour (home, department, product, cart, purchase, cancel) |
| `orders` | Order-level information including timestamps, status and customer identifiers |
| `order_items` | Product-level transaction records including sale price and product identifiers |
| `products` | Product catalogue containing brand, category, department and retail price |
| `inventory_items` | Inventory information including cost, distribution centre and stock status |
| `distribution_centers` | Warehouse and distribution centre locations |

## Entity Relationship Overview

The dataset follows a relational database design:

```
Users
  │
  ├────────────┐
  │            │
Orders       Events
  │
Order Items
  │
Products
  │
Inventory Items
  │
Distribution Centers
```

This schema enables analyses at multiple levels:

- Customer level
- Session level
- Order level
- Product level
- Inventory level

## Dataset Characteristics

| Characteristic | Description |
|---|---|
| Industry | Fashion E-commerce |
| Database | Google BigQuery |
| Type | Relational SQL Database |
| Records | Millions of event and transaction records |
| Time Series | Yes |
| Behavioural Data | Yes |
| Transaction Data | Yes |
| Customer Data | Yes |
| Product Data | Yes |

The dataset combines transactional, behavioural, and demographic information, making it suitable for a broad range of analytics applications.

## Why this Dataset?

The dataset was selected because it supports a complete end-to-end analytics workflow covering descriptive, diagnostic, predictive, and causal analyses.

It enables the investigation of business questions across multiple domains, including:

- customer behaviour and acquisition
- sales and revenue analysis
- product performance
- conversion funnel optimisation
- cohort and retention analysis
- revenue forecasting
- A/B testing
- causal inference using Propensity Score Matching

The relational structure also allows realistic feature engineering and the application of statistical and machine learning methods commonly used in commercial analytics environments.

## Dataset Limitations

Although TheLook closely resembles a production e-commerce database, it is a **synthetic dataset** generated for educational purposes. Consequently, some behavioural patterns are more uniform than would typically be expected in real-world commercial data. For example, acquisition channels often exhibit very similar conversion rates, and certain customer behaviours may lack the heterogeneity observed in operational businesses.

These characteristics should be considered when interpreting analytical results. While the dataset is highly valuable for demonstrating technical and analytical skills, findings should not be interpreted as evidence of real consumer behaviour.
