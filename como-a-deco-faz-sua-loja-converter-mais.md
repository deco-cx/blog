Com dezenas de milhões de e-commerces, o varejo digital nunca enfrentou tanta competição. Por outro lado, com o grande aumento do número de consumidores online, nunca houve maior oportunidade pra crescer. Neste contexto, **oferecer experiências distintas é crucial.**

Contudo, mesmo as maiores marcas tem dificuldade construir algo além do previsível - páginas lentas e estáticas para todos os usuários. O resultado todos já sabem: **baixa conversão** -- pessoas deixam de comprar na loja porque não viram um conteúdo que lhe agrada ou porquê as páginas demoraram pra carregar em seus celulares.

Vamos entender primeiro porque isso acontece.


## Por quê seu site performa mal?

### 1. Sua loja demora para construir

O time de tecnologia para ecommerce é pouco produtivo pois trabalha com frameworks e tech stacks complexas de aprender e fazer manutenção - e que vão ficando ainda mais complexas com o tempo, além do talento em tech ser escasso.

Pessoas desenvolvedoras gastam horas e horas cada mês com a complexidade acidental das tecnologias usadas: esperando o tempo de deploy, cuidando de milhares de linhas de código, ou lidando com dependências no npm - sobra pouco tempo para codar de verdade.

Resultado: o custo de novas funcionalidades é caro e a entrega é demorada, além de ser operacionalmente complexo contratar e treinar devs.


### 2. Sua loja demora para carregar

Sabe-se que a velocidade de carregamento de uma página afeta drastricamente a taxa de conversão e o SEO. Em um site "médio", é esperado que cada 100ms a menos no tempo de carregamento de uma página, aumente em 1% a conversão.

Ainda assim, a maior parte das lojas tem storefronts (frentes de loja de ecommerce) com nota abaixo de 50 no [Google Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/). E poucos parecem saber resolver.

Com isso, o ecommerce global perde trilhões (!) de dólares em vendas.

Parte do problema é a escolha do framework e das tecnologias envolvidas:

a.  SPA (Single Page Application) não é a tecnologia ideal para ecommerce, especialmente para performance e SEO.

b.  A complexidade de criar código com esse paradigma cria bases de código difíceis de manter e adicionar novas funcionalidades.


### 3. Sua loja demora para evoluir

Nos negócios e na vida, a evolução contínua e o aprendizado diário é o que gera sucesso. Especialmente no varejo, que vive de otimização contínua de margem.

Contudo, times de ecommerce dependem de devs para editar, testar, aprender e evoluir suas lojas.

Devs, por sua vez, estão geralmente sobrecarregadas de demandas, e demoram demais para entregar o que foi pedido, ainda que sejam tasks simples.

Para piorar, as ferramentas necessárias para realizar o ciclo completo de CRO (conversion rate optimization) como teste A/B, analytics, personalização e content management system (CMS) estão fragmentadas, o que exige ter que lidar com várias integrações e diversos serviços terceirizados diferentes.

Tudo isso aumenta drasticamente a complexidade operacional, especialmente em storefronts de alta escala, onde o ciclo de evolução é lento e ineficaz.


## Nossa solução

Nosso time ficou mais de 10 anos lidando com estes mesmo problemas. Sabemos que existem tecnologias para criar sites e lojas de alto desempenho, mas a maioria parece não ter a coragem de utilizá-las.

Foi quando decidimos criar a deco.cx.

Para habilitarmos a criação de experiências de alto desempenho foi necessário um novo paradigma, que simplifique a criação de lojas rápidas, sem sacrificar a capacidade de **personalização e de evolução contínua.**

Criamos uma plataforma headless que integra tudo o que uma marca ou agência precisa para gerenciar e otimizar sua experiência digital, tornando fácil tomar decisões em cima de dados reais, e aumentando continuamente as taxas de conversão.

## Como fazemos isso:

### 1. Com deco.cx fica rápido de construir

Aceleramos desenvolvimento de lojas, apostando em uma combinação de tecnologias de ponta que oferecem uma experiência de desenvolvimento frontend otimizada e eficiente. A stack inclui:

