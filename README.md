# Projeto Antibullying

Site estático de um projeto estudantil para a feira de ciências da EETEPA Vilhena Alves. Apresenta informações sobre bullying, atitudes de prevenção e caminhos para buscar ajuda.

**Site publicado:** https://albertomateus9.github.io/projeto-antibullying/

O formulário anônimo ainda não tem endereço configurado. Para ativá-lo, informe uma URL em `FORMULARIO_URL` no início de `script.js`; enquanto ela estiver vazia, o site mostra orientações de ajuda em vez de um botão de envio.

## Redesign visual (branch de revisão)

O redesign segue a direção editorial **Caderno de convivência**, aprovada antes da implementação. A página funciona como site estático, sem framework nem etapa de build:

- `index.html`: estrutura semântica, conteúdo educativo, acesso à ajuda e créditos dos estudantes.
- `style.css`: sistema visual consolidado, layout responsivo, foco visível e modo de alto contraste.
- `script.js`: menu móvel, pesquisa, ajuste de texto até 200%, contraste e lógica do formulário.
- `assets/fonts/`: fonte Newsreader hospedada no próprio site, com licença OFL.

**Teste local:** execute `python -m http.server 8000` na raiz do repositório e abra `http://localhost:8000`. Sem Python, pode usar `npx serve .`. O site continua compatível com GitHub Pages e não precisa de processo de build.

**Verificações realizadas nesta branch:**

1. Larguras 320, 390, 768, 1024 e 1440 px, sem rolagem horizontal, também com texto a 200%.
2. Menu móvel, pesquisa, contraste e visibilidade condicional do formulário.
3. Detector Impeccable sobre código e página renderizada; relatórios em `docs/audits/`.
4. Revisão visual completa em desktop e celular.

O formulário continua indisponível até que exista uma URL real e um procedimento de acolhimento definido pela escola. Os números de telefone são links `tel:` e devem ser conferidos no dispositivo de destino antes de publicar. Esta branch é uma proposta de revisão; o site público permanece vinculado à branch principal.

Consulte `PRODUCT.md`, `DESIGN.md`, `docs/DIAGNOSTICO.md` e `docs/FERRAMENTAS.md` para decisões de produto, sistema visual, diagnóstico e ferramentas.

## Impeccable

O [Impeccable](https://github.com/pbakaus/impeccable) está instalado neste repositório para uso com Codex. O skill fica em `.agents/skills/impeccable/`, e o detector de qualidade visual é acionado pelos hooks em `.codex/hooks.json` durante a edição da interface.

Abra este repositório no Codex, autorize o hook do projeto em `/hooks` e use `$impeccable` para ver os comandos. Para registrar o contexto do projeto, execute `$impeccable init`. Depois, por exemplo, use `$impeccable critique index.html` para revisar a experiência ou `$impeccable audit index.html` para verificar qualidade técnica e acessibilidade.

O Impeccable é uma ferramenta de desenvolvimento e não é carregado no navegador dos visitantes.

