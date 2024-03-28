# Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML
Projeto da DIO

Detectar rostos no Vision Studio
As soluções de visão geralmente exigem que a IA seja capaz de detectar rostos humanos. Suponha que a empresa varejista fictícia Northwind Traders queira localizar onde os clientes estão em uma loja para melhor atendê-los. Uma maneira de fazer isso é determinar se há algum rosto nas imagens e, em caso afirmativo, retornar as coordenadas da caixa delimitadora que mostram sua localização.

Para testar as capacidades de deteção facial do serviço Azure AI Face, utilizará o Azure Vision Studio . Esta é uma plataforma baseada em UI que permite explorar os recursos do Azure AI Vision sem a necessidade de escrever nenhum código.


Crie um recurso de serviços de IA do Azure

Você pode usar o serviço Azure AI Face com um recurso multisserviço de serviços de IA do Azure . Se ainda não o fez, crie um recurso de serviços de IA do Azure na sua assinatura do Azure.
1. Em outra guia do navegador, abra o portal do Azure em https://portal.azure.com , entrando com a conta da Microsoft associada à sua assinatura do Azure.
2. Clique no botão ＋Criar um recurso e pesquise os serviços de IA do Azure . Selecione criar um plano de serviços de IA do Azure . Você será levado a uma página para criar um recurso de serviços de IA do Azure. Configure-o com as seguintes configurações:
    Assinatura : sua assinatura do Azure .
    Grupo de recursos : selecione ou crie um grupo de recursos com um nome exclusivo .
    Região : Leste dos EUA.
    Nome : Insira um nome exclusivo .
    Nível de preços : Padrão S0.
    Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo : Selecionado .
3. Selecione Revisar + criar e depois Criar e aguarde a conclusão da implantação.


Conecte seu recurso de serviço de IA do Azure ao Vision Studio

Em seguida, conecte o recurso de serviços de IA do Azure provisionado acima ao Vision Studio.
1. Em outra guia do navegador, navegue até Vision Studio em https://portal.vision.cognitive.azure.com .
2. Entre com sua conta e certifique-se de usar o mesmo diretório onde você criou seu recurso de serviços de IA do Azure.
3. Na página inicial do Vision Studio, selecione Visualizar todos os recursos no título Introdução ao Vision .
![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/4dae5db9-bfc8-4976-88f9-98fea113c7bd)
4. Na página Selecione um recurso para trabalhar , passe o cursor do mouse sobre o recurso que você criou acima na lista e marque a caixa à esquerda do nome do recurso e selecione Selecionar como recurso padrão .

Nota : Se o seu recurso não estiver listado, pode ser necessário atualizar a página.

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/c060142a-ac1e-4b9a-952d-261a29baaaac)
5. Feche a página de configurações selecionando o “x” no canto superior direito da tela.


Detecte rostos no Vision Studio

1. Num navegador web, navegue até Vision Studio em https://portal.vision.cognitive.azure.com .
2. Na página inicial Introdução ao Vision , selecione a guia Face e, em seguida, selecione o bloco Detectar rostos em uma imagem .
3. No subtítulo Experimente , reconheça a política de uso de recursos lendo e marcando a caixa.
4. Selecione cada uma das imagens de amostra e observe os dados de detecção facial retornados.
5. Agora vamos tentar com algumas de nossas próprias imagens. Selecione https://aka.ms/mslearn-detect-faces para baixar detect-faces.zip . Em seguida, abra a pasta no seu computador.
6. Localize o arquivo chamado store-camera-1.jpg ; que contém a seguinte imagem:

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/ee4c7129-54e1-4c02-b57e-1a29f2b21a32)

7. Faça upload de store-camera-1.jpg e revise os detalhes de detecção de rosto retornados.
8. Localize o arquivo chamado store-camera-2.jpg ; que contém a seguinte imagem:

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/4680696e-50da-49f3-aee4-63061d948c4f)

9. Faça upload de store-camera-2.jpg e revise os detalhes de detecção de rosto retornados.
10. Localize o arquivo chamado store-camera-3.jpg ; que contém a seguinte imagem:

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/1d0e9423-3dfb-4377-bb31-ab955ff0d5d7)

11. Faça upload de store-camera-3.jpg e revise os detalhes de detecção de rosto retornados. Observe como o Azure AI Face não detectou o rosto que está obscurecido.

Neste exercício você explorou como os serviços de IA do Azure podem detectar rostos em imagens. Se você tiver tempo, sinta-se à vontade para experimentar as imagens de amostra ou algumas de suas próprias imagens.


Limpar

Se não pretende fazer mais exercícios, exclua todos os recursos que não precisa mais. Isso evita acumular custos desnecessários.

1. Abra o portal do Azure em https://portal.azure.com e selecione o grupo de recursos que contém o recurso que você criou.
2. Selecione o recurso e selecione Excluir e depois Sim para confirmar. O recurso é então excluído.


Saber mais

