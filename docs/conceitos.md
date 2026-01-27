# Resumo conceitos do trabalho

## Estrutrura Principal do HTML

``` CSS

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>

```

## Header

- precisamos da div para o "GABRIELA OLIVEIRA software engineer" para haver uma separação entre a imagem esse texto e conseguir centralizar cada um para um lado no flexbox. o div é como se fosse uma **caixa invisível**. Para o navegador compilar, ele vera 2 itens: a foto, e a caixa de texto. A div serve para dizer ao flexbox: "trata este grupo de coisas como se fosse uma peça única".

- usamos class na header e no div porque para as estilizarmos com o css precisamos especificar exatamente esses blocos. se nao, iriamos estilizar usando os blocos semanticos html no css e todos os blocos semanticos ficariam com aquela estilização.

### alinhar foto e bloco de texto lado a lado com o flexbox

### rem e pix

- rem é flexivel e o px é fixo. usamos rem para partes do html onde sabemos que o navegador vai "se meter"

## div vs section

## implementacoes a fazer

- menu lateral com os links para cada card de projeto
- pagina inteira para cada projeto, com:
    - um video demonstrando o programa a rodar
    - um wiki com resumo dos conceitos aprendidos
    - um guiao para os projetos da 42 para ajudar outros alunos
- links para linkedin e email no header