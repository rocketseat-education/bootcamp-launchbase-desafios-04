<h1 align="center">
    <img alt="Launchbase" src="https://storage.googleapis.com/golden-wind/bootcamp-launchbase/logo.png" width="400px" />
</h1>

<h3 align="center">
  Desafio: Administração do Foodfy
</h3>

<blockquote align="center">“Quem sabe concentrar-se numa coisa e insistir nela como único objetivo, obtém a capacidade de fazer qualquer coisa.”</blockquote>

<p align="center">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%23F8952D">
  </a>

  <a href="LICENSE" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F8952D">
  </a>

</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#calendar-entrega">Entrega</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

Nesse desafio você irá criar uma área administrativa para o Foodfy, aplicação que desenvolvemos nos desafios anteriores.

Você utilizará o mesmo projeto do Foodfy desenvolvido no desafio anterior e somente adicionar essa área administrativa, que será responsável por cadastrar, editar e deletar os dados que estão no seu arquivo: `data.js`

### Rotas do administrador

Usando os conhecimentos adquiridos até aqui, você deve criar rotas para uma área administrativa, onde o usuário poderá cadastrar novas receitas, apresentá-las, além de atualizar e deletar também.

Use a seguinte ideia para criar suas rotas.

```js
routes.get("/admin/recipes", recipes.index); // Mostrar a lista de receitas
routes.get("/admin/recipes/create", recipes.create); // Mostrar formulário de nova receita
routes.get("/admin/recipes/:id", recipes.show); // Exibir detalhes de uma receita
routes.get("/admin/recipes/:id/edit", recipes.edit); // Mostrar formulário de edição de receita

routes.post("/admin/recipes", recipes.post); // Cadastrar nova receita
routes.put("/admin/recipes", recipes.put); // Editar uma receita
routes.delete("/admin/recipes", recipes.delete); // Deletar uma receita
```

Dica: Você pode criar pasta(s) para organizar os arquivos do seu projeto.

### Detalhes da Receita

Para facilitar a busca de uma receita cadastrada, você pode usar a mesma forma de busca pelo index do `array` de `recipes` que foi apresentada no desafio anterior e desconsiderar o uso de um `id` único para cada receita, como apresentado nas aulas deste módulo.

Mais pra frente entenderemos o uso dos ID's de forma mais profunda :wink:

### Layout do painel de administração

<div align="center">
   <img src="https://rocketseat-cdn.s3-sa-east-1.amazonaws.com/launchbase/mockup-desafio-04.png" />
</div>

**Download dos arquivos:** https://github.com/Rocketseat/bootcamp-launchbase-desafios-04/archive/master.zip

Acesse o arquivo `layouts/specs/index.html` para ver todas especificações do layout da página.

### Dados do projeto

No desafio passado você criou um arquivo de dados chamado `data.js` para servir de dados da sua aplicação.

Utilize agora, um arquivo que levará o nome `data.json` seguindo o que você aprendeu nesse módulo, porém, mantenha a estrutura de dados que você tinha no seu arquivo: `data.js`.

Exemplo:

```json
{
  "recipes": []
}
```

Nesse `array` de `recipes` irão as receitas cadastradas pelo seu sistema.

A fim de testar as funcionalidades da sua área administrativa, cadastre, pela área administrativa, os dados que você tinha anteriormente no seu `data.js`

### Adicionar Campo Dinâmico

Os campos de "Ingredientes" e "Modo de preparo", serão campos dinâmicos, onde você irá adicionar quantos campos forem necessários, usando JavaScript para isso.

#### GIF Exemplo

<p align="center">
  <img alt="Gif Campo Dinâmico" src="https://i.imgur.com/EOYWaJW.gif"/>
</p>

#### Código de exemplo

```html
<div id="ingredients">
  <div class="ingredient">
    <input type="text" name="ingredients[]" value="" placeholder="Ingredient" />
  </div>
</div>
<button type="button" class="add-ingredient">Add Ingredient</button>
```

Veja que o nome do nosso input contém `[]` no fim, isso significa que ele será um vetor, ou seja, quando o usuário enviar o formulário teremos algo assim:

```js
{
  "ingredients": [
    "Batata",
    "Queijo",
    "Bacon"
  ]
}
```

#### Exemplo de JavaScript

```js
function addIngredient() {
  const ingredients = document.querySelector("#ingredients");
  const fieldContainer = document.querySelectorAll(".ingredient");

  // Realiza um clone do último ingrediente adicionado
  const newField = fieldContainer[fieldContainer.length - 1].cloneNode(true);

  // Não adiciona um novo input se o último tem um valor vazio
  if (newField.children[0].value == "") return false;

  // Deixa o valor do input vazio
  newField.children[0].value = "";
  ingredients.appendChild(newField);
}

document
  .querySelector(".add-ingredient")
  .addEventListener("click", addIngredient);
```

### Apresentação no site

Altere as rotas desenvolvidas no desafio anterior para exibir as receitas do novo arquivo `data.json` para o nosso site do Foodfy, no fim do desafio você deve ter então tanto a área administrativa do projeto quando o website consumindo os mesmos dados :smile:

## :calendar: Entrega

Esse desafio **não precisa ser entregue** e não receberá correção. Após concluí-lo, adicionar esse código ao seu Github é uma boa forma de demonstrar seus conhecimentos para oportunidades futuras.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](../LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
