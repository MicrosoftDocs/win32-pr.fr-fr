---
description: Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846681"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="9e7ef-103">AVDecVideoAcceleration \_ propriété H264 –</span><span class="sxs-lookup"><span data-stu-id="9e7ef-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="9e7ef-104">Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="9e7ef-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="9e7ef-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9e7ef-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9e7ef-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="9e7ef-106">Data type</span></span>

<span data-ttu-id="9e7ef-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9e7ef-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9e7ef-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="9e7ef-108">Property GUID</span></span>

<span data-ttu-id="9e7ef-109">**CODECAPI \_ AVDecVideoAcceleration \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="9e7ef-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="9e7ef-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9e7ef-110">Remarks</span></span>

<span data-ttu-id="9e7ef-111">Si la valeur est égale à zéro, le décodeur n’utilise pas DirectX Video Acceleration (DXVA) pour le décodage vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="9e7ef-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="9e7ef-112">Pour les filtres DirectShow, définissez cette propriété avant que la broche de sortie du décodeur soit connectée.</span><span class="sxs-lookup"><span data-stu-id="9e7ef-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7ef-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e7ef-113">Requirements</span></span>



| <span data-ttu-id="9e7ef-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e7ef-114">Requirement</span></span> | <span data-ttu-id="9e7ef-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e7ef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7ef-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7ef-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9e7ef-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9e7ef-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7ef-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9e7ef-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9e7ef-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e7ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e7ef-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7ef-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7ef-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e7ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7ef-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="9e7ef-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9e7ef-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9e7ef-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




