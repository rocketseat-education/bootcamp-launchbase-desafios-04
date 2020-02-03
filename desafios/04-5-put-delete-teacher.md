<h1 align="center">
    <img alt="Launchbase" src="https://storage.googleapis.com/golden-wind/bootcamp-launchbase/logo.png" width="400px" />
</h1>

<h3 align="center">
  Desafio 4-5: HTTP: PUT e DELETE
</h3>

<blockquote align="center">“A impaciência é um grande obstáculo para o bom êxito.”</blockquote>

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

Nessa etapa você irá implementar duas rotas: PUT e DELETE para a atualização e remoção, respectivamente, dos dados cadastrados de um professor.

### PUT

Crie uma rota para receber os dados do formulário de edição e propagar no arquivo `json`. Lembre de sobrescrever o método POST do form para PUT (utilize a lib `method-override`). Dentro do arquivo `teachers.js`, crie um método `update` para buscar e retornar o professor a partir do `id` fornecido na rota. Faça a busca pelo professor a partir do `id` e atualize no arquivo `json` os dados que foram alterados (utilize o constructor `Number` para formatar o id como número). Por fim, redirecione para a página de apresentação dos dados de um professor (show).

### DELETE

Crie um botão na página de apresentação dos dados do professor. Esse botão irá chamar uma rota para deletar o professor do arquivo `json`. Lembre de sobrescrever o método POST do form para DELETE (utilize a lib `method-override`). Dentro do arquivo `teachers.js`, crie um método `delete` e gere um array com todos os professores, exceto o que deve ser removido (`filter`). Por fim, redirecione para a página de listagem dos professores.

### Estilização

Você tem liberdade para escolher a estilização que preferir para esse desafio. Porém algumas coisas são obrigatórias:

- O botão de deletar deve ficar ao lado do botão de editar;
- O botão de deletar deve ser da cor vermelha.

## :calendar: Entrega

Esse desafio **não precisa ser entregue** e não receberá correção. Após concluí-lo, adicionar esse código ao seu Github é uma boa forma de demonstrar seus conhecimentos para oportunidades futuras.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](../LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
