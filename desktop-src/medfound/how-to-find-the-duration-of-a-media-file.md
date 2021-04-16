---
description: Comment rechercher la durée d’un fichier multimédia.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Recherche de la durée d’un fichier multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530502"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Recherche de la durée d’un fichier multimédia

Pour déterminer la durée d’un fichier multimédia, procédez comme suit :

1.  Utilisez le programme de [résolution source](source-resolver.md) pour créer une source de média qui peut analyser le fichier multimédia.
2.  Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source du média. Cette méthode retourne le descripteur de présentation qui décrit le contenu du fichier multimédia.
3.  Interrogez le descripteur de présentation pour l’attribut de [ \_ \_ durée MF PD](mf-pd-duration-attribute.md) en appelant la méthode [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) . La valeur de l’attribut, le cas échéant, est la durée du fichier en unités de 100 nanosecondes.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> </dl>

 

 



