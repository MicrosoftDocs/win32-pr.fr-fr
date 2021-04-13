---
description: Active le traitement vidéo avancé par le lecteur source, notamment la conversion de l’espace colorimétrique, le désentrelacement, le redimensionnement vidéo et la conversion de la fréquence d’images.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Attribut MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525996"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="095b9-103">\_Lecteur source MF-activer l’attribut de \_ \_ \_ \_ traitement vidéo avancé \_</span><span class="sxs-lookup"><span data-stu-id="095b9-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="095b9-104">Active le traitement vidéo avancé par le [lecteur source](source-reader.md), notamment la conversion de l’espace colorimétrique, le désentrelacement, le redimensionnement vidéo et la conversion de la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="095b9-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="095b9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="095b9-105">Data type</span></span>

<span data-ttu-id="095b9-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="095b9-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="095b9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="095b9-107">Remarks</span></span>

<span data-ttu-id="095b9-108">Si cet attribut a la **valeur true**, le lecteur source peut insérer un processeur vidéo dans le pipeline de traitement, ce qui permet les types de conversion de format suivants :</span><span class="sxs-lookup"><span data-stu-id="095b9-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="095b9-109">Conversion de l’espace colorimétrique (YUV en RVB-32)</span><span class="sxs-lookup"><span data-stu-id="095b9-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="095b9-110">Entrelac</span><span class="sxs-lookup"><span data-stu-id="095b9-110">Deinterlacing</span></span>
-   <span data-ttu-id="095b9-111">Redimensionnement vidéo</span><span class="sxs-lookup"><span data-stu-id="095b9-111">Video resizing</span></span>
-   <span data-ttu-id="095b9-112">Conversion de la fréquence des images</span><span class="sxs-lookup"><span data-stu-id="095b9-112">Frame-rate conversion</span></span>

<span data-ttu-id="095b9-113">Si cet attribut a la **valeur true**, l’attribut de [ \_ \_ \_ convertisseurs de désactivation MF ReadWrite](mf-readwrite-disable-converters.md) doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="095b9-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="095b9-114">Le lecteur source recherche les processeurs vidéo inscrits dans la catégorie **du \_ \_ \_ processeur vidéo de catégorie MFT** , y compris les MFTS enregistrés pour le processus local.</span><span class="sxs-lookup"><span data-stu-id="095b9-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="095b9-115">(Pour plus d’informations sur l’inscription locale de MFTs, consultez [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) .) Le lecteur source utilise le processeur vidéo de transcodage (XVP) si aucun autre processeur vidéo approprié n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="095b9-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="095b9-116">L’application spécifie le type de sortie souhaité en appelant [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="095b9-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="095b9-117">Lorsque le lecteur source configure le processeur vidéo, il tente de faire correspondre les attributs suivants du type de sortie :</span><span class="sxs-lookup"><span data-stu-id="095b9-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="095b9-118">Fréquence d’images[( \_ \_ \_ fréquence d’images MF MT](mf-mt-frame-rate-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="095b9-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="095b9-119">Taille de trame ([ \_ \_ \_ taille de trame MF MT](mf-mt-frame-size-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="095b9-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="095b9-120">Mode entrelacé ([ \_ \_ \_ mode entrelacé MF MT](mf-mt-interlace-mode-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="095b9-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="095b9-121">Proportions en pixels (proportions de[ \_ pixels MF MT \_ \_ \_ ](mf-mt-pixel-aspect-ratio-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="095b9-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="095b9-122">SubType (sous-type[MF \_ MT \_ ](mf-mt-subtype-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="095b9-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="095b9-123">Cet attribut est similaire à l' [attribut \_ lecteur source MF activer l’attribut de \_ \_ \_ \_ traitement vidéo](mf-source-reader-enable-video-processing.md) , mais offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="095b9-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="095b9-124">Une plus grande plage de conversions de format est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="095b9-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="095b9-125">Les applications peuvent inscrire leurs propres convertisseurs.</span><span class="sxs-lookup"><span data-stu-id="095b9-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="095b9-126">Certaines conversions peuvent être effectuées dans le matériel à l’aide du GPU.</span><span class="sxs-lookup"><span data-stu-id="095b9-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="095b9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="095b9-127">Requirements</span></span>



| <span data-ttu-id="095b9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="095b9-128">Requirement</span></span> | <span data-ttu-id="095b9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="095b9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="095b9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="095b9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="095b9-131">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="095b9-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="095b9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="095b9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="095b9-133">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="095b9-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="095b9-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="095b9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="095b9-135"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="095b9-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="095b9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="095b9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095b9-137">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="095b9-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="095b9-138">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="095b9-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="095b9-139">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="095b9-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




