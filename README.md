# JPlayer

Player de música offline (PWA) com IA.

## Publicar no GitHub Pages
1. Crie um repositório no GitHub (ex.: `jplayer`).
2. Envie todos os arquivos desta pasta para a raiz do repositório.
3. Em **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main` / `(root)` → Save.
4. Aguarde 1–2 min e abra `https://SEU-USUARIO.github.io/jplayer/` no Chrome do celular.
5. Menu ⋮ → **Instalar app** / **Adicionar à tela inicial**.

## Transformar em app Android (APK/AAB)
1. Com o site no ar, abra https://www.pwabuilder.com e cole a URL do GitHub Pages.
2. Clique em **Package for stores → Android** e baixe o pacote.
3. Instale o `.apk` no celular (ou use o `.aab` na Play Store).

## Atualizar
Ao mudar o app, aumente o número em `CACHE` no `service-worker.js` (ex.: `jplayer-v2`).

## IA do chat
- A cada mensagem, a IA recebe o catálogo **atualizado** da biblioteca (títulos, artistas e estilos). Música nova importada já é conhecida na próxima mensagem.
- Ao adicionar músicas, a IA avisa no chat e classifica o estilo delas (com internet).
- Biblioteca muito grande: a IA vê os artistas principais + as músicas mais relevantes ao pedido.
- Sem internet (ou com a opção "só no Wi-Fi" ligada no 4G/5G), o chat usa o modo local: estilos, climas e artistas.

## Letras automáticas
- Toda música importada tem a letra procurada e salva sozinha (LRCLIB, precisa de internet). Se a música já traz letra no arquivo, ela é mantida.
- Ao abrir o app, as músicas que ainda estão sem letra entram na fila. Sem internet, a busca continua quando a conexão voltar.
- Letra não encontrada é tentada de novo depois de 7 dias; o botão "Buscar letra online" tenta na hora.
- A opção "só no Wi-Fi" também vale para a busca de letras.
- A letra aparece num cartão colorido embaixo do player (botão "Letra"). Quando existe versão sincronizada, a linha atual acompanha a música, e tocar numa linha pula para ela.