Para saber mais sobre o que você pode fazer com este serviço, consulte a página do serviço Azure AI Face (https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity).



Ler texto no Vision Studio

Neste exercício, você usará o serviço Azure AI para explorar os recursos de reconhecimento óptico de caracteres do Azure AI Vision. Você usará o Vision Studio para experimentar a extração de texto de imagens, sem precisar escrever nenhum código.

Um desafio comum da visão computacional é detectar e interpretar texto incorporado em uma imagem. Isso é conhecido como reconhecimento óptico de caracteres (OCR). Neste exercício você usará um recurso de serviços de IA do Azure, que inclui serviços do Azure AI Vision. Em seguida, você usará o Vision Studio para testar o OCR com diferentes tipos de imagens.



Crie um recurso de serviços de IA do Azure

Você pode usar os recursos de OCR do Azure AI Vision com um recurso multisserviço de serviços de IA do Azure . Se ainda não o fez, crie um recurso de serviços de IA do Azure na sua assinatura do Azure.
1. Em outra guia do navegador, abra o portal do Azure em https://portal.azure.com , entrando com a conta da Microsoft associada à sua assinatura do Azure.
2. Clique no botão ＋Criar um recurso e pesquise os serviços de IA do Azure . Selecione criar um plano de serviços de IA do Azure . Você será levado a uma página para criar um recurso de serviços de IA do Azure. Configure-o com as seguintes configurações:
    Assinatura : sua assinatura do Azure .
    Grupo de recursos : selecione ou crie um grupo de recursos com um nome exclusivo .
    Região : Leste dos EUA.
    Nome : Insira um nome exclusivo .
    Nível de preços : Padrão S0.
    Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo : Selecionado .
3. Selecione Revisar + criar e depois Criar e aguarde a conclusão da implantação.



Conecte seu recurso de serviço de IA do Azure ao Vision Studio

Em seguida, conecte o recurso de serviços de IA do Azure provisionado acima ao Vision Studio.
1. Em outra guia do navegador, navegue até Vision Studio em https://portal.vision.cognitive.azure.com .
2. Entre com sua conta e certifique-se de usar o mesmo diretório onde você criou seu recurso de serviços de IA do Azure.
3. Na página inicial do Vision Studio, selecione Visualizar todos os recursos no título Introdução ao Vision .

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/9de273bd-2c71-40ea-92b8-db6b637ab50f)

4. Na página Selecione um recurso para trabalhar , passe o cursor do mouse sobre o recurso que você criou acima na lista e marque a caixa à esquerda do nome do recurso e selecione Selecionar como recurso padrão .

Nota : Se o seu recurso não estiver listado, pode ser necessário atualizar a página.

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/f8f450da-3924-423a-8a97-647ac1700441)

5. Feche a página de configurações selecionando o “x” no canto superior direito da tela.



Extraia texto de imagens no Vision Studio

1. Num navegador web, navegue até Vision Studio em https://portal.vision.cognitive.azure.com .
2. Na página inicial Introdução ao Vision , selecione Reconhecimento óptico de caracteres e, em seguida, o bloco Extrair texto de imagens .
3. No subtítulo Experimente , reconheça a política de uso de recursos lendo e marcando a caixa.
4. Selecione https://aka.ms/mslearn-ocr-images para baixar ocr-images.zip . Em seguida, abra a pasta.
5. No portal, selecione Procurar um arquivo e navegue até a pasta em seu computador onde você baixou ocr-images.zip . Selecione advert.jpg e selecione Abrir .
6. Agora revise o que é retornado:
    Nos atributos detectados , qualquer texto encontrado na imagem é organizado em uma estrutura hierárquica de regiões, linhas e palavras.
    Na imagem, a localização do texto é indicada por uma caixa delimitadora, conforme mostrado aqui:
![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/75000724-c0cb-4f7d-96ce-8923d3c1d7a0)

7. Agora você pode tentar outra imagem. Selecione Procurar um arquivo e navegue até a pasta onde você salvou os arquivos do GitHub. Selecione carta.jpg .

![image](https://github.com/ThiagoMouraP/Reconhecimento-Facial-e-Transforma-o-de-Imagens-em-Dados-no-Azure-ML/assets/43223265/976585dc-92ea-4db7-9a0d-9f9b5eaf4fae)

8. Revise os resultados da segunda imagem. Deve retornar o texto e as caixas delimitadoras do texto. Se você tiver tempo, tente note.jpg e recibo.jpg .



Limpar

Se não pretende fazer mais exercícios, exclua todos os recursos que não precisa mais. Isso evita acumular custos desnecessários.

1. Abra o portal do Azure em https://portal.azure.com e selecione o grupo de recursos que contém o recurso que você criou.
2. Selecione o recurso e selecione Excluir e depois Sim para confirmar. O recurso é então excluído.
Saber mais
Para saber mais sobre o que você pode fazer com este serviço, consulte a documentação do Azure AI Vision sobre reconhecimento óptico de caracteres (https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr).
