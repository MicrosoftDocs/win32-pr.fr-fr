---
description: Active ou désactive l’accélération matérielle pour le décodage vidéo MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: AVDecVideoAcceleration_MPEG2, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747252"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a><span data-ttu-id="d8b0d-103">AVDecVideoAcceleration \_ MPEG2, propriété</span><span class="sxs-lookup"><span data-stu-id="d8b0d-103">AVDecVideoAcceleration\_MPEG2 property</span></span>

<span data-ttu-id="d8b0d-104">Active ou désactive l’accélération matérielle pour le décodage vidéo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d8b0d-104">Enables or disables hardware acceleration for MPEG-2 video decoding.</span></span>

<span data-ttu-id="d8b0d-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d8b0d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d8b0d-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="d8b0d-106">Data type</span></span>

<span data-ttu-id="d8b0d-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d8b0d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d8b0d-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="d8b0d-108">Property GUID</span></span>

<span data-ttu-id="d8b0d-109">**CODECAPI \_ AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d8b0d-109">**CODECAPI\_AVDecVideoAcceleration\_MPEG2**</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b0d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d8b0d-110">Remarks</span></span>

<span data-ttu-id="d8b0d-111">Si la valeur est égale à zéro, le décodeur n’utilise pas DirectX Video Acceleration (DXVA) pour le décodage vidéo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d8b0d-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for MPEG-2 video decoding.</span></span> <span data-ttu-id="d8b0d-112">Pour les filtres DirectShow, définissez cette propriété avant que la broche de sortie du décodeur soit connectée.</span><span class="sxs-lookup"><span data-stu-id="d8b0d-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b0d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8b0d-113">Requirements</span></span>



| <span data-ttu-id="d8b0d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8b0d-114">Requirement</span></span> | <span data-ttu-id="d8b0d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8b0d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b0d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b0d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b0d-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8b0d-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d8b0d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b0d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b0d-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8b0d-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d8b0d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8b0d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b0d-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b0d-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b0d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b0d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b0d-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="d8b0d-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d8b0d-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d8b0d-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




