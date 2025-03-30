# <p align="center"><font color='#FF79C6'><strong>Learn the CSS Box Model Building a Rothko Painting</strong></font></p>

<p align="center"> <i>Módulo de treinamento para a certificação <a href="https://www.freecodecamp.org/learn/2022/responsive-web-design/"><em>Responsive Web Design Certification</em></a> da plataforma FreeCodeCamp</i>.
<p>

<p align="center">
    <img src="https://skillicons.dev/icons?i=html,css,md,vscode,git,github,figma" height="30px">
</p>


<br>

## :memo: <font color='#8BE9FD'><strong>Notas de Aula</strong></font>

<br>





:ballot_box_with_check: No modelo de caixa do CSS (**CSS Box Model**), cada elemento HTML é tratado como uma caixa composta por quatro áreas principais:


1. **Content (Conteúdo)** – A área onde o texto e outros elementos filhos aparecem.
2. **Padding (Preenchimento)** – O espaço entre o conteúdo e a borda do elemento.
3. **Border (Borda)** – A linha que envolve o padding e o conteúdo.
4. **Margin (Margem)** – O espaço externo ao redor da borda, separando o elemento de outros elementos.

<br>

<p align="center">
    <img src="https://live.staticflickr.com/65535/54418788054_5c9e56be28_w.jpg">
</p>



<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.box {
  width: 200px;  /* Largura do conteúdo */
  padding: 10px; /* Espaço interno entre o conteúdo e a borda */
  border: 2px solid black; /* Borda ao redor do elemento */
  margin: 15px; /* Espaço externo entre este elemento e outros */
}
```

</details>
<br>

> [!IMPORTANT]
> `box-sizing: border-box;`
> 
> Por padrão, o `width` e `height` consideram apenas a área de **conteúdo**. Se quiser incluir **padding e borda** no cálculo da largura e altura, use: 
> ```css 
> * {
> box-sizing: border-box; 
>} 
> ```
> Isso facilita o design responsivo e evita cálculos complicados de dimensionamento.


:ballot_box_with_check: Para definir a largura do elemento com a classe `.canvas`, basta criar uma regra CSS s ajustando a largura para **500 pixels** por exemplo.

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
}
```

Isso garante que qualquer elemento `<div class="canvas">` (ou outro elemento com essa classe) terá uma largura fixa de **500 pixels**.

Caso precise centralizá-lo, você pode adicionar:
```css
.canvas {
  width: 500px;
  margin: 0 auto; /* Centraliza horizontalmente */
}
```

</details>
<br>

:ballot_box_with_check: Se você deseja adicionar uma **moldura** (frame) ao seu elemento `.canvas`, pode usar a propriedade `border` no CSS.

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
  height: 300px; /* Defina uma altura para visualização */
  border: 10px solid black; /* Moldura preta com 10px de espessura */
  background-color: white; /* Fundo branco, como uma tela real */
  margin: 20px auto; /* Centraliza a "tela" */
}
```
</details>
<br>

:ballot_box_with_check: Se quiser um **efeito mais realista**, pode usar `box-shadow` para criar profundidade

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
  height: 300px;
  border: 15px solid #8B4513; /* Moldura marrom imitando madeira */
  background-color: white;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5); /* Sombra para efeito 3D */
  margin: 20px auto;
}
```

</details>
<br>

:ballot_box_with_check: O `padding` no CSS define o **espaço interno** entre o conteúdo de um elemento e sua borda. Se aplicarmos `padding` à `.canvas`, aumentamos a área dentro da moldura antes de atingir o conteúdo.  

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
  height: 300px;
  border: 15px solid #8B4513; /* Moldura marrom */
  background-color: white;
  padding: 20px; /* Adiciona espaçamento interno */
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
  margin: 20px auto;
}
```
</details>

<br> 

:ballot_box_with_check: Como funciona o `padding`?

- `padding: 20px;` → Adiciona **20px de espaçamento interno** em todos os lados.


- Podemos definir valores diferentes para cada lado:


  ```css
  padding: 10px 15px 20px 25px;
  ```
  **Ordem:** `top right bottom left` (sentido horário).

<br> 

:ballot_box_with_check: O `margin` no CSS define o **espaço externo** ao redor de um elemento, afastando-o de outros elementos na página.  

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
  height: 300px;
  border: 15px solid #8B4513; /* Moldura marrom */
  background-color: white;
  padding: 20px; /* Espaçamento interno */
  margin: 50px auto; /* Espaçamento externo */
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
}
```


</details>

<br> 

:ballot_box_with_check: Como funciona o `margin`:
- `margin: 50px auto;`
  - **50px** → Espaçamento acima e abaixo.
  - **auto** → Centraliza horizontalmente o elemento dentro do contêiner pai.
  - Para definir margens diferentes para cada lado


```css
margin: 10px 20px 30px 40px; /* Ordem: top, right, bottom, left */
```

<br> 

