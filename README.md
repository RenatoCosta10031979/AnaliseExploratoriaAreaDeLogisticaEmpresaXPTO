# Análise e Exploração de Dados Descritiva: Eficiência e Reestruturação Logística no Distrito Federal

## Descrição do Projeto
Este projeto tem como objetivo otimizar as operações logísticas da empresa fictícia XPTO, que atua no Distrito Federal. Através da análise de dados, o projeto visa melhorar a distribuição de veículos, analisar o impacto geográfico nas entregas, reestruturar hubs e ajustar a capacidade da frota, visando aumentar a eficiência operacional e a satisfação do cliente.

## Dicionário de Dados

- **empresa XPTO**: Empresa fictícia de logística no Distrito Federal.
- **name**: Nome único da instância.
- **region**: Nome da região do hub.
- **origin**: Latitude e longitude da região do hub.
- **vehicle_capacity**: Capacidade de carga dos veículos no hub.
- **deliveries**: Lista de entregas a serem realizadas.
  - **id**: ID único da entrega.
  - **point**: Latitude e longitude da entrega.
  - **size**: Tamanho ou carga ocupada pela entrega no veículo.

## Objetivos
- Otimizar as operações logísticas da XPTO no Distrito Federal.
- Melhorar a distribuição de veículos nas regiões (df-0, df-1, df-2).
- Analisar o impacto geográfico nas entregas, especialmente na região df-0 (vermelha).
- Ajustar a capacidade e quantidade de veículos para melhorar a eficiência e satisfação do cliente.

## Perguntas de Negócio
- Como podemos otimizar a distribuição dos veículos entre as três regiões para melhorar a eficiência das entregas?
- Qual o impacto da dispersão geográfica das entregas na eficiência operacional?
- Como podemos ajustar a capacidade dos veículos para melhor atender às demandas variáveis?

## Instalação de Pacotes

```pip install --upgrade pandera typeguard geopandas```

## Instalação de Bibliotecas
- import geopy
- from geopy.geocoders import Nominatim
- import json
- import pandas as pd
- from google.colab import drive
- import gdown
- import numpy as np
- import os
- import pandera as pa
- import warnings
- from geopy.extra.rate_limiter import RateLimiter
- import geopandas as gpd
- import matplotlib.pyplot as plt

## ETL (Extract, Transform, Load)

O processo de ETL envolve a extração dos dados de diferentes fontes, sua transformação para garantir a qualidade e integridade, e, por fim, o carregamento em um repositório ou sistema adequado para análise. Abaixo, detalhamos a etapa de pré-análise e transformação dos dados.

## Pré-Análise

Essa etapa de pré-análise permite identificar e tratar problemas como valores ausentes, inconsistências ou dados duplicados, assegurando a confiabilidade e integridade dos dados. Além disso, a pré-análise auxilia na seleção das variáveis mais relevantes para a análise subsequente.

### Atividades na Pré-Análise:

- Visualização inicial dos dados;
- Avaliação das possíveis abordagens para análise;
- Identificação e escolha das colunas importantes para a análise;
- Verificação de colunas duplicadas;
- Tratamento de valores duplicados;
- Identificação e tratamento de valores nulos;
- Verificação e tratamento de valores únicos (ou com pouca variabilidade);
- Identificação e correção de inconsistências nos dados;
- Renomeação de colunas (quando necessário);
- Ajuste dos tipos de dados, garantindo que estejam no formato adequado.

## Transformação

Após selecionar as colunas importantes, o objetivo nesta etapa é garantir a qualidade e a integridade dos dados do DataFrame. Essas verificações ajudam a identificar e tratar problemas que poderiam comprometer futuras análises e tomadas de decisão.

### Atividades na Transformação:

- Verificação e tratamento de colunas duplicadas;
- Tratamento de valores únicos (observações com baixa variabilidade);
- Tratamento de valores duplicados;
- Identificação e correção de inconsistências;
- Tratamento de valores nulos;
- Tradução ou renomeação de colunas (se necessário);
- Conversão dos tipos de dados para os formatos adequados;
- Garantia da qualidade e integridade final dos dados.


## Exploração de Dados

- **Coleta de Dados**: Os dados foram coletados a partir de um arquivo JSON contendo informações sobre entregas.
  
- **Conversão de JSON para DataFrame**: Transformação dos dados do JSON em um DataFrame utilizando `pd.DataFrame`.
  
- **Wrangling**: Normalização e estruturação dos dados, incluindo operações como `flatten` e `explode`.
  
- **Geocodificação**: Enriquecimento dos dados com informações geográficas através da geocodificação reversa usando a API Nominatim do OpenStreetMap.


## Visualização

- **Utilização** do Geopandas** para visualizar as coordenadas dos hubs e das entregas no mapa do Distrito Federal.

## Resultados e Conclusões

Após a análise e exploração dos dados, foram gerados insights valiosos sobre a distribuição de veículos e o impacto geográfico nas entregas. As sugestões para reestruturação dos hubs e ajustes na frota prometem melhorias significativas na eficiência logística da empresa fictícia XPTO.

## Considerações Finais

Este projeto exemplifica como a análise de dados pode ser utilizada para otimizar operações logísticas. As técnicas e ferramentas empregadas, como Pandas, Geopandas e geocodificação reversa, são essenciais para transformar dados brutos em insights acionáveis.

## Links da Documentação

- [Geopy](https://geopy.readthedocs.io/)
- [Nominatim (Geopy Geocoders)](https://geopy.readthedocs.io/en/stable/#nominatim)
- [JSON (Módulo Padrão do Python)](https://docs.python.org/3/library/json.html)
- [Pandas](http://pandas.pydata.org/docs/)
- [Google Colab](https://colab.research.google.com/notebooks/)
- [Gdown](https://pypi.org/project/gdown/)
- [NumPy](https://numpy.org/doc/)
- [OS (Módulo Padrão do Python)](https://docs.python.org/3/library/os.html)
- [Pandera](https://pandera.readthedocs.io/)
- [Warnings (Módulo Padrão do Python)](https://docs.python.org/3/library/warnings.html)
- [RateLimiter (Geopy Extra)](https://geopy.readthedocs.io/en/stable/#module-geopy.extra.rate_limiter)
- [Geopandas](https://geopandas.org/)
- [Matplotlib](https://matplotlib.org/stable/contents.html)



