---
description: Montre comment implémenter un effet vidéo en tant que transformation de Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Exemple de MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114394"
---
# <a name="mft_grayscale-sample"></a>\_Exemple de nuances de gris MFT

Montre comment implémenter un effet vidéo en tant que transformation de Media Foundation (MFT). La MFT en nuances de gris convertit la vidéo YUV en nuances de gris en définissant les valeurs de chrominance dans la vidéo sur neutre. La table MFT accepte les vidéos non compressées dans les formats UYVY, YUY2 ou NV12.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Utilisation

L’exemple MFT en \_ nuances de gris génère une dll qui est un serveur com pour la MFT. Avant d’utiliser la MFT, vous devez inscrire la DLL.

Pour voir la MFT en nuances de gris en cours d’utilisation, exécutez l' [exemple PlaybackFX](/previous-versions//bb970336(v=vs.85)). Vous pouvez également utiliser l’outil TopoEdit pour créer une topologie qui comprend la MFT en nuances de gris. Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la vidéo YUV](about-yuv-video.md)
</dt> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[\_Exemple AUDIODELAY MFT](mft-audiodelay-sample.md)
</dt> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 
