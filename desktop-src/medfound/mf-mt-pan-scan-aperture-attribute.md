---
description: Définit l’ouverture panoramique/numérisation, qui est la 4&\# 215 ; 3 régions de vidéo qui doivent être affichées en mode panoramique/numérisation.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Attribut MF_MT_PAN_SCAN_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521421"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="5136d-103">Attribut d’ouverture de l' \_ \_ analyse panoramique MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="5136d-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="5136d-104">Définit l’ouverture Pan/Scan, qui est la région 4 × 3 de la vidéo qui doit être affichée en mode panoramique/numérisation.</span><span class="sxs-lookup"><span data-stu-id="5136d-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="5136d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5136d-105">Data type</span></span>

<span data-ttu-id="5136d-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="5136d-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5136d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5136d-107">Remarks</span></span>

<span data-ttu-id="5136d-108">La valeur de l’attribut est une structure [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="5136d-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="5136d-109">Cet attribut est utilisé pour rogner la vidéo grand écran avec un proportions de 4:3.</span><span class="sxs-lookup"><span data-stu-id="5136d-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="5136d-110">L’ouverture Pan/Scan est utilisée uniquement en mode panoramique/numérisation, qui est activée en affectant la **valeur true** à l’attribut [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-enabled-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5136d-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="5136d-111">Si le mode panoramique/numérisation n’est pas activé, utilisez l’ouverture d’affichage, spécifiée par l’attribut de l' [**\_ \_ \_ \_ ouverture d’affichage minimum MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5136d-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="5136d-112">Si cet attribut n’est pas défini, l’ouverture Pan/Scan est supposée être la totalité de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="5136d-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="5136d-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5136d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5136d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5136d-114">Requirements</span></span>



| <span data-ttu-id="5136d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5136d-115">Requirement</span></span> | <span data-ttu-id="5136d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5136d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5136d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5136d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5136d-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="5136d-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5136d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5136d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5136d-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5136d-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5136d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5136d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5136d-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5136d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5136d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5136d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5136d-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5136d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5136d-125">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="5136d-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="5136d-126">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="5136d-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="5136d-127">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="5136d-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="5136d-128">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="5136d-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5136d-129">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="5136d-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5136d-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5136d-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5136d-131">**\_ \_ ouverture géométrique MF \_ MF**</span><span class="sxs-lookup"><span data-stu-id="5136d-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="5136d-132">**\_ouverture de \_ l' \_ affichage \_ de la version MF**</span><span class="sxs-lookup"><span data-stu-id="5136d-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="5136d-133">**\_ \_ analyse panoramique MF \_ MT \_ activée**</span><span class="sxs-lookup"><span data-stu-id="5136d-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




