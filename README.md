# Heat Map - Passo a Passo


- Com o elasticmaps é possivel utilizar recursos de georeferencia de maneira simples para visualização de dados.

- No plugin X-Pack, existem recursos destinados a bigdata, dentre eles o Grid aggregation



- No Grid Aggregation são disponibilizados metricas como: 

- Points: 
Cria uma camada vetorial com um ponto para cada célula na grade. A localização do ponto é o centróide ponderado para todos os pontos geográficos na célula em grade.

- Grid rectangles:
Cria uma camada vetorial com um polígono de caixa delimitadora para cada célula em grade.

- Heat map:
Cria uma camada de mapa de calor que agrupa os centróides ponderados para cada célula na grade.


O nosso interesse é no HeatMap:
A camada do HeatMap tem como definição: 
Dados geoespaciais agrupados em grades com métricas para cada célula na grade. O índice deve conter pelo menos um campo mapeado como geo_point.


# Kibana

- No kibana, entre na parte de Maps
- Cria uma nova visualização
- Adiciona uma nova camada importada pelo Index do Elastic, ja alimentada com Geo_Point
- Em 'Choose Data Source' : Opte pelo Grid Aggregation 

- Selecione seu Index Pattern
- Geospatial field
- E em Show As: Selecione HeatMap



A partir dai, customize de acordo com suas demandas.


# Documentação referente ao Elastic maps
https://www.elastic.co/guide/en/kibana/current/maps-getting-started.html

https://www.elastic.co/guide/en/kibana/current/maps.html

https://www.elastic.co/guide/en/kibana/current/maps-grid-aggregation.html

https://www.elastic.co/guide/en/kibana/current/heatmap-layer.html
