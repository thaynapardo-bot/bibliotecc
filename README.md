# Bibliotec — Front-end de referência

Este é um protótipo visual do front-end para servir de referência durante a implementação do back-end com Flask e PostgreSQL.

## Páginas
- index.html — Home
- catalogo.html — Catálogo, busca e filtros
- livro.html — Detalhes do livro
- leitura.html — Tela de leitura
- login.html — Login
- cadastro.html — Cadastro
- biblioteca.html — Biblioteca pessoal
- favoritos.html — Favoritos
- comunidade.html — Comunidade
- contato.html — Contato
- admin.html — Painel administrativo

## Onde o Flask entra

Cada página HTML deverá virar um template Jinja em `templates/`.

Exemplo:
- `index.html` -> `templates/index.html`
- `catalogo.html` -> `templates/catalogo.html`

O Flask substituirá os dados fictícios por dados do PostgreSQL.

## Exemplo de integração

No front:
`href="/livro/{{ livro.id }}"`

No Flask:
`@app.route("/livro/<int:id>")`

O Flask consulta o PostgreSQL e envia:
`render_template("livro.html", livro=livro)`

## Importante
O protótipo usa dados fictícios e JavaScript apenas para simular interações. No sistema real, login, favoritos, biblioteca, avaliações, comentários, progresso, administração e API serão ligados ao Flask/PostgreSQL.
