---
description: Spécifie le niveau de mixage, en décibels (dB), dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Propriété AVEncDDProductionMixLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516353"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="78924-104">Propriété AVEncDDProductionMixLevel</span><span class="sxs-lookup"><span data-stu-id="78924-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="78924-105">Spécifie le niveau de mixage, en décibels (dB), dans un flux audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="78924-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="78924-106">Cette propriété s’applique aux encodeurs audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="78924-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="78924-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="78924-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="78924-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="78924-108">Data type</span></span>

<span data-ttu-id="78924-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="78924-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="78924-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="78924-110">Property GUID</span></span>

<span data-ttu-id="78924-111">**CODECAPI \_ AVEncDDProductionMixLevel**</span><span class="sxs-lookup"><span data-stu-id="78924-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="78924-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="78924-112">Property value</span></span>

<span data-ttu-id="78924-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="78924-113">This property has a linear range of values.</span></span> <span data-ttu-id="78924-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="78924-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="78924-115">Notes</span><span class="sxs-lookup"><span data-stu-id="78924-115">Remarks</span></span>

<span data-ttu-id="78924-116">Si vous définissez cette propriété, affectez la valeur **true** à la propriété [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) .</span><span class="sxs-lookup"><span data-stu-id="78924-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78924-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78924-117">Requirements</span></span>



| <span data-ttu-id="78924-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78924-118">Requirement</span></span> | <span data-ttu-id="78924-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="78924-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78924-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78924-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78924-121">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="78924-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="78924-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78924-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78924-123">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="78924-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="78924-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="78924-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="78924-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78924-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78924-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78924-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78924-127">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="78924-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="78924-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="78924-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




