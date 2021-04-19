---
description: Définit l’utilisation de la vidéo pour un encodeur vidéo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: CODECAPI_AVEncVideoUsage, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514767"
---
# <a name="codecapi_avencvideousage-property"></a><span data-ttu-id="1a87e-103">CODECAPI \_ propriété AVEncVideoUsage</span><span class="sxs-lookup"><span data-stu-id="1a87e-103">CODECAPI\_AVEncVideoUsage property</span></span>

<span data-ttu-id="1a87e-104">Définit l’utilisation de la vidéo pour un encodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="1a87e-104">Sets the video usage for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="1a87e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1a87e-105">Data type</span></span>

<span data-ttu-id="1a87e-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="1a87e-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="1a87e-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="1a87e-107">Property GUID</span></span>

<span data-ttu-id="1a87e-108">**CODECAPI \_ AVEncVideoUsage**</span><span class="sxs-lookup"><span data-stu-id="1a87e-108">**CODECAPI\_AVEncVideoUsage**</span></span>

## <a name="remarks"></a><span data-ttu-id="1a87e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1a87e-109">Remarks</span></span>

<span data-ttu-id="1a87e-110">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="1a87e-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="1a87e-111">[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI \_ AVEncVideoUsage et [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sont des propriétés d’encodeur statiques.</span><span class="sxs-lookup"><span data-stu-id="1a87e-111">[CODECAPI\_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI\_AVEncVideoUsage, and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="1a87e-112">Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média set sur la broche de sortie de l’appareil photo s.</span><span class="sxs-lookup"><span data-stu-id="1a87e-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a87e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a87e-113">Requirements</span></span>



| <span data-ttu-id="1a87e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a87e-114">Requirement</span></span> | <span data-ttu-id="1a87e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a87e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a87e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a87e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1a87e-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1a87e-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="1a87e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a87e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1a87e-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="1a87e-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1a87e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a87e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a87e-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a87e-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a87e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a87e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a87e-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a87e-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

