# Objetivo do Projeto

---

- **README.md**: Este é o arquivo principal que aparece na página inicial de um repositório GitHub e serve para fornecer uma visão geral do projeto, incluindo informações sobre o que ele faz, como configurá-lo e usá-lo, as tecnologias envolvidas e links para documentação adicional. O README.md é escrito em Markdown, o que permite uma formatação simples e a inclusão de links, imagens e outros elementos para tornar a documentação mais clara e acessível. O objetivo é criar um README.md do projeto de forma que quando um recrutador, funcionário da empresa ou um profissional da área de análise de dados o leia, eles possam entender o projeto como um todo: desde o dicionário (significado das colunas), ferramentas utilizadas (e suas funcionalidades) e links de documentação das ferramentas. O README.md deve conter informações importantes para situar o leitor ou o profissional da área de análise de dados, de modo que eles compreendam do que se trata o projeto e possam utilizá-lo de forma eficiente e otimizada. O texto deve ser objetivo, claro e didático, de modo que até mesmo um recrutador de vagas de analista de dados possa entender do que se trata o projeto, especialmente o gerente ou coordenador.

---

## **O Projeto Desenvolvido é Delimitado pela Tag <projeto></projeto>:**

Bom dia, Analista de Dados!

# **Contextualização da Tarefa**

- Você é uma persona que é expert e especialista em documentar projetos de análise de dados. Você possui 15 anos de experiência e vivência em grandes projetos de big techs. Você também possui 10 anos de experiência em desenvolver projetos e armazená-los no GitHub. Você possui altas habilidades de produzir um README.md no GitHub para o arquivo principal que aparece na página inicial de um repositório GitHub e serve para fornecer uma visão geral do projeto, incluindo informações sobre o que ele faz, como configurá-lo e usá-lo, as tecnologias envolvidas e links para documentação adicional. Tenho um projeto armazenado no GitHub, porém não tem um README.md, e preciso que você desenvolva um README.md altamente interessante, objetivo, didático, usando as boas práticas que as empresas usam no dia a dia e que esteja bem estruturado. Vou te enviar o projeto. O projeto que está no GitHub sem o README.md está delimitado pela tag <projeto></projeto>.

### **Projeto:**

**<projeto>**

1. **Análise e Exploração de Dados: Eficiência e Reestruturação Logística no Distrito Federal**

Nota: A empresa XPTO mencionada neste projeto é fictícia e utilizada apenas para fins educacionais.

2. **Dicionário**

- `empresa XPTO`: uma empresa fictícia que atua na área de logística no Distrito Federal (Brasília);
- `name`: uma string com o nome único da instância;
- `region`: uma string com o nome único da região do hub;
- `origin`: um dicionário com a latitude e longitude da região do hub;
- `vehicle_capacity`: um inteiro com a soma da capacidade de carga dos veículos do hub;
- `deliveries`: uma lista de dicionários com as entregas que devem ser realizadas;
- `id`: uma string com o id único da entrega;
- `point`: um dicionário com a latitude e longitude da entrega;
- `size`: um inteiro com o tamanho ou a carga que a entrega ocupa no veículo.

3. **Objetivos**

Otimizar as operações logísticas da empresa XPTO no Distrito Federal, através da distribuição eficiente de veículos, análise do impacto geográfico nas entregas, possível reestruturação dos hubs e ajuste da capacidade da frota à variabilidade das entregas, visando melhorar a eficiência operacional, reduzir tempos de entrega e aumentar a satisfação do cliente.

4. **Perguntas de Negócio**

- Como podemos otimizar a distribuição dos veículos entre as três regiões (df-0, df-1, df-2) para melhorar a eficiência das entregas? Qual é o impacto da dispersão geográfica das entregas, especialmente na região df-0 (vermelha), na eficiência operacional e no tempo de entrega? Como podemos ajustar a capacidade e quantidade de veículos, considerando a variação no tamanho das entregas e a densidade de entregas em cada região, para melhorar a eficiência e satisfação do cliente?

5. **Instalação de Pacotes**

```
!pip install --upgrade pandera
!pip install --upgrade typeguard
!pip3 install geopandas
```

