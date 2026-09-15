# Launchguard
Projeto em Python que analisa dados de telemetria e verifica se uma nave está segura para decolar.

# Sistema de Telemetria da Nave Espacial

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

## O que o programa verifica

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
    
## Limites usados no projeto

Temperatura interna - Entre 15 °C e 26,5 °C

Temperatura externa - Entre 15 °C e 25 °C

Integridade estrutural - Deve ser igual a 1

Carga da bateria - Entre 80% e 100%

Energia restante - Deve ser maior ou igual a 50 kWh

Pressão do hélio - Entre 280 e 320 bar

Pressão do combustível - Entre 24 e 26 bar

Pressão do comburente - Entre 24 e 26 bar

Módulos críticos - Todos devem estar como ok

## Cálculo da energia

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

## Exemplo de cálculo

Consideramos uma bateria com capacidade total de 100 kWh e carga atual de 90%.

Capacidade total: 100 kWh 
Carga atual: 90% 
Energia inicial: 90 kWh 

Consumo na decolagem: 20 kWh 

Energia após o consumo: 70 kWh 

Perda energética: 10% 

Perda: 7 kWh 

Energia restante: 63 kWh`

Nesse exemplo, a nave termina com 63 kWh de energia. Como esse valor é maior que 50 kWh, a energia está dentro do limite definido no projeto.
