# Fluxo — Monitoramento Inteligente de Estações

**FIAP | Global Solution 2026/2 — CitizenTech**  
Disruptive Architectures: IoT, IoB & Generative IA

## Integrantes

| Nome completo            | RM     |
|--------------------------|--------|
| Mateus Ribeiro Azevedo   | 566630 |
| Paulo Gustavo Moraes     | 568580 |
| Luana Alves de Oliveira  | 566621 |
| Isabely Marques da Silva | 566663 |


## 1. Identificação do problema e proposta CitizenTech

A superlotação nas estações de metrô das grandes cidades compromete a segurança, o conforto e a eficiência do transporte público, afetando diretamente a qualidade de vida dos passageiros.

O **Fluxo** propõe um sistema inteligente de monitoramento da ocupação das estações, utilizando sensores para contabilizar a entrada e a saída de passageiros. Os dados gerados permitem identificar situações de ocupação elevada e apoiar os controladores na tomada de decisões, como avaliar o reforço de composições, a redução dos intervalos entre trens e o controle de acesso às estações.

A solução busca contribuir para uma mobilidade urbana mais segura, eficiente e atrativa, reduzindo os impactos da superlotação no cotidiano dos cidadãos. Futuramente, o armazenamento de históricos poderá auxiliar na identificação de horários de pico e na previsão de demanda.

## 2. Desenvolvimento do protótipo

O protótipo foi desenvolvido no Tinkercad, utilizando Arduino Uno e dois sensores ultrassônicos. Um sensor representa a entrada da estação e o outro representa a saída.

Quando um objeto é detectado, o Arduino registra uma entrada ou saída. Uma nova detecção no mesmo sensor só é permitida após o objeto se afastar, evitando contagens repetidas durante uma passagem.

A capacidade de referência foi definida em 10 pessoas. O percentual de ocupação é calculado pela relação entre a quantidade atual de pessoas e essa capacidade.

| Ocupação | Indicador | Situação |
| --- | --- | --- |
| Abaixo de 70% | 🟢 LED verde | Normal |
| De 70% até 90% | 🟡 LED amarelo | Elevada |
| A partir de 90% | 🔴 LED vermelho | Crítica |

O Monitor Serial apresenta a quantidade de pessoas, o percentual de ocupação, a situação atual e, em caso de ocupação crítica, uma recomendação de aumento da frequência dos trens. A contagem pode ultrapassar a capacidade para representar situações de excesso de ocupação.
