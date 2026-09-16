# LaunchGuard

### Sistema de Telemetria da Nave Espacial

Projeto em Python que analisa dados de telemetria e verifica se uma nave está segura para decolar.

# Explicação do Projeto

Neste projeto, desenvolvemos um programa em Python para simular a verificação das condições de segurança de uma nave antes da decolagem.

A ideia foi criar um sistema que recebe informações importantes da nave, como temperatura, pressão dos tanques, nível da bateria, integridade estrutural e situação dos módulos principais. Depois de receber esses dados, o programa realiza uma análise para verificar se os valores estão dentro dos limites seguros definidos para a simulação.

Se todos os parâmetros estiverem adequados e os módulos estiverem funcionando corretamente, o sistema exibe a mensagem:

**PRONTO PARA DECOLAR**

Por outro lado, se algum valor estiver fora do limite estabelecido ou algum módulo apresentar falha, o programa exibe:

**DECOLAGEM ABORTADA**

Além da verificação de segurança, também adicionamos uma etapa de análise energética. Nela, o programa calcula a quantidade de energia disponível no início da operação, o consumo previsto durante a decolagem, as perdas de energia e a quantidade de energia restante ao final.

A proposta deste projeto é aplicar conceitos de programação em Python em um cenário de simulação, trabalhando com entrada de dados, variáveis, condições, operadores lógicos e cálculos matemáticos.

Este é um projeto de estudo. Os valores de temperatura, pressão e energia foram definidos exclusivamente para a simulação e não representam dados reais, limites operacionais ou especificações técnicas de uma nave espacial.

# Limites de segurança utilizados

- Temperatura interna: 15 °C a 26,5 °C
- Temperatura externa: 15 °C a 25 °C
- Integridade estrutural: igual a 1
- Carga da bateria: 80% a 100%
- Energia restante: mínimo de 50 kWh
- Pressão do hélio: 280 a 320 bar
- Pressão do combustível: 24 a 26 bar
- Pressão do comburente: 24 a 26 bar
- Módulos críticos: todos devem estar em "ok"

# Análise energética

Para a simulação, foi considerada uma capacidade total de 100 kWh e uma carga inicial de 90%.

Energia inicial:

100 x 90 / 100 = 90 kWh

Após o consumo estimado de 20 kWh:

90 - 20 = 70 kWh

Considerando uma perda energética de 10%:

70 x 10 / 100 = 7 kWh

Energia restante:

70 - 7 = 63 kWh

Portanto, na simulação realizada, a nave termina a etapa de decolagem com 63 kWh de energia restante.

# Como executar

1. Abra o arquivo `Projeto Launchguard.ipynb`.
2. Execute as células do notebook.
3. Informe os valores solicitados pelo programa.
4. O sistema realizará os cálculos de energia e verificará os parâmetros de segurança.
5. Ao final, será exibido `PRONTO PARA DECOLAR` ou `DECOLAGEM ABORTADA`.

Os valores utilizados no projeto são de uma simulação acadêmica e não representam parâmetros reais de uma nave espacial.

# Análise Assistida por Inteligência Artificial

A Inteligência Artificial foi utilizada como ferramenta de apoio à análise dos dados de telemetria da nave. Os parâmetros são classificados de acordo com as condições definidas no projeto, permitindo identificar possíveis anomalias e riscos operacionais.

Na simulação analisada, os dados de temperatura, integridade estrutural, pressões dos tanques, energia e módulos críticos foram verificados. A análise também considerou a energia restante de 63 kWh após o consumo estimado e as perdas energéticas. 

Possíveis anomalias incluem temperaturas ou pressões fora das faixas estabelecidas, falha estrutural, nível de energia inadequado ou falha em algum dos módulos críticos.

A IA atua como ferramenta de apoio à identificação de padrões e possíveis anomalias. A decisão operacional permanece baseada nos critérios de segurança definidos pelo sistema e na supervisão humana.


# O que o programa verifica

No programa, verificamos os seguintes dados:

- Temperatura interna da nave
- Temperatura externa
- Integridade estrutural
- Pressão do tanque de hélio
- Pressão do tanque de combustível
- Pressão do tanque de comburente
- Capacidade total da bateria
- Carga atual da bateria
- Consumo estimado durante a decolagem
- Perda energética
    
- Status do módulo de propulsão
- Status do módulo de navegação
- Status do módulo de energia
- Status do módulo de separação
    

# Cálculo da energia

Para calcular a energia da nave, usamos quatro etapas:

1. Calcular a energia inicial de acordo com a capacidade total e a porcentagem de carga.
    
2. Retirar o consumo estimado para a decolagem.
    
3. Calcular a perda energética.
    
4. Mostrar a energia que restou.
    

As fórmulas usadas foram:

energia_inicial = capacidade_total * (carga_atual / 100) 

energia_apos_consumo = energia_inicial - consumo_decolagem 

perda = energia_apos_consumo * (perda_energetica / 100) 

energia_restante = energia_apos_consumo - perda

# Evidências da execução

# Simulação normal

Com os parâmetros dentro dos limites definidos, o sistema apresentou:

**PRONTO PARA DECOLAR**

[imagem da execução]

### Simulação com anomalia

Foi realizada uma segunda simulação com a temperatura externa em 30 °C, acima do limite operacional definido. O sistema identificou a condição e apresentou:

**DECOLAGEM ABORTADA**

[imagem da execução]