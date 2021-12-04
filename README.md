<h1> Seus dados foram salvos</h1>

<?php

 $n = $_POST["n"];
 $data = $_POST["data"];
 $firma = $_POST["firma"];
 $ender = $_POST["ender"];
 $compl = $_POST["compl"];
 $bairro = $_POST["bairro"];
 $cidade = $_POST["cidade"];
 $estado = $_POST["estado"];
 $cep = $_POST["cep"];
 $cnpj = $_POST["cnpj"];
 $inscri = $_POST["inscr"];
 $tels = $_POST["tels"];
 $cel = $_POST["cel"];
 $email = $_POST["email"];
 $obs = $_POST["obs"];

 if(empty($firma)) {
     echo "<p>O nome da firma deve ser informado</p>";
 } 
 else {
     
     file_put_contents("dados.csv", "$n,$data,$firma,$ender,$compl,$bairro,$cidade,$estado,$cep,$cnpj,$inscri,$tels,$cel,$email,$obs\n", FILE_APPEND);
  }
?>
