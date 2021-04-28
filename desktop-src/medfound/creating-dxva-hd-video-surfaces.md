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
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="6e384-103">Création de surfaces vidéo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="6e384-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="6e384-104">L’application doit créer une ou plusieurs surfaces Direct3D à utiliser pour les trames d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6e384-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="6e384-105">Celles-ci doivent être allouées dans le pool de mémoire spécifié par le membre **InputPool** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="6e384-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="6e384-106">Les types de surface suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="6e384-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="6e384-107">Une surface vidéo créée en appelant [**IDXVAHD \_ Device :: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) et en spécifiant le type de **\_ surface DXVAHD \_ \_ \_ entrée vidéo** ou le type de surface **DXVAHD \_ \_ \_ vidéo \_ d’entrée \_ privée** .</span><span class="sxs-lookup"><span data-stu-id="6e384-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="6e384-108">Ce type de surface est équivalent à une surface ordinaire hors écran.</span><span class="sxs-lookup"><span data-stu-id="6e384-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="6e384-109">Surface de rendu de décodeur-cible, créée en appelant [**IDirectXVideoAccelerationService :: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) et en spécifiant le type de surface **\_ VideoDecoderRenderTarget DXVA2** .</span><span class="sxs-lookup"><span data-stu-id="6e384-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="6e384-110">Ce type de surface est utilisé pour le décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="6e384-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="6e384-111">Surface ordinaire hors écran.</span><span class="sxs-lookup"><span data-stu-id="6e384-111">An off-screen plain surface.</span></span>

<span data-ttu-id="6e384-112">Le code suivant montre comment allouer une surface vidéo à l’aide de [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span><span class="sxs-lookup"><span data-stu-id="6e384-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6e384-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e384-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e384-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="6e384-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



