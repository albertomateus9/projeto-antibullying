# Ferramentas de design do projeto

As habilidades abaixo ficam em `.agents/skills/` e entram no contexto do Codex ao abrir este repositório. Não fazem parte do JavaScript servido aos visitantes.

| Ferramenta | Uso no fluxo | Licença |
| --- | --- | --- |
| [Impeccable](https://github.com/pbakaus/impeccable) | Contexto, crítica, auditoria, detector e revisão final; já instalado antes desta tarefa | Apache-2.0 |
| [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Pesquisa local de padrões, tokens, acessibilidade e tipografia | MIT |
| [Frontend Design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) | Direção artística e crítica de soluções genéricas | Apache-2.0 |
| [Review Animations](https://github.com/emilkowalski/skills/tree/main/skills/review-animations) | Revisão de movimento e `prefers-reduced-motion` | MIT |

Para usar no Codex, abra o repositório e invoque `$impeccable`, `$ui-ux-pro-max`, `$frontend-design` ou `$review-animations` no chat. O hook existente do Impeccable continua em `.codex/hooks.json` e pode exigir autorização em `/hooks` no Codex. As habilidades recém-instaladas ficam disponíveis após reabrir o projeto ou iniciar uma nova conversa.

A instalação do UI UX Pro Max inclui os scripts de busca e design system, orientações CSV, referências e licença. Testes internos e catálogos brutos de origem, que não são lidos por esses scripts, ficaram fora do controle de versão para reduzir o tamanho da branch.

O [Web Interface Guidelines da Vercel](https://github.com/vercel-labs/web-interface-guidelines) será consultado diretamente para a auditoria; não foi copiado ao projeto porque o repositório de habilidades não declara uma licença no metadado do GitHub. `react-best-practices` foi descartado porque não há React.

[Taste Skill](https://github.com/Leonxlnx/taste-skill) e [Garden Skills: Web Design Engineer](https://github.com/ConardLi/garden-skills/tree/main/skills/web-design-engineer) foram avaliados e não instalados: suas orientações se sobrepõem às três habilidades principais. O Taste Skill também prescreve momentos animados obrigatórios, inadequados à prioridade de calma, acessibilidade e baixo custo desta campanha.

Nenhuma biblioteca, serviço pago ou dependência de execução do site foi adicionada.
