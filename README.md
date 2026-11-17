# SIG – Maranguape (dados secundários)

Mapa web exportado do QGIS (qgis2web / Leaflet). Não precisa de servidor próprio nem de build: é só publicar a pasta no GitHub Pages.

## Publicar no GitHub Pages

O projeto tem mais de 1.100 arquivos. O envio pelo navegador (Upload files) aceita no máximo 100 arquivos por vez, então use Git ou o GitHub Desktop.

1. Crie um repositório vazio no GitHub (ex.: `sig-maranguape`).
2. Dentro desta pasta, rode:

```
git init
git add .
git commit -m "SIG Maranguape"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/sig-maranguape.git
git push -u origin main
```

3. No GitHub, abra **Settings > Pages**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`, e salve.
4. Em alguns minutos o mapa fica em `https://SEU-USUARIO.github.io/sig-maranguape/`.

## Estrutura

- `index.html`: página do mapa.
- `data/`: camadas em GeoJSON (arquivos `.js`).
- `legend/`: imagens das legendas.
- `js/`, `css/`, `webfonts/`: bibliotecas do mapa.

## Atenção

- Os nomes de arquivos foram mantidos sem acentos, porque nomes acentuados costumam quebrar no GitHub Pages.
- O mapa de fundo usa os servidores de tiles do Google (`mt1.google.com`), cujo uso direto fora dos produtos do Google não é previsto nos termos de uso e pode ser bloqueado a qualquer momento. Se quiser um fundo mais estável, troque por OpenStreetMap ou outro provedor.
- Para atualizar o mapa, exporte de novo no QGIS, substitua os arquivos e rode `git add .`, `git commit` e `git push`.
