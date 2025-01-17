---
uid: GetElementAlarmCountForView
---

# GetElementAlarmCountForView

Use this method to retrieve the elements with the largest/smallest number of alarms for each alarm severity for the specified view.

## Input

| Item | Format | Description |
|--|--|--|
| Connection | String | The connection ID. See [ConnectApp](xref:ConnectApp). |
| ViewID | Integer | The view ID. |
| Limit | Integer | The number of elements with the most/least alarms that should be retrieved. |
| SortASC | Boolean | Indicates whether the elements with the largest or the smallest number of alarms should be retrieved. |
| UtcStartTime | Long integer | The start time of the timespan for which the alarm count should be retrieved, in UTC format (milliseconds since midnight January 1, 1970 GMT). |
| UtcEndTime | Long integer | The end time of the timespan for which the alarm count should be retrieved, in UTC format (milliseconds since midnight January 1, 1970 GMT). |

## Output

| Item | Format | Description |
|--|--|--|
| GetElementAlarmCount­ForViewResult | Array of [DMATopAlarmCountData](xref:DMATopAlarmCountData) | The elements with the largest/smallest number of alarms for each alarm severity. |
