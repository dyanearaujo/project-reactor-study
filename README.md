# Project Reactor Study
Learning about reactive programming.

<h2>Reactive Streams</h2>

* Trabalhando com Reactive Streams que implementa 4 interfaces e quem está provendo essa implementações, precisa que o código seja:

1. Assíncrona - Asynchronous 

* Permite que você continue com a execução do seu programa na thread principal enquanto uma tarefa de longa duração é executada na sua própria thread separadamente da thread principal.

2. Não Bloqueante - Non-blocking 

* É a capacidade de fazer operações de entrada e saída (acessar sistema de arquivos, banco de dados, rede, servidores, etc.) sem que a aplicação fique impedida de executar outras coisas em paralelo.

3. Contrapressão - Backpressure

* Define como regular a transmissão de elementos de fluxo. Em outras palavras, controle quantos elementos o destinatário pode consumir.

<h3>Trabalha com Emissão de Eventos</h3>

1. Publisher - Responsável por emitir os eventos. Ele somente emite se alguém dê Subscriber nele, e então é criado o Subscription após alguém dar o Subscriber. O Publisher chama o Subscriber pelo onNext e é executado até que algumas das chamadas seguintes são executadas, como por exemplo o Publisher enviar todos os objetos gerando Backpressure gerando o onComplete ou quando gera algum erro e é gerando OnError e tanto em um como no outro o Subscriber e Subscription são cancelados.

2. Subscriber 

3. Subscription - É enviado pelo Publisher através do onSubscribe. Ele consegue gerenciar a requisição, informando por exemplo a quantidade de elementos que ele deseja. Ele gerencia o Backpressure

<hr/>

<h4>Mono</h4>

* Mono significa que você tem um objeto ou não tem nada, mono ou void.

<h4>Consumer</h4>

* Consumer é possibilidade de executar uma ação no momento da Subscribe.

<h4>Fallback to Errors</h4>

* Plano B para resume e return sobre erros.

<h4>Flux</h4>

* Flux significa que você tem um objeto ou N objetos, mono ou vários.

<h4>Backpressure</h4>

* Criação de Backpressure por interface ou abstract.

