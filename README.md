# Sofistic
# Landing page — Sofistic perfumes

Essa landing page contém informações básicas do comércio de venda de perfumes, com uma galeria responsiva de vídeos e fotos dos perfumes e uma lista de formas de contato.

O layout é em tema escuro com destaques em neon e uma imagem em paralax de fundo, inclui versões desktop e mobile, e um redirecionamento simples que leva usuários móveis a uma versão dedicada.

<a href="https://sofistic.pages.dev">Deploy da landing page rodando</a> 

## Estrutura principal

- `index.html` — Página inicial (desktop)
- `services.html` — Galeria de perfumes (desktop)
- `contact.html` — Lista de formas de contato (desktop)
- `menuMobile.html`, `servicesMobile.html`, `contactMobile.html` — Versões simplificadas para dispositivos móveis
- `css/styles.css` — Estilos do site (variáveis CSS, componentes, responsividade)
- `img/` — Imagens usadas no site (ex.: `logo.jpg`)

## Funcionalidades e detalhes técnicos

- Redirecionamento mobile: cada página desktop contém um script que redireciona para `menuMobile.html` quando `window.innerWidth < 640`.
- Estilos principais estão em `css/styles.css` com variáveis (`--bg`, `--neon`, `--text`) para facilitar personalização.
- Componentes notáveis no CSS:
  - `.thumb` — área de imagem dos perfumes, com `overflow: hidden` e `img { object-fit: cover }` para manter proporção.
  - `.nav-list a` — botões do menu com borda arredondada e animação de hover (translateY + box-shadow).
  - Regras de responsividade (`@media (max-width:640px)` e `@media (min-width:800px)`) para ajustar layout e grid de projetos.

## Como usar localmente

1. Clone o repositório:

```bash
git clone https://github.com/cl3af/Sofistic.git
cd Sofistic
```

2. Abra os arquivos `.html` diretamente no navegador ou use um servidor local:

```bash
# Com Python 3
python -m http.server 8000

# Ou com Node (http-server)
npx http-server

# Acesse: http://localhost:8000
```

3. Para testes mobile abra as páginas `*Mobile.html` ou redimensione a janela para <640px e deixe o script redirecionar (necessário reiniciar a página).

## Como editar / adicionar conteúdo

- Para adicionar um projeto, edite `services.html` e `servicesMobile.html` adicionando um novo `<article class="project">` com uma imagem em `img/` e descrição.
- Para mudar cores, edite as variáveis em `css/styles.css` no seletor `:root`.
- Para ajustar o comportamento mobile, altere o valor do breakpoint no script (atualmente 640px) ou converta o redirecionamento para uma abordagem baseada em CSS/JS mais avançada.

## Boas práticas / sugestões

- Adicione um arquivo `.gitignore` para evitar enviar arquivos do OneDrive e do sistema:

```
# Exemplo mínimo
.DS_Store
node_modules/
.env
Thumbs.db
*.tmp
```

- Use GitHub Pages, Netlify ou Vercel para hospedar facilmente o site estático.

## Histórico de alterações (local)

- 2026 — Criação do site, adição de versões mobile e ajustes de estilo.

## Contato

- Autor: Alexandre Soares
- GitHub: https://github.com/cl3af

---

_README gerado / atualizado localmente para documentar o projeto._
