# Relatório de Análise do HTML/CSS: Riot Games

Created by: Romero Antonio Ramos de Mendonça
Created time: October 6, 2023 1:42 AM
Tags: Product

# Relatório de Análise do HTML/CSS: Riot Games

[Home](https://www.riotgames.com/pt-br)

## Breakpoints

### Principais

1. Telas com largura de até 960 pixels (Celular)
2. Telas com largura de até 1280 pixels (Tablet)
3. Telas com largura acima de 1280 pixels (Notebook)

### Grandes Secções

1. Barra de navegação (.riot-bar)
    1. Composto por 3 divs:
        1. Logo: está mais à esquerda, ocupando o mínimo de espaço possível
        2. Acesso a outras páginas (Quem Somos, Trabalhe Conosco, Notícias): Está mais ao centro, ocupando todo o espaço máximo (talvez o único que tenha a propriedade “flex:1”) possível, como seus filhos alinhados a esquerda.
        3. Barra de Pesquisa + Botão Login: Mais à direita, ocupando o mínimo de espaço possível.
    2. Quando a largura da tela é reduzido (abaixo de 1024px), a segunda e a terceira divs são ocultadas e substituídas por um ícone de sanduíche.
2. Secção Inicial (.hero-new)
    1. Composto duas divs:
        1. Imagem de background, que sofre um recorte quando a largura da tela é menor que 960px
        2. Conteúdo: composto pela logo do destaque, mais o título, uma breve descrição e um botão de ação
    2. A segunda div está sobreposta à primeira, e seu conteúdo está alinha a esquerdas.
    3. Quando a largura da tela é menor que 960px, a descrição é ocultada
3. Secção Novidades (.whats-happening)
    1. Composto por duas divs:
        1. Título + Botão de ação: Ambos na mesma coluna com um espaçamento entre eles (justify-content: space-between)
        2. Conteudo:
            1. Imagem + Título sobrepondo-a: ocupando cerca de 3/5 do tamanho do componente pai.
            2. Lista de cards (artigos, notícias, etc.): Lista vertical (flex-direction: collumn) de cartões compostos por um título, uma tag relacionada e uma imagem
    2. Quando a largura da tela é menor que 1280px, a segunda div que antes era organizada num linha (flex-direction: row) é transformada em uma coluna (flex-direction: collumn) e a lista de cards, que anteriormente estava configurada como um display flexível (display: flex, flex-direction: columns), será configurando como um grid (display: grid) compostos por duas colunas. A imagem que também aparecia dentro de cada cartão da lista é substituída por um sutil ícone posicionar no canto superior direito do componente.
    3. Quando a largura da tela é menor que 960px o conteúdo ainda continua formatado como uma coluna. Entretanto a lista de cards volta a ser configurada como um display flexível, mas dessa vez como uma coluna (display: flex, flex-direction: collumn). A imagem do card também volta a ser visível. O botão de ação que antes ficava junto ao título da seção na parte superior, é transferido para a parte inferior da secção. 
4. Secção Jogos (.our-games)
    1. Composto por duas divs:
        1. Título: Alinhado a direita
        2. Lista de Cards de jogos: com display configurado como grid, com seus item centralizados (display: grid). Quando a largura da tela é menor que 960px, a lista é alterada par um display flexivel centralizado (display: flex, justify-content: center).
5. Secção Esports (.our-games)
    1. Composto por duas divs:
        1. Título: Alinhado a direita
        2. Lista de Cards de Campeonatos: com display configurado como grid, com seus item centralizados (display: grid). Quando a largura da tela é menor que 960px, a lista é alterada par um display flexível centralizado (display: flex, justify-content: center).
6. Secção Entretenimento (.our-games)
    1. Composto por duas divs:
        1. Título: Alinhado a direita
        2. Lista de Cards de Conteúdos de Entretenimento: com display configurado como grid, com seus item centralizados (display: grid). Quando a largura da tela é menor que 960px, a lista é alterada par um display flexível centralizado (display: flex, justify-content: center).
7. Secção Riot Forge (.product-carousel)
    1. Composto por duas divs:
        1. Título: Alinhado a direita
        2. Lista de Cards de Jogos: organizados em formato de carrossel, deixando 3 cards visíveis por página do carrossel. Quando a largura da tela é menor que 960px, apenas 1 card é exibido por vez.
8. Secção Carreiras (.careers)
    1. Composto por duas divs:
        1. Conteúdo informativo (Textos, Vagas Abertas, Escritórios, Botão de ação ): Alinhado a direito, sob um fundo branco.
        2. Imagem ilustrativa de algum jogo. 
        3. Secção com itens organizados no eixo horizontal (display: flex, flex-direction: row). Quando a largura da tela é menor que 960px, a secção tem seus itens organizados na vertical (flex-direction: collumn). O Elemento da primeira div são centralizado dentro do componente pai
9. Rodapé (.footer)
    1. Composto por três divs:
        1. Logo da Riot: mais à esquerda, ocupando o mínimo de espaco possível
        2. Links de acesso a outras páginas: mais ao centro, ocupando o máximo de espaço possível, no formato de um grid (display: grid)
        3. Links de redes sociais: mais a direita, com um pequeno espaçamento entre seus filhos
    2. Quando a largura da tela é diminuída para um valor menor que 960px, o rodapé tem seu eixo principal alterado para o eixo vertical (flex-direction: collumn). E quando a largura for menor que 550px, A lista de links terá seu eixo vertical definido num container flexível (display: flex, flex-direction: row, justify-content: center)