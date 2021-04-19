---
title: Utilisation de flux audio et vidéo non compressés
description: Utilisation de flux audio et vidéo non compressés
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- flux, configuration de flux audio et vidéo non compressés
- codecs, configuration des flux audio et vidéo non compressés
- flux vidéo, non compressés
- flux audio, non compressés
- flux audio et vidéo non compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511472"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="d9939-108">Utilisation de flux audio et vidéo non compressés</span><span class="sxs-lookup"><span data-stu-id="d9939-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="d9939-109">Dans la plupart des cas, le support non compressé présente des exigences de stockage et de remise excessives, mais pour certains scénarios de lecture locale, le niveau de qualité est suffisamment important pour ne pas utiliser la compression.</span><span class="sxs-lookup"><span data-stu-id="d9939-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="d9939-110">Les paramètres d’un flux multimédia non compressé doivent refléter les paramètres du média source.</span><span class="sxs-lookup"><span data-stu-id="d9939-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="d9939-111">Lors de la configuration d’un flux non compressé, vous devez calculer la vitesse de transmission du média et définir le flux de manière appropriée en appelant [**IWMStreamConfig :: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span><span class="sxs-lookup"><span data-stu-id="d9939-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="d9939-112">Étant donné que les flux non compressés ne sont pas viables pour la diffusion en continu, vous devez toujours définir la fenêtre de mémoire tampon pour les flux de média non compressés sur zéro en appelant [**IWMStreamConfig :: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span><span class="sxs-lookup"><span data-stu-id="d9939-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="d9939-113">Les formats de pixels suivants sont pris en charge pour les flux vidéo non compressés :</span><span class="sxs-lookup"><span data-stu-id="d9939-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="d9939-114">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d9939-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="d9939-115">WMMEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d9939-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d9939-116">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d9939-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d9939-117">WMMEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="d9939-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="d9939-118">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="d9939-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="d9939-119">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="d9939-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="d9939-120">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="d9939-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="d9939-121">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d9939-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="d9939-122">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="d9939-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9939-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9939-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9939-124">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="d9939-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="d9939-125">**Configuration de flux audio**</span><span class="sxs-lookup"><span data-stu-id="d9939-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="d9939-126">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="d9939-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="d9939-127">**Configuration de flux vidéo**</span><span class="sxs-lookup"><span data-stu-id="d9939-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




