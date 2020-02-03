<h1 align="center">
    <img alt="Launchbase" src="https://storage.googleapis.com/golden-wind/bootcamp-launchbase/logo.png" width="400px" />
</h1>

<h3 align="center">
  Desafio 4-7: Estruturando estudantes
</h3>

<blockquote align="center">“Tudo o que um sonho precisa para ser realizado é alguém que acredite que ele possa ser realizado.”</blockquote>

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

Nessa etapa você deve reaproveitar para os estudantes toda a estrutura já criada para os professores. Além disso, deve implementar a lógica do menu ativo.

### Estrutura

Reaproveite o código obecendo os seguintes padrões:

- Crie um arquivo `students.js` com a mesma estrutura que o `teachers.js`. Insira ambos os arquivos dentro uma pasta `controllers`;
- Crie um array `students` vazio dentro do arquivo `json`;
- Crie uma pasta `students` com a mesma estrutura de views que os professores;
- Crie as rotas dos estudantes seguindo a mesma estrutura dos professores.

### Menu Ativo

Crie um arquivo `scripts.js` e implemente a lógica do menu ativo utilizando o `location` e o `includes` da string. Além disso, implemente um botão de cadastro nas páginas de listagem de professores e estudantes.

### Formulário

Faça os ajustes de professores para estudantes no formulário de criação. Além disso, remova os campos:

- Grau de escolaridade;
- Tipo de aula;
- Acompanhamento;
- Desde.

e adicione os campos:

- Email: campo do tipo `email`;
- Ano escolar: campo do tipo `select` com todas as opções de anos escolares entre 5º ano do ensino fundamental e 3º ano do ensino médio;
- Carga horária semanal: campo do tipo `number` que indica a quantidade de horas de aulas particulares que o aluno irá ter por semana.

### Salvando os dados

Faça os ajustes de professores para estudantes no método `post` do arquivo `students.js`. Além disso, implemente a nova estratégia de `id` (evitar repetição).

### Apresentação

Faça os ajustes de professores para estudantes na página de apresentação dos dados de um estudante. Além disso, faça duas alterações no arquivo `utils.js`:

- Altere o retorno da função `date` para `day`, `month`, `year`, `iso` e `birthDay` (lembre de fazer o ajuste no método `edit` para buscar o `.iso`).
- Crie uma função chamada `grade` que retorna os dados formatados a partir do valor selecionado no select (ex.: o valor 1EF representa **1º Ano do Ensino Fundamental**).

### Edição

Faça os ajustes de professores para estudantes na página de edição dos dados de um estudante. Implemente o campo `Aniverśario` onde é apresentado o dia e o mês do aniversário do estudante. Além disso, altere tanto no `edit.njk` dos professores quanto no dos alunos a `url` da seção de avatar. Utilize o campo `avatar_url` cadastrado em vez da api do unsplash.

### Remoção

Crie um arquivo `confirm.njk` e importe ele no seu arquivo `edit.njk`. Esse arquivo deve ser responsável por escutar o evento (`addEventListener`) de submit do form de remoção e solicitar pela confirmação do usuário (`confirm`). Caso o usuário cancele a remoção, deve-se cancelar o form (método `preventDefault`).

### Listagem

Faça os ajustes de professores para estudantes na página de listagem dos dados de um estudante. Remova a coluna de `Acompanhamento` e adicione as de `Email` e `Ano escolar`.

### Estilização

Você tem liberdade para escolher a estilização que preferir para esse desafio.

## :calendar: Entrega

Esse desafio **não precisa ser entregue** e não receberá correção. Após concluí-lo, adicionar esse código ao seu Github é uma boa forma de demonstrar seus conhecimentos para oportunidades futuras.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](../LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
