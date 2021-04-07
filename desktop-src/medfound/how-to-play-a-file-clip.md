---
description: Cette rubrique explique comment lire un segment d’un fichier multimédia dans MFPlay, en définissant les heures de démarrage et d’arrêt pour la lecture.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Lecture d’un clip de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863290"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="29949-103">Lecture d’un clip de fichier</span><span class="sxs-lookup"><span data-stu-id="29949-103">How to Play a File Clip</span></span>

<span data-ttu-id="29949-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="29949-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="29949-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="29949-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="29949-106">\]</span><span class="sxs-lookup"><span data-stu-id="29949-106">\]</span></span>

<span data-ttu-id="29949-107">Cette rubrique explique comment lire un segment d’un fichier multimédia dans MFPlay, en définissant les heures de démarrage et d’arrêt pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="29949-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="29949-108">**Pour lire un clip**</span><span class="sxs-lookup"><span data-stu-id="29949-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="29949-109">Appelez [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer :: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) pour créer un élément multimédia pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="29949-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="29949-110">Si vous le souhaitez, vous pouvez connaître la durée totale du fichier, comme décrit dans [Comment faire pour connaître la durée de lecture](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="29949-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="29949-111">Appelez [**IMFPMediaItem :: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) pour définir les heures de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="29949-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="29949-112">L’heure d’arrêt ne doit pas dépasser la durée du fichier.</span><span class="sxs-lookup"><span data-stu-id="29949-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="29949-113">Appelez [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) pour démarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="29949-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="29949-114">L’exemple suivant utilise la version de blocage de [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="29949-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="29949-115">Si la version non bloquante est utilisée, le code qui apparaît après **CreateMediaItemFromURL** doit être placé dans le gestionnaire pour le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ created** Event.</span><span class="sxs-lookup"><span data-stu-id="29949-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="29949-116">Pour plus d’informations sur les événements dans MFPlay, consultez [réception d’événements à partir du lecteur](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="29949-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="29949-117">Pour connaître la durée du fichier, cet exemple appelle la `GetPlaybackDuration` fonction indiquée dans la rubrique [Comment faire pour connaître la durée de lecture](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="29949-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="29949-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29949-118">Requirements</span></span>

<span data-ttu-id="29949-119">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29949-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29949-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29949-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29949-121">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="29949-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



