---
title: Configuration de flux de capture d’écran
description: Configuration de flux de capture d’écran
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- flux, configuration des flux de capture d’écran
- codecs, configuration des flux de capture d’écran
- flux de capture d’écran
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940660"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="f4ffc-106">Configuration de flux de capture d’écran</span><span class="sxs-lookup"><span data-stu-id="f4ffc-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="f4ffc-107">Les flux qui utilisent le codec Windows Media® Video 9 Screen sont configurés par les applications de la même façon que les flux vidéo normaux.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="f4ffc-108">Toutefois, si vous définissez le niveau de complexité de la vidéo sur 0, l’enregistreur ignore toute valeur de qualité vidéo définie avec [**IWMVideoMediaProps :: SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span><span class="sxs-lookup"><span data-stu-id="f4ffc-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="f4ffc-109">Pour plus d’informations, consultez [obtenir de bons résultats avec le codec d’écran Windows Media Video 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span><span class="sxs-lookup"><span data-stu-id="f4ffc-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4ffc-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4ffc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4ffc-111">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="f4ffc-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="f4ffc-112">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="f4ffc-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="f4ffc-113">**Configuration de flux vidéo**</span><span class="sxs-lookup"><span data-stu-id="f4ffc-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




