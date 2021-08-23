---
description: Négociation de type de média sur l’encodeur
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Négociation de type de média sur l’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ac5dd5a107633feba4ce2a74da7e9aea7e9f71d51be1b5cad5b85ab4adda35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941509"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Négociation de type de média sur l’encodeur

Dans Microsoft Media Foundation, les encodeurs sont implémentés en tant que [Media Foundation transformations](media-foundation-transforms.md) (MFTS) avec une entrée et une sortie. Avant une session d’encodage, un encodeur doit connaître les caractéristiques du flux qu’il recevra en tant qu’entrée et le format du flux qu’il produira comme sortie. Vous devez définir les types de média d’entrée et de sortie et les caractéristiques associées avant de transmettre des données via l’encodeur. Vous devez fournir les formats d’entrée et de sortie en spécifiant les [GUID de type de média](media-type-guids.md) appropriés et définir les caractéristiques du flux de sortie en définissant les attributs de type de [média](media-type-attributes.md) appropriés sur le type de média de sortie. Un encodeur nouvellement instancié n’a aucun type de média défini.

Le type de média d’entrée est un format non compressé, tel qu’une vidéo PCM audio ou RVB. Les types de format utilisés par l’encodeur sont limités à ceux décrits par les structures **VIDEOINFOHEADER** et **WAVEFORMATEX** . pour plus d’informations sur ces structures, consultez la documentation SDK Windows. Media Foundation fournit des fonctions d’assistance pour créer des types de média à partir de structures de format. Par exemple, la fonction [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) Initialise un type de vidéo à partir d’une structure **VIDEOINFOHEADER** , et la fonction [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) Initialise un type de vidéo à partir d’une structure **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** . Pour plus d’informations, consultez [conversions de type de média](media-type-conversions.md). Vous devez définir le type de média d’entrée sur l’encodeur en appelant [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

Le type de média de sortie est le format de compression utilisé dans le fichier ou le flux de source final. Vous pouvez définir le type de média de sortie disponible uniquement après avoir défini le type de média d’entrée. Vous pouvez récupérer les types de sortie pris en charge en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) dans une boucle jusqu’à ce que l’encodeur retourne **MF E plus de \_ \_ \_ \_ types**. Incrémentez l’index de type avec chaque itération. Lorsque vous trouvez un type de média approprié, définissez le type de média de sortie en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

Le facteur déterminant dans le choix du type de média de sortie dépend du type d’encodage et de vos exigences d’encodage. Par exemple, pour les flux audio qui sont encodés CBR, vous souhaitez rechercher un type de média qui correspond à votre entrée et une vitesse de transmission aussi proche que possible d’une valeur cible.

Si vous souhaitez utiliser un mode d’encodage autre que CBR, vous devez définir le mode, puis énumérer les types de sortie pour ce mode, car l’encodeur modifie les types de sortie pris en charge en fonction du jeu de modes. Les propriétés qui contrôlent le mode d’encodage sont [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) et [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Par exemple, si vous énumérez les types de sortie pour l’encodage VBR-Quality, le type de média dépend de la valeur de qualité que vous décidez d’utiliser. Pour plus d’informations sur la définition de ces propriétés, consultez [Propriétés de codage](configuring-the-encoder.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Encodeurs multimédias](windows-media-encoders.md)
</dt> </dl>

 

 



