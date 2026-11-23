# County Rainfall and Planting Advisory

## Project summary

A farmer-support NGO sends SMS planting advice to farmers in five counties (Nairobi, Nakuru, Kisumu, Mombasa and Machakos). This project cleans the hand-typed Machakos rainfall readings (invalid entries are imputed with the rounded average of the valid months), combines all five counties into a 5 x 12 NumPy array, and calculates annual totals, monthly averages, wettest months, dry-month counts (below 50 mm) and the best two-consecutive-month planting window for each county. Results are saved to `rainfall_summary.csv`.

## How to run

1. Install the requirements: `pip install -r requirements.txt`
2. Open `rainfall_analysis.ipynb` in Jupyter or Google Colab and choose **Restart and Run All**.
3. The notebook writes `rainfall_summary.csv` in the same folder.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/origopeter009-collab/plp-da-a2-rainfall-advisory/blob/main/rainfall_analysis.ipynb)

## Planting advisory

- Farmers in Nairobi, Nakuru, Kisumu and Mombasa should plant in April-May, the wettest two-month window in all four counties (265 mm combined in Nakuru up to 420 mm in Kisumu).
- Machakos is the driest county (811 mm a year, 6 dry months) and its rains come later, so farmers there should plant in November-December (278 mm combined) with drought-tolerant crops.
- Caveat: Machakos's April and September readings were missing and were filled with the 68 mm average, so its totals and dry-month count should be confirmed with the station before advice is sent.
