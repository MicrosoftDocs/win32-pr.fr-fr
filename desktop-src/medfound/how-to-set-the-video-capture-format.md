---
description: Un périphérique de capture vidéo peut prendre en charge plusieurs formats de capture. Les formats sont généralement différents selon le type de compression, l’espace colorimétrique (YUV ou RVB), la taille du cadre ou la fréquence d’images.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Comment définir le format de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519056"
---
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="c1a07-104">Comment définir le format de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="c1a07-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="c1a07-105">Un périphérique de capture vidéo peut prendre en charge plusieurs formats de capture.</span><span class="sxs-lookup"><span data-stu-id="c1a07-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="c1a07-106">Les formats sont généralement différents selon le type de compression, l’espace colorimétrique (YUV ou RVB), la taille du cadre ou la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="c1a07-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="c1a07-107">La liste des formats pris en charge est contenue dans le *descripteur de présentation*.</span><span class="sxs-lookup"><span data-stu-id="c1a07-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="c1a07-108">Pour plus d’informations, consultez [descripteurs de présentation](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="c1a07-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="c1a07-109">Pour énumérer les formats pris en charge :</span><span class="sxs-lookup"><span data-stu-id="c1a07-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="c1a07-110">Créez la source du média pour l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="c1a07-110">Create the media source for the capture device.</span></span> <span data-ttu-id="c1a07-111">Consultez [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="c1a07-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="c1a07-112">Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source du média pour récupérer le descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="c1a07-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="c1a07-113">Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour obtenir le descripteur de flux du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c1a07-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="c1a07-114">Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="c1a07-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="c1a07-115">Appelez [**IMFMediaTypeHandler :: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) pour connaître le nombre de formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c1a07-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="c1a07-116">Dans une boucle, appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) pour obtenir chaque format.</span><span class="sxs-lookup"><span data-stu-id="c1a07-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="c1a07-117">Le format est représenté par un *type de média*.</span><span class="sxs-lookup"><span data-stu-id="c1a07-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="c1a07-118">Pour plus d’informations, consultez [Video Media types](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="c1a07-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="c1a07-119">L’exemple suivant énumère les formats de capture d’un appareil :</span><span class="sxs-lookup"><span data-stu-id="c1a07-119">The following example enumerates the capture formats for a device:</span></span>


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="c1a07-120">La `LogMediaType` fonction utilisée dans cet exemple est indiquée dans la rubrique [Code de débogage du type de média](media-type-debugging-code.md).</span><span class="sxs-lookup"><span data-stu-id="c1a07-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="c1a07-121">Pour définir le format de capture :</span><span class="sxs-lookup"><span data-stu-id="c1a07-121">To set the capture format:</span></span>

1.  <span data-ttu-id="c1a07-122">Obtenir un pointeur vers l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="c1a07-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="c1a07-123">Appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) pour connaître le format souhaité, spécifié par index.</span><span class="sxs-lookup"><span data-stu-id="c1a07-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="c1a07-124">Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) pour définir le format.</span><span class="sxs-lookup"><span data-stu-id="c1a07-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="c1a07-125">Si vous ne définissez pas le format de capture, l’appareil utilise son format par défaut.</span><span class="sxs-lookup"><span data-stu-id="c1a07-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="c1a07-126">L’exemple suivant définit le format de capture :</span><span class="sxs-lookup"><span data-stu-id="c1a07-126">The following example sets the capture format:</span></span>


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="c1a07-127">L’ordre dans lequel les formats sont retournés dépend de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c1a07-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="c1a07-128">En règle générale, ils sont regroupés tout d’abord par type de compression ou espace colorimétrique. et de la taille d’image la plus petite à la plus grande taille de trame au sein de chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="c1a07-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="c1a07-129">La fréquence d’images est traitée légèrement différemment des autres attributs de format.</span><span class="sxs-lookup"><span data-stu-id="c1a07-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="c1a07-130">Pour plus d’informations, consultez [comment définir la fréquence d’images de capture vidéo](how-to-set-the-video-capture-frame-rate.md).</span><span class="sxs-lookup"><span data-stu-id="c1a07-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="c1a07-131">Dans certains appareils, la liste format contient une entrée dupliquée pour chaque format.</span><span class="sxs-lookup"><span data-stu-id="c1a07-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="c1a07-132">Par exemple, si l’appareil prend en charge 15 formats de capture distincts, la liste contiendra 30 entrées.</span><span class="sxs-lookup"><span data-stu-id="c1a07-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="c1a07-133">Au sein de chaque paire, l’un des types de média aura [**le \_ \_ type de \_ format \_ de fichier MF MT**](mf-mt-am-format-type-attribute.md) d’attribut égal au **format \_ videoinfo**, et l’autre aura un type de **\_ \_ format de AM \_ \_ MT MF** égal au **format \_ VideoInfo2**.</span><span class="sxs-lookup"><span data-stu-id="c1a07-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="c1a07-134">(Ces deux valeurs sont définies dans le fichier d’en-tête UUID. h.) Le deuxième type peut également contenir des informations supplémentaires sur la couleur ([informations sur la couleur étendue](extended-color-information.md)) ou afficher une valeur différente pour l’entrelacement ([**\_ \_ \_ mode entrelacé MF MT**](mf-mt-interlace-mode-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="c1a07-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="c1a07-135">Ces types dupliqués sont disponibles pour prendre en charge les anciennes applications DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c1a07-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="c1a07-136">Dans une application Media Foundation, vous devez ignorer le **format \_ videoinfo** type chaque fois qu’un type **\_ VideoInfo2 de format** dupliqué est listé.</span><span class="sxs-lookup"><span data-stu-id="c1a07-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c1a07-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1a07-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1a07-138">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="c1a07-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



