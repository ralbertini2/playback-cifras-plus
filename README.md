# Playback Cifras+ Business Alpha

Base: Playback Cifras v12-2 estável.

Subtítulo: **A forma mais inteligente de organizar seu repertório.**

## Objetivo
Transformar a interface atual em uma versão comercial inicial, mantendo as funcionalidades existentes.

## Estrutura analisada
- `index.html`: layout principal, sidebar, visualizador PDF, player e navegação.
- `styles.css`: tema, responsivo, rodapé, menu lateral e componentes visuais.
- `app.js`: login Google, Google Drive, biblioteca, PDF, MP3, player, favoritos, playlists, zoom, rolagem e navegação.
- `config.js`: Client ID e API Key do Google.
- `manifest.webmanifest`: instalação PWA.
- `service-worker.js`: cache do app.

## Arquivos alterados
- `index.html`
- `styles.css`
- `app.js`
- `README.md`

## Arquivos criados
- Nenhum arquivo funcional novo. A versão usa os assets já existentes, incluindo `logo-playback-cifras.jpg`.

## Alterações aplicadas
- Marca atualizada para **Playback Cifras+**.
- Subtítulo comercial incluído: “A forma mais inteligente de organizar seu repertório.”
- Identificação visual: **Business Alpha · v12+**.
- Logo pequeno no topo esquerdo.
- Layout escuro, limpo e mais comercial.
- Barra inferior com botões grandes e flat:
  - Músicas
  - Categorias
  - Favoritos
  - Setlists
  - Configurações
- Telas/abas iniciais para Setlists e Configurações.
- Favoritos e Categorias reaproveitam a lógica atual sem alterar a estrutura do Drive.
- Responsivo ajustado para celular, tablet/iPad e desktop.

## Funcionalidades preservadas
- Login Google.
- Leitura do Google Drive.
- Seleção de pasta do Drive.
- Abertura de PDFs.
- Execução dos MP3s.
- Navegação anterior/próxima.
- Zoom do PDF.
- Rolagem automática.
- Favoritos.
- Playlists/eventos.
- Modo palco.
- Tela cheia.

## Não alterado nesta versão
- Lógica de sincronização do Drive.
- Modelo de assinatura.
- Banco de dados.
- Pagamento.
- Limite de usuários.

## Testes realizados
- Verificação de sintaxe JavaScript com `node --check app.js`.
- Validação da presença dos IDs usados pelo app no HTML.
- Teste de empacotamento ZIP.
- Verificação estática de `index.html`, `styles.css` e `app.js`.

## Possíveis riscos
- A barra inferior comercial aumenta a altura do rodapé e pode reduzir a área visível do PDF em telas pequenas.
- O Google Drive/OAuth precisa do `GOOGLE_CLIENT_ID` e `GOOGLE_API_KEY` reais após o upload ao GitHub.
- O cache do PWA pode exigir atualização forçada ou remoção/reinstalação na tela inicial do iPad após trocar a versão.

## Configuração após subir no GitHub
Editar `config.js` e inserir novamente:

```js
GOOGLE_CLIENT_ID: "SEU_CLIENT_ID",
GOOGLE_API_KEY: "SUA_API_KEY",
```
