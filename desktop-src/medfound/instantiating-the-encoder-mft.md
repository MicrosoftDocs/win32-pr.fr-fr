---
description: Instanciation d’une table MFT d’encodeur
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Instanciation d’une table MFT d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203870"
---
# <a name="instantiating-an-encoder-mft"></a>Instanciation d’une table MFT d’encodeur

Dans Microsoft Media Foundation, les encodeurs sont implémentés en tant que [transformations Media Foundation](media-foundation-transforms.md) (MFTS). Avant de créer un encodeur, vous devez d’abord Rechercher l’encodeur qui convient le mieux à vos besoins.

-   Codecs audio Windows Media

    Catégorie : **\_ \_ \_ encodeur audio de catégorie MFT**

    Type majeur : MFMediaType \_ audio

    Sous-type : MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Codecs Windows Media Video

    Catégorie : **\_ \_ \_ encodeur vidéo de catégorie MFT**

    Type majeur : \_ vidéo MFMediaType

    SubType : MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Media Foundation fournit plusieurs fonctions que votre application peut appeler pour énumérer les différents encodeurs disponibles dans votre système. Les encodeurs sont enregistrés en tant qu’objets COM et l’entrée de Registre suit le format standard pour les fabriques de classes COM. Le registre gère les CLSID des encodeurs, qui sont catégorisés par le format multimédia (audio ou vidéo). Les identificateurs de classe des encodeurs Windows Media sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h. Dans Media Foundation, les encodeurs peuvent être inscrits par le biais d’appels à [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) en spécifiant le catégorie, les types d’entrée pris en charge et les types de sortie pris en charge. Une fois l’inscription réussie via ces fonctions, les MFTs sont considérés par les fonctions d’énumération Media Foundation.

Pour créer une instance d’une table MFT d’encodeur, une application peut choisir les options suivantes.

-   Créez directement la MFT de l’encodeur et recevez un pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Pour plus d’informations, consultez [création d’un encodeur à l’aide de CoCreateInstance](using-an-encoder-s-imftransform--interface.md).
-   Créez une instance de l’objet d’activation pour la table MFT de l’encodeur et recevez un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Pour plus d’informations, consultez [utilisation des objets d’activation d’un encodeur](using-an-encoder-s-activation-objects.md).

Si votre application utilise des [composants ASF de couche de pipeline](pipeline-layer-asf-components.md) pour encoder un fichier au format ASF, vous devez insérer la table MFT de l’encodeur dans le pipeline en tant que nœud de transformation. Lors de la création du nœud transformer dans la topologie d’encodage, vous pouvez soit définir le type d’objet en tant que pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , soit l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Media Foundation fournit des objets d’activation pour les encodeurs Windows Media afin qu’ils puissent être définis facilement comme nœud de transformation dans la topologie d’encodage. Lorsque la topologie est résolue, la session multimédia utilise l’objet d’activation pour créer une instance de la MFT de l’encodeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodeurs Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



