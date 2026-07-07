# Visitas LM Consig

App de controle de visitas a lojas credenciadas. Funciona como PWA (Progressive Web App) — pode ser instalado direto no celular pelo Chrome.

## Arquivos

| Arquivo | Descrição |
|---|---|
| `index.html` | App completo (HTML + CSS + JS em um arquivo) |
| `manifest.json` | Configuração do PWA |
| `sw.js` | Service Worker (cache offline) |
| `android-chrome-*.png` | Ícones Android |
| `apple-touch-icon.png` | Ícone iOS |
| `favicon.*` | Favicons |

## Publicar no GitHub Pages

1. Suba todos os arquivos para um repositório GitHub
2. Vá em **Settings → Pages**
3. Em "Source" selecione **Deploy from a branch → main → / (root)**
4. Salve — em 1-2 minutos o site estará no ar

## Configuração

As credenciais do Supabase estão dentro do `index.html`:
```
SUPABASE_URL  → linha com 'supabaseUrl'
SUPABASE_KEY  → linha com 'supabaseKey'
```

## Banco de dados (Supabase)

Tabelas necessárias: `lojas` e `visitas`  
Coluna extra necessária: `ALTER TABLE lojas ADD COLUMN potencial text;`
