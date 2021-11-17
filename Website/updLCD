<?php     
  require 'database.php';
  
  if (!empty($_POST)) {
    $notice = $_POST['notice'];
      
    // insert data
    $pdo = Database::connect();
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    $sql = "UPDATE notice SET notice = ?;
    $p = $pdo->prepare($sql);
    $p->execute(array($notice));
    Database::disconnect();
    header("Location: Main.php");
  }
?>
