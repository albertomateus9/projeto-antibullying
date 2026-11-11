# Diagnóstico do redesign

Análise da branch `design/redesign-campanha-2026` e da PR #1 antes da reformulação. O site é um projeto estudantil da feira de ciências, conforme confirmação do autor.

## Prioridades

| Prioridade | Achado | Evidência | Ação planejada |
| --- | --- | --- | --- |
| P1 | Texto em cartões abaixo de 4,5:1 | Detector Impeccable: relações de 4,3–4,4:1 em três combinações | Ajustar tokens e verificar no navegador |
| P1 | A interface ainda depende de cartões repetidos e decoração em gradiente | Inspeção desktop/mobile; detector: `nested-cards` e `radial-spotlight-glow` | Substituir por composição editorial e listas claras |
| P1 | Duas folhas CSS acumulam regras e sobreposições | `style.css` mais `redesign.css` (655 linhas na segunda camada) | Consolidar estilos após a direção visual ser aprovada |
| P1 | O serviço de denúncia não está disponível | `FORMULARIO_URL` vazio; aviso já aparece no site | Manter estado indisponível claro; não criar formulário fictício |
| P2 | Tipografia e hierarquia variam entre áreas | Inspeção da página e CSS | Definir escala e tokens em `DESIGN.md` |
| P2 | Navegação móvel e ampliação ainda precisam da matriz completa | PR lista testes manuais, sem evidência dos cinco breakpoints e 200% | Testar 320, 390, 768, 1024 e 1440 px, teclado e zoom |
| P2 | Animações decorativas podem competir com a leitura | CSS de hover e composição atual | Manter movimento mínimo e respeitar redução de movimento |

O detector registrou 10 achados no código e 11 na página renderizada antes das mudanças. Os relatórios completos estão em `docs/audits/baseline-source.json` e `docs/audits/baseline-render.json`; não são um atestado de conformidade WCAG. A auditoria final deve ser repetida após a implementação.

## Direções consideradas

| Direção | Legibilidade e acessibilidade | Adequação ao público | Identidade | Custo | Decisão |
| --- | --- | --- | --- | --- | --- |
| Caderno de convivência | Alta: tipografia forte, fundo claro e índice textual | Alta: acolhedor sem infantilizar | Editorial e ligado ao ambiente escolar | Baixo, com HTML/CSS | Aprovada pelo autor e implementada |
| Mural escolar | Média: blocos e notas exigem controle de contraste e ordem | Média: pode parecer infantil | Escolar, porém literal | Médio | Alternativa se o autor preferir |
| Guia de acolhimento | Alta: estrutura simples e previsível | Média: pode parecer institucional demais | Menos autoral | Baixo | Alternativa mais sóbria |

A composição aprovada preserva o conteúdo real. A imagem de direção é apenas referência visual; o texto do HTML foi revisado separadamente.
