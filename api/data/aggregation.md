# Aggregation

## Statistical Functions

| Name | Description |
|:---|---|
| `MIN`| Minimum value of selected samples.
| `MAX`| Maximum value of selected samples.
| `AVG`| Average value of selected samples.
| `SUM`| Sum of selected samples.
| `COUNT`| Number of selected samples.
| `FIRST`| First value of selected samples.
| `LAST`| Last value of selected samples.
| `DELTA`| Difference between last and first values in selected samples.
| `COUNTER` | Sum of positive differences between consecutive values of selected samples.
| `PERCENTILE_999` | 99.9% Percentile
| `PERCENTILE_995` | 99.5% Percentile
| `PERCENTILE_99` | 99% Percentile
| `PERCENTILE_95` | 95% Percentile
| `PERCENTILE_90` | 90% Percentile
| `PERCENTILE_75` | 75% Percentile
| `PERCENTILE_50` | 50% Percentile
| `PERCENTILE_25` | 25% Percentile
| `PERCENTILE_10` | 10% Percentile
| `PERCENTILE_5` | 5% Percentile
| `PERCENTILE_1` | 1% Percentile
| `PERCENTILE_05` | 0.5% Percentile
| `PERCENTILE_01` | 0.1% Percentile
| `MEDIAN` | Median value of selected samples.<br>Same as `PERCENTILE_50`  
| `STANDARD_DEVIATION` | Standard deviation of selected samples.
| `SLOPE` | Linear regression slope of selected samples.
| `INTERCEPT` | Linear regression intercept of selected samples.
| `WAVG` | Weighted average of selected samples.
| `WTAVG` | Weighted time average of selected samples.
| `THRESHOLD_COUNT` | Number of threshold violations in selected samples.
| `THRESHOLD_DURATION` | Cumulative duration of threshold violations in selected samples.
| `THRESHOLD_PERCENT` | Percentage of selected samples which violate threshold.
| `MIN_VALUE_TIME` | Unix time in milliseconds for maximum value in selected samples.
| `MAX_VALUE_TIME` | Unix time in milliseconds for minimum value in selected samples.
