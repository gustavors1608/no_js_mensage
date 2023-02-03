# Notice of desactived javascript 

Esse projeto gera uma mensagem ao usuário caso o js do mesmo não esteja ativado, o indicando a ligar o javascript para utilizar o seu sistema corretamete.

## Features 
- Pouca utilização de memoria / leve para rodar
- Não atrapalha em nada o seu sistema já implementado
- Pode ser implementado em 3 comandos de php (conferir abaixo)

## Implementation

Em seu arquivo php que você deseja implementar esse sistema, inclua o seguinte: 


```php
<?php 

$session = curl_init("https://cdn.jsdelivr.net/gh/gustavors1608/no_js_mensage/main.html");

$html = curl_exec($session);

?>

<!DOCTYPE HTML>
<html>
<head></head>

    <body>
        <!-- your code-->

        <?php echo $html?>
    </body>
</html>
```

Esse codigo acima acima irá importar o codigo html desse repositorio para o final do body do seu projeto e assim irá verificar o js, como pode conferir no arquivo main.html, para um exemplo completo veja o arquivo example.php

## Printscreen
Mensagem mostrada após 5 segundos caso o navegador não permita.

![mensagem mostrada apos 5 segundos caso não permita js](/docs/img1.png "mensagem mostrada apos 5 segundos caso não permita js")

## Dependencias
- Php > 7.0
