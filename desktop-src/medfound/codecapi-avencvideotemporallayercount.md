---
description: Définit le nombre de couches temporelles vidéo pour un encodeur vidéo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484113"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="fce5a-103">CODECAPI \_ propriété AVEncVideoTemporalLayerCount</span><span class="sxs-lookup"><span data-stu-id="fce5a-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="fce5a-104">Définit le nombre de couches temporelles vidéo pour un encodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fce5a-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="fce5a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="fce5a-105">Data type</span></span>

<span data-ttu-id="fce5a-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="fce5a-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="fce5a-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="fce5a-107">Property GUID</span></span>

<span data-ttu-id="fce5a-108">**CODECAPI \_ AVEncVideoTemporalLayerCount**</span><span class="sxs-lookup"><span data-stu-id="fce5a-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="fce5a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="fce5a-109">Remarks</span></span>

<span data-ttu-id="fce5a-110">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="fce5a-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="fce5a-111">CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)et [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sont des propriétés d’encodeur statiques.</span><span class="sxs-lookup"><span data-stu-id="fce5a-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="fce5a-112">Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média set sur la broche de sortie de l’appareil photo s.</span><span class="sxs-lookup"><span data-stu-id="fce5a-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce5a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fce5a-113">Requirements</span></span>



| <span data-ttu-id="fce5a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fce5a-114">Requirement</span></span> | <span data-ttu-id="fce5a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fce5a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fce5a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce5a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fce5a-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fce5a-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="fce5a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce5a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fce5a-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="fce5a-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fce5a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fce5a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce5a-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce5a-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce5a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce5a-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fce5a-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

