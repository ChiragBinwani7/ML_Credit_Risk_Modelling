# ML-Based Credit Risk Modelling

A machine learning project built with Streamlit that predicts credit risk using various financial features. The application evaluates user inputs and calculates a **Default Probability**, a corresponding **Credit Score**, and a categorical **Rating** (Poor, Average, Good, Excellent).

## Features

- **Interactive UI**: Built with Streamlit for a smooth and responsive user experience.
- **Credit Risk Evaluation**: Considers key financial factors including:
  - Age & Income
  - Loan Amount & Tenure
  - Loan-to-Income & Credit Utilization Ratios
  - Delinquency History (DPD, Delinquency Ratio)
  - Open Loan Accounts
  - Residence Type, Loan Purpose, and Loan Type
- **Scoring System**: Outputs a standardized credit score scaled between 300 and 900.
- **Instant Feedback**: Color-coded probability and score markers (Green for healthy, Red for risky).

## Tech Stack

- **Python** (Data processing and backend logic)
- **Streamlit** (Frontend interface)
- **Scikit-learn** (Machine learning model and data scaling)
- **Pandas & NumPy** (Data manipulation)
- **Joblib** (Model loading)

## Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/ChiragBinwani7/ML_Credit_Risk_Modelling.git
   cd ML_Credit_Risk_Modelling
   ```

2. **Create a Virtual Environment (Optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**
   ```bash
   streamlit run main.py
   ```

## Project Structure

- `main.py`: The entry point for the Streamlit web application. Contains all UI components and input fields.
- `predictionhelper.py`: Helper functions to prepare input data, handle missing values, apply scaling, and interact with the loaded ML model.
- `artifacts/`: Directory containing the serialized ML model and preprocessing scalers (`model_data11.joblib`).
- `requirements.txt`: List of Python dependencies required to run the project.

## How it Works

1. The user inputs their financial data into the Streamlit interface.
2. The data is processed and scaled in `predictionhelper.py` using a pre-trained `MinMaxScaler`.
3. The model computes the default probability using a logistic function based on the feature weights.
4. The probability is converted into a traditional credit score (300-900) and categorized into a rating (Poor, Average, Good, Excellent).
5. Results are displayed instantly on the dashboard.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.