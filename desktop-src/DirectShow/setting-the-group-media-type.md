---
description: Définition du type de support de groupe
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Définition du type de support de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539389"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="8d137-103">Définition du type de support de groupe</span><span class="sxs-lookup"><span data-stu-id="8d137-103">Setting the Group Media Type</span></span>

<span data-ttu-id="8d137-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="8d137-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8d137-105">Tous les groupes doivent définir un type de média non compressé, audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="8d137-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="8d137-106">Le type de média non compressé est le format que les observateurs voient ou entendent pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="8d137-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="8d137-107">En règle générale, le résultat final est dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="8d137-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="8d137-108">Pour plus d’informations, consultez [rendu d’un projet](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="8d137-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="8d137-109">Pour définir le format non compressé, créez une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) et remplissez-la avec le type principal, le sous-type et l’en-tête de format appropriés.</span><span class="sxs-lookup"><span data-stu-id="8d137-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="8d137-110">Pour la vidéo, allouez une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour le bloc de format et définissez la largeur, la hauteur et la profondeur de bit.</span><span class="sxs-lookup"><span data-stu-id="8d137-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="8d137-111">Pour l’audio, allouez une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) pour le bloc de format et définissez le taux d’échantillonnage, la profondeur de bit et le nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="8d137-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="8d137-112">Si vous ne définissez que le type principal, l’algorithme DES fournit des valeurs par défaut raisonnables pour les autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="8d137-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="8d137-113">Dans la pratique, vous devez définir les valeurs explicitement pour contrôler la sortie.</span><span class="sxs-lookup"><span data-stu-id="8d137-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="8d137-114">Après l’initialisation de la structure du type de média, appelez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) pour définir le type de média pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="8d137-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="8d137-115">L’exemple suivant spécifie une vidéo RGB de 16 bits, 320 pixels de large par 240 pixels de haut :</span><span class="sxs-lookup"><span data-stu-id="8d137-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



<span data-ttu-id="8d137-116">L’exemple suivant spécifie un groupe audio, en définissant le type de support de groupe sur stéréo 16 bits, 44100 échantillons par seconde :</span><span class="sxs-lookup"><span data-stu-id="8d137-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



<span data-ttu-id="8d137-117">Vous pouvez également utiliser la classe [**CMediaType**](cmediatype.md) dans les [classes de base DirectShow](directshow-base-classes.md) pour gérer les types de médias.</span><span class="sxs-lookup"><span data-stu-id="8d137-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="8d137-118">Elle contient des méthodes d’assistance utiles et libère automatiquement le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="8d137-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d137-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d137-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d137-120">À propos des types de média</span><span class="sxs-lookup"><span data-stu-id="8d137-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="8d137-121">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="8d137-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
