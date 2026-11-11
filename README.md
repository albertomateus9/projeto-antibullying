# Projeto Antibullying

Site estático da campanha contra o bullying da EETEPA Vilhena Alves.

**Site publicado:** https://albertomateus9.github.io/projeto-antibullying/

O formulário anônimo ainda não tem endereço configurado. Para ativá-lo, informe uma URL em `FORMULARIO_URL` no início de `script.js`; enquanto ela estiver vazia, o site mostra orientações de ajuda em vez de um botão de envio.

## Impeccable

O [Impeccable](https://github.com/pbakaus/impeccable) está instalado neste repositório para uso com Codex. O skill fica em `.agents/skills/impeccable/`, e o detector de qualidade visual é acionado pelos hooks em `.codex/hooks.json` durante a edição da interface.

Abra este repositório no Codex, autorize o hook do projeto em `/hooks` e use `$impeccable` para ver os comandos. Para registrar o contexto do projeto, execute `$impeccable init`. Depois, por exemplo, use `$impeccable critique index.html` para revisar a experiência ou `$impeccable audit index.html` para verificar qualidade técnica e acessibilidade.

O site publicado continua usando apenas `index.html`, `style.css` e `script.js`. O Impeccable é uma ferramenta de desenvolvimento e não precisa ser carregado no navegador dos visitantes.

