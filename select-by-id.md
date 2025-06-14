## Select By ID
Query all columns for a city in **CITY** with the _ID_ `1661`.

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
SELECT * FROM CITY WHERE ID = 1661;
```