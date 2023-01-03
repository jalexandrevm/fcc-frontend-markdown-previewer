# Pré Visualizador de Markdown

Neste projeto iremos criar um visualizador de MarkDown

## Tecnologia usada  

- HTML
- BootStrap (CSS)
- JavaScript

## Introdução

Com todas as tecnologias disponíveis, desta vez acabei escolhendo a mais simples desta vez  

Não teremos o React neste projeto, será apenas nosso bom e velho HTML com o CSS via BootStrap e um pouco de JavaScript via a tag de script na própria página do nosso HTML  

## Iniciando com o BootStrap

Pra começar, fiz uma rápida consulta na documentação do BootStrap e consegui um template básico pra conseguir usá-lo no HTML simples  

## Criando Estrutura Inicial

A partir deste template construiremos toda a estrutura do projeto começando com uma **\<div>** principal para servir de container  

A primeira *div* levou em seu atributo de *class* como `class="container-fluid"` para ocupar toda a largura da tela, ou *viewport*  

Dentro dela, temos mais 2 que usei para nosso título do projeto e a outra para mostrar nosso editor e o pré visualizador do MarkDown  

## Título e Telas

As duas *div's* internas receberam no seu *class* o valor de *row* e dentro da primeira *.row* incluí outra *div* pra dentro dela colocar o título do projeto com uma *h1*  

A *div* que contem o *h1* ficou com o *class* igual a *class="col text-center text-black-50 bg-success"* para definí-la como uma coluna com o texto centralizado e cor em preto a 50% e cor de fundo seguindo o padrão do BootStrap em verde do *bg-success*  

A segunda *div* com *.row* também recebeu o valor de *bg-warning* o deixando em amarelo e aproveitando as cores disponíveis pelo BootStrap  

## Separando as áreas do Editor e Visualizador

Dentro desta segunda *.row* incluí mais 2 *div's* para separar as telas do editor e do pré visualizador e difini seus tamanhos também usando o BootStrap definindo suas classes como *col-5* e *col-7* respectivamente  

Aproveitei e já defini seus *padding* como *p-2* para separar o conteúdo interno das bordas para melhor visualizá-lo  

Na primeira *div*, da tela do editor, a defini como flex com orientação em coluna usando *d-flex flex-column* do BootStrap  

### Títulos das telas

Usei a tag *h2* pra descrever os lados do editor e do visualizador e em ambos defini suas classes com `class="text-center text-white"` deixando-os centralizados e em branco  

Abaixo de ambas as tag's *h2* incluí mais uma *div* e do lado do editor coloquei a tag *textarea* dentro da *div* incluída pra ser nosso editor  

### Preparando espaço do Editor

Na *div* abaixo do *h2* que fica do lado do editor defini sua *class* como `class="form-group flex-grow-1 d-flex flex-column"` definindo como um grupo de um formulário do tipo flex, também com orientação em column e para preenchimento automático ocupando o necessário  

Dentro desta *div* temos um *textarea* que teve sua *class* definida como `class="col-12 bg-info text-white m-0 p-1 form-control flex-grow-1"` fazendo com que a tag ocupe toda a largura da sua *div* pai, com sua cor de fundo em azul e texto em branco, todas as suas margens em 0 e padding em 1  

#### Adiconando um evento

Nesta *textarea* usamos o evento *onchange* para atualizar a *div* do visualizador com o conteúdo do editor convertido em MarkDown executando a função `handleEditorChange()`  

### Preparando o Visualizador

Por fim, na *div* abaixo do *h2* do lado do visualizador, apenas definimos sua *class* como `class="m-0 p-1 text-dark bg-white"` deixando suas margens em 0 e padding em 1 e texto com a fonte em dark e cor de fundo em branco  

### Finalizando

Para finalizar tudo, apenas criei outra função `setExample()`, dentro do *script* da própria página, pra carregar o exemplo exigido no teste via o evento *onload* da tag *body*  