Requirement already satisfied: pandera in /usr/local/lib/python3.10/dist-packages (0.20.3)
Requirement already satisfied: multimethod<=1.10.0 in /usr/local/lib/python3.10/dist-packages (from pandera) (1.10)
Requirement already satisfied: numpy>=1.19.0 in /usr/local/lib/python3.10/dist-packages (from pandera) (1.26.4)
Requirement already satisfied: packaging>=20.0 in /usr/local/lib/python3.10/dist-packages (from pandera) (24.1)
Requirement already satisfied: pandas>=1.2.0 in /usr/local/lib/python3.10/dist-packages (from pandera) (2.1.4)
Requirement already satisfied: pydantic in /usr/local/lib/python3.10/dist-packages (from pandera) (2.8.2)
Requirement already satisfied: typeguard in /usr/local/lib/python3.10/dist-packages (from pandera) (4.3.0)
Requirement already satisfied: typing-inspect>=0.6.0 in /usr/local/lib/python3.10/dist-packages (from pandera) (0.9.0)
Requirement already satisfied: wrapt in /usr/local/lib/python3.10/dist-packages (from pandera) (1.16.0)
Requirement already satisfied: python-dateutil>=2.8.2 in /usr/local/lib/python3.10/dist-packages (from pandas>=1.2.0->pandera) (2.8.2)
Requirement already satisfied: pytz>=2020.1 in /usr/local/lib/python3.10/dist-packages (from pandas>=1.2.0->pandera) (2024.1)
Requirement already satisfied: tzdata>=2022.1 in /usr/local/lib/python3.10/dist-packages (from pandas>=1.2.0->pandera) (2024.1)
Requirement already satisfied: mypy-extensions>=0.3.0 in /usr/local/lib/python3.10/dist-packages (from typing-inspect>=0.6.0->pandera) (1.0.0)
Requirement already satisfied: typing-extensions>=3.7.4 in /usr/local/lib/python3.10/dist-packages (from typing-inspect>=0.6.0->pandera) (4.12.2)
Requirement already satisfied: annotated-types>=0.4.0 in /usr/local/lib/python3.10/dist-packages (from pydantic->pandera) (0.7.0)
Requirement already satisfied: pydantic-core==2.20.1 in /usr/local/lib/python3.10/dist-packages (from pydantic->pandera) (2.20.1)
Requirement already satisfied: six>=1.5 in /usr/local/lib/python3.10/dist-packages (from python-dateutil>=2.8.2->pandas>=1.2.0->pandera) (1.16.0)
Requirement already satisfied: typeguard in /usr/local/lib/python3.10/dist-packages (4.3.0)
Requirement already satisfied: typing-extensions>=4.10.0 in /usr/local/lib/python3.10/dist-packages (from typeguard) (4.12.2)
Requirement already satisfied: geopandas in /usr/local/lib/python3.10/dist-packages (0.14.4)
Requirement already satisfied: fiona>=1.8.21 in /usr/local/lib/python3.10/dist-packages (from geopandas) (1.9.6)
Requirement already satisfied: numpy>=1.22 in /usr/local/lib/python3.10/dist-packages (from geopandas) (1.26.4)
Requirement already satisfied: packaging in /usr/local/lib/python3.10/dist-packages (from geopandas) (24.1)
Requirement already satisfied: pandas>=1.4.0 in /usr/local/lib/python3.10/dist-packages (from geopandas) (2.1.4)
Requirement already satisfied: pyproj>=3.3.0 in /usr/local/lib/python3.10/dist-packages (from geopandas) (3.6.1)
Requirement already satisfied: shapely>=1.8.0 in /usr/local/lib/python3.10/dist-packages (from geopandas) (2.0.6)
Requirement already satisfied: attrs>=19.2.0 in /usr/local/lib/python3.10/dist-packages (from fiona>=1.8.21->geopandas) (24.2.0)
Requirement already satisfied: certifi in /usr/local/lib/python3.10/dist-packages (from fiona>=1.8.21->geopandas) (2024.7.4)
Requirement already satisfied: click~=8.0 in /usr/local/lib/python3.10/dist-packages (from fiona>=1.8.21->geopandas) (8.1.7)
Requirement already satisfied: click-plugins>=1.0 in /usr/local/lib/python3.10/dist-packages (from fiona>=1.8.21->geopandas) (1.1.1)
Requirement already satisfied: cligj>=0.5 in /usr/local/lib/python3.10/dist-packages (from fiona>=1.8.21->geopandas) (0.7.2)
Requirement already satisfied: six in /usr/local/lib/python3.10/dist-packages (from fiona>=1.8.21->geopandas) (1.16.0)
Requirement already satisfied: python-dateutil>=2.8.2 in /usr/local/lib/python3.10/dist-packages (from pandas>=1.4.0->geopandas) (2.8.2)
Requirement already satisfied: pytz>=2020.1 in /usr/local/lib/python3.10/dist-packages (from pandas>=1.4.0->geopandas) (2024.1)
Requirement already satisfied: tzdata>=2022.1 in /usr/local/lib/python3.10/dist-packages (from pandas>=1.4.0->geopandas) (2024.1)

