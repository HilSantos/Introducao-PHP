# Introducao-PHP
Criação de variaveis no PHP

<form action="pg2.php" method="get">
    <label>Digite seu nome:</label>
    <input type="text" name="user" placeholder="Digite seu nome">
    <input type="text" name="ln" placeholder="Digite seu sobrenome">
    <input type="submit" value="Enviar">
</form>

-- Digite na barra de endereço o caminho do arquivo pg1 na pasta e atualize --

<?php
$nome = $_GET['user'];
$sobrenome = $_GET['ln'];
?>
<h1>
    <p> Olá <?= $nome . " " . $sobrenome ?> </p>
    <br><br>
<a ref="pg1.php">Voltar</a>
</h1>
-- O mesmo exemplo anterior pelo arquivo pg2 --

------------------------------------------------------------------------------------------------------------------------------------------------

-- Outro exemplo --

<?php
echo("<h1>Olá Mundo!!!</h1>");
echo("<br>");

$nome = "Louis Johanson";
$msg = "Boa tarde";
?>

<?php echo($msg); ?>
<br>
<?= $msg ?>
