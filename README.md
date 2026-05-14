# ConectaLojas - Instalador

Repositório público para distribuição do app **ConectaLojas** (versão Android) para testes.

## Para testadores

Abra este link no navegador do seu Android e siga as instruções da página:

**https://donizetti-junior.github.io/ConectaLojas-APP-Instalador/**

(troque pelo domínio próprio quando configurar)

## Para o desenvolvedor

### Como atualizar o APK aqui

No projeto **ConectaLojas-APP**, rode:

```bat
publicar.bat
```

O script:
1. Roda o build de debug (`cordova build android`)
2. Copia o `app-debug.apk` pra este repo como `ConectaLojas.apk`
3. Atualiza `version.json` com a versão atual (lida do `config.xml`) e a data
4. Faz `git add` + `commit` + `push` neste repo

Depois disso, os testadores que abrirem a página já pegam a versão nova.

### Arquivos deste repo

| Arquivo | Descrição |
|---|---|
| `index.html` | Landing page com botão de download e instruções |
| `ConectaLojas.apk` | APK do app (atualizado pelo publicar.bat) |
| `version.json` | Versão e data da última publicação |
| `icon.png` | Ícone do app exibido na landing page |

### Ativando o GitHub Pages (1 vez só)

1. Acesse `https://github.com/donizetti-junior/ConectaLojas-APP-Instalador/settings/pages`
2. Em **Source**, selecione `Deploy from a branch`
3. Em **Branch**, escolha `main` e pasta `/ (root)`
4. Clique em **Save**
5. Aguarde ~1 minuto e acesse o link gerado (aparece no topo da mesma página)

### Observações

- O APK é **de debug**, suficiente para testes internos. Para publicar futuramente na Play Store, precisará gerar um APK release com keystore própria.
- Repo é público para que o link de download funcione sem login.
