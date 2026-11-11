# Projeto Antibullying

Site estático da campanha contra o bullying da EETEPA Vilhena Alves.

**Site publicado:** https://albertomateus9.github.io/projeto-antibullying/

O formulário anônimo ainda não tem endereço configurado. Para ativá-lo, informe uma URL em `FORMULARIO_URL` no início de `script.js`; enquanto ela estiver vazia, o site mostra orientações de ajuda em vez de um botão de envio.

## Redesign visual (branch de revisão)

O layout foi modernizado sem migrar para frameworks. A estrutura pedagógica permanece nos arquivos originais:

- `index.html`: conteúdo e HTML semântico, com acessos rápidos na página inicial e números úteis acionáveis no celular.
- `style.css`: estilos originais, mantidos para facilitar o estudo e preservar os recursos já existentes.
- `redesign.css`: nova camada visual, carregada depois de `style.css`, com tokens de cor, tipografia editorial, cartões, layouts responsivos e regras específicas para alto contraste.
- `script.js`: mantém pesquisa, ajuste de fonte, contraste e a lógica do formulário, com melhoria no fechamento do menu mobile.

**Teste local:** execute `python -m http.server 8000` na raiz do repositório e abra `http://localhost:8000`. Sem Python, pode usar `npx serve .`. O site continua compatível com GitHub Pages e não precisa de processo de build.

**Checklist de revisão antes de publicar:**

1. Testar larguras 390, 768, 1024 e 1440 px, rolagem e ausência de barra horizontal.
2. Testar Tab, Shift+Tab, Enter e Esc, incluindo menu mobile, pesquisa e links de ajuda.
3. Ativar alto contraste e alterar o texto para 150%, verificando legibilidade e sobreposições.
4. Verificar modo de movimento reduzido e testar telefone `190`, `100` e `188` em um dispositivo móvel.
5. Confirmar que o formulário de denúncia **não aparece como disponível** até que exista uma URL real, acompanhada de procedimento institucional de acolhimento e privacidade.
6. Executar `npx impeccable detect http://localhost:8000` e registrar os achados antes do merge.

Para retornar ao visual anterior sem mexer na estrutura, remova apenas o link `redesign.css` de `index.html`.

## Impeccable

O [Impeccable](https://github.com/pbakaus/impeccable) está instalado neste repositório para uso com Codex. O skill fica em `.agents/skills/impeccable/`, e o detector de qualidade visual é acionado pelos hooks em `.codex/hooks.json` durante a edição da interface.

Abra este repositório no Codex, autorize o hook do projeto em `/hooks` e use `$impeccable` para ver os comandos. Para registrar o contexto do projeto, execute `$impeccable init`. Depois, por exemplo, use `$impeccable critique index.html` para revisar a experiência ou `$impeccable audit index.html` para verificar qualidade técnica e acessibilidade.

O site publicado continua usando apenas `index.html`, `style.css` e `script.js`. O Impeccable é uma ferramenta de desenvolvimento e não precisa ser carregado no navegador dos visitantes.

