# Análise do PIB Mensal Brasileiro: Ajuste pela Inflação com IPCA via API do Banco Central

Este repositório apresenta uma análise do Produto Interno Bruto (PIB) mensal do Brasil com ajuste inflacionário, convertendo valores nominais em valores reais com base no IPCA. O objetivo é possibilitar comparações mais precisas ao longo do tempo, eliminando os efeitos da inflação.

##📂 Conteúdo
pib_mensal.xls: Base de dados contendo a série histórica do PIB mensal, obtida a partir do IPEAdata.

deflator.ipynb: Notebook em Python que realiza:

Leitura e pré-processamento da série histórica do PIB;

Consulta ao IPCA mensal via API SGS do Banco Central do Brasil;

Cálculo do PIB real (valores deflacionados);

Visualizações comparativas entre PIB nominal e PIB real.

##🔗 API Utilizada
Utilizamos a API de Séries Temporais (SGS) do Banco Central do Brasil para obter os valores mensais do IPCA. O código 433 é empregado para acessar o IPCA amplo consolidado. Os dados são requisitados diretamente via JSON, garantindo atualizações automatizadas e consistência metodológica.

##📐 Cálculo do PIB Real (Deflacionamento)

O processo de deflação consiste em corrigir os valores nominais do PIB pela inflação, convertendo todos os valores para uma mesma base de comparação.
O resultado representa o valor do PIB a preços constantes, ou seja, com o mesmo poder de compra de junho/2025.

##📈 Importância da Deflação em Séries Temporais
Trabalhar com valores nominais pode gerar interpretações distorcidas, pois aumentos nos dados podem ser explicados apenas pela inflação. A deflação permite:

Comparar a evolução real da economia ao longo do tempo;

Medir o poder de compra real da produção nacional;

Identificar períodos de crescimento, estagnação ou recessão real;

Apoiar decisões econômicas e políticas públicas com base em dados consistentes.

##📊 Análise do Gráfico: PIB Nominal x PIB Real

O gráfico acima evidencia a diferença entre os valores nominais (linha azul) e reais (linha verde com marcadores) do PIB mensal:

A linha azul (PIB Nominal) apresenta crescimento contínuo, impulsionado tanto pelo aumento da atividade econômica quanto pela inflação acumulada.

A linha verde (PIB Real) mostra o comportamento do PIB ajustado, revelando:

Crescimento mais moderado;

Períodos de estagnação e retração não visíveis na série nominal;

Um desempenho mais realista da economia.

🔍 O encontro entre as duas curvas no final da série ocorre porque todos os valores foram corrigidos com base no mês de junho de 2025, ou seja, expressos no poder de compra daquele período.

