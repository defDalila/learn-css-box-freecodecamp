# <p align="center"><font color='#FF79C6'><strong>Learn the CSS Box Model Building a Rothko Painting</strong></font></p>

<p align="center"> <i>Módulo de treinamento para a certificação <a href="https://www.freecodecamp.org/learn/2022/responsive-web-design/"><em>Responsive Web Design Certification</em></a> da plataforma FreeCodeCamp</i>.
<p>

<p align="center">
    <img src="https://skillicons.dev/icons?i=html,css,md,vscode,git,github" height="30px">
</p>


<br>

## :memo: <font color='#8BE9FD'><strong>Notas de Aula</strong></font>

<br>

:ballot_box_with_check: No modelo de caixa do CSS (**CSS Box Model**), cada elemento HTML é tratado como uma caixa composta por quatro áreas principais:

1. **Content (Conteúdo)** – A área onde o texto e outros elementos filhos aparecem.
2. **Padding (Preenchimento)** – O espaço entre o conteúdo e a borda do elemento.
3. **Border (Borda)** – A linha que envolve o padding e o conteúdo.
4. **Margin (Margem)** – O espaço externo ao redor da borda, separando o elemento de outros elementos.

### Representação do **Box Model**:

```
+-------------------------+  ← Margin
|                         |
|  +-------------------+  |  ← Border
|  |                   |  |
|  |   +-----------+   |  |  ← Padding
|  |   | Content   |   |  |
|  |   +-----------+   |  |
|  |                   |  |
|  +-------------------+  |
|                         |
+-------------------------+
```

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





