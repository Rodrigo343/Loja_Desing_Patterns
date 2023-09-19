# Loja-Desing-Patterns

## Desing Patterns✨

:dart:Esse README tem como objetivo conter as informações que anoitei ao longo do curso, contendo meus entendimentos e oque consegui absorver de cada aula e de cada solução.

---
Padrões Comportamentais
---
### Problema 1

:red_circle:**Problema→**Uma classe a qual nunca vai parar de crescer e com isso terá muitos if/else, switch/case e por este motivo dificultará a manutenção dessa classe. Cenário: Uma determina regra de negócio, só que varia de acordo com algum parâmetro.

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto strategy, qual a ideia é sempre que existir um algoritmo seja qual for seu tipo e o mesmo apenas varia de acordo com o parâmetro, gera uma sequencia de if/else, com o strategy em vez do parâmetro ser uma String, um Enum pode ser uma própria classe a qual pode usufruir de alguns recursos como polimorfismo, interface para diminuir esse trecho de código repetitivo e fazer com que cada classe tenha sua implementação especifica.

:information_source:**Objetivo do strategy →** Deixar o código mais coeso, pois cada classe tem sua estratégia especifica e  uma não conhece a  outra.

---
### Problema 2

:red_circle:**Problema 2 →** Cenário parecido com o primeiro, mas com a diferença de que não sabemos qual das inúmeras regra iremos aplicar, o sistema pode se utilizar ou parar em qualquer uma delas. Existe uma complexidade maior no que se deve ser feito pelo algoritmo além dos if/else. Como não sabemos qual é a regra a ser utilizada, não conseguimos utilizar o strategy pois ele depende de quando sabemos qual parâmetro a ser utilizado para aplicar a regra em especifico.

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto **Chain of Responsibility**, aplicamos uma cadeia de chamada das regras, como não sabemos qual vai ser aplicada. Realizamos essa cadeia de chamada para verificação e no final se nenhuma dela for aplicadas retornamos que não teve nenhum retorno. Assim solucionamos o problema de não saber qual regra vai ser aplicada.

:information_source:**Objetivo do Chain of Responsibility →** Deixar o código mais coeso, e facilitar a manutenção código por meio da cadeia de chamadas que realizamos com o mesmo. Pois assim se surgir uma nova regra apenas adicionamos ela na cadeia para ser validade juntamente a outras. Devemos levar em consideração que se utilizarmos esse padrão, por causa da cadeia uma regra irá conhecer a outra por consequência.

---
### Problema 3

:red_circle:**Problema 3 →** Algumas classes que compartilham uma lógica parecida como por exemplo uma lógica para realizar uma ação. Como por exemplo varias classes que tem um if parecido o qual é responsável por uma ação se atender uma determinada condição, realiza uma ação com mesmo intuito, mudando apenas a condição para realização

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto Template Method, como o próprio nome diz um método que serve como template para as outras classes utilizarem, no método que será o template ele ficara responsável pela parte principal da lógica que se repete nas outras classes, não contendo os detalhes e delegando esses detalhes para as outras classes que irão utiliza-lo. Com esse padrão melhoramos a coesão do código e diminuindo o código duplicado.

:information_source:**Objetivo do Template Method →** Aproveitar trechos repetidos de código que mais de uma classe utiliza que mesmo que não sejam iguais mas que contenham uma parte a qual seja igual, seja ela uma condição para que algo aconteça ou algum tipo de ação necessária que seja repetido em mais de um lugar. Delegar essa parte repetitiva para uma classe só e utilizar a partir dela nas outras, diminuindo o trecho repetitivo do código e aumentando a coesão. 

---
### Problema 4

:red_circle:**Problema 4 →** Problema parecido com o primeiro cenário mas com a diferença de que agora estamos trabalhando com estados. Como por exemplo estado de uma situação de algo, como de um pedido. E precisamos melhorar isso para não fica com código duplicado, melhorar a coesão de cada funcionalidade.

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto State, o qual nos ajuda nessa questão de estado, a ir de um estado para outro. O mesmo no ajuda a implementar a regra de cada estado, como passamos por eles, a diminuir questão de código duplicado para que fique mais fácil de entender a regra de cada estado, como se interagem entre si e oque é possível ou não realizar entre eles.

:information_source:**Objetivo do State →** Melhorar a coesão do código quando implementando no cenário que temos algo que possua estados, para separa melhor funcionalidade de cada um, assim como suas interações e delimitações.

---
### Problema 5

:red_circle:**Problema 5 →** Problema onde temos uma classe que contenha as suas informações mas a utilização dessa classe se encontra no rquivo da CLI, controller ou algo do tipo, onde os dados das mesma são utilizados de formas diversas, como por exemplo, salvar as informações no banco de dados, enviar uma notificação para um e-mail que foi salvo os dados entre outras dependências de funcionalidades. Todas as funcionalidades que citei a cima tem correlação com o processo de utilização da classe mencionada

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto Command Handlers, conseguimos separa tanto as informações dessa classe que precisamos preencher em um local especifico. E além disso separamos suas ações que utilizam-se das informações dessa classe em outro local para felicitar o entendimento e melhorar a construção do código, ou seja, uma classe é responsável pelos atributos e outra pelas ações relacionadas a classe que contem os atributos.

:information_source:**Objetivo do Command Handlers →** Com esse padrão conseguimos separa as características de uma classe e a aplicação de funcionalidades que utilizam seus dados. Fazendo assim um local específicos que utilizam as informações daquela classe em especifico. Facilitando a compreensão e melhorando a coesão. Pois separamos as informações das ações realizadas com aqueles dados.

---
### Problema 6

:red_circle:**Problema 6 →** Problema onde temos uma classe que contenha ações especificas de uma funcionalidades que crescerá constantemente pois não sabemos se será necessário adicionar mais ações para aquela funcionalidade.

:heavy_check_mark:**Solução →** Utilizado o padrão de projeto Observer não precisamos chamar todas as  ações secundarias que são necessárias depois da ação principal, ou seja, nossa classe não crescerá constantemente quanto mais ações secundarias criamos. Não é mais necessário instanciar todas elas e delegar a execução da sua ação, agora as mesma ficam esperando a execução da ação principal para realizar seus papeis. Assim diminuindo o acoplamento e amentando a coesão.

:information_source:**Objetivo do Observer→** Com esse padrão conseguimos criar classes que servem de observadores/ouvintes que ficam esperando a execução de determinada ação para realizar algo. Com isso conseguimos separar essas outras ações que dependes da ação principal. Ao invés de chamar cada uma das classes que não seja principal, invertemos o controle e delegamos apenas para eles esperaram a ação principal para depois realizar seus processos.
