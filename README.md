# PFConsumoElectrico 🔌

A data integration project using SQL Server Integration Services (SSIS) to populate data warehouse dimensions from electrical companies' data.

## 📝 Description

This project extracts data from a source database containing information from three electricity companies and loads it into dimensional tables in a data warehouse. The ETL process is implemented using SQL Server Integration Services (SSIS).

## 🏗️ Architecture

The solution includes the following components:

- Source Database: `DB_DatosElectronorte`
- Destination Database: `DM_ConsumoEnergetico`
- Dimension Tables:
  - `DIM_TIEMPO` (Time Dimension)
  - `DIM_UBICACION` (Location Dimension)
  - `DIM_EMPRESA` (Company Dimension)
  - `DIM_CARTERA` (Portfolio Dimension)

## 🔄 Data Flow

The SSIS package includes the following transformations:

1. Load `DIM_TIEMPO`
2. Load `DIM_UBICACION`
3. Load `DIM_EMPRESA`
4. Load `DIM_CARTERA`
5. Load `CONSUMO_FACT`

## 🛠️ Technical Details

- Platform: SQL Server Integration Services (SSIS)
- Server: AN5-DS
- Authentication: SQL Server Authentication
- Data Provider: SQLOLEDB.1

## 📊 Dimensions

<details>
<summary>⏰ Time Dimension</summary>

- Year
- Month
- Month Name
- Season Name
</details>

<details>
<summary>📍 Location Dimension</summary>

- Department
- Province
- District
- Ubigeo Code
</details>

<details>
<summary>🏢 Company Dimension</summary>

- Company ID
- Company Name
</details>

<details>
<summary>📋 Cartera Dimension</summary>

- Cartera Code
- Cartera Description
- Rate Code
- Rate Description
</details>

## 🚀 Getting Started

1. Open the solution in Visual Studio
2. Configure the connection managers for source and destination databases
3. Execute the SSIS package to populate the dimensions

## 📄 Prerequisites

- SQL Server 2022
- SQL Server Integration Services
- Visual Studio with SSIS tools

## 👥 Authors

- Sair Bautista
- Americo Cordova
- Jose Ramirez
- [David Sandoval](https://github.com/sandovaldavid)

## 📝 License

This project is licensed under the terms of the `LICENSE.txt` file included in the repository.
