# Desafio 02 do Rocketseat Ignite - Componentizando a aplicação

Nesse desafio comecamos com uma aplicação feita com toda a logica dentro do app.tsx.
Foi pedido para separar a parte logica do app em mais dois compomentes, um pra sidebar e outro pra mostrar o conteudo.

## Requesitos:

- A aplicação possui apenas uma funcionalidade principal que é a listagem de filmes;
- Na sidebar é possível selecionar qual categoria de filmes deve ser listada;
- A primeira categoria da lista (que é "Ação") já deve começar como marcada;
- O header da aplicação possui apenas o nome da categoria selecionada que deve mudar dinamicamente.

## Solução

A parte que faz a requesição na API ficou toda na app.tsx que é o parente dos outros componentes.
Os parametros foram passados para os compomentes SideBar e Content, de acordo com o que cada um precisava para funcionar corretamente.

### O que aprendi

De inicio peguei toda a logica e as requesicoes de api e coloquei dentro da sidebar, e separei o Content com a logica para mostrar o conteudo
de acordo com o que era selecionado pela sidebar, porem, não funcionou.

Depois de um pouco de pesquisa e dicas de usuarios da comunidade, vi que era melhor deixar as requesicoes de api e o useState
dentro a app principal (parente), e depois passar os mesmos como parametros para os componentes filhos. Isso fez com que tudo funcione corretamente.
A app principal monitora tudo, e atualiza de acordo com as seleções feitas pelo usuario na sidebar.
