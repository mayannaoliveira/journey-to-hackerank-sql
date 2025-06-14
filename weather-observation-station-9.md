## Weather Observation Station 9

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.

**Input Format**

The STATION table is described as follows:

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

where LAT_N is the northern latitude and LONG_W is the western longitude.

### Solution

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE NOT (CITY LIKE 'A%' 
           OR CITY LIKE 'E%' 
           OR CITY LIKE 'I%' 
           OR CITY LIKE 'O%' 
           OR CITY LIKE 'U%');
```