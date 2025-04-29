# 📊 Data Pipeline for Market Data Integration

This project implements a data pipeline to extract, transform, and load (ETL) data from multiple sources into a unified dataset. The pipeline processes data from two companies, standardizes their formats, and combines them into a single CSV file for further analysis.

## 📁 Project Structure

- **`data_raw/`**: Contains raw data files:
  - 📄 `dados_empresaA.json`: JSON file with data from Company A.
  - 📄 `dados_empresaB.csv`: CSV file with data from Company B.
- **`data_processed/`**: Stores processed data:
  - ✅ `dados_combinados.csv`: Combined and standardized dataset.
- **`scripts/`**: Contains Python scripts for the ETL process:
  - 🛠️ `fusao_mercado_fev_refatorado.py`: Main script for the ETL pipeline.
  - 🧩 `processamento_dados_refatorado.py`: Module with helper functions for data processing.
- **`notebook/`**: 📓 Jupyter notebooks for data exploration and validation.

## 🔄 ETL Process

1. **Extract**:
   - 📥 Reads data from `dados_empresaA.json` and `dados_empresaB.csv` using the `Dados.leitura_dados` method.

2. **Transform**:
   - 🔧 Standardizes column names using a mapping dictionary.
   - 🔗 Merges data from both sources into a unified dataset.

3. **Load**:
   - 💾 Saves the combined dataset to `data_processed/dados_combinados.csv`.

## ✨ Key Features

- **📝 Data Standardization**: Ensures consistent column names across datasets.
- **🔗 Data Integration**: Combines data from multiple sources into a single file.
- **📈 Scalability**: Modular design allows easy extension for additional data sources.

## 📥 How to Download the Project

1. Clone the repository using Git:
```bash
   git clone https://github.com/vitorlinsbinski/pipeline_de_dados_python.git
```

2. Navigate to the project directory:
```bash
    cd pipeline_de_dados_python
```

## 🛠️ Setup
To ensure a clean and isolated environment for running the project, follow these steps:

1. Create a virtual environment:
```bash
    python3 -m venv .venv
```

2. Activate the virtual environment:
• On Linux/MacOS:
```bash
    source .venv/bin/activate
```
• On Windows:
```bash
    venv\Scripts\activate
```

3. Install dependencies:
```bash
    pip install -r requirements.txt
```

## 🚀 Usage

1. 📂 Place raw data files in the `data_raw/` directory.
2. ▶️ Run the main script:
```bash
   python scripts/fusao_mercado_fev_refatorado.py
```