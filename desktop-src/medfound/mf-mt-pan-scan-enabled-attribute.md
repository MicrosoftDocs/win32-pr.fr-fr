---
description: Spécifie si le mode panoramique/numérisation est activé.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Attribut MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528755"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="8406c-103">\_Attribut activé pour l' \_ analyse panoramique MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="8406c-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="8406c-104">Spécifie si le mode panoramique/numérisation est activé.</span><span class="sxs-lookup"><span data-stu-id="8406c-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="8406c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8406c-105">Data type</span></span>

<span data-ttu-id="8406c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8406c-106">**UINT32**</span></span>

<span data-ttu-id="8406c-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="8406c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8406c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8406c-108">Remarks</span></span>

<span data-ttu-id="8406c-109">Si cet attribut a la **valeur true**, seule la zone pan/scan de la vidéo doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="8406c-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="8406c-110">La région Pan/Scan est spécifiée par l’attribut d’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8406c-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="8406c-111">Si cet attribut a la **valeur false** ou n’est pas défini, la totalité de l’ouverture de la vidéo doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="8406c-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="8406c-112">L’ouverture d’affichage est spécifiée par l’attribut de l' [**\_ \_ \_ \_ ouverture d’affichage minimum de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8406c-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="8406c-113">Si vous affectez la valeur **true** à cet attribut, définissez également la valeur de l’attribut d’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8406c-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="8406c-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8406c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8406c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8406c-115">Requirements</span></span>



| <span data-ttu-id="8406c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8406c-116">Requirement</span></span> | <span data-ttu-id="8406c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8406c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8406c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8406c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8406c-119">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="8406c-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8406c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8406c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8406c-121">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="8406c-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8406c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8406c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8406c-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8406c-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8406c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8406c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8406c-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8406c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8406c-126">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8406c-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8406c-127">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8406c-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8406c-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8406c-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="8406c-129">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="8406c-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="8406c-130">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="8406c-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




