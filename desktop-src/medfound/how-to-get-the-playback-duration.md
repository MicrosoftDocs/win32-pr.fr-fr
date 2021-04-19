---
description: Cette rubrique explique comment obtenir la durée de lecture d’un fichier multimédia à l’aide de MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Comment connaître la durée de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531822"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="70c24-103">Comment connaître la durée de lecture</span><span class="sxs-lookup"><span data-stu-id="70c24-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="70c24-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="70c24-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="70c24-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70c24-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="70c24-106">\]</span><span class="sxs-lookup"><span data-stu-id="70c24-106">\]</span></span>

<span data-ttu-id="70c24-107">Cette rubrique explique comment obtenir la durée de lecture d’un fichier multimédia à l’aide de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="70c24-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="70c24-108">**Pour connaître la durée de lecture**</span><span class="sxs-lookup"><span data-stu-id="70c24-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="70c24-109">Appelez [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer :: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) pour créer un élément multimédia pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="70c24-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="70c24-110">Appelez [**IMFPMediaItem :: GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span><span class="sxs-lookup"><span data-stu-id="70c24-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="70c24-111">Spécifiez **MFP \_ POSITIONTYPE \_ 100 ns** pour le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="70c24-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="70c24-112">La durée est retournée sous la forme d’un **PROPVARIANT** qui contient une valeur **\_ entière importante** .</span><span class="sxs-lookup"><span data-stu-id="70c24-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="70c24-113">La durée est donnée en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="70c24-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="70c24-114">L’exemple suivant illustre l’étape 2 :</span><span class="sxs-lookup"><span data-stu-id="70c24-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="70c24-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70c24-115">Requirements</span></span>

<span data-ttu-id="70c24-116">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70c24-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70c24-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70c24-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70c24-118">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="70c24-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



