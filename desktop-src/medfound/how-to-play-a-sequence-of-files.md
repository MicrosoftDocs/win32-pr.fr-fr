---
description: Cette rubrique explique comment lire une séquence de fichiers audio/vidéo à l’aide de MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Comment lire une séquence de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525009"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="735fb-103">Comment lire une séquence de fichiers</span><span class="sxs-lookup"><span data-stu-id="735fb-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="735fb-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="735fb-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="735fb-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="735fb-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="735fb-106">\]</span><span class="sxs-lookup"><span data-stu-id="735fb-106">\]</span></span>

<span data-ttu-id="735fb-107">Cette rubrique explique comment lire une séquence de fichiers audio/vidéo à l’aide de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="735fb-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="735fb-108">La rubrique [prise en main avec MFPlay](getting-started-with-mfplay.md) montre comment lire un fichier multimédia unique.</span><span class="sxs-lookup"><span data-stu-id="735fb-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="735fb-109">Vous pouvez également utiliser MFPlay pour lire une séquence de fichiers.</span><span class="sxs-lookup"><span data-stu-id="735fb-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="735fb-110">Méthode synchrone (blocage)</span><span class="sxs-lookup"><span data-stu-id="735fb-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="735fb-111">Appelez la méthode [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="735fb-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="735fb-112">La méthode crée un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="735fb-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="735fb-113">Appelez [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) pour la mise en file d’attente de l’élément multimédia pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="735fb-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="735fb-114">Appelez [**IMFPMediaPlayer ::P poser**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) pour démarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="735fb-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="735fb-115">Ces étapes sont présentées dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="735fb-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="735fb-116">La méthode [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="735fb-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="735fb-117">Le premier paramètre est l’URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="735fb-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="735fb-118">Le deuxième paramètre spécifie si la méthode bloque.</span><span class="sxs-lookup"><span data-stu-id="735fb-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="735fb-119">Si vous spécifiez la valeur **true**, comme illustré ici, la méthode est bloquée jusqu’à la création de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="735fb-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="735fb-120">Le troisième paramètre associe une **valeur \_ ptr DWORD** arbitraire à l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="735fb-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="735fb-121">Vous pouvez récupérer cette valeur ultérieurement en appelant [**IMFPMediaItem :: GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span><span class="sxs-lookup"><span data-stu-id="735fb-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="735fb-122">Le quatrième paramètre reçoit un pointeur vers l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="735fb-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="735fb-123">Méthode asynchrone (sans blocage)</span><span class="sxs-lookup"><span data-stu-id="735fb-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="735fb-124">Évitez l’option de blocage si vous appelez [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) à partir de votre thread d’interface utilisateur, car cela peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="735fb-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="735fb-125">En général, la méthode ouvre une connexion de fichier ou réseau et lit suffisamment de données pour analyser les en-têtes de fichier, ce qui peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="735fb-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="735fb-126">Par conséquent, il est généralement préférable d’affecter la valeur **false** au second paramètre.</span><span class="sxs-lookup"><span data-stu-id="735fb-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="735fb-127">Cette option fait en sorte que la méthode s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="735fb-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="735fb-128">Lorsque l’option asynchrone est utilisée, le dernier paramètre doit avoir la **valeur null**:</span><span class="sxs-lookup"><span data-stu-id="735fb-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="735fb-129">Lorsque l’élément multimédia est créé, votre application reçoit un événement de **\_ type MFP \_ \_ MEDIAITEM \_ créé** .</span><span class="sxs-lookup"><span data-stu-id="735fb-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="735fb-130">La structure de données de cet événement contient un pointeur vers l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="735fb-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="735fb-131">Transmettez ce pointeur à la méthode [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) pour la mise en file d’attente de l’élément pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="735fb-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="735fb-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="735fb-132">Requirements</span></span>

<span data-ttu-id="735fb-133">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="735fb-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="735fb-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="735fb-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="735fb-135">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="735fb-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



