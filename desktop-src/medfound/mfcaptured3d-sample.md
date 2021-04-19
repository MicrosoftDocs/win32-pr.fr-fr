---
description: Montre comment afficher un aperçu de la vidéo d’une caméra vidéo, en utilisant Direct3D pour afficher la vidéo.
ms.assetid: fe241201-f2b5-467c-9d6a-5fc147fa5e2a
title: Exemple MFCaptureD3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ead8a026d3014c60e2411a031d43fe20214aa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518561"
---
# <a name="mfcaptured3d-sample"></a><span data-ttu-id="d3d2d-103">Exemple MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="d3d2d-103">MFCaptureD3D Sample</span></span>

<span data-ttu-id="d3d2d-104">Montre comment afficher un aperçu de la vidéo d’une caméra vidéo, en utilisant Direct3D pour afficher la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3d2d-104">Shows how to preview video from a video camera, using Direct3D to render the video.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="d3d2d-105">API illustrées</span><span class="sxs-lookup"><span data-stu-id="d3d2d-105">APIs Demonstrated</span></span>

<span data-ttu-id="d3d2d-106">Cet exemple illustre les API suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3d2d-106">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="d3d2d-107">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="d3d2d-107">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="d3d2d-108">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="d3d2d-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
-   [<span data-ttu-id="d3d2d-109">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="d3d2d-109">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="requirements"></a><span data-ttu-id="d3d2d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3d2d-110">Requirements</span></span>



| <span data-ttu-id="d3d2d-111">Produit</span><span class="sxs-lookup"><span data-stu-id="d3d2d-111">Product</span></span>                                                        | <span data-ttu-id="d3d2d-112">Version</span><span class="sxs-lookup"><span data-stu-id="d3d2d-112">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d3d2d-113">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="d3d2d-113">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d3d2d-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3d2d-114">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d3d2d-115">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="d3d2d-115">Downloading the Sample</span></span>

<span data-ttu-id="d3d2d-116">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFCaptureD3D).</span><span class="sxs-lookup"><span data-stu-id="d3d2d-116">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFCaptureD3D).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3d2d-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3d2d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3d2d-118">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="d3d2d-118">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="d3d2d-119">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3d2d-119">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