:ballot_box_with_check: Para evitar que a `.one` empurre a `.canvas` para baixo devido à margem superior, podemos adicionar um pequeno `padding` à `.canvas`, garantindo que o conteúdo dentro dela tenha um espaço interno sólido para "empurrar" contra a moldura.  

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.canvas {
  width: 500px;
  height: 300px;
  border: 15px solid #8B4513; /* Moldura marrom */
  background-color: white;
  padding: 1px; /* Pequeno padding para evitar colapso de margem */
  margin: 20px auto; /* Mantém a centralização */
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
}
```
</details>

<br> 

> [!WARNING]
> Por que isso acontece?
> - O **colapso de margens** ocorre quando a margem superior de `.one` entra em contato diretamente com a borda superior da `.canvas`. Como não há um conteúdo sólido antes dela, a margem "vaza" para fora, deslocando a `.canvas` para baixo.  
> Adicionar `padding: 1px;` cria um **espaço interno mínimo**, impedindo que as margens se fundam. 
>  Agora, `.one` permanecerá corretamente dentro da "tela", sem deslocar a moldura! 🖼️✨

<br>

:ballot_box_with_check: Quando adicionamos `padding: 1px;`, o tamanho total da `.canvas` aumentou porque o `padding` adiciona espaço **dentro** do elemento, expandindo sua largura e altura. Para manter as dimensões originais (**500px x 600px**), podemos remover o `padding` e, em vez disso, usar `overflow: hidden;`.  

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
  height: 600px;
  border: 15px solid #8B4513; /* Moldura marrom */
  background-color: white;
  overflow: hidden; /* Evita o colapso da margem sem alterar o tamanho */
  margin: 20px auto;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
}
```
</details>

<br> 


> [!IMPORTANT]
> Como isso funciona?
> - **`overflow: hidden;`** → Impede que qualquer conteúdo (incluindo margens) "vaze" para fora do `.canvas`, sem alterar suas dimensões.
> - Isso resolve o problema do **colapso de margens**, pois o navegador trata `.canvas` como uma "barreira" sólida para o elemento `.one`, evitando que a margem de `.one` desloque a `.canvas`.
> 
> Agora a `.canvas` mantém suas dimensões exatas, sem ser empurrada para baixo! 🎨✨

<br>

:ballot_box_with_check: Para suavizar as cores e formas da sua "pintura" e deixá-la mais parecida com uma obra de **Mark Rothko**, podemos aplicar um desfoque de **2px** usando a propriedade `filter`.  

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.canvas {
  width: 500px;
  height: 600px;
  border: 15px solid #8B4513; /* Moldura marrom */
  background-color: white;
  overflow: hidden; /* Evita o colapso da margem */
  margin: 20px auto;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
  filter: blur(2px); /* Suaviza as bordas e cores */
}
```

</details>

<br>

> [!NOTE]
> - **`filter: blur(2px);`** → Aplica um efeito de desfoque de 2 pixels, suavizando as transições de cores e tornando os contornos menos definidos.
> - Isso ajuda a imitar o estilo de **Rothko**, que usava transições sutis entre cores para criar profundidade e emoção.
>
> Agora sua "pintura" tem um toque mais artístico e abstrato! 🎨✨
>

<br>

:ballot_box_with_check: Para suavizar os cantos do elemento `.one`, podemos usar a propriedade `border-radius` com um valor de **9px**. Isso dará um aspecto mais arredondado às bordas do retângulo.  

<details>
  <summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.one {
  border-radius: 9px; /* Arredonda os cantos em 9 pixels */
}
```

- **`border-radius: 9px;`** → Faz com que os cantos fiquem suavemente arredondados, reduzindo a nitidez das formas.
- Isso ajuda a dar um toque mais suave e abstrato ao estilo da pintura.


</details>

<br>

:ballot_box_with_check:  Para arredondar os cantos do elemento `.two` com valores diferentes para cada canto, usamos a propriedade `border-radius` especificando quatro valores na seguinte ordem:  

**`top-left top-right bottom-right bottom-left`**  

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.two {
  border-radius: 8px 10px 8px 10px;
}
```

- **`border-radius: 8px 10px 8px 10px;`**  
  - **8px** → Canto superior esquerdo (top-left).  
  - **10px** → Canto superior direito (top-right).  
  - **8px** → Canto inferior direito (bottom-right).  
  - **10px** → Canto inferior esquerdo (bottom-left). 

 </details> 

<br>

:ballot_box_with_check: Para dar um visual mais **imperfeito e artístico**, podemos usar a propriedade `transform: rotate()` para girar os retângulos em ângulos ligeiramente diferentes. Isso fará com que pareçam pintados à mão, como nas obras de **Mark Rothko**.  

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.one {
  transform: rotate(-3deg); /* Rotação leve para a esquerda */
}

.two {
  transform: rotate(2deg); /* Rotação leve para a direita */
}
```

- **`transform: rotate(-3deg);`** → Inclina levemente `.one` para a esquerda.
- **`transform: rotate(2deg);`** → Inclina `.two` para a direita.
- Pequenas rotações criam um efeito **mais natural e orgânico**, como se os retângulos tivessem sido pintados manualmente.


 </details> 

<br>