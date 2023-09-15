# Loja-Desing-Patterns

### Desing Patterns✨


<span style="color:red">Texto com cor vermelha</span>.

<font color=\"red\">**Problema 1 →**</font> Uma classe a qual nunca vai parar de crescer e com isso terá muitos if/else, switch/case e por este motivo dificultará a manutenção dessa classe. Cenário: Uma determina regra de negócio, só que varia de acordo com algum parâmetro.

Solução → Utilizado o padrão de projeto strategy, qual a ideia é sempre que existir um algoritmo seja qual for seu tipo e o mesmo apenas varia de acordo com o parâmetro, gera uma sequencia de if/else, com o strategy em vez do parâmetro ser uma String, um Enum pode ser uma própria classe a qual pode usufruir de alguns recursos como polimorfismo, interface para diminuir esse trecho de código repetitivo e fazer com que cada classe tenha sua implementação especifica. 
Objetivo do strategy → Deixar o código mais coeso, pois cada classe tem sua estratégia especifica e  uma não conhece a  outra.
