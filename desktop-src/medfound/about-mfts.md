---
description: À propos de MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: À propos de MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04bfc09cbd17e5f0810f46eb6e42b230010348e89040b3cd407e98ee069c8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035706"
---
# <a name="about-mfts"></a>À propos de MFTs

Les transformations de Media Foundation (MFTs) fournissent un modèle générique pour le traitement des données multimédias. Les MFTs sont utilisés pour les décodeurs, les encodeurs et les processeurs de signal numérique (DSP). En bref, tout ce qui se trouve dans le pipeline de média entre la source du média et le récepteur multimédia est une table MFT.

Pour la plupart des applications, les détails du traitement des données MFT sont masqués par les couches supérieures de l’architecture Media Foundation. De nombreuses applications Media Foundation n’effectuent jamais un appel direct à une table MFT. Toutefois, il est certainement possible d’héberger une table MFT directement dans votre application.

Les MFTs sont une évolution du modèle de transformation introduit pour la première fois avec DirectX Media Objects (DMOs). En fait, il est relativement facile de créer une transformation qui prend en charge les deux modèles. Par rapport à DMOs, les comportements requis de MFTs sont plus clairement spécifiés, ce qui facilite l’écriture d’une implémentation correcte. En outre, MFTs peut prendre en charge le traitement vidéo accéléré par le matériel.

Cette rubrique donne un bref aperçu du modèle de traitement MFT, en se concentrant sur la conception globale plutôt que sur des appels de méthode spécifiques. Pour obtenir une description pas à pas plus détaillée, consultez modèle de [traitement MFT de base](basic-mft-processing-model.md).

## <a name="streams"></a>Flux

Une table MFT contient des flux d’entrée et des flux de sortie. Les flux d’entrée reçoivent des données, et les flux de sortie produisent des données. Par exemple, un décodeur possède un flux d’entrée, qui reçoit les données encodées, et un flux de sortie, qui produit les données décodées.

Les flux sur une table MFT ne sont pas représentés en tant qu’objets COM distincts. Au lieu de cela, chaque flux a un identificateur de flux désigné, et les méthodes de l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) prennent des identificateurs de flux en tant que paramètres d’entrée.

Certains MFTs ont un nombre fixe de flux. Par exemple, les décodeurs et les encodeurs ont normalement une seule entrée et une sortie. D’autres MFTs ont un nombre dynamique de flux. Si une table MFT prend en charge les flux dynamiques, le client peut ajouter de nouveaux flux d’entrée. Le client ne peut pas ajouter des flux de sortie, mais la table MFT peut ajouter ou supprimer des flux de sortie pendant le traitement. Par exemple, les multiplexeurs permettent généralement au client d’ajouter des flux d’entrée et d’avoir une sortie pour le flux multiplexé. Les démultiplexeurs sont l’inverse, avec une entrée, mais un nombre dynamique de flux de sortie, selon le contenu du flux d’entrée. L’illustration suivante montre la différence entre multiplexeur et démultiplexeur.

![Diagramme montrant un encodeur/décodeur (1 entrée, 1 sortie), un multiplexeur (2 entrées, 1 sortie) et un démultiplexeur (1 entrée, 2 sorties)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Types de médias

Quand une table MFT est créée pour la première fois, aucun des flux n’a un format établi. Avant que la MFT puisse traiter des données, le client doit définir les formats des flux. Par exemple, avec un décodeur, le format d’entrée est le format de compression utilisé dans le fichier source d’origine, et le format de sortie est un format non compressé, tel qu’une vidéo PCM audio ou RVB. Les formats de flux sont décrits à l’aide des [types de médias](media-types.md).

En fonction de l’état interne de la MFT, elle peut fournir une liste de types de média possibles pour chaque flux. Vous pouvez utiliser cette liste comme indication lorsque vous définissez les types de médias. La définition du type de média sur un flux peut modifier la liste des types possibles pour un autre flux. Par exemple, un décodeur ne peut généralement pas fournir de types de sortie tant que le client n’a pas défini le type d’entrée. Le type d’entrée contient les informations dont le décodeur a besoin pour retourner une liste de types de sortie possibles.

Pour définir le type de média sur un flux, appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) ou [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Pour obtenir la liste des types de média possibles pour un flux, appelez [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) ou [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Traitement des données

Une fois que le client a défini les types de média sur les flux, la MFT est prête à traiter les données. Pour ce faire, le client alterne entre la fourniture de données d’entrée à la MFT et l’obtention des données de sortie de la MFT :

-   Pour fournir des données d’entrée à la MFT, appelez [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Pour extraire des données de sortie de la table MFT, appelez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

La méthode [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) prend un pointeur vers un exemple de support alloué par le client. L’exemple de support contient une ou plusieurs mémoires tampons, et chaque mémoire tampon contient des données d’entrée pour le traitement de la table MFT.

La méthode [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) prend en charge deux modèles d’allocation différents : soit le MFT alloue les mémoires tampons de sortie, soit le client alloue les mémoires tampons de sortie. Certains MFTs prennent en charge les deux modèles d’allocation, mais il n’est pas nécessaire qu’un MFT prenne en charge les deux. Par exemple, une table MFT peut nécessiter que le client alloue les tampons de sortie. La méthode [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retourne des informations sur un flux de sortie, notamment le modèle d’allocation pris en charge par la table MFT.

Les MFTs sont conçus pour mettre en mémoire tampon le moins de données possible, afin de réduire la latence dans le pipeline. Par conséquent, à un moment donné, la table MFT peut signaler l’une des conditions suivantes :

-   La table MFT requiert davantage de données d’entrée. Dans cet État, la table MFT ne peut pas produire de sortie tant que le client n’a pas appelé [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) au moins une fois.
-   La MFT n’acceptera plus d’entrée tant que le client n’aura pas appelé [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) au moins une fois.

Par exemple, supposons que vous utilisez un décodeur vidéo pour décoder un flux vidéo contenant un mélange d’images clés et d’images Delta. Au départ, la table MFT requiert une entrée avant de pouvoir décoder des frames. Le client appelle [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) pour remettre le premier frame. Supposons que la première image est une image Delta (illustrée dans le diagramme suivant comme « P » pour le cadre prédit). Le décodeur conserve sur ce frame, mais ne peut pas produire de sortie tant qu’il n’a pas obtenu l’image clé suivante.

![Diagramme montrant la MFT qui nécessite une entrée, pointant vers un frame prédit](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

Le client continue d’appeler [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) et finit par atteindre la prochaine image clé (illustrée dans le schéma suivant sous le terme « I » pour le frame à code interne). À présent, le décodeur a suffisamment d’images pour démarrer le décodage. À ce stade, il cesse d’accepter l’entrée et le client doit appeler [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour récupérer les frames décodés.

![Diagramme montrant une table MFT qui n’accepte pas d’entrée, pointant vers une image intra-codée et trois frames prédites](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

L’approche la plus simple pour le client est simplement d’alterner les appels à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) et [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un algorithme plus sophistiqué est décrit dans la rubrique [modèle de traitement MFT de base](basic-mft-processing-model.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



