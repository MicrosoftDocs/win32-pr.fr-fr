---
description: Cette rubrique explique comment utiliser MFPlay pour afficher un aperçu de la vidéo d’une caméra vidéo.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Aperçu de la vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516957"
---
# <a name="video-preview"></a><span data-ttu-id="a73aa-103">Aperçu de la vidéo</span><span class="sxs-lookup"><span data-stu-id="a73aa-103">Video Preview</span></span>

<span data-ttu-id="a73aa-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a73aa-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a73aa-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a73aa-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a73aa-106">\]</span><span class="sxs-lookup"><span data-stu-id="a73aa-106">\]</span></span>

<span data-ttu-id="a73aa-107">Cette rubrique explique comment utiliser MFPlay pour afficher un aperçu de la vidéo d’une caméra vidéo.</span><span class="sxs-lookup"><span data-stu-id="a73aa-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="a73aa-108">MFPlay fournit la manière la plus simple de Microsoft Media Foundation pour afficher un aperçu de la vidéo à partir d’un appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="a73aa-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="a73aa-109">Vous devez utiliser MFPlay si les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="a73aa-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="a73aa-110">Vous n’avez pas besoin de capturer la vidéo dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="a73aa-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="a73aa-111">Vous n’avez pas besoin d’un contrôle affiné sur la façon dont la vidéo est rendue.</span><span class="sxs-lookup"><span data-stu-id="a73aa-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="a73aa-112">(Par exemple, vous n’avez pas besoin de contrôler la création du périphérique Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="a73aa-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="a73aa-113">Vous n’avez pas besoin de traiter les données vidéo de l’appareil photo avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="a73aa-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="a73aa-114">Dans le cas contraire, le [lecteur source](source-reader.md) peut être une meilleure option.</span><span class="sxs-lookup"><span data-stu-id="a73aa-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="a73aa-115">Pour utiliser MFPlay avec un périphérique de capture vidéo, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a73aa-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="a73aa-116">Créez une source de média pour l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="a73aa-116">Create a media source for the capture device.</span></span> <span data-ttu-id="a73aa-117">Consultez [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a73aa-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="a73aa-118">Appelez [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) pour créer une instance de l’objet Player.</span><span class="sxs-lookup"><span data-stu-id="a73aa-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="a73aa-119">Appelez la méthode [**IMFPMediaPlayer :: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) .</span><span class="sxs-lookup"><span data-stu-id="a73aa-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="a73aa-120">Transmettez un pointeur vers l’interface IMFMediaSource de la source du média.</span><span class="sxs-lookup"><span data-stu-id="a73aa-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="a73aa-121">La méthode reçoit un pointeur vers l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="a73aa-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="a73aa-122">Appelez [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span><span class="sxs-lookup"><span data-stu-id="a73aa-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="a73aa-123">Appelez [**IMFPMediaPlayer ::P poser**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) pour commencer l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="a73aa-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="a73aa-124">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="a73aa-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="a73aa-125">Dans une application classique, vous devez fournir un pointeur vers une interface de rappel dans la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) et utiliser l’interface de rappel pour obtenir des événements à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a73aa-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="a73aa-126">Par souci de simplicité, le code présenté ici ignore ces étapes.</span><span class="sxs-lookup"><span data-stu-id="a73aa-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="a73aa-127">Pour plus d’informations, consultez [prise en main avec MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="a73aa-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="a73aa-128">Arrêt en cours</span><span class="sxs-lookup"><span data-stu-id="a73aa-128">Shutting Down</span></span>

<span data-ttu-id="a73aa-129">Avant de quitter l’application, arrêtez la source du média et l’objet lecteur comme suit :</span><span class="sxs-lookup"><span data-stu-id="a73aa-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="a73aa-130">Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="a73aa-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="a73aa-131">Appelez [**IMFPMediaPlayer :: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) sur l’objet Player.</span><span class="sxs-lookup"><span data-stu-id="a73aa-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="a73aa-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a73aa-132">Requirements</span></span>

<span data-ttu-id="a73aa-133">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a73aa-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a73aa-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a73aa-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a73aa-135">MFPlay</span><span class="sxs-lookup"><span data-stu-id="a73aa-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="a73aa-136">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="a73aa-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



