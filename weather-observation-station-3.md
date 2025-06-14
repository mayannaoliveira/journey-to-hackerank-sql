## Weather Observation Station 3

Query a list of **CITY** names from **STATION** for cities that have an even **ID** number. Print the results in any order, but exclude duplicates from the answer.  
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

where **LAT_N** is the northern latitude and **LONG_W** is the western longitude.

### Solution 

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE MOD(ID, 2) = 0;
```