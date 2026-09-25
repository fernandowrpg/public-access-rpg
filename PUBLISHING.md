# Publicando uma versão (manual)

Repositório: https://github.com/fernandowrpg/public-access-rpg

Os usuários instalam pelo **link do manifesto**, que sempre aponta para a última release:

```
https://github.com/fernandowrpg/public-access-rpg/releases/latest/download/system.json
```

## Primeira vez

```bash
npm install
git init -b main
git remote add origin https://github.com/fernandowrpg/public-access-rpg.git
git add .
git commit -m "Public Access 1.3.0"
git push -u origin main
```

## A cada versão

1. Anote as mudanças em `CHANGELOG.md`.
2. Se você mudou `tools/latchkey-moves.mjs` ou `tools/mysteries.mjs`, regere os compêndios com `npm run build:packs`.
3. Gere a release. O script atualiza `version`, `manifest` e `download` no `system.json` e no `package.json`, e cria `dist/system.json` e `dist/public-access.zip`:
   ```bash
   npm run release -- 1.4.0
   ```
   Sem número de versão, ele usa a versão que já está no `system.json`.
4. Faça commit e push:
   ```bash
   git add .
   git commit -m "Release 1.4.0"
   git push
   ```
5. No GitHub, vá em **Releases → Draft a new release**:
   - **Tag:** `v1.4.0`. Precisa ser exatamente `v` + a versão, porque o link de download aponta para essa tag.
   - Cole as notas do `CHANGELOG.md`.
   - Anexe **os dois arquivos** de `dist/`: `system.json` e `public-access.zip`.
   - Publique como *Latest release*.
6. Teste no Foundry: *Configuração → Sistemas de Jogo → Instalar Sistema → URL do manifesto* (o link acima).

## Checklist

- [ ] `version` do `system.json` igual à tag (sem o `v`)
- [ ] Os dois arquivos de `dist/` anexados à release
- [ ] A release marcada como *Latest*
- [ ] Nenhum texto copiado dos PDFs no repositório (o `.gitignore` já bloqueia `*.txt` e `*.pdf`)

## Listar no site do Foundry (opcional)

Em https://foundryvtt.com/me/packages, submeta um pacote do tipo *System* com o id `public-access` e o link do manifesto acima.
