---
description: Définit l’ouverture géométrique d’un type de média vidéo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Attribut MF_MT_GEOMETRIC_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951534"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="6c0d8-103">\_Attribut d' \_ ouverture géométrique MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6c0d8-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="6c0d8-104">Définit l’ouverture géométrique d’un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c0d8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6c0d8-105">Data type</span></span>

<span data-ttu-id="6c0d8-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="6c0d8-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="6c0d8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6c0d8-107">Remarks</span></span>

<span data-ttu-id="6c0d8-108">La valeur de cet attribut est une structure [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="6c0d8-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="6c0d8-109">Les proportions de l’image sont calculées par rapport à l’ouverture géométrique, à l’aide de la formule suivante : proportions de l’image = (largeur d’ouverture géométrique/hauteur d’ouverture géométrique) × proportions de pixels.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="6c0d8-110">Si cet attribut n’est pas défini, l’ouverture géométrique est supposée être la totalité de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="6c0d8-111">Vous devez définir cet attribut uniquement lorsque le type de média décrit une norme vidéo avec une zone active définie.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="6c0d8-112">Par exemple, dans la télévision NTSC, le cadre vidéo est 720 × 480 avec une zone active de 704 × 480 et un rapport hauteur/largeur des pixels de 10:11.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="6c0d8-113">L’image résultante a un rapport hauteur/largeur de (704/480) × (10/11) = 4:3.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="6c0d8-114">Le présentateur par défaut pour le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) affiche l’ouverture géométrique de la vidéo, si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="6c0d8-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="6c0d8-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="6c0d8-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="6c0d8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c0d8-117">Requirements</span></span>



| <span data-ttu-id="6c0d8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c0d8-118">Requirement</span></span> | <span data-ttu-id="6c0d8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c0d8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0d8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c0d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0d8-121">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="6c0d8-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6c0d8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c0d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0d8-123">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="6c0d8-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6c0d8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c0d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c0d8-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c0d8-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c0d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c0d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0d8-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6c0d8-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c0d8-128">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6c0d8-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c0d8-129">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="6c0d8-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="6c0d8-130">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="6c0d8-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="6c0d8-131">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6c0d8-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6c0d8-132">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="6c0d8-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6c0d8-133">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6c0d8-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6c0d8-134">**\_ouverture de \_ l' \_ affichage \_ de la version MF**</span><span class="sxs-lookup"><span data-stu-id="6c0d8-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="6c0d8-135">**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**</span><span class="sxs-lookup"><span data-stu-id="6c0d8-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




