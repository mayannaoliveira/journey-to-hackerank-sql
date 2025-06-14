## Select All

Query all columns (attributes) for every row in the **CITY** table.

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
SELECT ID, NAME, COUNTRYCODE, DISTRICT, POPULATION 
FROM CITY;
```