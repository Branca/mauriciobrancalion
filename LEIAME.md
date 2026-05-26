# Site Mauricio Brancalion
## Estrutura de arquivos

```
/                        ← raiz do servidor
├── index.html           ← site principal
├── dados.json           ← TODO o conteúdo do site (texto, links, obras)
├── admin/
│   └── index.html       ← painel admin (acesse em seusite.com/admin/)
├── assets/
│   ├── css/
│   │   └── base.css
│   ├── js/
│   │   └── main.js
│   └── images/
│       ├── artista.jpg      ← sua foto (substitua este arquivo)
│       ├── og-image.jpg     ← imagem para redes sociais (1200x630px)
│       └── obras/
│           ├── quadrinhos/
│           ├── animacao/
│           ├── musica/
│           ├── games/
│           ├── escrita/
│           └── design/
└── obras/               ← páginas individuais por universo (futuro)
```

---

## Como usar o painel admin

1. Acesse `seusite.com/admin/`
2. Senha padrão: **brancalion2025** (troque no arquivo admin/index.html, linha onde está `const SENHA`)
3. **Adicionar obra:**
   - Clique em "+ Adicionar obra"
   - Escolha o universo, preencha título, ano, descrição
   - Arraste ou selecione uma imagem (fica salva em base64 no JSON)
   - OU informe o caminho da imagem (ex: `assets/images/obras/quadrinhos/tira001.jpg`)
   - Salve
4. **Exportar:**
   - Vá em "Exportar" no menu lateral
   - Clique em "⬇ Baixar dados.json"
   - Faça upload do arquivo baixado para a raiz do servidor (via FTP/cPanel)
   - O site atualiza automaticamente

---

## Fluxo de trabalho recomendado

### Para adicionar obras com imagens grandes:
1. Suba a imagem via FTP para `assets/images/obras/[universo]/nome.jpg`
2. No admin, informe o caminho: `assets/images/obras/quadrinhos/nome.jpg`
3. Exporte e faça upload do dados.json

### Para obras pequenas ou testes rápidos:
1. Arraste a imagem direto no admin (salva embutida no JSON)
2. Exporte e faça upload do dados.json

---

## Personalização inicial

### Sua foto
Substitua o arquivo `assets/images/artista.jpg` pela sua foto.
Proporção recomendada: 3:4 (ex: 600x800px)

### E-mail
Edite em `dados.json` ou pelo painel admin > "Artista & Bio"

### Senha do admin
Abra `admin/index.html`, procure a linha:
```js
const SENHA = 'brancalion2025';
```
Troque pela senha que quiser.

### Redes sociais
Painel admin > "Redes Sociais" — adicione/remova/edite os links.

---

## Upload via FTP (cPanel)

1. Conecte no FTP do seu servidor
2. Navegue até a pasta do seu site (normalmente `public_html/`)
3. Faça upload de TODOS os arquivos mantendo a estrutura de pastas
4. Acesse `seudominio.com` — pronto!

Para atualizar só o conteúdo:
- Basta fazer upload do `dados.json` atualizado

---

## Suporte
Criado com Claude — Estúdio Brancalion, 2025
