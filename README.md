# 🎶 Geração de Músicas com Algoritmos Evolutivos

Este projeto utiliza algoritmos evolutivos para gerar sequências de acordes musicais harmônicos de acordo com o tom definido (C, D, E, F, G, A ou B). O objetivo é simular, de forma simples e criativa, como técnicas de inteligência artificial podem ser aplicadas na composição musical.

## 💡 Como funciona

- Um **algoritmo evolutivo** é utilizado para gerar e otimizar sequências de acordes.
- A cada geração, os acordes são avaliados com base em um critério de fitness: a quantidade de acordes desejados para o tom escolhido.
- Quando a sequência ideal (com todos os 7 acordes esperados) é encontrada, ela é impressa no terminal e convertida em áudio.

## 🧠 Lógica do Algoritmo

- **Indivíduos**: cada indivíduo é uma sequência de 7 acordes representados por números.
- **População**: conjunto de indivíduos gerados aleatoriamente.
- **Fitness**: mede quantos acordes da sequência pertencem ao conjunto de acordes do tom escolhido.
- **Seleção, Crossover e Mutação**: são aplicados para gerar novas populações a cada geração, buscando sempre a melhoria da "qualidade musical".

## 🎼 Mapeamento de acordes

O sistema usa um conjunto fixo de acordes, que é mapeado por índices. Exemplo:

```chord_mapping = ['C', 'D', 'E', 'F', 'G', 'A', 'B', 'Dm', 'Em', ...]``` 

## 🎧 Geração de Áudio
Quando o algoritmo encontra a melhor sequência (fitness máximo), ela é:

- Convertida em uma estrutura music21
- Exportada como .midi e posteriormente em .wav com o auxílio da biblioteca pydub

## 📈 Visualização
O histórico de fitness é plotado ao longo das gerações para cada tom musical, permitindo acompanhar a evolução da qualidade das sequências.

<p align="center"> <img src="exemplo_grafico.png" alt="Exemplo de gráfico de fitness" width="500"> </p>
