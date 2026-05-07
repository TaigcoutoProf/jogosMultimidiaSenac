# Como adicionar jogos

Esta primeira refatoracao usa o arquivo `data/jogos.json` como fonte central da galeria.

Para cadastrar um novo jogo, copie um bloco existente, altere os campos e mantenha o formato JSON valido.

Campos principais:

- `id`: identificador unico, sem espacos e sem acentos.
- `titulo`: nome exibido no card.
- `turma`: turma do projeto, como `T3`, `T4` ou `T5`.
- `ano`: ano da mostra.
- `autores`: lista de estudantes ou grupo.
- `docente`: docente responsavel.
- `descricaoCurta`: texto breve para o card.
- `descricaoCompleta`: texto para a janela de detalhes.
- `categoria`: genero ou tipo do jogo.
- `tipoProjeto`: use `Unitario`, `Final em equipe` ou outro padrao combinado pela turma.
- `tags`: palavras-chave exibidas no card.
- `tecnologias`: ferramentas usadas.
- `capa`: caminho da imagem de capa. Pode ficar vazio.
- `linkJogo`: caminho para abrir o jogo.
- `destaque`: `true` para aparecer na area de destaques.
- `status`: use `publicado` para exibir na galeria.

O contexto da turma, como tema gerador e proposta de trabalho, fica em `data/turmas.json`. O tema tem dois campos: `temaTitulo` e `temaDescricao`.

Exemplo:

```json
{
  "id": "novo-jogo",
  "titulo": "Novo Jogo",
  "turma": "T6",
  "ano": "2027",
  "autores": ["Nome 1", "Nome 2"],
  "docente": "Nome do docente",
  "descricaoCurta": "Descricao curta para o card.",
  "descricaoCompleta": "Descricao mais completa para a janela de detalhes.",
  "categoria": "Aventura",
  "tipoProjeto": "Unitario",
  "tags": ["2D", "Web", "Interativo"],
  "tecnologias": ["Construct", "HTML"],
  "capa": "turmas/t6/banners/novo-jogo.png",
  "linkJogo": "turmas/t6/novo-jogo/index.html",
  "destaque": false,
  "status": "publicado",
  "observacoes": ""
}
```
