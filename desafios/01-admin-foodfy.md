# Administração do Foodfy

Nesse desafio você irá criar uma área administrativa no Foodfy.

Você irá manter o padrão que vinha utilizando no Foodfy, e somente adicionar essa área administrativa, que será responsável por trabalhar nos dados que estão no seu arquivo: `data.js`

## Rotas

Usando os conhecimentos adquiridos até aqui, você irá criar rotas para uma área administrativa, onde poderá cadastrar novas receitas, apresentá-las, além de atualizar e deletar também. 

Use a seguinte ideia para criar suas rotas.

```js
routes.get('/admin/recipes', recipes.index)
routes.get('/admin/recipes/create', recipes.create)
routes.get('/admin/recipes/:id', recipes.show)
routes.get('/admin/recipes/:id/edit', recipes.edit)
routes.post('/admin/recipes', recipes.post)
routes.put('/admin/recipes', recipes.put)
routes.delete('/admin/recipes', recipes.delete)
```

Dica: Você pode criar pasta(s) para organizar os arquivos do seu projeto.

## Detalhes da Receita

Para facilitar a busca de uma receita cadastrada, você pode usar a mesma forma de busca pelo index do `array` de `recipes` que foi apresentada no desafio anterior e desconsiderar o uso de um `id` único para cada receita, como apresentado nas aulas deste módulo.

## Dados do projeto 

No desafio passado você criou um arquivo de dados chamado `data.js` para servir de dados da sua aplicação. 

Utilize agora, um arquivo que levará o nome `data.json` seguindo o que você aprendeu nesse módulo, porém, mantenha a estrutura de dados que você tinha no seu arquivo: `data.js`.

Exemplo:

```json
{
	"recipes": []
}
```

Nesse `array recipes` irão as receitas cadastradas pelo seu sistema.

A fim de testar as funcionalidades da sua área administrativa, cadastre, pela área administrativa, os dados que você tinha anteriormente no seu `data.js`

## Adicionar Campo Dinâmico

Os campos de Ingredientes e Preparação, serão campos dinâmicos, onde você irá adicionar quantos campos forem necessários, usando JavaScript para isso. 

### Vídeo Exemplo

<p align="center">
<img alt="Gif Campo Dinâmico" src="https://i.imgur.com/EOYWaJW.gif"/>
</p>

### Código
**html**
```html
<div id="ingredients">
  <div class="ingredient">
    <input
      type="text"
      name="ingredients"
      value=""
      placeholder="Ingredient"
    />
  </div>
</div>
<a class="add-ingredient" href="#">Add Ingredient</a>
```

**javascript**
```javascript
function addIngredient() {
  const ingredients = document.querySelector("#ingredients");
  const fieldContainer = document.querySelectorAll(".ingredient"); // select all ingredients fields
  const newField = fieldContainer[fieldContainer.length - 1].cloneNode(
    true
  ); // clone last ingredient field

  // do not add ingredient if last one was not filled
  if (newField.children[0].value == "") return false;

  // empty value, so field can be fresh
  newField.children[0].value = ""; 
  ingredients.appendChild(newField);
}

document
  .querySelector(".add-ingredient")
  .addEventListener("click", addIngredient);
```

## Apresentação no site

Sua apresentação de dados já foi concluída no desafio anterior, portanto, consuma agora o seu novo  arquivo de dados `data.json` ao invés do `data.js`