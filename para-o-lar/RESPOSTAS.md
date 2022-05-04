# Respostas

Pesquise sobre os níveis de maturidade de Richardsson e responda:

1. Qual nivel de maturidade corresponde ao CRUD (Create, Read, Update, Delete)?

   API REST Maturidade 2 - a API fica muito mais legível para manutenções, reduzindo seu custo e passando ser mais fácil de ser consumida. Um detalhe interessante é que no nível 1 já usamos os verbos HTTP de forma correta.

2. Qual a relação entre os metodos HTTP e o CRUD?

    Hoje a estrutura do REST é baseada no protocolo HTTPe, consequentemente, nos verbos do HTTP: POST, GET, PUT E DELETE. É comum desenvolvedores implementarem esses verbos mapeando-os em termos CRUD - CREATE, READ, UPDATE E DELETE.
    

3. O que é HATEOAS? Ele é obrigatório para que uma API seja considerada RESTfull?

   HATEOAS(Hypertext As Teh Engine Of Application State) - Nível 3 - Controles HiperMídia.
   Ele é uma pré-condição do RESTfull.

   (RestFull é o estado mais alto do REST. Ela precisa atentes no mínimo os quatro níveis de maturidade teorizado por Leonard Richardson.)

   Uma API que implementa esse nível fornece aos seus clientes links que indicarão como poderá ser feita a navegação entre seus recursos. Ou seja, quem for consumir a API precisará saber apenas a rota principal e a resposta dessa requisição terá todas as demais rotas possíveis.

4. O que quer dizer quando dizemos que uma API é indepotente?

   A idempotência é a propriedade que algumas operações têm de poderem ser aplicadas várias vezes sem que o valor do resultado se altere após a aplicação inicial. — Wikipedia

   Um método HTTP idempotente é um método HTTP que pode ser chamado muitas vezes sem resultados diferentes. Não importa se o método é chamado apenas uma vez ou dez vezes. O resultado deve ser o mesmo. Essencialmente, significa que o resultado de uma solicitação executada com sucesso é independente do número de vezes que ela é executada. Por exemplo, na aritmética, adicionar zero a um número é uma operação idempotente. — W3C

   Quando falamos em idempotência em API’s REST, podemos concluir que os seguintes os verbos:

   GET, PUT, DELETE, HEAD e OPTIONS são idempotentes.
   POST não é idempotente. 
   
   Uma pequena observação aqui, gostaria de citar sobre métodos seguros e não seguros, seguros são aqueles que não alteram o estado da aplicação e não seguros que podem alterar.


5. Qual a diferença entre os métodos PUT e PATCH?

    PUT é um método de modificação de recurso onde o cliente envia dados que atualizam todo o recurso. PUT é semelhante ao POST no sentido de que pode criar recursos, mas o faz quando há uma URL definida em que PUT substitui todo o recurso, se existir, ou cria novos, se não existir.

    Ao contrário da Solicitação PUT, PATCH faz atualização parcial, por exemplo, Campos que precisam ser atualizados pelo cliente, apenas esse campo é atualizado sem modificar o outro campo.