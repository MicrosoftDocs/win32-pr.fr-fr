---
description: Important déconseillé.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Exemple MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863430"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="b60ff-103">Exemple MFPlayer2</span><span class="sxs-lookup"><span data-stu-id="b60ff-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b60ff-104">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b60ff-104">Deprecated.</span></span> <span data-ttu-id="b60ff-105">Cette API peut être supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="b60ff-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="b60ff-106">Les applications doivent utiliser la [session multimédia](media-session.md) pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="b60ff-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="b60ff-107">Présente certaines des fonctionnalités de lecture qui sont omises de l’exemple [SimplePlay](simpleplay-sample.md) , par exemple :</span><span class="sxs-lookup"><span data-stu-id="b60ff-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="b60ff-108">Cherche</span><span class="sxs-lookup"><span data-stu-id="b60ff-108">Seeking</span></span>
-   <span data-ttu-id="b60ff-109">Contrôle du taux (avance rapide et rembobinage)</span><span class="sxs-lookup"><span data-stu-id="b60ff-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="b60ff-110">Contrôles de volume audio et de sourdine</span><span class="sxs-lookup"><span data-stu-id="b60ff-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="b60ff-111">Zoom vidéo</span><span class="sxs-lookup"><span data-stu-id="b60ff-111">Video zoom</span></span>

<span data-ttu-id="b60ff-112">L’illustration suivante montre les contrôles utilisés pour ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b60ff-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="b60ff-113">capture d’écran de l’exemple mfplayer</span><span class="sxs-lookup"><span data-stu-id="b60ff-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="b60ff-114">API illustrées</span><span class="sxs-lookup"><span data-stu-id="b60ff-114">APIs Demonstrated</span></span>

<span data-ttu-id="b60ff-115">Cet exemple illustre les API suivantes.</span><span class="sxs-lookup"><span data-stu-id="b60ff-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="b60ff-116">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="b60ff-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="b60ff-117">**IAudioSessionManager**</span><span class="sxs-lookup"><span data-stu-id="b60ff-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="b60ff-118">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="b60ff-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="b60ff-119">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="b60ff-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="b60ff-120">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="b60ff-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="b60ff-121">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="b60ff-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="b60ff-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="b60ff-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="b60ff-123">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="b60ff-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="b60ff-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b60ff-124">Requirements</span></span>



| <span data-ttu-id="b60ff-125">Produit</span><span class="sxs-lookup"><span data-stu-id="b60ff-125">Product</span></span>                                                        | <span data-ttu-id="b60ff-126">Version</span><span class="sxs-lookup"><span data-stu-id="b60ff-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b60ff-127">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="b60ff-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b60ff-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b60ff-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b60ff-129">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b60ff-129">Downloading the Sample</span></span>

<span data-ttu-id="b60ff-130">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span><span class="sxs-lookup"><span data-stu-id="b60ff-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b60ff-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b60ff-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b60ff-132">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b60ff-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="b60ff-133">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="b60ff-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
