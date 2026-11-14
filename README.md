# MTG Print Conversor

Conversor de printings por prioridades de coleções de Magic: The Gathering, utilizando a API pública do Scryfall. Interface em português e inglês.

## Publicação no GitHub Pages

1. Crie um repositório **público** no GitHub (por exemplo, `mtg-print-conversor`).
2. Na raiz do repositório, envie **todos os arquivos e a pasta `assets/`**, mantendo `index.html` na raiz.
3. Abra **Settings → Pages → Build and deployment**.
4. Em **Source**, escolha `Deploy from a branch`; em **Branch**, escolha `main` e `/(root)`; clique em **Save**.
5. O endereço normalmente fica `https://SEU-USUARIO.github.io/mtg-print-conversor/`.

## Como modificar o favicon

Substitua `assets/favicon.svg` pelo seu SVG, mantendo o nome. Para suporte a outros dispositivos, substitua também `favicon-32.png`, `apple-touch-icon.png`, `icon-192.png` e `icon-512.png`. Os arquivos já estão prontos como modelos. O preview de compartilhamento é `assets/social-preview.png`.

## Como personalizar o site

- Textos e layout: `index.html` (CSS e JS estão incorporados para facilitar a publicação sem ferramentas extras).
- Ícone do navegador: `assets/favicon.svg`.
- Imagem ao compartilhar: `assets/social-preview.png`.
- Configurações de instalação: `manifest.webmanifest`.
- Informações do projeto: este `README.md`.

## Funcionamento e privacidade

Não há backend nem banco de dados. A conversão acontece no navegador. A aplicação acessa a API pública do Scryfall para consultar coleções e cartas e salva apenas a preferência de idioma localmente. Não há upload da decklist para um servidor do projeto. É necessária conexão com a internet, e a disponibilidade depende da API do Scryfall.

A ferramenta é independente, não afiliada à Wizards of the Coast ou ao Scryfall. Respeite as regras de uso da API do Scryfall; para alto volume, considere otimizações e limites de consulta.

## Ícones de coleções (Set Icons)

Os símbolos exibidos no catálogo e na lista de prioridades vêm diretamente de `icon_svg_uri` presente nos dados de `https://api.scryfall.com/sets`. O aplicativo reutiliza o catálogo já carregado, sem consultar cada coleção individualmente. SVGs são carregados pelo navegador apenas conforme necessário (`loading=lazy`). Se o URL não estiver disponível ou falhar, aparece o símbolo genérico ◇. Os ícones usam filtro CSS de contraste para o fundo escuro; há suporte CSS para um tema claro (`data-theme="light"`) caso seja implementado futuramente. A escolha das coleções no catálogo é feita por checkbox; a ordem continua ajustável pelas setas.
