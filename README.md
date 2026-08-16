# Vitrine de Demos

Demonstrações navegáveis de cinco ferramentas internas de marketing. Todas rodam no
navegador, sem servidor, sem build e sem login. **Todos os dados são fictícios.**

| # | Demo | O que é |
|---|---|---|
| 01 | Central de Links | Portal único de busca para os recursos digitais da empresa |
| 02 | Central de Pagamentos | Rateio de mídia paga e preparação de lançamentos para o Financeiro |
| 03 | Central de Eventos | Calendário corporativo, mapa do Brasil e solicitação de eventos |
| 04 | Dashboard de Leads | Funil de captação em feiras e eventos, com drill-down |
| 05 | UTM Builder | Assistente de padronização de links UTM |
| 06 | Registro de Lead | Captação de leads no stand, com resumo em texto ou áudio |

Cada demo tem alternador **PT | EN** no topo e tema claro/escuro. A escolha de idioma é
compartilhada entre todos: quem entrar em inglês na vitrine continua em inglês ao abrir
qualquer demo.

---

## Como publicar no GitHub Pages

**1.** Descompacte o arquivo `vitrine-demos.zip` no seu computador. Você vai ter esta estrutura:

```
index.html          ← a vitrine
README.md           ← este arquivo
*.html              ← as 6 demonstrações
```

**2.** No GitHub, abra o repositório e clique em **Add file → Upload files**.

**3.** Arraste **todos os arquivos** de dentro da pasta para a área de upload. São só
arquivos soltos, nenhuma pasta, então nada pode se perder no caminho.

**4.** Escreva uma mensagem no campo de commit (ex.: `primeira versão da vitrine`) e clique
em **Commit changes**.

**5.** Vá em **Settings → Pages**. Em *Source*, escolha **Deploy from a branch**; em
*Branch*, escolha **main** e **/ (root)**. Clique em **Save**.

**6.** Aguarde de 1 a 2 minutos. O site fica no ar em:

```
https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/
```

O endereço aparece na própria tela de Settings → Pages quando a publicação termina.

---

## Como atualizar depois

Para trocar um arquivo, entre na pasta pelo site do GitHub, clique em **Add file → Upload
files** e suba a versão nova com o **mesmo nome** — ela substitui a anterior. O GitHub Pages
republica sozinho em cerca de 1 minuto.

Se a página não atualizar no navegador, force a recarga com `Ctrl + Shift + R`
(ou `Cmd + Shift + R` no Mac) — é cache do navegador, não do GitHub.

---

## Estrutura dos arquivos

```
index.html                              vitrine (índice com busca e filtros)
central-de-links.html                   demo 01
central-de-pagamentos.html              demo 02
central-de-eventos.html                 demo 03
dashboard-de-leads.html                 demo 04
utm-builder.html                        demo 05
registro-de-lead.html                   demo 06
```

Todos os arquivos são autocontidos: CSS, JavaScript, miniaturas e a biblioteca de gráficos
estão embutidos dentro do próprio HTML. Não existe nenhuma pasta de apoio, então cada arquivo
funciona sozinho e a ordem de upload não importa.

O Registro de Lead grava áudio pelo microfone. Navegadores só liberam o microfone em páginas
servidas por **HTTPS** ou em `localhost` — no GitHub Pages funciona normalmente, mas se você
abrir o arquivo direto do disco (`file://`) a gravação pode ser bloqueada. O áudio gravado
fica apenas na memória do navegador: dá para ouvir, mas nada é enviado nem armazenado.

Para publicar uma demo isolada em outro lugar, basta copiar o `.html` dela.

---

## Requisitos e limites

- **Repositório público.** O GitHub Pages não publica repositórios privados no plano gratuito.
- **Só arquivos estáticos.** Não há banco de dados nem back-end: todos os dados são gerados
  dentro do próprio HTML.
- **Fontes via Google Fonts.** Sem internet, a tipografia cai para a fonte do sistema e o
  layout continua íntegro.
- **O código-fonte fica visível** para qualquer visitante. Por isso não inclua nenhuma chave,
  token, endereço interno ou dado real nos arquivos.
