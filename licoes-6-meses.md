# 6 Meses de Lojas em Produção: Um Estudo de Caso

Nos últimos seis meses acumulamos um valioso conjunto de lições ao levar lojas para produção. Nesse período, aprendemos o que deve ser evitado, o que não funciona e a melhor maneira de iniciar o desenvolvimento de uma loja online. A seguir, compartilhamos um resumo das lições que adquirimos durante essa jornada.

## Início do Desenvolvimento de uma Loja

Todos projetos criados na Deco partem de um template pré-configurado com diversos componentes, integrações e temas. Observamos que, após criar a loja, alguns desenvolvedores recorrem ao GitHub para modificar componentes e temas diretamente no código. Embora isso seja um reflexo natural do trabalho de um desenvolvedor, notamos que os projetos nos quais o desenvolvimento se concentra principalmente no CMS (Content Management System) tendem a ser concluídos mais rapidamente e com melhor desempenho.

O fluxo que descobrimos ser o ideal é o seguinte:

1. Criar o projeto.
2. Personalizar o tema, componentes, otimização de SEO, entre outros através do admin da deco.
3. Apresentar o resultado ao cliente final e coletar feedback.
4. Com base no feedback, ajustar a loja no CMS, usando as seções predefinidas e voltar ao passo 3.
6. Se o cliente estiver satisfeito, migrar o domínio para a Deco.
7. Caso seja necessário fazer alterações no código, adicionar seções específicas para o caso de uso em questão.

## A Tag `<dialog>`

Em versões anteriores de nossos templates, utilizávamos a tag HTML5 `<dialog>`. Essa tag permitia a criação de modais com suporte à acessibilidade. No entanto, identificamos dois problemas principais relacionados a ela:

1. Exigia JavaScript para funcionar corretamente, o que ia de encontro à nossa filosofia de minimizar o uso de JavaScript na página.
2. Versões recentes do iPhone (10, 11 e 12) não oferecem suporte a essa tag, o que nos forçava a inserir "polyfills". Essa inserção era síncrona e prejudicava significativamente o desempenho dos sites.

Devido a esses dois pontos mencionados, adotamos uma abordagem alternativa usando a tag `<input type="checkbox>`, que é amplamente suportada por todos os navegadores. Essa mudança resolveu ambos os problemas. Migramos nossos templates para essa técnica e observamos um aumento na compatibilidade entre nossos sites e dispositivos móveis.

Se o seu site ainda estiver usando a tag `<dialog>`, recomendamos fazer a migração o mais rápido possível para `<input type="checkbox>` para evitar incompatibilidades com iPhones. Para obter mais informações sobre essa abordagem, consulte [este link](https://daisyui.com/components/modal/#method-2-using-a-hidden-checkbox-legacy).

## Unidades absolutas

Percebemos que algumas de nossas lojas apresentavam taxas de conversão abaixo do esperado em determinados dispositivos, especialmente em iPhones e dispositivos Android. Após uma análise mais aprofundada, identificamos que o botão "Ir para o checkout" estava sendo ocultado pela barra de endereços dos navegadores Chrome e Safari em alguns desses dispositivos.

Esse problema ocorreu devido ao uso de unidades absolutas, como `vh` (viewport height) e `vw` (viewport width), em vez de unidades relativas. As unidades absolutas fazem referência ao tamanho total da tela do dispositivo, não levando em consideração a área de renderização da janela, o que pode ocultar partes da interface do usuário.

Para evitar esse tipo de problema, é fundamental evitar o uso de unidades absolutas, como `vh` e `vw`. Recomendamos revisar sua loja para garantir que essas unidades não estejam sendo usadas, especialmente no minicart.

## Flexbox e Unidades Percentuais

Outro problema que identificamos em algumas lojas diz respeito ao layout quebrado em versões mais antigas do Safari. Isso ocorre geralmente quando unidades percentuais são usadas em conjunto com flexbox. Um exemplo disso é o seguinte trecho de código:

```html
<div class="flex">
   <div class="w-full"/>
</div>
```

Nesse exemplo, estamos combinando flexbox (classe `flex`) com unidades percentuais (`width: 100%`). Isso pode funcionar em navegadores mais recentes, mas causa problemas em versões mais antigas do Safari, como o iPhone 10, 11 e 12.

Para solucionar esse problema, recomendamos substituir `w-full` por classes relacionadas ao flexbox:
 ```html
<div class="flex">
   <div class="flex-grow"/>
</div>
```

Isso garantirá que o layout funcione corretamente em todos os navegadores.


Estamos sempre acompanhando os novos projetos, coletando os apresentados e melhorando o template [Storefront](https://github.com/deco-sites/storefront).
