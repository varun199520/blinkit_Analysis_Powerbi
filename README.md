# Blinkit Analytics Dashboard

A comprehensive analytics solution for Blinkit (quick commerce platform) featuring data generation, visualization, and database management tools.

## 🚀 Features

### 📊 Power BI Dashboard
- Interactive Power BI dashboard for comprehensive business analytics
- Real-time data visualization and reporting
- KPI tracking and performance metrics
- Multiple data sources integration
- **Live Dashboard**: [View Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNDA1YWI0NTAtNGRhMi00ODNhLWI0ODItMjY4NWU5ZWE5NzIxIiwidCI6Ijk4NGJiNWVmLTEyMmItNDU0NC05NzVkLTRhOWFjYTVhNGNjOCIsImMiOjZ9)

### 🐍 Python Data Generation
- **DataCreator.py**: Advanced Python script for generating realistic Blinkit business data
- Generates comprehensive datasets including:
  - Customer data with segments and order history
  - Product catalog with categories and inventory
  - Order transactions and delivery performance
  - Customer feedback and ratings
  - Marketing campaign performance
  - Inventory management data

### 🗄️ Database Management
- **test_db.sql**: Database schema and sample queries
- MySQL database structure for storing analytics data
- Optimized for quick commerce operations

### 📤 Excel Uploader
- Flask-based web application for data upload
- Support for CSV and Excel file formats
- Automated table creation and data insertion
- Database connection management
- Secure file handling and validation

### 🌐 Portfolio Website
- Professional portfolio showcase
- Responsive HTML design
- Project documentation and demos

## 📁 Project Structure

```
Blinkit Dashboard V-2/
├── Blinkit Dashboard.pbix              # Power BI dashboard file
├── Python Script to Generate Data/
│   ├── DataCreator.py                  # Main data generation script
│   ├── blinkit_customers.csv           # Customer dataset
│   ├── blinkit_products.csv            # Product catalog
│   ├── blinkit_orders.csv              # Order transactions
│   ├── blinkit_order_items.csv         # Order line items
│   ├── blinkit_inventory.csv           # Inventory tracking
│   ├── blinkit_delivery_performance.csv # Delivery metrics
│   ├── blinkit_customer_feedback.csv   # Customer reviews
│   └── blinkit_marketing_performance.csv # Marketing analytics
├── Excel Uploader/
│   └── excel_uploader/
│       ├── app.py                      # Flask application
│       └── templates/
│           ├── index.html              # Database connection page
│           └── upload.html             # File upload interface
├── Database/
│   └── test_db.sql                     # Database schema
└── Blinkit Portfolio/
    ├── index.html                      # Portfolio website
    └── img/                            # Project images and assets
```

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.7+
- MySQL Database
- Power BI Desktop (for dashboard)
- Flask (for Excel Uploader)

### Python Dependencies
```bash
pip install pandas numpy faker mysql-connector-python flask werkzeug
```

### Database Setup
1. Create a MySQL database
2. Import the schema from `Database/test_db.sql`
3. Configure connection parameters in the Excel Uploader

### Running the Data Generator
```bash
cd "Python Script to Generate Data"
python DataCreator.py
```

### Running the Excel Uploader
```bash
cd Excel\ Uploader/excel_uploader
python app.py
```
Access the application at `http://localhost:5000`

## 📊 Data Generated

The system generates comprehensive datasets covering:

- **Customers**: 25,000+ customer records with demographics, segments, and order history
- **Products**: 300+ products across 11 categories with pricing and inventory data
- **Orders**: 50,000+ transactions with delivery performance metrics
- **Inventory**: Daily stock levels and movements
- **Feedback**: Customer ratings and reviews with sentiment analysis
- **Marketing**: Campaign performance across multiple channels

## 🎯 Key Metrics Tracked

- **Operational**: Order volume, delivery times, inventory turnover
- **Customer**: Acquisition, retention, satisfaction scores
- **Financial**: Revenue, margins, payment methods
- **Marketing**: Campaign ROI, conversion rates, channel performance
- **Quality**: Product ratings, delivery performance, customer feedback

## 📈 Dashboard Features

- Real-time KPI monitoring
- Trend analysis and forecasting
- Customer segmentation analysis
- Product performance insights
- Delivery optimization recommendations
- Marketing campaign effectiveness

## 🔧 Customization

### Data Generation Parameters
Modify `DataCreator.py` to adjust:
- Date ranges for data generation
- Number of orders and customers
- Product categories and pricing
- Delivery performance scenarios
- Customer segments and behavior patterns

### Database Configuration
Update connection parameters in `Excel Uploader/app.py`:
```python
# Configure your database connection
db_config = {
    'host': 'your_host',
    'user': 'your_username', 
    'password': 'your_password',
    'database': 'your_database'
}
```

## 🚀 Usage Examples

### Generate Sample Data
```python
from DataCreator import generate_complete_blinkit_data, save_blinkit_data

# Generate data for 2024
data = generate_complete_blinkit_data(
    num_orders=50000,
    start_date='2024-01-01',
    end_date='2024-12-31'
)

# Save to CSV files
save_blinkit_data(data, prefix='blinkit_2024_')
```

### Upload Data to Database
1. Start the Excel Uploader application
2. Connect to your MySQL database
3. Upload CSV files generated by the data creator
4. Data is automatically processed and stored

## 📝 License

This project is created for educational and demonstration purposes. Please ensure compliance with data privacy regulations when using with real customer data.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:
- Additional data generation scenarios
- Dashboard enhancements
- Database optimization
- New analytics features

## 📞 Support

For questions or support, please refer to the project documentation or open an issue in the repository.

---

**Note**: This is a demonstration project for Blinkit analytics. Ensure all data privacy and security measures are in place when working with real business data.
