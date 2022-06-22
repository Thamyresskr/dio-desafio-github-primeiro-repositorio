# Posicionando elementos com FlexBox em CSS



o FlexBox foi idealizado como modelo de layout unidimensional e como um método visa oferecer distribuição de espaço entre itens em uma interface e recursos de alinhamento.



### Flex Container

É a tag que envolve os itens, será nela que iremos aplicar a propriedade "display: flex". Transforma todos os seus itens filhos em flex itens.



Propriedades relacionadas

- display - Inicializador do container
- flex-direction - faz o direcionamento desses itens, sejá em linha ou coluna
- flex-wrap - se aplica para quebra de linha ou não.
- flex-flow - abreviação para o direction e o wrap.
- justify-content - alinha os itens do container de acordo com a sua direção.
- align-itens - alinha de acordo com o eixo do container.
- align-content - alinha as linhas desse container.

### Flex Item

São elementos filhos diretos do Flex Container. E também podem se tornar Flex Container através da propriedade display.

Propriedads relacionadas:

- flex-grow - define o fator de crescimento
- flex-basis - define o tamanho inicial antes da distribuição do espaço restante dentro do container.
- flex-shrink - define a capacidade de redução.
- flex - abreviação para o grow, basis e shrink.
- order - relacionado a ordem de distribuição e listagem desses itens.
- align-self - define o alinhamento de um item especificado do container.



### Fundamentos do FlexBox - parte 1

Display-flex - torna a tag um elemento do tipo flex container, e assim automaticamente todos os seus filhos diretos desta tag, tornam-se flex-itens.



Flex-direction - é a propriedade que estabelece o eixo principal do container definindo assim a direção que os flex-itens são colocados no flex container.

São basicamentes dois eixos:

Linha que é horizontal.

Coluna que é vertical.



Os Eixos

Começando com o primeiro eixo, que é quando a gente inicializa o container, ele vem setado como row.

row (padrão): á direção do texto, esquerda para direita.



row-reverse: sentido oposto á direção do texto. Ordenação inversa.



Column: ordenação de cima para baixo, em coluna única. Eixo vertical de coluna.



Column-reverse: ordenação inversa, de baixo para cima.



Estrutura básica do wrap

É a propriedade que define se os itens devem ou não quebrar a linha.

Por padrão eles não quebram linhas, isso faz com que os flex itens sejam compactados além do limite do conteúdo.



nowrap: é o padrão, não permite a quebra de linha.



wrap: permite a quebra de linha, assim que um dos flex itens não puder mais ser compactado.



wrap-reverse: permite a quebra de linha assim que um dos flex itens não puder mais ser compactado, porém na direção contrária da linha acima.



