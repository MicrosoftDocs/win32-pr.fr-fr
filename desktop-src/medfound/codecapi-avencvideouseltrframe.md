---
description: Spécifie que le frame actuel est encodé à l’aide d’un ou de plusieurs frames LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749356"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="19ef4-103">CODECAPI \_ propriété AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="19ef4-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="19ef4-104">Spécifie que le frame actuel est encodé à l’aide d’un ou de plusieurs frames LTR.</span><span class="sxs-lookup"><span data-stu-id="19ef4-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="19ef4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="19ef4-105">Data type</span></span>

<span data-ttu-id="19ef4-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="19ef4-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="19ef4-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="19ef4-107">Property GUID</span></span>

<span data-ttu-id="19ef4-108">**CODECAPI \_ AVEncVideoUseLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="19ef4-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="19ef4-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="19ef4-109">Property value</span></span>

<span data-ttu-id="19ef4-110">La valeur de ce contrôle inclut deux champs, où chaque champ a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="19ef4-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19ef4-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="19ef4-111">Value</span></span></th>
<th><span data-ttu-id="19ef4-112">Signification</span><span class="sxs-lookup"><span data-stu-id="19ef4-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="19ef4-113"><dt><strong>Les premiers bits de champ</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="19ef4-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="19ef4-114">Indique le ou les frames LTR autorisés pour l’encodage du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="19ef4-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="19ef4-115"><strong>Encodeurs H. 264/AVC :</strong></span><span class="sxs-lookup"><span data-stu-id="19ef4-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="19ef4-116">Il s’agit d’une image bitmap qui indique les cadres LTR qui peuvent être utilisés comme référence pour ce frame.</span><span class="sxs-lookup"><span data-stu-id="19ef4-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="19ef4-117">Le bit le moins significatif correspond à l’index LTR 0, le deuxième bit le moins significatif correspond à l’index 1 LTR, etc.</span><span class="sxs-lookup"><span data-stu-id="19ef4-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="19ef4-118">Cette valeur ne doit pas être égale à 0.</span><span class="sxs-lookup"><span data-stu-id="19ef4-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="19ef4-119">L’index le plus élevé spécifié par cette valeur ne doit pas être supérieur au nombre maximal de cadres LTR spécifié dans la propriété <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> moins un.</span><span class="sxs-lookup"><span data-stu-id="19ef4-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="19ef4-120"><dt><strong>Deuxième bits de champ</strong></dt> <dt>[16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="19ef4-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="19ef4-121">Indicateur qui spécifie si des limitations supplémentaires sont requises pour l’encodage des frames suivants.</span><span class="sxs-lookup"><span data-stu-id="19ef4-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="19ef4-122"><strong>Encodeurs H. 264/AVC :</strong></span><span class="sxs-lookup"><span data-stu-id="19ef4-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="19ef4-123">1 est la seule valeur valide pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="19ef4-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="19ef4-124">Toutes les autres valeurs sont non valides et réservées pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="19ef4-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="19ef4-125">Lorsque l’indicateur a la valeur 1, l’encodeur doit encoder les frames suivants dans l’ordre d’encodage selon les contraintes suivantes :</span><span class="sxs-lookup"><span data-stu-id="19ef4-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="19ef4-126">Elle n’utilise pas les frames de référence à long terme dans l’ordre de codage antérieur à l’image actuelle ou l’encodage futur dans l’ordre de codage.</span><span class="sxs-lookup"><span data-stu-id="19ef4-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="19ef4-127">Il ne doit pas utiliser les cadres LTR non décrits par le dernier contrôle de CODECAPI_AVEncVideoUseLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="19ef4-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="19ef4-128">Elle peut utiliser des images LTR mises à jour après le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="19ef4-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="19ef4-129">Notes</span><span class="sxs-lookup"><span data-stu-id="19ef4-129">Remarks</span></span>

<span data-ttu-id="19ef4-130">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="19ef4-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="19ef4-131">Cette propriété ne doit pas être appelée si un appel en attente d’utilisation d’un frame LTR a été émis à l’aide de la \_ propriété CODECAPI AVEncVideoUseLTRFrame et que l’encodeur n’a pas encore généré de frame qui a utilisé le LTR.</span><span class="sxs-lookup"><span data-stu-id="19ef4-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="19ef4-132">En d’autres termes, l’encodeur ne doit pas faire remonter les \_ demandes CODECAPI AVEncVideoUseLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="19ef4-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="19ef4-133">Si une \_ demande CODECAPI AVEncVideoUseLTRFrame est soumise alors qu’une autre \_ demande de AVEncVideoUseLTRFrame CODECAPI est toujours en attente, la demande plus ancienne doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="19ef4-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="19ef4-134">L’appel de CODECAPI \_ AVEncVideoUseLTRFrame sur un frame de couche non-base est valide et s’applique au frame de couche non-base, sans délai, à un frame de couche de base.</span><span class="sxs-lookup"><span data-stu-id="19ef4-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ef4-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19ef4-135">Requirements</span></span>



| <span data-ttu-id="19ef4-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19ef4-136">Requirement</span></span> | <span data-ttu-id="19ef4-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="19ef4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19ef4-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19ef4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="19ef4-139">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="19ef4-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="19ef4-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19ef4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="19ef4-141">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="19ef4-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="19ef4-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="19ef4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ef4-143"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ef4-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ef4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19ef4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ef4-145">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19ef4-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




