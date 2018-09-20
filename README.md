<!DOCTYPE html>
<html lang="srb">
<head>
	<meta charset="utf-8">
	<meta name="description" content="example HTML5">
	<meta name="keywords" content="primer, vezba">
	<meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0" /> 
	<title>PREKVALIFIKANT</title>
	<link rel="stylesheet" href="mystyles.css">
</head>
<body>
<div id="wrapper">
	<header id="main_header">
		<h1>Every Day Drinkers Affiliate</h1>
	</header>
	<nav id="main_menu">
		<ul>
			<li><a href="index.html" title="home" style="text-decoration:none">home</a></li>
			<li><a href="galerija.html" title="galerija" style="text-decoration:none">galerija</a></li>
			<li><a href="kontakt.html" title="kontakt" style="text-decoration:none">kontakt</a></li>
		</ul>
	</nav>
<section id="main_section">
<?php

include ('conn.php');
$query = "SELECT * FROM naslov_vesti";
$naslov_vesti = mysqli_query ($conn, $query);
	echo "<article>";
	echo "<header>";
	while ($row = mysqli_fetch_array($naslov_vesti)) {
		echo "<h1>";
		echo $row['naslov'];	
		echo "</h1>";
		echo "</header>";
		}
$queryNew = "SELECT * FROM vesti";
$vesti = mysqli_query ($conn, $queryNew);
	while ($rowNew = mysqli_fetch_array($vesti)){
	echo "<p>";
	echo $rowNew['vest'];
	echo "</p>";
	echo "</article>";}
	
$query_2 = "SELECT * FROM naslov_vesti_2";
$naslov_vesti_2 = mysqli_query ($conn, $query_2);
	echo "<article>";
	echo "<header>";
	while ($row_2 = mysqli_fetch_array($naslov_vesti_2)) {
		echo "<h1>";
		echo $row_2['naslov2'];	
		echo "</h1>";
		echo "</header>";
		}
$queryNew_2 = "SELECT * FROM vesti_2";
$vesti_2 = mysqli_query ($conn, $queryNew_2);
	while ($rowNew_2 = mysqli_fetch_array($vesti_2)){
	echo "<p>";
	echo $rowNew_2['vest2'];
	echo "</p>";
	echo "</article>";}
	?>
</section>

<aside id="main_aside">
		<blockquote>Integer convallis id metus vitae blandit</blockquote>
		<blockquote>Aliquam cursus magna sem, quis lobortis ante commodo et.</blockquote>
</aside>

<footer id="main_footer">
	Public GNU
</footer>	

</div>
</body>
</html>
