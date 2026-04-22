# Methodology

## Data Preparation
- Loaded market sentiment and trader datasets
- Converted timestamps into a common date format
- Merged datasets using date as the key
- Cleaned sentiment labels by combining extreme categories

## Data Cleaning
- Removed missing values after merging
- Renamed columns for clarity (PnL, sentiment)
- Filtered out trades with zero PnL to avoid distortion

## Feature Engineering
- Created a "Win" indicator:
  - 1 if PnL > 0
  - 0 otherwise

## Analysis Approach
- Compared performance across sentiment:
  - Average PnL
  - Win rate
  - Trade size
- Performed segmentation:
  - Divided trades into high and low size groups using median split
- Analyzed how different segments behave under different sentiment conditions