6. **Instalação de Bibliotecas**

```python
# Localização geográfica
import geopy
from geopy.geocoders import Nominatim
# Manipulação de dados no formato JSON
import json
# Manipulação e análise de dados
import pandas as pd
# Montar o Google Drive no ambiente Colab
from google.colab import drive
# Baixar arquivos do Google Drive
import gdown
# Importando a biblioteca Numpy
import numpy as np
# Importando a pandera
# Interagir com o sistema operacional
import os
import pandera as pa
# Manipulação de avisos
import warnings
# Ignorar avisos durante a execução do código
warnings.filterwarnings("ignore")
# Importar a classe RateLimiter do módulo geopy.extra.rate_limiter
# Para controlar a taxa de geocodificação
from geopy.extra.rate_limiter import RateLimiter
from geopy.geocoders import nominatim
# Importar o geopandas para visualizar as coordenadas dos hubs e das entregas do Distrito Federal
import geopandas
# Importar a biblioteca de plotagem
import matplotlib as plt
```

7. **Exploração de Dados**

7.1. **Coleta de Dados**

O dado bruto é um arquivo do tipo JSON com uma lista de instâncias de entregas. Cada instância representa um conjunto de entregas que devem ser realizadas pelos veículos do hub regional. Exemplo:

```json
[
  {
    "name": "cvrp-0-df-0",
    "region": "df-0",
    "origin": {"lng": -47.802664728268745, "lat": -15.657013854445248},
    "vehicle_capacity": 180,
    "deliveries": [
      {
        "id": "ed0993f8cc70d998342f38ee827176dc",
        "point": {"lng": -47.7496622016347, "lat": -15.65879313293694},
        "size": 10
      },
      {
        "id": "c7220154adc7a3def8f0b2b8a42677a9",
        "point": {"lng": -47.75887552060412, "lat": -15.651440380492554},
        "size": 10
      },
      ...
    ]
  }
]
...
```

7.1.1. **Conectar Google Colab ao Google Drive**

```python
# Conectar Colab ao Google Drive
from google.colab import drive
drive.mount('/content/drive')
```

Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount("/content/drive", force_remount=True).

7.1.2. **Download Arquivos do Google Drive**

```python
file_id = "1Rt5e8qaGKHawCiqF9wff2dSaAxil8C_l"
output = "deliveries.json"  # Nome do arquivo de saída

gdown.download(f"https://drive.google.com/uc?id={file_id}", output, quiet=False)
```

Downloading...
From: https://drive.google.com/uc?id=1Rt5e8qaGKHawCiqF9wff2dSaAxil8C_l
To: /content/deliveries.json
100%|██████████| 77.0M/77.0M [00:02<00:00, 34.3MB/s]
'deliveries.json'

7.1.3. **Carregar os dados do arquivo 'deliveries.json' em um dicionário Python chamado 'data'**

```python
with open('deliveries.json', mode='r', encoding='utf8') as file:
  data = json.load(file)
```

```json
[
  {
    "name": "cvrp-0-df-0",
    "region": "df-0",
    "origin": {
      "lng": -47.802664728268745,
      "lat": -15.657013854445248
    },
    "vehicle_capacity": 180,
    "deliveries": [
      {
        "id": "ed0993f8cc70d998342f38ee827176dc",
        "point": {
          "lng": -47.7496622016347,
          "lat": -15.65879313293694
        },
        "size": 10
      },
      {
        "id": "c7220154adc7a3def8f0b2b8a42677a9",
        "point": {
          "lng": -47.75887552060412,
          "lat": -15.651440380492554
        },
        "size": 10
      