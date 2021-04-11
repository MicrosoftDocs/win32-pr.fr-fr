---
description: Spécifie si un flux d’images ASF est un type JPEG dégradable.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Attribut MF_MT_IMAGE_LOSS_TOLERANT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862746"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="a5603-103">Attribut de tolérance de perte de l' \_ image MT MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a5603-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="a5603-104">Spécifie si un flux d’images ASF est un type JPEG dégradable.</span><span class="sxs-lookup"><span data-stu-id="a5603-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5603-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a5603-105">Data type</span></span>

<span data-ttu-id="a5603-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5603-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a5603-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="a5603-107">Get/set</span></span>

<span data-ttu-id="a5603-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a5603-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a5603-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a5603-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a5603-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="a5603-110">Applies to</span></span>

[<span data-ttu-id="a5603-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a5603-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="a5603-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a5603-112">Remarks</span></span>

<span data-ttu-id="a5603-113">Cet attribut s’applique au type de média pour les flux d’images en ASF.</span><span class="sxs-lookup"><span data-stu-id="a5603-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="a5603-114">Si la valeur est **true**, le flux est un type d’image JPEG dégradable.</span><span class="sxs-lookup"><span data-stu-id="a5603-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="a5603-115">Dans le cas contraire, le flux est un type d’image JFIF.</span><span class="sxs-lookup"><span data-stu-id="a5603-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="a5603-116">Pour plus d’informations sur ces types de flux, consultez la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="a5603-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="a5603-117">En plus de l’attribut de tolérance de perte d’image MF MF \_ \_ \_ \_ , le type de média pour un flux d’images ASF contient les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="a5603-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="a5603-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="a5603-118">Attribute</span></span>                                                 | <span data-ttu-id="a5603-119">Description</span><span class="sxs-lookup"><span data-stu-id="a5603-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="a5603-120">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a5603-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="a5603-121">Contient la valeur de l' **\_ image MFMediaType**.</span><span class="sxs-lookup"><span data-stu-id="a5603-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="a5603-122">**\_taille de \_ trame MF MF \_**</span><span class="sxs-lookup"><span data-stu-id="a5603-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="a5603-123">Donne la taille de l’image en pixels.</span><span class="sxs-lookup"><span data-stu-id="a5603-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="a5603-124">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a5603-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5603-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5603-125">Requirements</span></span>



| <span data-ttu-id="a5603-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5603-126">Requirement</span></span> | <span data-ttu-id="a5603-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5603-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5603-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5603-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5603-129">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a5603-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a5603-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5603-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5603-131">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a5603-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a5603-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5603-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5603-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5603-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5603-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5603-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5603-135">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5603-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5603-136">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="a5603-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




