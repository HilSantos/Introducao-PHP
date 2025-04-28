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

------------------------------------------------------------------------------------------------------------------------------------------------

-- Criação de Calculadora Basica --

<form action="calc2.php" method="get">
    <input type="number" name="n1" placeholder="Digite o valor">
    <select name="op">
        <option value="1">+</option>
        <option value="2">-</option>
        <option value="3">*</option>
        <option value="4">/</option>
    </select>
    <input type="number" name="n2" placeholder="Digite o valor">
    <input type="submit" value="Enviar">
</form>

-- Calc 2 --

<?php
if(!isset($_GET['n1']) || !isset($_GET['n2']) || !isset($_GET['op'])){
    header('Location: calc1.php');
    exit();
    
}



$num1 = $_GET['n1'];
$nun2 = $_GET['n2'];
$op = $_GET['op'];
if($op == 1){
    echo($num1 . " + " . $nun2 . " = " . $num1+$nun2);
}
elseif($op == 2){
    echo($num1 . " - " . $nun2 . " = " . $num1-$nun2);
}
elseif($op == 3){
    echo($num1 . " x " . $nun2 . " = " . $num1*$nun2);
}else{
    if($nun2 == 0){
        echo("É impossível dividir por zero.");
    }
    else{
        echo($num1 . " / " . $nun2 . " = " . $num1/$nun2);
    }
}
?>

<br><br>
<a href="calc1.php">Voltar</a>
