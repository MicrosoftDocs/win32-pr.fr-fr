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
# <a name="setting-the-group-media-type"></a>Définition du type de support de groupe

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Tous les groupes doivent définir un type de média non compressé, audio ou vidéo. Le type de média non compressé est le format que les observateurs voient ou entendent pendant la lecture. En règle générale, le résultat final est dans un format compressé. Pour plus d’informations, consultez [rendu d’un projet](rendering-a-project.md).

Pour définir le format non compressé, créez une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) et remplissez-la avec le type principal, le sous-type et l’en-tête de format appropriés. Pour la vidéo, allouez une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour le bloc de format et définissez la largeur, la hauteur et la profondeur de bit. Pour l’audio, allouez une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) pour le bloc de format et définissez le taux d’échantillonnage, la profondeur de bit et le nombre de canaux. Si vous ne définissez que le type principal, l’algorithme DES fournit des valeurs par défaut raisonnables pour les autres valeurs. Dans la pratique, vous devez définir les valeurs explicitement pour contrôler la sortie.

Après l’initialisation de la structure du type de média, appelez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) pour définir le type de média pour le groupe.

L’exemple suivant spécifie une vidéo RGB de 16 bits, 320 pixels de large par 240 pixels de haut :


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



L’exemple suivant spécifie un groupe audio, en définissant le type de support de groupe sur stéréo 16 bits, 44100 échantillons par seconde :


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



Vous pouvez également utiliser la classe [**CMediaType**](cmediatype.md) dans les [classes de base DirectShow](directshow-base-classes.md) pour gérer les types de médias. Elle contient des méthodes d’assistance utiles et libère automatiquement le bloc de format.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des types de média](about-media-types.md)
</dt> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 
