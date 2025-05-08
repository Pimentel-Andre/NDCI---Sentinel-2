# Aplicação de índice de clorofila para identificar eutrofização com Sentinel 2
![image](https://github.com/user-attachments/assets/8ebdf5f7-d694-4490-bc50-e5f81c55029e)

Este repositório contém um conjunto de ferramentas e análises para estimar concentrações de clorofila-a (chl-a) em corpos d'água utilizando imagens de satélite do Sentinel-2. O projeto implementa o Índice Normalizado de Clorofila (NDCI - Normalized Difference Chlorophyll Index) para monitoramento remoto da qualidade da água.  

## NDCI
O monitoramento da concentração de clorofila-a serve como um indicador crítico da produtividade e do estado trófico de ecossistemas aquáticos.  
O Sentinel oferece uma alternativa às técnicas tradicionais de amostragem in situ, permitindo análises espaciais e temporais mais abrangentes através do índice de clorofila por diferença normalizada. 

![image](https://github.com/user-attachments/assets/93e38496-3251-4c7d-8b6d-bd59e32acca2)

## Cadastro no site da Copernicus
Para iniciar as análises no script diff_ndvi_landslides.ipynb, crie um login no site abaixo. Utilizaremos o site da Copernicus para obter as imagens do Sentinel-2: 

https://dataspace.copernicus.eu/

## Autenticação 
No trecho do script que segue abaixo, é necessário entrar no link para autenticar seu acesso. Basta inserir login e senha e aceitar os termos:  

![image](https://github.com/user-attachments/assets/9a236899-ac49-4132-b574-5b8d9c0cc2c7)

## Região de estudo

A sua região de estudo precisa ser primeiramente definida no QGIS, ou qualquer outra ferramenta em que você possa selecionar a área de interesse e exporta-la como GeoJSON. Abaixo, demonstro o passo a passo para fazer isso no QGIS: 

### Passo 1 - Crie uma nova camada Shapefile

![image](https://github.com/user-attachments/assets/49a62bfc-eaab-4fed-9c55-189c4982d9b6)

Selecione o tipo de geometria como Polígono e se atente para definir a projeção como UTM 

![image](https://github.com/user-attachments/assets/d15153ed-081b-40a4-b1d5-e9cce28f6e09)

### Passo 2 - Clice no ícone de lápis (Alternar Edição) e em seguida em Adicionar Polígono (logo à direita)
![image](https://github.com/user-attachments/assets/d06542ae-560b-4823-98dd-d0295382b785)

### Passo 3 - Delimite a área  

Para isso, basta selecionar demarcar a região e, quando finalizar, clicar com o botão direito do mouse para finalizar o polígono

### Passo 4 - Exporte como GeoJSON  

![image](https://github.com/user-attachments/assets/adc57730-f639-4e7c-baa0-df3d1d514bce)

Agora, basta **salvar como GeoJSON e inserir na pasta**: ./veg_index/study_area no seu ambiente


