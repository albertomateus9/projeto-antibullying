# Validação do redesign

Data: 11 de novembro de 2026. Escopo: branch `design/redesign-campanha-2026`, página estática local. A imagem aprovada em `../.impeccable/mocks/decision/caderno-convivencia.png` orientou a composição, sem fornecer texto factual ao site.

## Verificações executadas

| Verificação | Resultado |
| --- | --- |
| `node --check script.js` e `git diff --check` | Sem erro de sintaxe ou espaço inválido |
| Navegador: 320, 390, 768, 1024 e 1440 px | Sem rolagem horizontal nas cinco larguras |
| Controle de texto a 200%, nas mesmas larguras | Sem rolagem horizontal; conteúdo refluindo |
| Menu móvel | Abre, fecha pelo link e por Esc; `aria-expanded` atualizado |
| Pesquisa | “cyber” retorna um resultado; “denúncia” encontra o aviso sobre o formulário; estado vazio e anúncio no `role=status` |
| Alto contraste | Alternância e `aria-pressed` atualizados |
| Teclado | Primeiro Tab alcança “Pular para o conteúdo”; Enter segue para `#conteudo`; Esc fecha menu e pesquisa |
| Links de ajuda | Três links `tel:` presentes para 190, 100 e 188 |
| Console do navegador | Nenhum erro na inspeção |
| Página completa em desktop e abertura em celular | Inspeção visual realizada |

Os telefones não foram discados em um dispositivo móvel. A URL do formulário permanece vazia: o botão e as etapas de envio ficam ocultos, com orientação alternativa visível.

## Impeccable e diretrizes de interface

O detector foi executado contra `index.html` e a página renderizada em 390 e 1440 px. Os relatórios JSON estão nesta pasta.

| Auditoria | Antes | Depois |
| --- | ---: | ---: |
| Código-fonte | 10 | 5 |
| Página renderizada | 11 | 2 em 390 px; 2 em 1440 px |

Os dois achados renderizados restantes são `cream-palette` e `italic-serif-display`: escolhas editoriais da composição aprovada, legíveis no contexto do projeto. Os três achados adicionais no código são `cramped-padding` em seções que receberam preenchimento visível na inspeção renderizada. O detector não substitui avaliação de WCAG.

Na checagem orientada pelas [Web Interface Guidelines](https://github.com/vercel-labs/web-interface-guidelines), foram verificados: foco visível e com contraste no painel escuro, hierarquia de títulos, rótulos e estados dos controles, `scroll-margin` para âncoras, ausência de `transition: all`, redução de movimento e reflow do conteúdo. Os pares principais de texto calculados ficam acima de 4,5:1: tinta/papel 15,76:1, texto secundário/papel 5,94:1, texto secundário/verde claro 5,40:1, branco/coral 5,29:1, branco/fundo de ajuda 11,67:1.

Uma revisão independente identificou três correções incorporadas antes da entrega: alinhamento do estilo de `aria-current="location"`, foco claro na área escura e no alto contraste, e inclusão do aviso do formulário na busca por “denúncia”.

## Pendências para publicação

- Obter URL real e procedimento institucional para denúncia anônima antes de habilitar o formulário.
- Fazer validação humana com estudantes e equipe escolar, inclusive leitor de tela e telefone físico, antes de publicar.
- O merge e a publicação dependem de decisão do mantenedor. Esta validação não declara conformidade WCAG integral.
