---
description: Spécifie le type de filtre de désaccentuation à utiliser lors du décodage. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Propriété AVEncMPAEmphasisType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515538"
---
# <a name="avencmpaemphasistype-property"></a><span data-ttu-id="3fb1e-104">Propriété AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="3fb1e-104">AVEncMPAEmphasisType property</span></span>

<span data-ttu-id="3fb1e-105">Spécifie le type de filtre de désaccentuation à utiliser lors du décodage.</span><span class="sxs-lookup"><span data-stu-id="3fb1e-105">Specifies the type of de-emphasis filter that should be used when decoding.</span></span> <span data-ttu-id="3fb1e-106">Cette propriété s’applique aux encodeurs audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="3fb1e-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="3fb1e-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3fb1e-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3fb1e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="3fb1e-108">Data type</span></span>

<span data-ttu-id="3fb1e-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="3fb1e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3fb1e-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="3fb1e-110">Property GUID</span></span>

<span data-ttu-id="3fb1e-111">**CODECAPI \_ AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="3fb1e-111">**CODECAPI\_AVEncMPAEmphasisType**</span></span>

## <a name="property-value"></a><span data-ttu-id="3fb1e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3fb1e-112">Property value</span></span>

<span data-ttu-id="3fb1e-113">La valeur de cette propriété est un membre de l’énumération [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .</span><span class="sxs-lookup"><span data-stu-id="3fb1e-113">The value of this property is a member of the [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb1e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3fb1e-114">Remarks</span></span>

<span data-ttu-id="3fb1e-115">Cette propriété définit les bits d’accentuation dans l’en-tête du frame.</span><span class="sxs-lookup"><span data-stu-id="3fb1e-115">This property sets the emphasis bits in the frame header.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb1e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fb1e-116">Requirements</span></span>



| <span data-ttu-id="3fb1e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fb1e-117">Requirement</span></span> | <span data-ttu-id="3fb1e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fb1e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb1e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fb1e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb1e-120">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3fb1e-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3fb1e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fb1e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb1e-122">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3fb1e-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3fb1e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fb1e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb1e-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb1e-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb1e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fb1e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb1e-126">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="3fb1e-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3fb1e-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3fb1e-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

