## Weather Observation Station 2

Query the following two values from the **STATION** table:

1. The sum of all values in _LAT_N_ rounded to a scale of  decimal places.
2. The sum of all values in _LONG_W_ rounded to a scale of  decimal places.

**Input Format**

The **STATION** table is described as follows:

<table><thead>
  <tr>
    <th>Field</th>
    <th>Type</th>
  </tr></thead>
<tbody>
  <tr>
    <td>ID</td>
    <td>NUMBER</td>
  </tr>
  <tr>
    <td>CITY</td>
    <td>VARCHAR2(21)</td>
  </tr>
  <tr>
    <td>STATE</td>
    <td>VARCHAR2(2)</td>
  </tr>
  <tr>
    <td>LAT_N</td>
    <td>NUMBER</td>
  </tr>
  <tr>
    <td>LONG_W</td>
    <td>NUMBER</td>
  </tr>
</tbody>
</table>

where _LAT_N_ is the northern latitude and _LONG_W_ is the western longitude.

**Output Format**

Your results must be in the form:

```
lat lon
```

where  is the sum of all values in _LAT_N_ and  is the sum of all values in _LONG_W_. Both results must be rounded to a scale of  decimal places.

### Solution

```sql
SELECT 
    TO_CHAR(ROUND(SUM(LAT_N), 2), '999999999.99') AS lat,
    TO_CHAR(ROUND(SUM(LONG_W), 2), '999999999.99') AS lon
FROM 
    STATION;
```