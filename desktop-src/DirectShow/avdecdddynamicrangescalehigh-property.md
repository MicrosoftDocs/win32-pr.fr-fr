---
description: Spécifie la coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique sur un flux audio Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Propriété AVDecDDDynamicRangeScaleHigh (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482280"
---
# <a name="avdecdddynamicrangescalehigh-property"></a><span data-ttu-id="bc0bc-103">Propriété AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="bc0bc-103">AVDecDDDynamicRangeScaleHigh property</span></span>

<span data-ttu-id="bc0bc-104">Spécifie la coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique sur un flux audio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="bc0bc-104">Specifies the high-level cut when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="bc0bc-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bc0bc-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bc0bc-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="bc0bc-106">Data type</span></span>

<span data-ttu-id="bc0bc-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="bc0bc-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bc0bc-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="bc0bc-108">Property GUID</span></span>

<span data-ttu-id="bc0bc-109">**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="bc0bc-109">**CODECAPI\_AVDecDDDynamicRangeScaleHigh**</span></span>

## <a name="property-value"></a><span data-ttu-id="bc0bc-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bc0bc-110">Property value</span></span>

<span data-ttu-id="bc0bc-111">La valeur de cette propriété est comprise dans la plage suivante.</span><span class="sxs-lookup"><span data-stu-id="bc0bc-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="bc0bc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc0bc-112">Value</span></span> | <span data-ttu-id="bc0bc-113">Description</span><span class="sxs-lookup"><span data-stu-id="bc0bc-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="bc0bc-114">0</span><span class="sxs-lookup"><span data-stu-id="bc0bc-114">0</span></span>     | <span data-ttu-id="bc0bc-115">Aucune compression de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="bc0bc-115">No dynamic range compression.</span></span> <span data-ttu-id="bc0bc-116">Conserver la plage dynamique complète.</span><span class="sxs-lookup"><span data-stu-id="bc0bc-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="bc0bc-117">100</span><span class="sxs-lookup"><span data-stu-id="bc0bc-117">100</span></span>   | <span data-ttu-id="bc0bc-118">Appliquez la compression de plage dynamique complète.</span><span class="sxs-lookup"><span data-stu-id="bc0bc-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="bc0bc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bc0bc-119">Remarks</span></span>

<span data-ttu-id="bc0bc-120">Cette propriété s’applique uniquement lorsque la valeur de la propriété [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) est eAVDecDDOperationalMode \_ .</span><span class="sxs-lookup"><span data-stu-id="bc0bc-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0bc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc0bc-121">Requirements</span></span>



| <span data-ttu-id="bc0bc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc0bc-122">Requirement</span></span> | <span data-ttu-id="bc0bc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc0bc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0bc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc0bc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc0bc-125">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="bc0bc-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bc0bc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc0bc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc0bc-127">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="bc0bc-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bc0bc-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc0bc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc0bc-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bc-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0bc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc0bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0bc-131">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="bc0bc-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bc0bc-132">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="bc0bc-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




