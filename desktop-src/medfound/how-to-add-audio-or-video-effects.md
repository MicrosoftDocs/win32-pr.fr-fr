---
description: Cette rubrique explique comment utiliser des effets audio/video avec MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Comment ajouter des effets audio ou vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519654"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="49814-103">Comment ajouter des effets audio ou vidéo</span><span class="sxs-lookup"><span data-stu-id="49814-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="49814-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="49814-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49814-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="49814-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="49814-106">\]</span><span class="sxs-lookup"><span data-stu-id="49814-106">\]</span></span>

<span data-ttu-id="49814-107">Cette rubrique explique comment utiliser des effets audio/video avec MFPlay.</span><span class="sxs-lookup"><span data-stu-id="49814-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="49814-108">Pour utiliser un effet avec MFPlay, l’effet doit être implémenté en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="49814-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="49814-109">Pour plus d’informations, consultez [Media Foundation transformations](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="49814-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="49814-110">**Pour ajouter un effet audio ou vidéo**</span><span class="sxs-lookup"><span data-stu-id="49814-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="49814-111">Créez une instance de la table MFT qui implémente l’effet.</span><span class="sxs-lookup"><span data-stu-id="49814-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="49814-112">Appelez [**IMFPMediaPlayer :: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span><span class="sxs-lookup"><span data-stu-id="49814-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="49814-113">Appelez [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) avant d’ouvrir le fichier multimédia pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="49814-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="49814-114">MFPlay détermine automatiquement si l’effet est un effet vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="49814-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="49814-115">La méthode [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) prend également un paramètre booléen qui spécifie si l’effet est facultatif ou obligatoire.</span><span class="sxs-lookup"><span data-stu-id="49814-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="49814-116">Si MFPlay ne peut pas ajouter un effet requis (par exemple, parce que le format de flux est incompatible), une erreur de lecture se produit.</span><span class="sxs-lookup"><span data-stu-id="49814-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="49814-117">Dans la plupart des cas, il est préférable de définir un effet comme facultatif.</span><span class="sxs-lookup"><span data-stu-id="49814-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="49814-118">MFPlay continue à utiliser l’effet pour la lecture suivante.</span><span class="sxs-lookup"><span data-stu-id="49814-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="49814-119">Pour supprimer l’effet, appelez [**IMFPMediaPlayer :: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) ou [**IMFPMediaPlayer :: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span><span class="sxs-lookup"><span data-stu-id="49814-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="49814-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49814-120">Requirements</span></span>

<span data-ttu-id="49814-121">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="49814-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49814-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49814-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49814-123">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="49814-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



