# Fase 1 - Experiencia da Plataforma

## Objetivo

Transformar o Arcade Multimidia em uma vitrine de jogos estudantis preparada para uso em feira de projetos e para crescimento em novas turmas.

A experiencia deve atender dois publicos principais:

- Visitantes da feira, que precisam entender rapidamente o que e a plataforma e acessar os jogos com poucos cliques.
- Docentes, que precisam inserir novos jogos de forma organizada, previsivel e sem depender de retrabalho visual ou estrutural a cada turma.

## Diagnostico do estado atual

O projeto atual funciona como um site estatico simples:

- Uma pagina inicial apresenta cards de turmas.
- Cada turma possui uma pagina propria.
- Os jogos ficam organizados manualmente dentro das pastas de cada turma.
- O visual usa uma estetica arcade muito literal, com fonte pixelada em toda a interface.
- A manutencao tende a ficar manual conforme novas turmas e jogos forem adicionados.

Principais problemas de experiencia:

- O visitante precisa escolher uma turma antes de ver os jogos.
- A pagina inicial nao mostra a riqueza dos projetos dos alunos.
- A tipografia compromete leitura em textos maiores.
- Os cards atuais tem pouca informacao para orientar a escolha.
- A estrutura atual nao favorece filtros, destaques ou crescimento por ano letivo.

## Direcao da nova experiencia

A plataforma deve se comportar como uma galeria curada de jogos, nao como uma lista de pastas.

Nova prioridade de navegacao:

1. Ver jogos em destaque.
2. Explorar todos os jogos.
3. Filtrar por turma, ano ou categoria.
4. Abrir detalhes de um jogo.
5. Jogar.

Turmas continuam importantes, mas entram como filtros e metadados, nao como primeira etapa obrigatoria.

## Estrutura recomendada de telas

### 1. Inicio / Galeria

Primeira tela da plataforma.

Deve conter:

- Nome da plataforma: Arcade Multimidia.
- Texto curto de contexto institucional.
- Area de destaques com 3 a 5 jogos.
- Galeria com todos os jogos.
- Filtros visiveis por turma, ano e categoria.
- Busca por nome do jogo.
- Botao claro para jogar em cada card.

### 2. Card de jogo

Cada card precisa funcionar como uma mini-vitrine do projeto.

Conteudo recomendado:

- Imagem de capa ou banner.
- Nome do jogo.
- Turma.
- Ano.
- Descricao curta.
- Tags, como genero, tecnologia ou tema.
- Acao principal: Jogar.
- Acao secundaria: Detalhes.

### 3. Detalhes do jogo

Pode ser uma pagina propria ou um modal. Para a primeira versao, uma pagina propria e mais simples de manter e compartilhar.

Conteudo recomendado:

- Capa/banner maior.
- Nome do jogo.
- Descricao completa.
- Turma e ano.
- Integrantes/autores.
- Docente responsavel.
- Tecnologias usadas.
- Controles ou observacoes, se necessario.
- Botao principal para jogar.
- Aviso quando o jogo funcionar melhor em desktop.

### 4. Area de organizacao docente

Na primeira etapa, nao precisa existir login nem painel complexo. A prioridade e definir o modelo de informacao para que depois possamos evoluir para cadastro.

Campos recomendados para cada jogo:

- id
- titulo
- turma
- ano
- autores
- docente
- descricaoCurta
- descricaoCompleta
- categoria
- tipoProjeto
- tags
- tecnologias
- capa
- linkJogo
- destaque
- status
- observacoes

## Arquitetura de conteudo

Para as proximas fases, recomenda-se mover o conteudo dos jogos para um arquivo central de dados, como `jogos.json`.

Isso permite:

- Adicionar jogos sem criar uma nova pagina manualmente.
- Gerar cards automaticamente.
- Filtrar por turma e ano.
- Destacar jogos na pagina inicial.
- Reaproveitar a mesma estrutura em futuras turmas.

Exemplo conceitual:

```json
{
  "id": "binx",
  "titulo": "Binx",
  "turma": "T3",
  "ano": "2026",
  "autores": ["Nome do estudante"],
  "docente": "Nome do docente",
  "descricaoCurta": "Uma aventura interativa desenvolvida na unidade curricular.",
  "categoria": "Aventura",
  "tags": ["2D", "Construct", "Arcade"],
  "capa": "turmas/t3/Banners/binx.png",
  "linkJogo": "turmas/t3/Binx/index.html",
  "destaque": true,
  "status": "publicado"
}
```

## Requisitos de experiencia

Para visitantes:

- Entender a proposta em ate 5 segundos.
- Ver jogos ja na primeira tela.
- Conseguir jogar com no maximo 2 cliques.
- Conseguir filtrar rapidamente por turma.
- Ter boa leitura em tela grande, notebook e celular.

Para docentes:

- Ter um modelo padrao para cadastrar novos jogos.
- Nao precisar duplicar paginas HTML por turma.
- Conseguir marcar um jogo como destaque.
- Conseguir registrar o tema gerador de cada turma.
- Conseguir diferenciar jogos unitarios e projetos finais em equipe.
- Conseguir manter dados consistentes entre turmas.

## Direcao visual para guiar o Figma

A identidade pode manter a ideia de arcade, mas com mais maturidade visual.

Recomendacoes:

- Usar fonte display apenas em titulos curtos ou marca da plataforma.
- Usar fonte legivel para descricoes, filtros e metadados.
- Trabalhar com fundo escuro, contraste alto e cores vibrantes pontuais.
- Dar protagonismo as imagens dos jogos.
- Evitar excesso de bordas neon e textos pixelados em todos os elementos.
- Criar componentes reutilizaveis: header, card, tag, botao, filtro, detalhe do jogo.

## Criterios de conclusao da Fase 1

A Fase 1 sera considerada concluida quando tivermos:

- Nova arquitetura de navegacao definida.
- Conteudo minimo de cada jogo definido.
- Modelo de card definido.
- Modelo de detalhes do jogo definido.
- Requisitos da experiencia docente definidos.
- Direcao visual inicial definida para alimentar o Figma.

## Proxima fase

A Fase 2 deve transformar esta arquitetura em design system e wireframes no Figma:

- Pagina inicial / galeria.
- Card de jogo.
- Estados dos filtros.
- Pagina de detalhes.
- Modelo visual de cadastro/organizacao docente.
