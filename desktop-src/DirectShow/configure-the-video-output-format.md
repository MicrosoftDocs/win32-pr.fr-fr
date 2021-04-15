---
description: Configurer le format de sortie vidéo
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurer le format de sortie vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562308"
---
# <a name="configure-the-video-output-format"></a><span data-ttu-id="dd368-103">Configurer le format de sortie vidéo</span><span class="sxs-lookup"><span data-stu-id="dd368-103">Configure the Video Output Format</span></span>

> [!Note]  
> <span data-ttu-id="dd368-104">La fonctionnalité décrite dans cette rubrique est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dd368-104">The functionality described in this topic is deprecated.</span></span> <span data-ttu-id="dd368-105">Pour configurer le format de sortie d’un périphérique de capture, une application doit utiliser la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) renvoyée par [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) dans le paramètre *VPM* .</span><span class="sxs-lookup"><span data-stu-id="dd368-105">To configure a capture device's output format, an application should use the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned by [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in the *pmt* parameter.</span></span>

 

<span data-ttu-id="dd368-106">Un périphérique de capture peut prendre en charge une plage de formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="dd368-106">A capture device can support a range of output formats.</span></span> <span data-ttu-id="dd368-107">Par exemple, un appareil peut prendre en charge les couleurs RVB 16 bits, 32 bits et YUYV.</span><span class="sxs-lookup"><span data-stu-id="dd368-107">For example, a device might support 16-bit RGB, 32-bit RGB, and YUYV.</span></span> <span data-ttu-id="dd368-108">Dans chacun de ces formats, l’appareil peut prendre en charge une plage de tailles d’image.</span><span class="sxs-lookup"><span data-stu-id="dd368-108">Within each of these formats, the device can support a range of frame sizes.</span></span>

<span data-ttu-id="dd368-109">Dans un périphérique WDM, l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) est utilisée pour signaler les formats pris en charge par l’appareil et pour définir le format.</span><span class="sxs-lookup"><span data-stu-id="dd368-109">In a WDM device, the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used to report which formats the device supports, and to set the format.</span></span> <span data-ttu-id="dd368-110">(Pour les appareils VFW hérités, utilisez la boîte de dialogue Format vidéo VFW, comme décrit dans [afficher des boîtes de dialogue de capture VFW](display-vfw-capture-dialog-boxes.md).) L’interface **IAMStreamConfig** est exposée sur le code confidentiel de capture, le code confidentiel de la préversion du filtre de capture ou les deux.</span><span class="sxs-lookup"><span data-stu-id="dd368-110">(For legacy VFW devices, use the Video Format VFW dialog box, as described in [Display VFW Capture Dialog Boxes](display-vfw-capture-dialog-boxes.md).) The **IAMStreamConfig** interface is exposed on the capture filter's capture pin, preview pin, or both.</span></span> <span data-ttu-id="dd368-111">Utilisez la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour accéder au pointeur d’interface :</span><span class="sxs-lookup"><span data-stu-id="dd368-111">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to get the interface pointer:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



<span data-ttu-id="dd368-112">L’appareil dispose d’une liste de types de médias qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="dd368-112">The device has a list of media types that it supports.</span></span> <span data-ttu-id="dd368-113">Pour chaque type de média, l’appareil fournit également un ensemble de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dd368-113">For each media type, the device also provides a set of capabilities.</span></span> <span data-ttu-id="dd368-114">Il s’agit notamment de la plage de tailles d’images disponibles pour ce format, de la façon dont l’appareil peut étirer ou réduire l’image, ainsi que de la plage de fréquences d’images.</span><span class="sxs-lookup"><span data-stu-id="dd368-114">These include the range of frame sizes that are available for that format, how well the device can stretch or shrink the image, and the range of frame rates.</span></span>

<span data-ttu-id="dd368-115">Pour connaître le nombre de types de médias, appelez la méthode [**IAMStreamConfig :: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="dd368-115">To get the number of media types, call the [**IAMStreamConfig::GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) method.</span></span> <span data-ttu-id="dd368-116">La méthode retourne deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="dd368-116">The method returns two values:</span></span>

-   <span data-ttu-id="dd368-117">Nombre de types de médias.</span><span class="sxs-lookup"><span data-stu-id="dd368-117">The number of media types.</span></span>
-   <span data-ttu-id="dd368-118">Taille de la structure qui contient les informations sur les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dd368-118">The size of the structure that holds the capabilities information.</span></span>

<span data-ttu-id="dd368-119">La valeur de taille est nécessaire car l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) est utilisée pour l’audio et la vidéo (et peut être étendue à d’autres types de média).</span><span class="sxs-lookup"><span data-stu-id="dd368-119">The size value is necessary because the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used for both audio and video (and could be extended to other media types).</span></span> <span data-ttu-id="dd368-120">Pour la vidéo, les fonctionnalités sont décrites à l’aide de la structure d' [**\_ \_ \_ embouts de la configuration de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) , tandis que l’audio utilise la structure de la [**\_ configuration de flux \_ \_ audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="dd368-120">For video, the capabilities are described using the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure, while audio uses the [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure.</span></span>

