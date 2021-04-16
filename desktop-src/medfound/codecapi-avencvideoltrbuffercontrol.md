---
description: Spécifie le nombre maximal de cadres de référence à long terme (LTR) contrôlés par l’application.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524631"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="5a324-103">CODECAPI \_ propriété AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="5a324-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="5a324-104">Spécifie le nombre maximal de cadres de référence à long terme (LTR) contrôlés par l’application.</span><span class="sxs-lookup"><span data-stu-id="5a324-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="5a324-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5a324-105">Data type</span></span>

<span data-ttu-id="5a324-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="5a324-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5a324-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="5a324-107">Property GUID</span></span>

<span data-ttu-id="5a324-108">**CODECAPI \_ AVEncVideoLTRBufferControl**</span><span class="sxs-lookup"><span data-stu-id="5a324-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="5a324-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5a324-109">Property value</span></span>

<span data-ttu-id="5a324-110">La valeur de ce contrôle inclut deux champs, où chaque champ a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5a324-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a324-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a324-111">Value</span></span></th>
<th><span data-ttu-id="5a324-112">Signification</span><span class="sxs-lookup"><span data-stu-id="5a324-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="5a324-113"><dt><strong>Les premiers bits de champ</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="5a324-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="5a324-114">Nombre de cadres LTR contrôlés par l’application.</span><span class="sxs-lookup"><span data-stu-id="5a324-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="5a324-115"><strong>Encodeurs H. 264/AVC :</strong></span><span class="sxs-lookup"><span data-stu-id="5a324-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="5a324-116">En supposant que la valeur est N et que N est une valeur différente de zéro, à chaque image de la base de connaissances, l’encodeur doit automatiquement marquer les frames qui suivent la trame de la base de connaissances (et inclure le cadre de la base de demande) comme des cadres LTR, à condition que les 3 des éléments suivants s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="5a324-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="5a324-117">Le cadre n’est pas déjà défini pour être marqué comme cadre de référence à long terme.</span><span class="sxs-lookup"><span data-stu-id="5a324-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="5a324-118">Le cadre est un cadre de couche de base.</span><span class="sxs-lookup"><span data-stu-id="5a324-118">The frame is a base layer frame.</span></span> <span data-ttu-id="5a324-119">Par exemple, l’élément de syntaxe <strong>temporal_id</strong> égal à 0.</span><span class="sxs-lookup"><span data-stu-id="5a324-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="5a324-120">Le nombre de frames actuellement marqués comme LTR est inférieur à N.</span><span class="sxs-lookup"><span data-stu-id="5a324-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="5a324-121"><dt><strong>Deuxième bits de champ</strong></dt> <dt>[16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="5a324-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="5a324-122">Mode d’approbation du contrôle LTR.</span><span class="sxs-lookup"><span data-stu-id="5a324-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="5a324-123"><strong>Encodeurs H. 264/AVC :</strong></span><span class="sxs-lookup"><span data-stu-id="5a324-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="5a324-124">1 (confiance jusqu’à) signifie que l’encodeur peut utiliser un frame LTR, sauf si l’application l’invalide explicitement via le contrôle <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> .</span><span class="sxs-lookup"><span data-stu-id="5a324-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="5a324-125">Les autres valeurs ne sont pas valides et réservées pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5a324-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="5a324-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5a324-126">Remarks</span></span>

<span data-ttu-id="5a324-127">Il s’agit d’une API statique.</span><span class="sxs-lookup"><span data-stu-id="5a324-127">This is a static API.</span></span>

<span data-ttu-id="5a324-128">La valeur par défaut doit être 0</span><span class="sxs-lookup"><span data-stu-id="5a324-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="5a324-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a324-129">Requirements</span></span>



| <span data-ttu-id="5a324-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a324-130">Requirement</span></span> | <span data-ttu-id="5a324-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a324-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a324-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a324-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5a324-133">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a324-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="5a324-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a324-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5a324-135">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a324-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5a324-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a324-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a324-137"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a324-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a324-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a324-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a324-139">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a324-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




