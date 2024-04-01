# TrabalhoJogoDaVida

## Introdução
Este é um projeto criado para a matéria Algoritmos e Estruturas de Dados I pelo professor Michel Pires Da Silva do curso de engenharia de computação do CEFET de Divinópolis.
Neste projeto, implementamos uma versão do Jogo da Vida em C++. O objetivo é criar um programa que simule a evolução de um tabuleiro bidimensional de células, onde cada célula pode estar viva ou morta. O estado futuro de cada célula depende do estado atual do tabuleiro e de algumas regras simples.

## Implementação

Para implementar o Jogo da Vida, seguimos as seguintes etapas:

1 - Criamos uma matriz N x N para representar o tabuleiro do Jogo da Vida.

2 - Inicializamos o tabuleiro com células vivas (1) e mortas (0) aleatoriamente.

3 - Implementamos uma função para exibir o estado atual do tabuleiro.

4 - Implementamos uma função para produzir um relatório de execução, guardando o histórico da evolução do jogo em arquivo.

5 - Implementamos uma função para calcular a próxima geração do Jogo da Vida com base nas regras estabelecidas.

6 - Executamos várias gerações do jogo e mostramos o estado do tabuleiro após cada geração.

## Explicando o código

### Funções

- #### JogoDaVida::JogoDaVida():
Este é o construtor da classe JogoDaVida. Ele não faz nada além de inicializar um objeto da classe.

- #### bool checarIgualdade(int **tabuleiro, int sub_tabuleiro, int tamanho):
Esta função compara dois tabuleiros bidimensionais para verificar se eles são iguais. Ela recebe dois tabuleiros e o tamanho dos tabuleiros como entrada e retorna verdadeiro se forem iguais e falso caso contrário.

- #### int verificacao(int tabuleiro, int x, int y, int tamanho):
Esta função verifica o número de vizinhos vivos para uma célula em coordenadas (x, y) no tabuleiro. Ela retorna o número de vizinhos vivos.

- #### void JogoDaVida::mostrarTabuleiro(int tabuleiro, int tamanho):
Esta função imprime o tabuleiro bidimensional na saída padrão. Ela recebe o tabuleiro e o tamanho como entrada e imprime os valores das células do tabuleiro.

- #### void JogoDaVida::relatorio(int tabuleiro, int tamanho, ManipulandoArquivo *arquivo, string mensagem, bool transferir):
Esta função imprime um relatório na saída padrão e, opcionalmente, transfere o tabuleiro para um arquivo de saída. Ela recebe o tabuleiro, o tamanho, um objeto de manipulação de arquivo, uma mensagem para ser exibida e um indicador se o tabuleiro deve ser transferido para o arquivo de saída.

- #### void JogoDaVida::iniciarJogo(int tabuleiro, int interacao, ManipulandoArquivo *arquivo):
Esta função inicia o jogo da vida. Ela recebe o tabuleiro inicial, o número de iterações e um objeto de manipulação de arquivo. A cada iteração, ela aplica as regras do jogo para atualizar o tabuleiro e imprime um relatório.

- #### void ManipulandoArquivo::ManipulandoArquivo():
Este é o construtor da classe ManipulandoArquivo. Ele não faz nada além de inicializar um objeto da classe.

- #### void ManipulandoArquivo::setInputArquivo(string input_arquivo):
Esta função define o nome do arquivo de entrada.

- #### void ManipulandoArquivo::setOutputArquivo(string output_arquivo):
Esta função define o nome do arquivo de saída.

- #### int ManipulandoArquivo::Input():
Esta função lê o tabuleiro inicial do arquivo de entrada. Ela retorna um ponteiro para o tabuleiro lido.

- #### void ManipulandoArquivo::Output(int tabuleiro):
Esta função escreve o tabuleiro atual para o arquivo de saída.

- #### int ManipulandoArquivo::getTamanho() const:
Esta função retorna o tamanho do tabuleiro.

- #### void ManipulandoArquivo::setTamanho(int tamanho):
Esta função define o tamanho do tabuleiro.

- #### int ** ManipulandoArquivo::criarTabuleiro():
Esta função aloca dinamicamente memória para um novo tabuleiro e retorna um ponteiro para ele.

## Compilação e Execução
O projeto disponibilizado possui um arquivo Makefile que realiza o procedimento de compilação e execução.

make clean -> Apaga a última compilação realizada contida na pasta build

make -> Executa a compilação do programa utilizando o gcc, e o resultado vai para a pasta build

make run -> Executa o programa da pasta build após a realização da compilação
