# simple-chart-patterns-detection

## Overview
This repository provides a Python script (`patterns.py`) for detecting various stock chart patterns using `pandas` and `numpy`. These patterns include:

- Head and Shoulders
- Multiple Tops and Bottoms
- Support and Resistance Levels
- Triangle Patterns
- Wedges
- Channels
- Double Tops and Bottoms
- Trendlines
- Pivot Points

## Installation

Ensure you have Python installed along with the required dependencies:

```bash
pip install pandas numpy
```

## Usage

### Importing the Script

```python
import pandas as pd
import patterns

# Example DataFrame
data = {
    'High': [110, 112, 115, 113, 116, 118, 117],
    'Low': [105, 107, 109, 108, 110, 112, 111],
    'Close': [108, 110, 113, 111, 114, 116, 115]
}
df = pd.DataFrame(data)

# Detect Head and Shoulders
result = patterns.detect_head_shoulder(df)
print(result[['High', 'Low', 'head_shoulder_pattern']])
```

### Available Functions

#### 1. Detect Head and Shoulders
```python
patterns.detect_head_shoulder(df, window=3)
```
Detects head and shoulders and inverse head and shoulders patterns.

#### 2. Detect Multiple Tops and Bottoms
```python
patterns.detect_multiple_tops_bottoms(df, window=3)
```
Identifies multiple top and bottom patterns.

#### 3. Calculate Support and Resistance
```python
patterns.calculate_support_resistance(df, window=3)
```
Calculates support and resistance levels using rolling statistics.

#### 4. Detect Triangle Patterns
```python
patterns.detect_triangle_pattern(df, window=3)
```
Identifies ascending and descending triangles.

#### 5. Detect Wedges
```python
patterns.detect_wedge(df, window=3)
```
Detects wedge-up and wedge-down patterns.

#### 6. Detect Channels
```python
patterns.detect_channel(df, window=3)
```
Finds channel-up and channel-down formations.

#### 7. Detect Double Tops and Bottoms
```python
patterns.detect_double_top_bottom(df, window=3, threshold=0.05)
```
Identifies double-top and double-bottom patterns.

#### 8. Detect Trendlines
```python
patterns.detect_trendline(df, window=2)
```
Calculates trendline support and resistance.

#### 9. Find Pivot Points
```python
patterns.find_pivots(df)
```
Finds pivot points based on price action.

## License
This project is licensed under the MIT License.

## Contributions
Feel free to open issues or submit pull requests to improve this script.

## Contact
For any questions, reach out via GitHub Issues.

