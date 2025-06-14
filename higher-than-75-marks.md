## Higher Than 75 Marks

Query the Name of any student in STUDENTS who scored higher than  Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

### Input Format

The STUDENTS table is described as follows:  The Name column only contains uppercase (A-Z) and lowercase (a-z) letters.

Sample Input

<table>
<tbody>
<tr>
<td>Colunm</td>
<td>Type</td>
</tr>
<tr>
<td>ID</td>
<td>Integer</td>
</tr>
<tr>
<td>Name</td>
<td>String</td>
</tr>
<tr>
<td>Marks</td>
<td>Integer</td>
</tr>
</tbody>
</table>

The Name column only contains uppercase (A-Z) and lowercase (a-z) letters.

### Sample Input

<table>
<tbody>
<tr>
<td>ID</td>
<td>NAME</td>
<td>MARKS</td>
</tr>
<tr>
<td>1</td>
<td>Ashley</td>
<td>81</td>
</tr>
<tr>
<td>2</td>
<td>Samantha</td>
<td>75</td>
</tr>
<tr>
<td>4</td>
<td>Julia</td>
<td>76</td>
</tr>
<tr>
<td>3</td>
<td>Belvet</td>
<td>84</td>
</tr>
</tbody>
</table>

### Sample Output

```
Ashley
Julia
Belvet
Explanation
```

Only Ashley, Julia, and Belvet have Marks > . If you look at the last three characters of each of their names, there are no duplicates and 'ley' < 'lia' < 'vet'.

### Solution

```sql

SELECT Name
FROM STUDENTS
WHERE Marks > 75
ORDER BY SUBSTR(Name, LENGTH(Name) - 2, 3), ID ASC;

```