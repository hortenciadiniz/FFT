# FFT - Report
- Fast Fourier Transform - PDS class
- Federal University of Campina Grande
- Hortencia Diniz Dultra e Silva - 05/10/23

É uma atividade que consiste na implementação da Transformada Rápida de Fourier (FFT) por decimação no Tempo, utilizando Python e o Colaboratory para executar o código.

# Build e Execução
1. As bibliotecas 'numpy' e 'matplotlib.pyplot' para realizar cálculos e plotagem, respectivamente;

2. Foi feito um teste para saber se o numero digitado estava em potencia de dois, caso contrario, use o método "Zero Pad";

3. Dois arrays são criados e preenchidos com sequencias pares e impares do sinal

4. A frequência de amostragem "fs" foi definida como 8KHz, que é a taxa de amostragem do sinal;

5. Foi criado um vetor de tempo t usando 'np.arange' que varia de 0 a 1 segundo com uma taxa de amostragem de 1/fs. Isso cria um vetor de tempo com pontos igualmente espaçados.

6. Foram definidas as frequências f1 e f2 como 1KHz e 2KHz, respectivamente, que são as frequências das duas senoides que compõem o sinal de entrada.

7. Foi calculado o vetor de frequência 'frequencies' correspondente à FFT usando a função np.fft.fftfreq. Isso nos fornece um vetor de frequência que corresponde aos coeficientes da FFT.

8. A plotagem foi limitada para mostrar apenas os primeiros 0.004 segundos (4 períodos) do sinal.

9. Por fim, fiz a IFFT - Inverse Fast Fourier Transform - para saber se o sinal reconstruído a partir da frequência gerava o sinal de inicio.

# Exemplo de resultado

com um sinal x(t) de entrada descrito por:

$$x(t) = \sin(2 \pi 1000 t) + 0.6 \cdot \sin(2 \pi 2000 t)$$

![Resultado da FFT do sinal x(t)](./sinal_original_entrada.png "FFT Result")

o resultado da operação de FFT é

![Resultado da FFT do sinal x(t)](./FFT.png "FFT Result")

![Resultado da FFT do sinal x(t)](./FFT_TAMANHO.png "FFT Result")

**Nota:** O código ainda requer testes para outros sinais de entrada.
