## Revising the Select Query I
Query all columns for all American cities in the **CITY** table with populations larger than `100000`. The **CountryCode** for America is `USA`.

The **CITY** table is described as follows:

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
<td>NAME</td>
<td>VARCHAR2(17)</td>
</tr>
<tr>
<td>COUNTRYCODE</td>
<td>VARCHAR2(3)</td>
</tr>
<tr>
<td>DISTRICT</td>
<td>VARCHAR2(20)</td>
</tr>
<tr>
<td>POPULATION</td>
<td>NUMBER</td>
</tr>
</tbody>
</table>

### Solution

```sql
SELECT *
FROM CITY
WHERE COUNTRYCODE = 'USA'
  AND POPULATION > 100000;
```