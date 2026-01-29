# WIKI - Conceitos de HTML e CSS

Este documento serve como guia de estudo e documentação sobre os conceitos teóricos e práticos aplicados no desenvolvimento deste portfólio.

---

## 1. Estrutura Básica do HTML

Todo o documento HTML segue uma estrutura padrão ("boilerplate") que diz ao navegador como interpretar o código.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- Links para CSS e Fontes ficam aqui -->
</head>
<body>
    <!-- O conteúdo visível vai aqui -->
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


----------------------

## Containers

O header do website tem muitos elementos, pelo que foi importante aprender o conceito de containers para facilitar o alinhamento deles no CSS.

** O que é um container?**

Na vida real, um container é uma caixa grande onde guardas várias coisas menores para ser mais fácil transportá-las. No HTML, é exatamente a mesma coisa.

Um container é qualquer elemento **pai** (geralmente uma ```<div>``` ou ```<section>```) que agrupa vários elementos **filhos** dentro dele. Um container serve para controlar, mover e estilizar um grupo de elementos de uma só vez!

## The ```<nav>``` tag

## ```<section>``` vs ```<div>```

## Implementar links com a tag <a>

## tag ```<aside>```

## tag ```<label>```

## tag ```<select>```

## tag ```<option>```

## tag ```<ul>```

## tag ```<li>```

## aplicar duas classes no mesmo elemento

``` HTML
    <li class="item-projeto ativo" data-id="cub3d">
        <span>Cub3D</span>
        <small>Mar 2024 • 42 Porto</small>
    </li>
```

## tag ```<span>```

``` HTML 
    <li class="item-projeto">
        <span>Cub3D</span>               <small>Mar 2024</small>          </li>
```

Usámos o ```<span>``` à volta do "Cub3D" apenas para podermos ir ao CSS e dizer: "O que estiver dentro do span, mete em Negrito e com letra tamanho 1rem."

Se não tivéssemos o ```span```, o texto "Cub3D" ficaria solto e não teríamos como mudar a fonte só dele sem afetar a data que está por baixo.

## tag ```<small>```

## O uso do label

Para estilizar os dropdown menus, eu uso do label na estrutura do html e depois o chamo no arquivo CSS. 

``` HTML 
    <div class="grupo-filtro">
        
        <label>FILTER BY SCHOOL</label>  <-- ESTE recebe o estilo!

        <select>...</select>

    </div>
```
``` CSS
    .grupo-filtro label {
        font-size: 0.75rem;
        color: var(--cor-roxo-claro);
        font-weight: bold;
        letter-spacing: 1px;
    }
```

Lê-se da direita para a esquerda, ou seja: "Estiliza todas as tags ```<label>``` QUE ESTEJAM DENTRO de um elemento com a classe ```.grupo-filtro```."

Ao escreveres .grupo-filtro label no CSS, estás a dizer: "Eu não quero pintar todos os labels do site. Eu quero pintar apenas os que estão "guardados" dentro da caixa dos filtros."

2. Por que fazemos isto? Por SEGURANÇA. 
Imagina que amanhã crias um Formulário de Contacto no rodapé do site. Lá também vais ter um ```<label>O teu Email:</label>```.

Se usasses apenas ```label { ... }``` no CSS: O label do formulário de contacto ia ficar minúsculo, roxo e com letras garrafais, igual ao do filtro. Ia ficar estranho!

Usando ```.grupo-filtro label```: O CSS protege os outros labels. Ele sabe que aquele estilo específico é exclusivo para a barra lateral.

## Brainstorming e ideias

- criar uma página "além do código"/"beyond de code"
- o filtre por tecnologias nao ta rosa como o filtre por escola

## o "fa" - font awesome que aparece em alguns elementos

O **`fa`** vem de **F**ont **A**wesome.

Esta linha de código no `<head>` do HTML:
```CSS
<link rel="stylesheet" href="...font-awesome...">
``` 
É instalar uma "biblioteca de símbolos" no seu site. O `fa` é o prefixo que diz ao navegador: *"Ei, esta classe pertence à biblioteca do FontAwesome, não é uma classe minha (Gabriela)"*.

Existem variações do estilo no footer:

* **`fa-brands`**: Para logótipos de marcas (LinkedIn, GitHub, Instagram).
* **`fa-solid`**: Para ícones preenchidos e grossos (como o envelope ✉️ ou o coração ❤️).
* **`fa-regular`**: Para ícones apenas com contorno (mais fininhos).

## The ```<i>``` tag

## Como eu faço os botoes/icones trocarem de cor ao passar o mouse e "pular" pra cima

## O uso do CSS Grid no projeto

## O uso do flexbox no projeto


----

1. Estrutura e Semântica HTML
Estrutura Básica (Boilerplate): O esqueleto de qualquer página (html, head, body).
Semântica: A diferença entre div (genérico) e tags com significado (header, nav, section, aside, footer).
Containers: O conceito de agrupar elementos em "caixas" para estilização.
2. Fundamentos de CSS
Variáveis CSS (:root): Como criar uma paleta de cores reutilizável.
Unidades de Medida: A diferença crucial entre px (fixo) e rem (relativo/acessível).
Seletores: Como selecionar elementos específicos (Classes, Múltiplas Classes e Seletores Descendentes como .grupo-filtro label).
Box Model: Margens, Bordas e Padding.
3. Layout e Posicionamento
Flexbox: Alinhamento numa direção (usado no Header, Nav e Footer).
CSS Grid: Layout em duas dimensões (usado na estrutura principal Dashboard e nos Cards).
Posicionamento: Como funciona o position: sticky (Barra Lateral e Menu fixo) e z-index.
4. Elementos de Texto e Mídia
Tipografia e Texto: Tags h1-h6, p, e a diferença entre span (estilo) e small (detalhe).
Listas: ul e li (usadas nos menus e listas de projetos).
Links: A tag a e atributos como target="_blank".
Imagens e Ícones: Tag img e o uso de bibliotecas como FontAwesome (<i>).
5. Estilização Avançada e Efeitos
Cores e Vidro: Gradientes, transparência (rgba) e o efeito Glassmorphism (backdrop-filter).
Sombras e Bordas: box-shadow (efeito neon) e border-radius.
6. Interatividade e Formulários
Animações: Como usar transition, transform e o estado :hover para criar movimento.
Formulários: Estrutura dos filtros (label, select, option).
Estados: O uso de classes como .ativo para marcar o item selecionado.
7. Responsividade
Media Queries: Como o site se adapta a tablets e telemóveis.
