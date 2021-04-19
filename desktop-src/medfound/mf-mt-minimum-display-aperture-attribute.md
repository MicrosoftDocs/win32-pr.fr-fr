---
description: Définit l’ouverture d’affichage, qui est la région d’une image vidéo qui contient des données d’image valides.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Attribut MF_MT_MINIMUM_DISPLAY_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516487"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="01623-103">\_Attribut d' \_ \_ ouverture d’affichage \_ de la version MF-minimum</span><span class="sxs-lookup"><span data-stu-id="01623-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="01623-104">Définit l’ouverture d’affichage, qui est la région d’une image vidéo qui contient des données d’image valides.</span><span class="sxs-lookup"><span data-stu-id="01623-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="01623-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="01623-105">Data type</span></span>

<span data-ttu-id="01623-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="01623-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="01623-107">Notes</span><span class="sxs-lookup"><span data-stu-id="01623-107">Remarks</span></span>

<span data-ttu-id="01623-108">La valeur de l’attribut est une structure [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="01623-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="01623-109">L’ouverture d’affichage minimale est la région qui contient la partie valide du signal.</span><span class="sxs-lookup"><span data-stu-id="01623-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="01623-110">Les pixels en dehors de l’ouverture contiennent des données non valides et ne doivent pas être affichés.</span><span class="sxs-lookup"><span data-stu-id="01623-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="01623-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="01623-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="01623-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01623-112">Requirements</span></span>



| <span data-ttu-id="01623-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01623-113">Requirement</span></span> | <span data-ttu-id="01623-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="01623-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01623-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01623-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01623-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="01623-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="01623-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01623-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01623-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="01623-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="01623-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="01623-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="01623-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="01623-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01623-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01623-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01623-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01623-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01623-123">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="01623-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="01623-124">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="01623-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="01623-125">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="01623-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="01623-126">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="01623-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="01623-127">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="01623-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="01623-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="01623-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="01623-129">**\_ \_ ouverture géométrique MF \_ MF**</span><span class="sxs-lookup"><span data-stu-id="01623-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="01623-130">**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**</span><span class="sxs-lookup"><span data-stu-id="01623-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