<span data-ttu-id="dd368-121">Pour énumérer les types de média, appelez la méthode [**IAMStreamConfig :: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) avec un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="dd368-121">To enumerate the media types, call the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method with a zero-based index.</span></span> <span data-ttu-id="dd368-122">La méthode **GetStreamCaps** retourne un type de média et la structure de fonctionnalité correspondante :</span><span class="sxs-lookup"><span data-stu-id="dd368-122">The **GetStreamCaps** method returns a media type and the corresponding capability structure:</span></span>


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



<span data-ttu-id="dd368-123">Notez comment les structures sont allouées pour la méthode [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="dd368-123">Note how the structures are allocated for the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="dd368-124">La méthode alloue la structure de type de média, tandis que l’appelant alloue la structure de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dd368-124">The method allocates the media type structure, whereas the caller allocates the capabilities structure.</span></span> <span data-ttu-id="dd368-125">Forcez la structure de fonctionnalités en pointeur de tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="dd368-125">Coerce the capabilities structure to a byte array pointer.</span></span> <span data-ttu-id="dd368-126">Une fois que vous avez terminé avec le type de média, supprimez la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , ainsi que le bloc de format du type de média.</span><span class="sxs-lookup"><span data-stu-id="dd368-126">After you are done with the media type, delete the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, along with the media type's format block.</span></span>

<span data-ttu-id="dd368-127">Vous pouvez configurer l’appareil pour qu’il utilise un format retourné dans la méthode [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="dd368-127">You can configure the device to use a format returned in the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="dd368-128">Appelez simplement [**IAMStreamConfig :: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) avec le type de média :</span><span class="sxs-lookup"><span data-stu-id="dd368-128">Simply call [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) with the media type:</span></span>


```C++
hr = pConfig->SetFormat(pmtConfig);
```



<span data-ttu-id="dd368-129">Si le code pin n’est pas connecté, il tente d’utiliser ce format quand il se connecte.</span><span class="sxs-lookup"><span data-stu-id="dd368-129">If the pin is not connected, it will attempt to use this format when it does connect.</span></span> <span data-ttu-id="dd368-130">Si le code PIN est déjà connecté, il tente de se reconnecter à l’aide du nouveau format.</span><span class="sxs-lookup"><span data-stu-id="dd368-130">If the pin is already connected, it attempts to reconnect using the new format.</span></span> <span data-ttu-id="dd368-131">Dans les deux cas, il est possible que le filtre en aval rejette le format.</span><span class="sxs-lookup"><span data-stu-id="dd368-131">In either case, it is possible that the downstream filter will reject the format.</span></span>

<span data-ttu-id="dd368-132">Vous pouvez également modifier le type de média avant de le passer à la méthode [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) .</span><span class="sxs-lookup"><span data-stu-id="dd368-132">You can also modify the media type before passing it to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method.</span></span> <span data-ttu-id="dd368-133">C’est là qu’intervient la structure de la [**\_ configuration du flux \_ \_ vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="dd368-133">This is where the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure comes in.</span></span> <span data-ttu-id="dd368-134">Il décrit toutes les méthodes valides pour modifier le type de média.</span><span class="sxs-lookup"><span data-stu-id="dd368-134">It describes all of the valid ways to change the media type.</span></span> <span data-ttu-id="dd368-135">Pour utiliser ces informations, vous devez comprendre les détails de ce type de média particulier.</span><span class="sxs-lookup"><span data-stu-id="dd368-135">To use this information, you must understand the details of that particular media type.</span></span>

<span data-ttu-id="dd368-136">Par exemple, supposons que [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retourne un format RGB de 24 bits, avec une taille de trame de 320 x 240 pixels.</span><span class="sxs-lookup"><span data-stu-id="dd368-136">For example, suppose that [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns a 24-bit RGB format, with a frame size of 320 x 240 pixels.</span></span> <span data-ttu-id="dd368-137">Vous pouvez accéder à ces informations en examinant le type principal, le sous-type et le bloc de format du type de média :</span><span class="sxs-lookup"><span data-stu-id="dd368-137">You can get this information by examining the major type, subtype, and format block of the media type:</span></span>


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



<span data-ttu-id="dd368-138">La structure d' [**\_ \_ \_ embouts de la configuration de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) donne la largeur et la hauteur minimales et maximales qui peuvent être utilisées pour ce type de média.</span><span class="sxs-lookup"><span data-stu-id="dd368-138">The [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure gives the minimum and maximum width and height that can be used for this media type.</span></span> <span data-ttu-id="dd368-139">Il vous donne également la taille d’étape, qui définit les incréments par lesquels vous pouvez ajuster la largeur ou la hauteur.</span><span class="sxs-lookup"><span data-stu-id="dd368-139">It also gives you the "step" size, which defines the increments by which you can adjust the width or height.</span></span> <span data-ttu-id="dd368-140">Par exemple, l’appareil peut retourner les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="dd368-140">For example, the device might return the following:</span></span>

-   <span data-ttu-id="dd368-141">MinOutputSize : 160 x 120</span><span class="sxs-lookup"><span data-stu-id="dd368-141">MinOutputSize: 160 x 120</span></span>
-   <span data-ttu-id="dd368-142">MaxOutputSize : 320 x 240</span><span class="sxs-lookup"><span data-stu-id="dd368-142">MaxOutputSize: 320 x 240</span></span>
-   <span data-ttu-id="dd368-143">OutputGranularityX : 8 pixels (taille d’étape horizontale)</span><span class="sxs-lookup"><span data-stu-id="dd368-143">OutputGranularityX: 8 pixels (horizontal step size)</span></span>
-   <span data-ttu-id="dd368-144">OutputGranularityY : 8 pixels (taille d’étape verticale)</span><span class="sxs-lookup"><span data-stu-id="dd368-144">OutputGranularityY: 8 pixels (vertical step size)</span></span>

<span data-ttu-id="dd368-145">À partir de ces nombres, vous pouvez définir la largeur sur n’importe quelle valeur dans la plage (160, 168, 176,... 304, 312, 320) et la hauteur à toute valeur comprise dans la plage (120, 128, 136,... 104, 112, 120).</span><span class="sxs-lookup"><span data-stu-id="dd368-145">Given these numbers, you could set the width to anything in the range (160, 168, 176, ... 304, 312, 320) and the height to anything in the range (120, 128, 136, ... 104, 112, 120).</span></span> <span data-ttu-id="dd368-146">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="dd368-146">The following diagram illustrates this process.</span></span>

![tailles de format vidéo](images/strmcap3.png)

<span data-ttu-id="dd368-148">Pour définir une nouvelle taille de frame, modifiez directement la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) renvoyée dans [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span><span class="sxs-lookup"><span data-stu-id="dd368-148">To set a new frame size, directly modify the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span></span>


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



<span data-ttu-id="dd368-149">Transmettez ensuite le type de média à la méthode [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="dd368-149">Then pass the media type to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method, as described previously.</span></span>

<span data-ttu-id="dd368-150">Les membres **MinFrameInterval** et **MaxFrameInterval** de [**la \_ configuration de flux \_ \_ vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) sont la longueur minimale et maximale de chaque image vidéo, que vous pouvez traduire en fréquences d’images comme suit :</span><span class="sxs-lookup"><span data-stu-id="dd368-150">The **MinFrameInterval** and **MaxFrameInterval** members of [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) are the minimum and maximum length of each video frame, which you can translate into frame rates as follows:</span></span>

`frames per second = 10,000,000 / frame duration`

<span data-ttu-id="dd368-151">Pour demander une fréquence d’images particulière, modifiez la valeur de **AvgTimePerFrame** dans la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="dd368-151">To request a particular frame rate, modify the value of **AvgTimePerFrame** in the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="dd368-152">L’appareil peut ne pas prendre en charge chaque valeur possible comprise entre le minimum et le maximum, de sorte que le pilote utilise la valeur la plus proche possible.</span><span class="sxs-lookup"><span data-stu-id="dd368-152">The device may not support every possible value between the minimum and maximum, so the driver will use the closest value that it can.</span></span> <span data-ttu-id="dd368-153">Pour voir quelle valeur le pilote a réellement utilisé, appelez [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) après avoir appelé [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span><span class="sxs-lookup"><span data-stu-id="dd368-153">To see what value the driver actually used, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) after you call [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span></span>

<span data-ttu-id="dd368-154">Certains pilotes peuvent signaler **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) pour la valeur de **MaxFrameInterval**, ce qui signifie qu’il n’y a pas de durée maximale.</span><span class="sxs-lookup"><span data-stu-id="dd368-154">Some drivers may report **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) for the value of **MaxFrameInterval**, which in effect means there is no maximum duration.</span></span> <span data-ttu-id="dd368-155">Toutefois, vous souhaiterez peut-être appliquer une fréquence d’images minimale dans votre application, par exemple 1 i/s.</span><span class="sxs-lookup"><span data-stu-id="dd368-155">However, you might want to enforce a minimum frame rate in your application, such as 1 fps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd368-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd368-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd368-157">À propos des types de média</span><span class="sxs-lookup"><span data-stu-id="dd368-157">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="dd368-158">Configuration d’un périphérique de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="dd368-158">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



