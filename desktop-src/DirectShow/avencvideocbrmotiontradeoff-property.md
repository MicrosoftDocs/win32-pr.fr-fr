---
description: Spécifie le compromis entre le mouvement et les images fixes. Cette propriété s’applique uniquement au mode de contrôle CBR (constant bit rate).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propriété AVEncVideoCBRMotionTradeoff (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950281"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="a1a35-104">Propriété AVEncVideoCBRMotionTradeoff</span><span class="sxs-lookup"><span data-stu-id="a1a35-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="a1a35-105">Spécifie le compromis entre le mouvement et les images fixes.</span><span class="sxs-lookup"><span data-stu-id="a1a35-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="a1a35-106">Cette propriété s’applique uniquement au mode de contrôle CBR (constant bit rate).</span><span class="sxs-lookup"><span data-stu-id="a1a35-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="a1a35-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a1a35-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a1a35-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="a1a35-108">Data type</span></span>

<span data-ttu-id="a1a35-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a1a35-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a1a35-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="a1a35-110">Property GUID</span></span>

<span data-ttu-id="a1a35-111">**CODECAPI \_ AVEncVideoCBRMotionTradeoff**</span><span class="sxs-lookup"><span data-stu-id="a1a35-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="a1a35-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a1a35-112">Property value</span></span>

<span data-ttu-id="a1a35-113">La valeur de cette propriété est comprise dans la plage suivante.</span><span class="sxs-lookup"><span data-stu-id="a1a35-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="a1a35-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1a35-114">Value</span></span> | <span data-ttu-id="a1a35-115">Description</span><span class="sxs-lookup"><span data-stu-id="a1a35-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="a1a35-116">0</span><span class="sxs-lookup"><span data-stu-id="a1a35-116">0</span></span>     | <span data-ttu-id="a1a35-117">Optimiser pour les images fixes</span><span class="sxs-lookup"><span data-stu-id="a1a35-117">Optimize for still images</span></span> |
| <span data-ttu-id="a1a35-118">100</span><span class="sxs-lookup"><span data-stu-id="a1a35-118">100</span></span>   | <span data-ttu-id="a1a35-119">Optimisez le mouvement.</span><span class="sxs-lookup"><span data-stu-id="a1a35-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="a1a35-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1a35-120">Requirements</span></span>



| <span data-ttu-id="a1a35-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1a35-121">Requirement</span></span> | <span data-ttu-id="a1a35-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1a35-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a35-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1a35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a35-124">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a1a35-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a1a35-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1a35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a35-126">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a1a35-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a1a35-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1a35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1a35-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a35-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1a35-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1a35-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a35-130">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="a1a35-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a1a35-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a1a35-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




