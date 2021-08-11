---
description: Un encodeur convertit le contenu audio ou vidéo non compressé en paquets compressés dans le format spécifié par l’application. pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les codecs audio et vidéo Windows media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Encodeurs multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d79ff55e98227c63e9761a8dec5ae068c8b1786c067230548ad0028dbe301a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237288"
---
# <a name="windows-media-encoders"></a>Windows Encodeurs multimédias

Un encodeur convertit le contenu audio ou vidéo non compressé en paquets compressés dans le format spécifié par l’application. pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les codecs audio et vidéo Windows media.

Un encodeur est identifié par le GUID qui représente la catégorie : audio ou vidéo. Le type de sortie de l’encodeur est représenté par le principal d’un type de média et le GUID de sous-type.

-   Windows Codecs audio de média

    Catégorie : **\_ \_ \_ encodeur audio de catégorie MFT**

    Type majeur : MFMediaType \_ audio

    Sous-type : MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Codecs vidéo multimédias

    Catégorie : **\_ \_ \_ encodeur vidéo de catégorie MFT**

    Type majeur : \_ vidéo MFMediaType

    SubType : MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Ces encodeurs sont implémentés en tant que [Media Foundation Transform](media-foundation-transforms.md) (MFT) et Media Foundation permettent d’accéder à l’application par le biais de l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de l’encodeur. Si vous utilisez des composants de couche de pipeline pour l’encodage ASF, la MFT d’encodeur est insérée dans le pipeline en tant que nœud de transformation, car il est chargé de transformer les données multimédias qui transitent par la source vers le récepteur. Si la source est un type compressé, le pipeline ajoute les décodeurs requis pour convertir la source en un type non compressé. Un encodeur a un flux d’entrée et un flux de sortie. L’encodeur reçoit des données d’entrée et produit des données encodées selon la configuration et le format définis par l’application avant la session d’encodage. Le format du flux de sortie est décrit par un type de média.

Cette section contient les rubriques suivantes :



| Rubrique                                                                              | Description                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)                  | Explique comment créer l’encodeur.                                                         |
| [Propriétés d’encodage](configuring-the-encoder.md)                                 | Explique comment configurer l’encodeur en définissant les propriétés appropriées sur la MFT de l’encodeur. |
| [Négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md) | Explique comment définir les types de média d’entrée et de sortie sur l’encodeur.                            |
| [Configuration d’un encodeur WMV](configuring-a-wmv-encoder.md)                         | explique comment configurer un encodeur Windows Media Video (WMV).                              |
| [Définition d’un type de sortie pour un encodeur WMA](configuring-a-wma-encoder.md)          | explique comment définir un type de sortie sur un encodeur Windows Media Audio (WMA).                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



