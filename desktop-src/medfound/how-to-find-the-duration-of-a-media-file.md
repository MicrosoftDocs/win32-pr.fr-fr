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
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="307a0-103">Recherche de la durée d’un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="307a0-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="307a0-104">Pour déterminer la durée d’un fichier multimédia, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="307a0-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="307a0-105">Utilisez le programme de [résolution source](source-resolver.md) pour créer une source de média qui peut analyser le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="307a0-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="307a0-106">Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="307a0-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="307a0-107">Cette méthode retourne le descripteur de présentation qui décrit le contenu du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="307a0-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="307a0-108">Interrogez le descripteur de présentation pour l’attribut de [ \_ \_ durée MF PD](mf-pd-duration-attribute.md) en appelant la méthode [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) .</span><span class="sxs-lookup"><span data-stu-id="307a0-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="307a0-109">La valeur de l’attribut, le cas échéant, est la durée du fichier en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="307a0-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="307a0-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="307a0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="307a0-111">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="307a0-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



