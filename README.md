# 📊 Projeto Análise Exploratória de Dados em Python

![Logo-Loggi](https://github.com/laurencedata/projeto-analise-dados/assets/124643687/428c0017-5fa5-46b6-905d-03619cff7f2f)

# 📌 Introdução 

Com o constante crescimento do comércio eletrônico e a evolução das expectativas dos consumidores em relação à rapidez e eficiência das entregas, o setor de logística tornou-se um dos pilares fundamentais para o sucesso das empresas em um mercado cada vez mais competitivo.

Neste cenário desafiador, a Loggi destaca-se como uma das principais empresas de logística do mercado, oferecendo soluções inovadoras e tecnologicamente avançadas para atender às demandas de seus clientes de forma ágil e confiável.

A Loggi é uma startup unicórnio brasileira de tecnologia focada em logística, avaliada em US$ 1 bilhão, com investimentos de grandes empresas como SoftBank, Microsoft, GGV Capital, Monashees e Kaszek (fonte). Inicialmente, a empresa começou suas operações entregando documentos entre 2013 e 2014. Posteriormente, expandiu seu escopo para o segmento de e-commerce e, desde 2017, tem atuado também nas entregas de alimentos.

Este repositório concentra-se na análise exploratória dos dados fornecidos pela Loggi, uma abordagem essencial para entender melhor o desempenho atual da empresa e identificar áreas de oportunidade para aprimoramento. Utilizando técnicas estatísticas e visuais, buscamos extrair insights valiosos dos dados operacionais, realizando o rastreamento de entregas inicializando pelos Hubs (ponto central de conexão onde ocorre a concentração de entrega redistribuição/transferência de mercadorias) por toda a região do Distrito Federal. 

Nosso principal objetivo é fornecer à Loggi informações estratégicas que possam impulsionar melhorias significativas em seus processos de entrega, aumentando a eficácia, reduzindo custos operacionais e aprimorando a experiência do cliente. Ao explorar os dados, buscamos identificar padrões, tendências e possíveis gargalos, além de propor sugestões concretas para otimização da logística, roteirização mais eficiente, alocação de recursos e muito mais.

# 🗺️ Visão Geral do Projeto

Este projeto visa explorar os dados, cujo o objetivo é identificar áreas de oportunidade e sugerir melhorias significativas em suas operações de entrega. Utilizando técnicas avançadas de análise exploratória de dados, buscamos entender padrões e tendências que impactam a eficiência operacional da Loggi, com o objetivo de fornecer recomendações práticas para otimizar processos logísticos, reduzir custos, minimizar tempos de entrega e aprimorar a experiência do cliente. 

# 📋 Requerimentos

Para este projeto, utilizamos os próprios dados disponibilizados pela Loggi nos formatos "JSON”, "SHP”, "SHX” e "CSV”. A análise foi realizada utilizando ambiente VS Code Python, complementado com pacotes e bibliotecas de manipulação e visualização dos dados. O **dado bruto** é um formato semi-estruturado do tipo `JSON` com uma lista de instâncias de entregas. Cada instância representa um conjunto de **entregas** que devem ser realizadas pelos **veículos** do **hub** regional. Exemplo:

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

- name: Identifica unicamente essa instância.
- region: Região do Hub de distribuição (vamos explorar os 3 Hub's na base de dados: "df-0”, "df-1” e "df-2”).
- origin: Coordenadas geográficas do Hub de distribuição.
    - lng: A longitude indica a posição a leste ou a oeste do meridiano de Greenwich.
    - lat: A latitude indica a posição ao norte ou ao sul do equador.
- vehicle_capacity: Soma da capacidade de todos os veículos que aquele Hub tem.
- deliveries: Lista de entregas que devem ser feitas.
    - id: Identificador das entregas, são identificadores únicos das entregas.
    - point: Coordenadas geográficas da própria entrega.
        - lng: A longitude indica a posição a leste ou a oeste do meridiano de Greenwich.
        - lat: A latitude indica a posição ao norte ou ao sul do equador.
    - size: Tamanho do item específico.

# 🔎 Análise Exploratória de Dados (AED):

A Análise Exploratória de Dados (AED) é uma abordagem estatística para investigar padrões, tendências e relações nos dados, com o objetivo de compreender seu significado e revelar insights úteis. Utilizando técnicas visuais e quantitativas, a AED ajuda a identificar padrões emergentes, outliers e relações entre variáveis, fornecendo uma base sólida para a tomada de decisões informadas e a formulação de hipóteses em estudos mais aprofundados. No contexto deste projeto, esse tipo de análise é empregada para explorar e compreender os dados coletados, permitindo uma melhor compreensão do fenômeno em questão e orientando o desenvolvimento de estratégias e análises adicionais.

Agora iremos abrir o arquivo [Projeto_Loggi_AED.ipynb](https://github.com/laurencedata/projeto-analise-dados/blob/main/Projeto_Loggi_AED.ipynb) e conferir afundo a análise feita.

