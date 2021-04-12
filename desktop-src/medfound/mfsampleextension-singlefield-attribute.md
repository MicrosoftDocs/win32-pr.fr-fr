---
description: Spécifie si un exemple de vidéo contient un champ unique ou deux champs entrelacés. Cet attribut s’applique aux exemples de supports.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Attribut MFSampleExtension_SingleField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527927"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="8b708-104">\_Attribut MFSampleExtension SingleField</span><span class="sxs-lookup"><span data-stu-id="8b708-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="8b708-105">Spécifie si un exemple de vidéo contient un champ unique ou deux champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="8b708-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="8b708-106">Cet attribut s’applique aux exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="8b708-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b708-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="8b708-107">Data type</span></span>

<span data-ttu-id="8b708-108">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b708-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8b708-109">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8b708-109">Get/set</span></span>

<span data-ttu-id="8b708-110">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8b708-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8b708-111">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8b708-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8b708-112">S’applique à</span><span class="sxs-lookup"><span data-stu-id="8b708-112">Applies to</span></span>

[<span data-ttu-id="8b708-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="8b708-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="8b708-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8b708-114">Remarks</span></span>

<span data-ttu-id="8b708-115">Si la valeur est **true**, l’exemple contient un champ.</span><span class="sxs-lookup"><span data-stu-id="8b708-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="8b708-116">Si la valeur est **false** ou si l’attribut n’est pas défini, l’exemple contient une image complète.</span><span class="sxs-lookup"><span data-stu-id="8b708-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="8b708-117">(Deux champs si entrelacé ou une image progressive.)</span><span class="sxs-lookup"><span data-stu-id="8b708-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="8b708-118">Si le type de média est une trame progressive ou des champs entrelacés, cet attribut doit avoir la **valeur false** ou n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8b708-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="8b708-119">Si le type de média est un champ unique, cet attribut doit avoir la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="8b708-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="8b708-120">Définissez l’attribut [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) sur l’exemple pour indiquer s’il s’agit du champ supérieur ou du champ inférieur.</span><span class="sxs-lookup"><span data-stu-id="8b708-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="8b708-121">Actuellement, le convertisseur vidéo amélioré (EVR) ne prend pas en charge le contenu qui bascule entre les trames entrelacées et les champs uniques.</span><span class="sxs-lookup"><span data-stu-id="8b708-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="8b708-122">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8b708-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b708-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b708-123">Requirements</span></span>



| <span data-ttu-id="8b708-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b708-124">Requirement</span></span> | <span data-ttu-id="8b708-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b708-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b708-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b708-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8b708-127">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b708-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8b708-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b708-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8b708-129">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b708-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8b708-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b708-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b708-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b708-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b708-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b708-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b708-133">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b708-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b708-134">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="8b708-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b708-135">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="8b708-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="8b708-136">Entrelacement de vidéos</span><span class="sxs-lookup"><span data-stu-id="8b708-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




