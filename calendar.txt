<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calender</title>
</head>
<body>
<?php
$columns = array('Tumi','Andrea','Zinza');
$num_cols = count($columns);
echo "<table>";
echo "<tr>";
foreach($columns as $col)
{
   echo "<td>$col</td>";
   for($i=1;$i<12;$i++)
{
    echo "<tr>";
    $datetime = new DateTime();
    for($j=0;$j<$num_cols;$j++){
        $datetime->modify('+1 hour');

        echo '<td>' . $datetime->format('H:i:s') . '</td>';
    }

    echo "</tr>";
 }
}
echo "</tr>";

echo "</table>";

 
?>
</body>
</html>


