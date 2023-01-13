# Minha experiência criando uma página com deco.cx

Recriando a página da deno-land utilizando a plataforma da deco.cx com as tecnologias: Deno, Fresh, Preact e Twind.

03 jan 2023, por Guilherme Tavano

![Minha experiência criando uma página com deco.cx](https://images.prismic.io/tavanoblog/e9e653f9-966a-4faa-a206-63a85f82f5f5_deco-cx-deno-land.jpg?auto=compress,format&w=3840&q=75)

## Desafio

Recentemente aceitei um desafio e quero compartilhar como foi a minha experiência.

O desafio era reconstruir a Home da [https://deno.land/](https://deno.land/) utilizando a plataforma deco.cx como CMS.

## O que é deco.cx?

É uma plataforma criada por um time de pessoas que trabalharam na Vtex, para construir páginas e lojas virtuais performáticas e em um curto período de tempo.

Com o slogan "Crie, teste e evolua sua loja. Todos os dias.", a plataforma foca na simplicidade no desenvolvimento, autonomia para edições/testes e foco em performance.

## Primeira etapa - Conhecendo a Stack

Antes de iniciar o desenvolvimento, precisei correr atrás das tecnologias que a deco.cx sugere para utilização.

São elas:

### Preact

Preact é uma biblioteca JS baseada no React, mas que promete ser mais leve e mais performática.

A adaptação aqui, para quem já tem o React, não tende a ser complicada.

### Deno

Deno é um ambiente de execução de Javascript e Typescript, criado pelo mesmo criador do Node.js.

Com uma boa aceitação entre os devs, a alternativa melhorada do Node.js promete se destacar no futuro.

### Fresh

Fresh é um Framework que me deixou bem curioso. Nessa stack, podemos dizer que ele atua como um Next.

Apesar de não ter me aprofundado no Framework, não tive problemas aqui, afinal um dos pilares do Fresh é não precisar de configuração, além de não ter etapa de build.

### Twind

Twind é uma alternativa mais leve, rápida e completa do tão conhecido Tailwind.

A adaptação é extremamente fácil para quem já trabalha com Tailwind, mas não era o meu caso.

Pequenos gargalos no começo, mas a curva de aprendizagem é curta e nas últimas seções eu já estava sentindo os efeitos (positivos).

## Segunda Etapa - Conhecendo a ferramenta da deco.cx

Meu objetivo aqui, era entender como a ferramenta me ajudaria a recriar a página deno.land, tornando os componentes editáveis pelo painel CMS.

### Criação da Conta

O Login foi bem simples, pode ser feito com Github ou Google.

### Criação do Projeto

Na primeira página, após logado, temos a opção de Criar um Novo Site.

Tive que dar um nome ao projeto e escolher o template padrão para ser iniciado.

![](https://images.prismic.io/tavanoblog/2aa05cf7-37c8-4f0f-a9e6-305a61148f41_Screenshot+from+2023-01-02+23-40-38.png?auto=compress,format)

Assim que o site é criado, **automaticamente** um repositório é montado no GitHub da [deco-sites](https://github.com/deco-sites) e um link da sua página na internet também.

A partir dai, cada push que você fizer resultará no Deploy da aplicação no servidor e rapidamente será refletido em produção

### Entendendo páginas e seções

Dentro do painel, podemos acessar a aba de "Pages"

![](https://images.prismic.io/tavanoblog/e0ca9a8b-39f7-494d-845f-251115fbd3cf_Screenshot+from+2023-01-02+23-46-00.png?auto=compress,format)

Nessa parte, cada página do seu site estará listada, e assim que você clicar, você pode ver as seções que estão sendo utilizadas.

![](https://prismic-io.s3.amazonaws.com/tavanoblog/4e0e9aac-b71b-4a9d-b05c-5f5866db1ff4_Screenshot+from+2023-01-02+23-47-36.png)

Dessa forma, fica fácil para uma pessoa não técnica conseguir criar novas páginas e adicionar/editar as seções.

Mas para entender como criar um modelo de seção, vamos para a terceira etapa.

## Terceira Etapa - Integração do Código com a deco.cx

Como eu tinha o objetivo de tornar as seções da página editáveis, eu precisei entender como isso deveria ser escrito no código.

E é tão simples, quanto tipagem em Typescript, literalmente.

Dentro da estrutura no GitHub, temos uma pasta chamada _sections_, e cada arquivo _.tsx_ lá dentro se tornará uma daquelas seções no painel.

![](https://images.prismic.io/tavanoblog/86021ef8-4a16-4256-be35-f4b6edb57ae5_Screenshot+from+2023-01-02+23-59-21.png?auto=compress,format)

Em cada arquivo, deve ser exportado uma função default, que retorna um código HTML.

Dentro desse HTML, podemos utilizar dados que vem do painel, e para definir quais dados deverão vir de lá, fazemos dessa forma:

export interface Props {
  image: LiveImage;
  imageMobile: LiveImage;
  altText: string;
  title: string;
  subTitle: string;
}

Esses são os campos que configurei para a seção _Banner_, e o resultado é esse no painel:

![](https://images.prismic.io/tavanoblog/485b3680-82af-4c06-9a27-d3c1cde28404_Screenshot+from+2023-01-03+00-19-45.png?auto=compress,format)

Depois recebi esses dados como Props, assim:

export default function Banner({ image, imageMobile, altText, subTitle, title }: Props,) {
  return (
    <>
      //Your HTML code here
    </>
  );
}

E o resultado final da seção é:

![](https://images.prismic.io/tavanoblog/b0db1859-a120-49ba-8831-e0ef78034f4d_Screenshot+from+2023-01-03+00-07-08.png?auto=compress,format)

### Dev Mode

É importante ressaltar, que durante o desenvolvimento, a ferramenta oferece uma função "Dev Mode".

Isso faz com que os campos editáveis do painel se baseiem no código feito no localhost e não do repositório no Github.

Garantindo a possibilidade de testes durante a criação.

## Resultado Final + Conclusão

O resultado final, pode ser conferido em: [https://deno-land.deco.site/](https://deno-land.deco.site/)

Consegui atingir nota 97 no Pagespeed Mobile e isso me impressionou bastante.

Particularmente, gostei muito dos pilares que a deco.cx está buscando entregar, em especial a autonomia de edição e o foco na velocidade de carregamento.

A ferramenta é nova e já entrega muita coisa legal. A realização desse desafio foi feita após 3 meses do início do desenvolvimento da plataforma da deco.

Minha recomendação a todos é que entrem na [Comunidade no Discord](https://discord.gg/RZkvt5AE) e acompanhem as novidades para não ficar para trás.

Se possível, criem um site na ferramenta e façam os seus próprios testes.
