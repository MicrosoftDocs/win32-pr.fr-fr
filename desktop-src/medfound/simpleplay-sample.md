---
description: Montre comment lire un fichier multimédia à l’aide de l’API MFPlay.
ms.assetid: 1acd6f98-af59-47fd-9a3e-38a668fb6acf
title: Exemple SimplePlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02fee507ffed7bd91664f67ffb725565f47c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527357"
---
# <a name="simpleplay-sample"></a><span data-ttu-id="e619f-103">Exemple SimplePlay</span><span class="sxs-lookup"><span data-stu-id="e619f-103">SimplePlay Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e619f-104">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e619f-104">Deprecated.</span></span> <span data-ttu-id="e619f-105">Cette API peut être supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="e619f-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="e619f-106">Les applications doivent utiliser la [session multimédia](media-session.md) pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="e619f-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="e619f-107">Montre comment lire un fichier multimédia à l’aide de l’API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="e619f-107">Shows how to play a media file using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="e619f-108">API illustrées</span><span class="sxs-lookup"><span data-stu-id="e619f-108">APIs Demonstrated</span></span>

<span data-ttu-id="e619f-109">Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="e619f-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="e619f-110">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="e619f-110">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="e619f-111">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="e619f-111">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="e619f-112">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="e619f-112">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="e619f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e619f-113">Requirements</span></span>



| <span data-ttu-id="e619f-114">Produit</span><span class="sxs-lookup"><span data-stu-id="e619f-114">Product</span></span>                                                        | <span data-ttu-id="e619f-115">Version</span><span class="sxs-lookup"><span data-stu-id="e619f-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="e619f-116">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="e619f-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="e619f-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e619f-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e619f-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e619f-118">Downloading the Sample</span></span>

<span data-ttu-id="e619f-119">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay).</span><span class="sxs-lookup"><span data-stu-id="e619f-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e619f-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e619f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e619f-121">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e619f-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="e619f-122">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="e619f-122">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



