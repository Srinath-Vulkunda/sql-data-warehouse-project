USE DataWarehouse;

select * from bronze.crm_cust_info;

USE DataWarehouse;

-- =====================================================
-- Load Bronze Layer
-- Description:
-- Loads raw data from CSV files into Bronze tables.
-- Update the file paths according to your MySQL
-- secure-file-priv directory.
-- =====================================================

-- =============================================
-- Load CRM Customer Information
-- =============================================
TRUNCATE TABLE bronze.crm_cust_info;
SET GLOBAL local_infile = 1;

LOAD DATA LOCAL INFILE "Your file path"
INTO TABLE bronze.crm_cust_info
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;

SELECT COUNT(*) AS total_records
FROM bronze.crm_cust_info;

-- =============================================
-- Load CRM Product Information
-- =============================================
TRUNCATE TABLE bronze.crm_prd_info;

LOAD DATA LOCAL INFILE "C:/Users/srina/Downloads/sql-data-warehouse-project/sql-data-warehouse-project/datasets/source_crm/prd_info.csv"
INTO TABLE bronze.crm_prd_info
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;

SELECT COUNT(*) AS total_records
FROM bronze.crm_prd_info;

-- =============================================
-- Load CRM Sales Details
-- =============================================
TRUNCATE TABLE bronze.crm_sales_details;

LOAD DATA LOCAL INFILE "C:/Users/srina/Downloads/sql-data-warehouse-project/sql-data-warehouse-project/datasets/source_crm/sales_details.csv"
INTO TABLE bronze.crm_sales_details
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;

SELECT COUNT(*) AS total_records
FROM bronze.crm_sales_details;

-- =============================================
-- Load ERP Customer Location
-- =============================================
TRUNCATE TABLE bronze.erp_loc_a101;

LOAD DATA LOCAL INFILE "C:/Users/srina/Downloads/sql-data-warehouse-project/sql-data-warehouse-project/datasets/source_erp/CUST_AZ12.csv"
INTO TABLE bronze.erp_loc_a101
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;

SELECT COUNT(*) AS total_records
FROM bronze.erp_loc_a101;

-- =============================================
-- Load ERP Customer Information
-- =============================================
TRUNCATE TABLE bronze.erp_cust_az12;

LOAD DATA LOCAL INFILE "C:/Users/srina/Downloads/sql-data-warehouse-project/sql-data-warehouse-project/datasets/source_erp/LOC_A101.csv"
INTO TABLE bronze.erp_cust_az12
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;

SELECT COUNT(*) AS total_records
FROM bronze.erp_cust_az12;

-- =============================================
-- Load ERP Product Categories
-- =============================================
TRUNCATE TABLE bronze.erp_px_cat_g1v2;

LOAD DATA LOCAL INFILE "C:/Users/srina/Downloads/sql-data-warehouse-project/sql-data-warehouse-project/datasets/source_erp/PX_CAT_G1V2.csv"
INTO TABLE bronze.erp_px_cat_g1v2
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;

SELECT COUNT(*) AS total_records
FROM bronze.erp_px_cat_g1v2;
