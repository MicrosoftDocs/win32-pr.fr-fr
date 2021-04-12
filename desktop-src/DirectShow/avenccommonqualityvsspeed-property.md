---
description: Spécifie le compromis entre la qualité et la vitesse du codage. Cette propriété est valide dans tous les modes de contrôle de taux.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propriété AVEncCommonQualityVsSpeed (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109663"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="31f79-104">Propriété AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="31f79-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="31f79-105">Spécifie le compromis entre la qualité et la vitesse du codage.</span><span class="sxs-lookup"><span data-stu-id="31f79-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="31f79-106">Cette propriété est valide dans tous les modes de contrôle de taux.</span><span class="sxs-lookup"><span data-stu-id="31f79-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="31f79-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="31f79-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="31f79-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="31f79-108">Data type</span></span>

<span data-ttu-id="31f79-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="31f79-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="31f79-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="31f79-110">Property GUID</span></span>

<span data-ttu-id="31f79-111">**CODECAPI \_ AVEncCommonQualityVsSpeed**</span><span class="sxs-lookup"><span data-stu-id="31f79-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="31f79-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="31f79-112">Property value</span></span>

<span data-ttu-id="31f79-113">La valeur de cette propriété est comprise dans la plage suivante.</span><span class="sxs-lookup"><span data-stu-id="31f79-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="31f79-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="31f79-114">Value</span></span> | <span data-ttu-id="31f79-115">Description</span><span class="sxs-lookup"><span data-stu-id="31f79-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="31f79-116">0</span><span class="sxs-lookup"><span data-stu-id="31f79-116">0</span></span>     | <span data-ttu-id="31f79-117">Une qualité inférieure, un encodage plus rapide.</span><span class="sxs-lookup"><span data-stu-id="31f79-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="31f79-118">100</span><span class="sxs-lookup"><span data-stu-id="31f79-118">100</span></span>   | <span data-ttu-id="31f79-119">Qualité supérieure, encodage plus lent.</span><span class="sxs-lookup"><span data-stu-id="31f79-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="31f79-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31f79-120">Requirements</span></span>



| <span data-ttu-id="31f79-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31f79-121">Requirement</span></span> | <span data-ttu-id="31f79-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="31f79-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31f79-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31f79-123">Minimum supported client</span></span><br/> | <span data-ttu-id="31f79-124">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="31f79-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="31f79-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31f79-125">Minimum supported server</span></span><br/> | <span data-ttu-id="31f79-126">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="31f79-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="31f79-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="31f79-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f79-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="31f79-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f79-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31f79-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f79-130">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="31f79-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="31f79-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="31f79-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




