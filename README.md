<? php
    session_start() ;  // Initialize the session
// store the submitted data sent
// via POST method, stored. 
$_SESSION['Name of Animal']=$_POST['user_name'];
$_SESSION['category']=$_POST['category'];
$_SESSION['submit']=$_POST['submit'];

? >

<?php
   session_start() ;

$insert_query="insert into data(Name of animal, category, Image, Description, Life expectancy)  values("$_SESSION['Name of Animal']",
           "$_SESSION['category']", 
           "$_SESSION['Image']", 
           "$_SESSION['Discription']", 
            "$_SESSION['Life expectancy']") ;"

   // run the query
mysql_query($insert_query) ;
? >

<pre> Successfully submitted</pre>
     
