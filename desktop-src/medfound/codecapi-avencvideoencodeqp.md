---
description: Spécifie le paramètre de quantification (QP) pour l’encodage vidéo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512915"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="def26-103">CODECAPI \_ propriété AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="def26-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="def26-104">Spécifie le paramètre de quantification (QP) pour l’encodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="def26-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="def26-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="def26-105">Data type</span></span>

<span data-ttu-id="def26-106">**ULONGLONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="def26-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="def26-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="def26-107">Property GUID</span></span>

<span data-ttu-id="def26-108">**CODECAPI \_ AVEncVideoEncodeQP**</span><span class="sxs-lookup"><span data-stu-id="def26-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="def26-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="def26-109">Property value</span></span>

<span data-ttu-id="def26-110">Ensemble de champs 4 16 bits utilisé pour spécifier le RPS de frame dans l’encodage Fixed-QP.</span><span class="sxs-lookup"><span data-stu-id="def26-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="def26-111">Les champs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="def26-111">The fields are:</span></span>

-   <span data-ttu-id="def26-112">Bits 0-15 : QP par défaut</span><span class="sxs-lookup"><span data-stu-id="def26-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="def26-113">Bits 16-31 : QP utilisé pour les frames I</span><span class="sxs-lookup"><span data-stu-id="def26-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="def26-114">Bits 32-47 : QP utilisé pour les frames P</span><span class="sxs-lookup"><span data-stu-id="def26-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="def26-115">Bits 48-63 : QP utilisé pour les frames B</span><span class="sxs-lookup"><span data-stu-id="def26-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="def26-116">Notes</span><span class="sxs-lookup"><span data-stu-id="def26-116">Remarks</span></span>

<span data-ttu-id="def26-117">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="def26-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="def26-118">Pour garantir une utilisation cohérente entre différents encodeurs, vous devez supposer que les encodeurs n’examineront que le QP par défaut et peuvent ignorer les valeurs de QP pour les images I/P/B.</span><span class="sxs-lookup"><span data-stu-id="def26-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="def26-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="def26-119">Requirements</span></span>



| <span data-ttu-id="def26-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="def26-120">Requirement</span></span> | <span data-ttu-id="def26-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="def26-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="def26-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="def26-122">Minimum supported client</span></span><br/> | <span data-ttu-id="def26-123">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="def26-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="def26-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="def26-124">Minimum supported server</span></span><br/> | <span data-ttu-id="def26-125">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="def26-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="def26-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="def26-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="def26-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="def26-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def26-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="def26-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def26-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="def26-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="def26-130">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="def26-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

