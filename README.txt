O código do repositório pode ser dividido em 2 partes:

#API para obter dados de estações climáticas

Foram importados o módulo get da biblioteca requests e a biblioteca json. Em seguida, foi criada uma variável chamada weather com o link da página da internet em que iremos utilizar para pegar os dados desejados. Criamos uma variável (station_id) com o id da estação mais próxima, que é da Universidade Federal de Santa Catarina (UFSC), e com a página e o id em mãos, utilizamos as duas bibliotecas para pegar o valor da temperatura da estação desejada. Por fim, utilizamos a função print para mostrar o valor, e rodando o código no terminal, conseguimos obtê-lo.

#Utilização da câmera conectada na Raspberry

Foram importados os módulos pprint da biblioteca pprint, PiCamera e Color da picamera, e a biblioteca time. Em seguida, foi criado uma variável chamada camera para inicializar a câmera, e em seguida foram ajustados os atributos rotation e framerate e o valor de alpha. Em seguida, ajustamos o brilho e mudamos as cores da imagem resgistradas (com o argumento colorswap). Como solicitado, anotamos o número USP de um dos integrantes do grupo na imagem. Em seguida, foi colocado um timer de 5 segundos do momento em que o código é rodado, até o momento em que a foto é tirada, e colocamos o nome e local em que a mesma será salva. Em seguida, foi colocado um timer de 10 segundos, entre a foto e o momento em que se inicia a gravação do vídeo, que dura 5 segundos, com a utilização de outro timer. E, mais uma vez, colocomaos o nome e o local em que ela será salva.
