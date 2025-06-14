## Employee Names

Write a query that prints a list of employee names (i.e.: the _name_ attribute) from the **Employee** table in alphabetical order.

**Input Format**

The **Employee** table containing employee data for a company is described as follows:

<table><thead>
  <tr>
    <th>Column</th>
    <th>Type</th>
  </tr></thead>
<tbody>
  <tr>
    <td>employee_id</td>
    <td>Integer</td>
  </tr>
  <tr>
    <td>name</td>
    <td>String</td>
  </tr>
  <tr>
    <td>months</td>
    <td>Integer</td>
  </tr>
  <tr>
    <td>salary</td>
    <td>Integer</td>
  </tr>
</tbody>
</table>

where _employee_id_ is an employee's ID number, _name_ is their name, _months_ is the total number of months they've been working for the company, and _salary_ is their monthly salary.

**Sample Input**

<table><thead>
  <tr>
    <th>employee_id</th>
    <th>name</th>
    <th>months</th>
    <th>salary</th>
  </tr></thead>
<tbody>
  <tr>
    <td>12228</td>
    <td>Rose</td>
    <td>15</td>
    <td>1960</td>
  </tr>
  <tr>
    <td>33645</td>
    <td>Angela</td>
    <td>1</td>
    <td></td>
  </tr>
  <tr>
    <td>45692</td>
    <td>Frank</td>
    <td>17</td>
    <td>1608</td>
  </tr>
  <tr>
    <td>56118</td>
    <td>Patrick</td>
    <td>7</td>
    <td>1345</td>
  </tr>
  <tr>
    <td>59725</td>
    <td>Lisa</td>
    <td>11</td>
    <td>2330</td>
  </tr>
  <tr>
    <td>74197</td>
    <td>Kimberly</td>
    <td>16</td>
    <td>4372</td>
  </tr>
  <tr>
    <td>78454</td>
    <td>Bonnie</td>
    <td>8</td>
    <td>1771</td>
  </tr>
  <tr>
    <td>83565</td>
    <td>Michael</td>
    <td>6</td>
    <td>2017</td>
  </tr>
  <tr>
    <td>98607</td>
    <td>Todd</td>
    <td>5</td>
    <td>3396</td>
  </tr>
  <tr>
    <td>99989</td>
    <td>Joe</td>
    <td>9</td>
    <td>3573</td>
  </tr>
</tbody>
</table>

**Sample Output**

```
Angela
Bonnie
Frank
Joe
Kimberly
Lisa
Michael
Patrick
Rose
Todd
```

### Solution

```sql
SELECT name 
FROM Employee 
ORDER BY name;
```