- [**Deno**](https://deno.land)
 Um runtime seguro para JavaScript e TypeScript, criado para resolver problemas do Node.js, como gerenciamento de dependências e configurações TypeScript.

- [**Fresh**](https://fresh.deno.dev)
Um framework web minimalista e rápido, que proporciona uma experiência de desenvolvimento mais dinâmica e eficiente, com tempos de compilação rápidos ou inexistentes.

- [**Twind**](https://twind.dev)
Uma biblioteca de CSS-in-JS que permite a criação de estilos dinâmicos, sem sacrificar o desempenho, e oferece compatibilidade com o popular framework Tailwind CSS.

- [**Preact**](https://deno.land)
Uma alternativa leve ao React, que oferece desempenho superior e menor tamanho de pacote para aplicações web modernas.

Essa combinação de tecnologias permite que a deco.cx ofereça uma plataforma de desenvolvimento frontend que melhora a produtividade e reduz o tempo de implementação, além de proporcionar sites de alto desempenho.

Os principais ganhos de produtividade da plataforma e tecnologia deco são:

-   O deploy (e rollback) instantâneo na edge oferecido pelo [deno Deploy](https://deno.com/deploy)

-   A bibliotecas de componentes universais e extensíveis ([Sections](https://www.deco.cx/docs/en/concepts/section)), além de funções pré-construídas e totalmente customizáveis ([Loaders](https://www.deco.cx/docs/en/concepts/loader)).

-   A facilidade de aprendizado. Qualquer desenvolvedor junior que sabe codar em React, Javascript, HTML e CSS consegue aprender rapidamente a nossa stack, que foi desenhada pensando na melhor experiência de desenvolvimento.


### 2. Com deco.cx fica ultrarrápido de navegar

As tecnologias escolhidas pela deco também facilitam drasticamente a criação de lojas ultrarrápidas.

Normalmente os storesfronts são criados com React e Next.Js - frameworks JavaScript que usam a abordagem de Single-Page Applications (SPA) para construir aplicativos web. Ou seja, o site é carregado em uma única página e o conteúdo é transportado dinamicamente com JavaScript.

Deno e Fresh, tecnologias que usamos aqui, são frameworks de JavaScript que trabalham com outro paradigma: o server-side-rendering, ou seja, o processamento dos componentes da página é feito em servidores antes de ser enviado para o navegador, ao invés de ser processado apenas no lado do cliente.

Isso significa que a página já vem pronta para ser exibida quando é carregada no navegador, o que resulta em um carregamento mais rápido e uma melhor experiência do usuário.

Além disso, essas tecnologias trabalham nativamente com computação na edge, o que significa que a maior parte da lógica é executada em servidores perto do usuário, reduzindo a latência e melhorando a velocidade de resposta.  Como o processamento é feito em servidores na edge, ele é capaz de realizar tarefas mais pesadas, como buscar e processar dados de fontes externas, de forma mais eficiente.

Ao usar essas ferramentas em conjunto, é possível construir e-commerces de alto desempenho, com tempos de carregamento de página mais rápidos e uma experiência geral melhorada.


### 3. Com deco.cx fica fácil de evoluir

A plataforma deco oferece, em um mesmo produto, tudo o que as agências e marcas precisam para rodar o ciclo completo de evolução da loja:

- **Library**: Onde os desenvolvedores criam (ou customizam) [loaders](https://www.deco.cx/docs/en/concepts/loader) que puxam dados de qualquer API externa, e usam os dados coletados para criar componentes de interface totalmente editáveis pelos usuários de negócio ([Sections](https://www.deco.cx/docs/en/concepts/section)).

- **Pages**: Nosso CMS integrado, para que o time de negócio consiga [compor e editar experiências rapidamente](https://www.deco.cx/docs/en/concepts/page), usando as funções e componentes de alto desempenho pré-construidos pelos seus desenvolvedores, sem precisar de uma linha de código.

- **Campanhas**: Nossa ferramenta de personalização que te permite agendar ou customizar a mudança que quiser por data ou audiência. Seja uma landing page para a Black Friday ou uma sessão para um público específico, você decide como e quando seu site se comporta para cada usuário.

- **Experimentos**: Testes A/B ou multivariados em 5 segundos - nossa ferramenta te permite acompanhar, em tempo real, a performance dos seus experimentos e relação à versão de controle.

- **Analytics**: Dados em tempo real sobre toda a jornada de compra e a performance da loja. Aqui você cria relatórios personalizados, que consolidam dados de qualquer API externa.


## O que está por vir

Estamos só começando. Nossa primeira linha de código na deco foi em Setembro 2022. De lá pra cá montamos [uma comunidade no Discord](http://deco.cx/discord), que já conta com 1.050+ membros, entre agências, estudantes, marcas e experts.

Se você está atrás de uma forma de criar sites e lojas ultrarrápidos, relevantes para cada audiência, e que evoluem diariamente através de experimentos e dados, [agende uma demo](http://deco.cx).
