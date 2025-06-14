## Weather Observation Station 5

Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.
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

Sample Input

For example, CITY has four entries: DEF, ABC, PQRS and WXY.

Sample Output

```
ABC 3
PQRS 4
Explanation
```

When ordered alphabetically, the CITY names are listed as ABC, DEF, PQRS, and WXY, with lengths and . The longest name is PQRS, but there are options for shortest named city. Choose ABC, because it comes first alphabetically.

Note
You can write two separate queries to get the desired output. It need not be a single query.

### Response 
Ordering City by Ascending

```sql
SELECT CITY, LENGTH(CITY) AS name_length
FROM STATION
ORDER BY LENGTH(CITY) ASC, CITY ASC
LIMIT 1;
```

### Response 
Ordering City by Descending

```sql
SELECT CITY, LENGTH(CITY) AS name_length
FROM STATION
ORDER BY LENGTH(CITY) DESC, CITY ASC
LIMIT 1;
```