---
description: Montre comment afficher un aperçu de la vidéo à partir d’un périphérique de capture vidéo, à l’aide de l’API MFPlay.
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: Exemple SimpleCapture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201844"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="39a26-103">Exemple SimpleCapture</span><span class="sxs-lookup"><span data-stu-id="39a26-103">SimpleCapture Sample</span></span>

<span data-ttu-id="39a26-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="39a26-104">\[Deprecated.</span></span> <span data-ttu-id="39a26-105">L’API MFPlay peut être supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="39a26-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="39a26-106">Les applications doivent utiliser le [lecteur source](source-reader.md) pour la capture vidéo.\]</span><span class="sxs-lookup"><span data-stu-id="39a26-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="39a26-107">Montre comment afficher un aperçu de la vidéo à partir d’un périphérique de capture vidéo, à l’aide de l’API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="39a26-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="39a26-108">API illustrées</span><span class="sxs-lookup"><span data-stu-id="39a26-108">APIs Demonstrated</span></span>

<span data-ttu-id="39a26-109">Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="39a26-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="39a26-110">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="39a26-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="39a26-111">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="39a26-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="39a26-112">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="39a26-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="39a26-113">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="39a26-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="39a26-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39a26-114">Requirements</span></span>



| <span data-ttu-id="39a26-115">Produit</span><span class="sxs-lookup"><span data-stu-id="39a26-115">Product</span></span>                                                        | <span data-ttu-id="39a26-116">Version</span><span class="sxs-lookup"><span data-stu-id="39a26-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="39a26-117">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="39a26-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="39a26-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39a26-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="39a26-119">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="39a26-119">Downloading the Sample</span></span>

<span data-ttu-id="39a26-120">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span><span class="sxs-lookup"><span data-stu-id="39a26-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="39a26-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39a26-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a26-122">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="39a26-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="39a26-123">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39a26-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



