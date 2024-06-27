⏱💰 Agilizando nossas análises com 'Gridspec'


A classe GridSpec da biblioteca Matplotlib é uma excelente opção para termos em nosso arcabouço de ferramentas. Com ela podemos criar layouts complexos de gráficos em apenas uma figura.


Exemplo prático:


Imagine uma situação de nosso cotidiano onde precisamos de um relatório detalhado para uma reunião com investidores. No relatório, apresentamos uma visão da performance das ações de uma empresa ao longo dos últimos anos, analisando diversos aspectos como cotação de fechamento, volume de transações, e tendências médias.


Precisamos analisar os dados históricos das ações de uma empresa, neste caso WEG S.A. e apresentar:


- A cotação de fechamento das ações.

- O volume de transações diárias, ajustado para milhões.

- A cotação de fechamento comparada com a média móvel de 30 dias para identificar tendências.


Solução com GridSpec


Utilizando GridSpec, podemos criar um layout organizado em uma única figura, combinando subplots de diferentes tamanhos e ajustar suas posições conforme cada necessidade.


Neste código temos como exemplo os dados históricos das ações de 'WEG S.A.', exibindo a cotação de fechamento, o volume de transações e a combinação da cotação de fechamento com a média móvel de 30 dias.


O volume de transações foi ajustado para milhões e teve seus outliers limitados. Para isso, utilizamos um parâmetro opcional 'upper_quantile', que calcula o limite superior utilizando o método '.quantile()' do Pandas para obter o valor no percentil especificado. Em seguida, utilizamos o método '.clip()' para limitar os valores da série até o limite superior calculado, garantindo que não haja valores fora do padrão devido aos 'outliers', o que pode se tornar distrações quando estivermos analisando os gráficos.
