---
description: Un périphérique de capture vidéo peut prendre en charge une plage de fréquences d’images.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Comment définir la fréquence d’images de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519781"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="fd9ee-103">Comment définir la fréquence d’images de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="fd9ee-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="fd9ee-104">Un périphérique de capture vidéo peut prendre en charge une plage de fréquences d’images.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="fd9ee-105">Si ces informations sont disponibles, les fréquences d’images minimale et maximale sont stockées en tant qu’attributs de type de média :</span><span class="sxs-lookup"><span data-stu-id="fd9ee-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="fd9ee-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="fd9ee-106">Attribute</span></span>                                                         | <span data-ttu-id="fd9ee-107">Description</span><span class="sxs-lookup"><span data-stu-id="fd9ee-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="fd9ee-108">\_plage de \_ fréquence d’images MF MT \_ \_ \_ Max</span><span class="sxs-lookup"><span data-stu-id="fd9ee-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="fd9ee-109">Fréquence d’images maximale.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="fd9ee-110">plage de fréquence d’images MF- \_ \_ \_ \_ \_ min</span><span class="sxs-lookup"><span data-stu-id="fd9ee-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="fd9ee-111">Fréquence d’images minimale.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="fd9ee-112">La plage peut varier en fonction du format de capture.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="fd9ee-113">Par exemple, avec des tailles d’image supérieures, la fréquence d’images maximale peut être réduite.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="fd9ee-114">Pour définir la fréquence d’images :</span><span class="sxs-lookup"><span data-stu-id="fd9ee-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="fd9ee-115">Créez la source du média pour l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-115">Create the media source for the capture device.</span></span> <span data-ttu-id="fd9ee-116">Consultez [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="fd9ee-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="fd9ee-117">Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source du média pour récupérer le descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="fd9ee-118">Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour obtenir le descripteur de flux du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="fd9ee-119">Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="fd9ee-120">Énumérez les formats de capture, comme décrit dans [comment définir le format de capture vidéo](how-to-set-the-video-capture-format.md).</span><span class="sxs-lookup"><span data-stu-id="fd9ee-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="fd9ee-121">Sélectionnez le format de sortie souhaité dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="fd9ee-122">Interrogez le type de média pour les attributs de plage de fréquence d’images [MF \_ MT \_ \_ \_ \_ Max](mf-mt-frame-rate-range-max.md) et [MF à \_ \_ \_ fréquence d' \_ \_ images MF](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="fd9ee-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="fd9ee-123">Ces valeurs donnent la plage de fréquences d’images prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="fd9ee-124">L’appareil peut prendre en charge d’autres fréquences d’images dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="fd9ee-125">Définissez l’attribut de [**\_ \_ Frame MT MF**](mf-mt-frame-rate-attribute.md) sur le type de média pour spécifier la fréquence d’images souhaitée.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="fd9ee-126">Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) avec le type de média modifié.</span><span class="sxs-lookup"><span data-stu-id="fd9ee-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="fd9ee-127">L’exemple suivant définit la fréquence d’images égale à la fréquence d’images maximale prise en charge par l’appareil :</span><span class="sxs-lookup"><span data-stu-id="fd9ee-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fd9ee-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd9ee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd9ee-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="fd9ee-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



