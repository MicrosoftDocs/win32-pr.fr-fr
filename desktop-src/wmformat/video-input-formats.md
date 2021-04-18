---
title: Formats d’entrée vidéo
description: Formats d’entrée vidéo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK, formats d’entrée vidéo
- ASF (Advanced Systems Format), formats d’entrée vidéo
- ASF (format des systèmes avancés), formats d’entrée vidéo
- formats d’entrée vidéo
- Windows Media Format SDK, formats vidéo
- ASF (Advanced Systems Format), formats vidéo
- ASF (format des systèmes avancés), formats vidéo
- formats vidéo
- Codecs Windows Media Video 9, formats d’entrée vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106512492"
---
# <a name="video-input-formats"></a><span data-ttu-id="b8cff-112">Formats d’entrée vidéo</span><span class="sxs-lookup"><span data-stu-id="b8cff-112">Video Input Formats</span></span>

<span data-ttu-id="b8cff-113">L’enregistreur accepte les formats vidéo suivants comme entrée à compresser à l’aide du codec Windows Media Video 9 :</span><span class="sxs-lookup"><span data-stu-id="b8cff-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="b8cff-114">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="b8cff-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="b8cff-115">WMMEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="b8cff-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="b8cff-116">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="b8cff-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="b8cff-117">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="b8cff-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="b8cff-118">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="b8cff-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="b8cff-119">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="b8cff-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="b8cff-120">WMMEDIASUBTYPE \_ YVU9</span><span class="sxs-lookup"><span data-stu-id="b8cff-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="b8cff-121">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="b8cff-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="b8cff-122">WMMEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="b8cff-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="b8cff-123">WMMEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="b8cff-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="b8cff-124">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="b8cff-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="b8cff-125">WMMEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="b8cff-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="b8cff-126">Vous devez toujours utiliser [**IWMWriter :: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) et [**IWMWriter :: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) pour énumérer les formats d’entrée disponibles et pour obtenir l’objet de propriétés de média d’entrée pour le format souhaité.</span><span class="sxs-lookup"><span data-stu-id="b8cff-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="b8cff-127">Les objets de propriétés de média d’entrée vidéo doivent être modifiés pour refléter la taille de trame et la fréquence d’images de votre média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b8cff-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8cff-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8cff-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8cff-129">**Identificateurs de type de média**</span><span class="sxs-lookup"><span data-stu-id="b8cff-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="b8cff-130">**Types de médias**</span><span class="sxs-lookup"><span data-stu-id="b8cff-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




