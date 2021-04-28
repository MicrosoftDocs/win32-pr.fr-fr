---
description: Création de surfaces vidéo DXVA-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Création de surfaces vidéo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20dea8f34a275aab59b2d57f68ca76d46b1c1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102547"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Création de surfaces vidéo DXVA-HD

L’application doit créer une ou plusieurs surfaces Direct3D à utiliser pour les trames d’entrée. Celles-ci doivent être allouées dans le pool de mémoire spécifié par le membre **InputPool** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Les types de surface suivants peuvent être utilisés :

-   Une surface vidéo créée en appelant [**IDXVAHD \_ Device :: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) et en spécifiant le type de **\_ surface DXVAHD \_ \_ \_ entrée vidéo** ou le type de surface **DXVAHD \_ \_ \_ vidéo \_ d’entrée \_ privée** . Ce type de surface est équivalent à une surface ordinaire hors écran.
-   Surface de rendu de décodeur-cible, créée en appelant [**IDirectXVideoAccelerationService :: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) et en spécifiant le type de surface **\_ VideoDecoderRenderTarget DXVA2** . Ce type de surface est utilisé pour le décodage DXVA.
-   Surface ordinaire hors écran.

Le code suivant montre comment allouer une surface vidéo à l’aide de [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



