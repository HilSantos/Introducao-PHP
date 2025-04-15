# Introducao-PHP
Criação de variaveis no PHP

-- Crie um novo arquivo chamado pg1.php --
<form action="pg2.php" method="get">
    <label>Digite seu nome:</label>
    <input type="text" name="identificacao">
    <input type="submit" value="Enviar">
</form>
-- Digite na barra de endereço o caminho do arquivo pg1 na pasta e atualize --

<?php
$usuario = $_GET['identificacao'];
?>
<h1> Olá <?= $usuario ?>
<br><br>
<a ref="pg1.php">Voltar</a>
</h1>
-- O mesmo exemplo anterior pelo arquivo pg2 --
