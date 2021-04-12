---
description: Spécifie le type de salle pour un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propriété AVEncDDProductionRoomType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109634"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="d5f99-104">Propriété AVEncDDProductionRoomType</span><span class="sxs-lookup"><span data-stu-id="d5f99-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="d5f99-105">Spécifie le type de salle pour un flux audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="d5f99-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="d5f99-106">Cette propriété s’applique aux encodeurs audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="d5f99-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="d5f99-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d5f99-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d5f99-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="d5f99-108">Data type</span></span>

<span data-ttu-id="d5f99-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d5f99-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d5f99-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="d5f99-110">Property GUID</span></span>

<span data-ttu-id="d5f99-111">**CODECAPI \_ AVEncDDProductionRoomType**</span><span class="sxs-lookup"><span data-stu-id="d5f99-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="d5f99-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d5f99-112">Property value</span></span>

<span data-ttu-id="d5f99-113">La valeur de cette propriété est un membre de l’énumération [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .</span><span class="sxs-lookup"><span data-stu-id="d5f99-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f99-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d5f99-114">Remarks</span></span>

<span data-ttu-id="d5f99-115">Le *type de salle* fait référence à la taille de l’espace utilisé pendant la production.</span><span class="sxs-lookup"><span data-stu-id="d5f99-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="d5f99-116">Si vous définissez cette propriété, affectez la valeur **true** à la propriété [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f99-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f99-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5f99-117">Requirements</span></span>



| <span data-ttu-id="d5f99-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5f99-118">Requirement</span></span> | <span data-ttu-id="d5f99-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5f99-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f99-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f99-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f99-121">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d5f99-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d5f99-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f99-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f99-123">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d5f99-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d5f99-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5f99-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f99-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f99-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f99-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5f99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f99-127">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="d5f99-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d5f99-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d5f99-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

