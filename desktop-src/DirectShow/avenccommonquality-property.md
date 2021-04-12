---
description: Spécifie le niveau de qualité pour l’encodage.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propriété AVEncCommonQuality (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482512"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="fd0eb-103">Propriété AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="fd0eb-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="fd0eb-104">Spécifie le niveau de qualité pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="fd0eb-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd0eb-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="fd0eb-106">Data type</span></span>

<span data-ttu-id="fd0eb-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fd0eb-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fd0eb-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="fd0eb-108">Property GUID</span></span>

<span data-ttu-id="fd0eb-109">**CODECAPI \_ AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="fd0eb-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fd0eb-110">Property value</span></span>

<span data-ttu-id="fd0eb-111">La valeur de cette propriété est comprise dans la plage suivante.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="fd0eb-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd0eb-112">Value</span></span> | <span data-ttu-id="fd0eb-113">Description</span><span class="sxs-lookup"><span data-stu-id="fd0eb-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="fd0eb-114">0</span><span class="sxs-lookup"><span data-stu-id="fd0eb-114">0</span></span>     | <span data-ttu-id="fd0eb-115">Qualité minimale, taille de sortie inférieure.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="fd0eb-116">100</span><span class="sxs-lookup"><span data-stu-id="fd0eb-116">100</span></span>   | <span data-ttu-id="fd0eb-117">Qualité maximale, taille de sortie supérieure.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="fd0eb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fd0eb-118">Remarks</span></span>

<span data-ttu-id="fd0eb-119">Cette propriété contrôle le niveau de qualité lorsque l’encodeur n’utilise pas une vitesse de transmission avec restriction.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="fd0eb-120">La propriété [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) détermine si la vitesse de transmission est restreinte.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0eb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd0eb-121">Requirements</span></span>



| <span data-ttu-id="fd0eb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd0eb-122">Requirement</span></span> | <span data-ttu-id="fd0eb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd0eb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0eb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd0eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0eb-125">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="fd0eb-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fd0eb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd0eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0eb-127">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="fd0eb-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fd0eb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd0eb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0eb-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0eb-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0eb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd0eb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0eb-131">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="fd0eb-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fd0eb-132">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




