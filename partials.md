# Partials: Revolucionando o Desenvolvimento Web

<div align="center" style="display: flex; justify-content: center; border-radius:4px; width: 100%" >
<img width="250px" height="250px" src="https://github.com/deco-cx/blog/assets/1753396/71348746-ddc0-49d0-9d2e-e5651e23176a" />
</div>

[Fresh](https://fresh.deno.dev/), o framework web utilizado pela Deco, é conhecido por possibilitar a criação de páginas de altíssimo desempenho. Uma das razões pelas quais as páginas criadas na Deco são tão eficientes é devido à arquitetura de ilhas. Essa arquitetura permite que os desenvolvedores removam partes não interativas do pacote final de JavaScript, reduzindo a quantidade total de JavaScript na página e aliviando o navegador para realizar outras tarefas.

No entanto, uma das limitações dessa arquitetura é que páginas muito complexas, com muita interatividade e, portanto, muitas ilhas, ainda exigem uma grande quantidade de JavaScript. Felizmente, essa limitação agora é coisa do passado, graças à introdução dos Partials.

## Como Funciona?

Os Partials, inspirados no [htmx](https://htmx.org/docs/), operam com um runtime que intercepta as interações do usuário com elementos de botão, âncora e formulário. Essas interações são enviadas para nosso servidor, que calcula o novo estado da página e responde ao navegador. O navegador recebe o novo estado da IU em HTML puro, que é então processado e as diferenças são aplicadas, alterando a página para o seu estado final. Para obter informações mais detalhadas sobre os Partials, consulte a [documentação](https://github.com/denoland/fresh/issues/1609) do Fresh.

## Partials em Ação

Estamos migrando os componentes da loja da Deco para a nova solução de Partials. Até o momento, migramos o seletor de SKU, que pode ser visualizado em ação [aqui](http://storefront-vtex.deco.site/camisa-masculina-xadrez-sun-e-azul/p?skuId=120). Mais mudanças, como `infinite scroll` e melhorias nos filtros, estão por vir.

Outra funcionalidade desbloqueada é a possibilidade de criar dobras na página. As páginas de comércio eletrônico geralmente são longas e contêm muitos elementos. Os navegadores costumam enfrentar problemas quando há muitos elementos no HTML. Para lidar com isso, foi inventada a técnica de dobra.

A ideia básica dessa técnica é dividir o conteúdo da página em duas partes: o conteúdo acima e o conteúdo abaixo da dobra. O conteúdo acima da dobra é carregado na primeira solicitação ao servidor. O conteúdo abaixo da dobra é carregado assim que a primeira solicitação é concluída. Esse tipo de funcionalidade costumava ser difícil de implementar em arquiteturas mais antigas. Felizmente, embutimos essa lógica em uma nova seção chamada `Deferred`. Esta seção aceita uma lista de seções como parâmetro que devem ter seu carregamento adiado para um momento posterior.

Para usar essa nova seção:

1. Acesse o painel de administração da Deco e adicione a seção `Rendering > Deferred` à sua página.
2. Mova as seções que deseja adiar para a seção `Deferred`.
3. Salve e publique a página.
4. Pronto! As seções agora estão adiadas sem a necessidade de alterar o código!

Veja `Deferred` em ação neste [link](https://storefront-vtex.deco.site/home-partial).

> Observe que, para a seção `Deferred` aparecer, você deve estar na versão mais recente do `fresh`, `apps` e deco!

Uma pergunta que você pode estar se fazendo agora é: Como escolher as seções que devo incluir no deferred? Para isso, use a aba de desempenho e comece pelas seções mais pesadas que oferecem o maior retorno!
