## Objetivo 🎯
Neste LAB, aplicaremos técnicas de organização de documentos e conduziremos pesquisas eficientes através da ingestão de dados, seguindo três passos essenciais: ingestão de conhecimento de IA, criação do índice correspondente e exploração dessas funcionalidades. 

Ao final, ganharemos uma visão prática das potencialidades oferecidas por essas ferramentas na mineração de conhecimento.

-- Autora do lab na DIO: 

Valéria Baptista

Head of Cloud and Cybersecurity, CloudData Tech & DevOps

---

### Azure Machine Learning.

Os elementos testados fazem parte da suite de inteligência artificial do Azure AI services. 
Então uma sequencia de passos é necessária:

1o. Ter uma conta na Azure. Acesso o  Azure portal no link https://portal.azure.com

2o. Ter uma assinatura válida (signature). É possível testar por 1 mês com 200 dólares de crédito.

3o. Criar um grupo de recursos

![image](https://github.com/toniacprado/DIO-Trabalhando-com-Machine-Learning-na-Pratica-no-Azure-ML/assets/105946569/2f5b7b4c-d3ee-49d4-9844-b015d6f59c2e)


4o. Criar um recurso Azure AI Search
![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/95c32312-f10f-421c-b95c-4d32de66f910)

Lembrar que para o AI Search é preciso selecionar o nível de custo Basic pelo menos.

4.1 Criar um novo recurso de AI:

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/54459e0a-0a47-4548-89f6-85d2b07e4b90)

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/1ed61fbc-cc7d-48f6-8ec3-596e34e2e69c)

4.2 Criar uma conta de armazenamento (Storage Account):

Pesquisar na barra superior por "Storage Account"

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/49389192-3381-457e-b384-cebd6a64e5b7)

#### Pode selecionar os itens mais simples para a cobrança para este laboratório:

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/a6bc7cdf-0e28-451a-bfbf-dda03718a49b)

### Configurando o Storage Account para o acesso anonimo -- Exigência do laboratório:

#### Permitir acesso anônimo de Blob:

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/537dfd97-a24a-4fcb-ab35-afd2308afc73)

#### Criar um novo container

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/9d0bc3ae-6741-47b3-a7da-8cf1a4f475b1)

Note que o nome para ser aceito do container precisa estar livre de maiúsculas e outros símbolos.

#### Selecionar o container criado e fazer o upload dos arquivos fornecidos na documentação (descompactar o reviews.zip) são 9 arquivos de exemplo:

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/c7706340-0c6e-4802-94f9-5de95208f43c)

#### Agora ir até o Mecanismo de Busca criado e importar os dados

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/7f4843ef-25cd-46ea-b9ec-a1e7d8e9a09d)

As informações de criação foi seguindo o que está informado na documentação oficial:

Data Source: Azure Blob Storage

Data source name: coffee-customer-data

Data to extract: Content and metadata

Parsing mode: Default

Connection string: *Select Choose an existing connection. Select your storage account, select the coffee-reviews container, and then click Select.

Managed identity authentication: None

Container name: this setting is auto-populated after you choose an existing connection.

Blob folder: Leave this blank.

Description: Reviews for Fourth Coffee shops.


![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/b3992f7c-1d72-49b6-92f2-9b033f248bf9)

### o detalhamento de como importar os dados seguiu a documentação oficial na parte do documento chamada: "Index the documents"


### exemplos de uso do Search Explorer

Podemos experimentar a ferramenta de pesquisa no campo de "Search" e usar os tags pesquisáveis como por exemplo:

search=sentiment="negaive"

![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/33c468a1-d359-4838-9935-91854c99b5ec)


ou search=location="chicago"


![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/92b1f999-fe11-4239-8d86-c1fd2f11fee8)


#### Vale resaltar que o portal disponibiliza o Knowledge Center com diversos recursos para expandir o aprendizado sobre as ferramentas de IA + Busca:


![image](https://github.com/toniacprado/DIO-Azure-Cognitive-Search-Utilizando-AI-Search-para-indexacao-e-consulta-de-Dados/assets/105946569/de84218d-5919-49fc-b1ea-30cb4e62ef72)


### Foi utilizado além das instruções das video aulas este link da documentação oficial: 


https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html