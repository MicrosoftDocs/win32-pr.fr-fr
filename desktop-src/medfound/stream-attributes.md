---
description: Attributs de flux
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Attributs de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531073"
---
# <a name="stream-attributes"></a>Attributs de flux

Les attributs suivants s’appliquent aux flux multimédias. Pour obtenir les attributs d’un exemple de média, utilisez la méthode [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .



| Attribut                                                                                   | Description                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [MFStreamExtension \_ CameraExtrinsics](mfstreamextension-cameraextrinsics.md)               | Extrinsics de l’appareil photo pour le flux.         |
| [MFStreamExtension \_ PinholeCameraIntrinsics](mfstreamextension-pinholecameraintrinsics.md) | L’appareil photo Pinhole est intrinsèque pour le flux. |



 

Tous les flux de médias ne contiennent pas tous les attributs répertoriés ici. Dans certains cas, un attribut s’applique uniquement à certains genres de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 



