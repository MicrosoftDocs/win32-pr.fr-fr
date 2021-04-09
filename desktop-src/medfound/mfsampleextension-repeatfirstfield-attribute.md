---
description: Spécifie s’il faut répéter le premier champ dans un frame entrelacé. Cet attribut s’applique aux exemples de supports.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Attribut MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114403"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="37a24-104">\_Attribut MFSampleExtension RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="37a24-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="37a24-105">Spécifie s’il faut répéter le premier champ dans un frame entrelacé.</span><span class="sxs-lookup"><span data-stu-id="37a24-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="37a24-106">Cet attribut s’applique aux exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="37a24-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="37a24-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="37a24-107">Data type</span></span>

<span data-ttu-id="37a24-108">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37a24-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="37a24-109">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="37a24-109">Get/set</span></span>

<span data-ttu-id="37a24-110">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="37a24-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="37a24-111">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="37a24-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="37a24-112">S’applique à</span><span class="sxs-lookup"><span data-stu-id="37a24-112">Applies to</span></span>

[<span data-ttu-id="37a24-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="37a24-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="37a24-114">Notes</span><span class="sxs-lookup"><span data-stu-id="37a24-114">Remarks</span></span>

<span data-ttu-id="37a24-115">Si la valeur est **false** ou si l’attribut n’est pas défini, le premier champ n’est pas répété.</span><span class="sxs-lookup"><span data-stu-id="37a24-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="37a24-116">Si la valeur est **true**, le premier champ est répété.</span><span class="sxs-lookup"><span data-stu-id="37a24-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="37a24-117">La valeur **true** est valide uniquement lorsque les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="37a24-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="37a24-118">Le type de média est mélangé entrelacé et progressif.</span><span class="sxs-lookup"><span data-stu-id="37a24-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="37a24-119">(L’attribut d’attribut [**\_ \_ \_ mode entrelacé MF MT**](mf-mt-interlace-mode-attribute.md) sur le type de média est **MFVideoInterlace \_ MixedInterlaceOrProgressive**.)</span><span class="sxs-lookup"><span data-stu-id="37a24-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="37a24-120">Le frame est progressif et l’attribut [**\_ entrelacé MFSampleExtension**](mfsampleextension-interlaced-attribute.md) sur l’exemple est **true**.</span><span class="sxs-lookup"><span data-stu-id="37a24-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="37a24-121">L’attribut [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) est défini sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="37a24-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="37a24-122">La valeur peut être **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="37a24-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="37a24-123">L’ordre des champs est déterminé par cet attribut.</span><span class="sxs-lookup"><span data-stu-id="37a24-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="37a24-124">Cet attribut est utilisé pour la conversion 3:2.</span><span class="sxs-lookup"><span data-stu-id="37a24-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="37a24-125">Le tableau suivant indique l’ordre dans lequel les champs sont affichés.</span><span class="sxs-lookup"><span data-stu-id="37a24-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="37a24-126">MFSampleExtension \_ RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="37a24-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="37a24-127">MFSampleExtension \_ BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="37a24-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="37a24-128">Ordre des champs</span><span class="sxs-lookup"><span data-stu-id="37a24-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="37a24-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="37a24-129">**TRUE**</span></span>                            | <span data-ttu-id="37a24-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="37a24-130">**TRUE**</span></span>                            | <span data-ttu-id="37a24-131">Inférieur, supérieur, inférieur</span><span class="sxs-lookup"><span data-stu-id="37a24-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="37a24-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="37a24-132">**TRUE**</span></span>                            | <span data-ttu-id="37a24-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="37a24-133">**FALSE**</span></span>                           | <span data-ttu-id="37a24-134">Haut, bas, haut</span><span class="sxs-lookup"><span data-stu-id="37a24-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="37a24-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="37a24-135">**FALSE**</span></span>                           | <span data-ttu-id="37a24-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="37a24-136">**TRUE**</span></span>                            | <span data-ttu-id="37a24-137">Inférieur, supérieur</span><span class="sxs-lookup"><span data-stu-id="37a24-137">Lower, upper</span></span>        |
| <span data-ttu-id="37a24-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="37a24-138">**FALSE**</span></span>                           | <span data-ttu-id="37a24-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="37a24-139">**FALSE**</span></span>                           | <span data-ttu-id="37a24-140">Supérieur, inférieur</span><span class="sxs-lookup"><span data-stu-id="37a24-140">Upper, lower</span></span>        |



 

<span data-ttu-id="37a24-141">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="37a24-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="37a24-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37a24-142">Requirements</span></span>



| <span data-ttu-id="37a24-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37a24-143">Requirement</span></span> | <span data-ttu-id="37a24-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="37a24-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37a24-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37a24-145">Minimum supported client</span></span><br/> | <span data-ttu-id="37a24-146">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="37a24-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="37a24-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37a24-147">Minimum supported server</span></span><br/> | <span data-ttu-id="37a24-148">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="37a24-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="37a24-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="37a24-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="37a24-150"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="37a24-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a24-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37a24-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a24-152">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37a24-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37a24-153">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="37a24-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="37a24-154">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="37a24-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="37a24-155">Entrelacement de vidéos</span><span class="sxs-lookup"><span data-stu-id="37a24-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




