# Loja-Desing-Patterns

## Desing Patterns✨

### Problema 1

:red_circle:**Problema→**Uma classe a qual nunca vai parar de crescer e com isso terá muitos if/else, switch/case e por este motivo dificultará a manutenção dessa classe. Cenário: Uma determina regra de negócio, só que varia de acordo com algum parâmetro.

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto strategy, qual a ideia é sempre que existir um algoritmo seja qual for seu tipo e o mesmo apenas varia de acordo com o parâmetro, gera uma sequencia de if/else, com o strategy em vez do parâmetro ser uma String, um Enum pode ser uma própria classe a qual pode usufruir de alguns recursos como polimorfismo, interface para diminuir esse trecho de código repetitivo e fazer com que cada classe tenha sua implementação especifica.

:information_source:**Objetivo do strategy →** Deixar o código mais coeso, pois cada classe tem sua estratégia especifica e  uma não conhece a  outra.

:red_circle:**Problema 2 →** Cenário parecido com o primeiro, mas com a diferença de que não sabemos qual das inúmeras regra iremos aplicar, o sistema pode se utilizar ou parar em qualquer uma delas. Existe uma complexidade maior no que se deve ser feito pelo algoritmo além dos if/else. Como não sabemos qual é a regra a ser utilizada, não conseguimos utilizar o strategy pois ele depende de quando sabemos qual parâmetro a ser utilizado para aplicar a regra em especifico.

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto **Chain of Responsibility**, aplicamos uma cadeia de chamada das regras, como não sabemos qual vai ser aplicada. Realizamos essa cadeia de chamada para verificação e no final se nenhuma dela for aplicadas retornamos que não teve nenhum retorno. Assim solucionamos o problema de não saber qual regra vai ser aplicada.

:information_source:**Objetivo do Chain of Responsibility →** Deixar o código mais coeso, e facilitar a manutenção código por meio da cadeia de chamadas que realizamos com o mesmo. Pois assim se surgir uma nova regra apenas adicionamos ela na cadeia para ser validade juntamente a outras. Devemos levar em consideração que se utilizarmos esse padrão, por causa da cadeia uma regra irá conhecer a outra por consequência.
