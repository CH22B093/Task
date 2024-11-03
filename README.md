# Option Chain Analysis

This project retrieves option chain data using yfinance and calculates margin requirements and premium earned.

## Usage
1. Install required libraries: `pip install yfinance pandas`
2. Run the script: `python main.py`

## Functions
* **`get_option_chain_data(instrument, expiry_date)`:** 
    Retrieves option chain data for a given instrument and expiry date.

    Args:
        instrument_name: Name of the instrument (e.g., NIFTY or BANKNIFTY).
        expiry_date: The expiration date of the options, in YYYY-MM-DD format.
        side: Type of option to retrieve. Use "PE" for Put and "CE" for Call.

    Returns:
        A Pandas DataFrame containing the option chain data.
  
* **`calculate_margin_and_premium(option_data)`:** Calculates margin requirement and premium earned for a given option chain DataFrame.

  Args:
    option_data (pd.DataFrame): DataFrame returned by get_option_chain_data.

  Returns:
    pd.DataFrame: DataFrame with additional columns:
      - margin: Margin requirement for each option contract
      - premium: Premium earned for each option contract


## Challenges
* Initially, I had issues with accessing real-time option chain data. I overcame this by using yfinance, which provides delayed data.

## Insights
* Using yfinance simplified the data retrieval process compared to other APIs.

## AI Tools
* I used Gemini to:
    * Find alternative APIs for option chain data.
    * Understand the yfinance library and generate code for data retrieval and processing.
