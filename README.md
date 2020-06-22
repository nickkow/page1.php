# page1.php
<!DOCTYPE html>
<html lang= "en" xmlns="http://www.w3.org./1999/xhtml">
    <head>
        <title>Registration Form</title>
    </head>
    <body>
<form actlon= "page1.php" mathod= "post">
<link rel="stylesheet" href="style.css" />

<h1><img class="inti" src="unnamed.png"></img><p>Clinical placement enrollment app </p></h1>

<table>
<tr>

<td><a>Name:</a><h2><input type="text" name ="name"></h2></td>
</tr>
<tr>
<td><a>ID:</a><h2><input type= "text" name = "ID"></h2></td>
</tr>
<tr>
<td><a>Sem:</a><h2><select name ="sem">
  <option value="2">2</option>
  <option value="3">3</option>
  <option value="4">4</option>
  <option value="5">5</option>
  <option value="6">6</option>
  <option value="7">7</option>
  <option value="8">8</option>
  <option value="9">9</option>
  </select></h2></td>
</tr>
<tr>
<td><a>Lecture:</a><h2><select name="lct">
  <option value="Yong YP">Yong YP</option>
  <option value="Yeoh BA"> Yeoh BA</option>
  <option value="Lim CZ">Lim CZ</option>
  <option value="Nyaw TN">Nyaw TN</option>
  <option value="Chin PM">Chin PM</option>
  <option value="Chong TF">Chong TF</option>
  <option value="Fu SS">Fu SS</option>
</select></h2></td>
</tr>
<tr>
<td><a>Date:</a><h2><input type="datetime-local"
       name="date"
       ></a></td>

</tr>
<tr>
<td><input type="submit" value= "Add Record"></td>
</tr>
</table>
</form>

<?php

$var1 = $_GET ['name'];
$var2 = $_GET ['ID'];
$var3 = $_GET ['sem'];
$var4 = $_GET ['lct'];
$var5 = $_GET ['date'];
$fileHandle = fopen("phpdatafile.txt",'w');


fwrite ($fileHandle,"NAME: " .$var1." | ");
fwrite ($fileHandle,"ID: ".$var2." | ");
fwrite ($fileHandle,"SEM: ".$var3." | ");
fwrite ($fileHandle,"LECTURE: ". $var4." | ");
fwrite ($fileHandle, "DATE: ".$var5."\n");


fclose ($fileHandle);


?>

</body>
</html>
