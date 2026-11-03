# Course Future

Landing page de cursos online (marca **BrandName**) feita em HTML e CSS puros, a partir de um design do Figma. O layout é fluido e responsivo, com o desktop (1440px) como referência visual.

## Seções

1. **Cabeçalho**: marca, links de navegação, login e botão "Tornar-se um membro".
2. **Introdução (hero)**: imagem de fundo, título "25K+ estudantes", texto e botão de chamada.
3. **Conselhos**: três cards com ícone, título e descrição.
4. **Sobre**: imagem de apresentação, título "Watch our Courses" e link "Saiba Mais".
5. **Produtos**: três cards de curso com selo de promoção, departamento, nota, vendas, preço (original e com desconto), duração, lições, progresso e botão.
6. **Depoimentos**: três cards com avaliação em estrelas, texto e autor.
7. **Novidades**: formulário de inscrição por e-mail.
8. **Rodapé**: contato, redes sociais, quatro colunas de links e faixa de direitos.

## Tecnologias

- HTML5 semântico (`header`, `nav`, `main`, `section`, `footer`)
- CSS3: variáveis (`:root`), Flexbox, Grid, pseudo-elementos e media queries
- Fonte [Montserrat](https://fonts.google.com/specimen/Montserrat) via Google Fonts
- JavaScript: o `index.html` referencia `assets/js/script.js` (sem funcionalidades documentadas até o momento)

## Estrutura de arquivos

```
.
├── index.html
├── README.md
└── assets/
    ├── css/
    │   ├── style.css          # estilos base (desktop)
    │   └── responsive.css     # ajustes para tablet e celular
    ├── js/
    │   └── script.js
    └── img/
        ├── background.png
        ├── Frame.png
        ├── thumb-concept-7.png
        ├── product-cover-124.png / 125 / 126
        ├── testimonial-user-cover-167.png / 169 / 124
        ├── coolicon/          # ícones dos cards de conselhos
        ├── icon/              # estrela, calendário, gráficos
        └── social/            # facebook, instagram, twitter
```

## Como executar

Não há dependências nem etapa de build. Abra o `index.html` no navegador ou sirva a pasta com qualquer servidor estático:

```bash
python3 -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Responsividade

| Largura da tela | Comportamento |
| --- | --- |
| acima de 1024px | Layout do Figma, conteúdo centralizado em um container de 1050px |
| até 1024px | Espaçamentos e títulos reduzidos |
| até 768px | Cabeçalho empilhado, seção "Sobre" em coluna, espaçamentos menores |
| até 480px | Títulos menores e formulário de e-mail em coluna |

Os grids dos cards usam `repeat(auto-fit, minmax(...))` e se reorganizam sozinhos. Os valores de largura, espaçamento e container ficam em variáveis no início do `style.css`.

## Personalização

- **Cores e fonte**: variáveis no `:root` do `style.css`.
- **Largura do container e margens laterais**: `--container` e `--gutter`.
- **Altura do fundo do hero**: `--hero-height`. Ela é fixa por breakpoint, então ajuste se o conteúdo do hero mudar de tamanho.

## Pendências

- Ícones de coração, carrinho e olho sobre as imagens dos cursos (presentes no Figma, ainda sem os arquivos).
- Menu hambúrguer para celular (hoje os links do cabeçalho apenas empilham).
- Título "Pacotes que são aprováveis", tradução literal do texto do Figma ("aprodable"), a revisar.
- Textos dos cards de conselhos e o título "Watch our Courses" ainda estão em inglês.
- Ajuste final do `--hero-height` com as imagens reais.

## Créditos

Layout baseado em design do Figma (Figmaland).
