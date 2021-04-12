---
description: Spécifie le mode de contrôle de la fréquence.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propriété AVEncCommonRateControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200823"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="0d67f-103">Propriété AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="0d67f-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="0d67f-104">Spécifie le mode de contrôle de la fréquence.</span><span class="sxs-lookup"><span data-stu-id="0d67f-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="0d67f-105">Les applications peuvent définir cette propriété pour spécifier le mode de contrôle de la fréquence.</span><span class="sxs-lookup"><span data-stu-id="0d67f-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="0d67f-106">Les encodeurs peuvent également retourner cette propriété en tant que fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0d67f-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="0d67f-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0d67f-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d67f-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="0d67f-108">Data type</span></span>

<span data-ttu-id="0d67f-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="0d67f-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0d67f-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="0d67f-110">Property GUID</span></span>

<span data-ttu-id="0d67f-111">**CODECAPI \_ AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="0d67f-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="0d67f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0d67f-112">Property value</span></span>

<span data-ttu-id="0d67f-113">La valeur de cette propriété est un membre de l’énumération [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .</span><span class="sxs-lookup"><span data-stu-id="0d67f-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d67f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0d67f-114">Remarks</span></span>

<span data-ttu-id="0d67f-115">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="0d67f-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="0d67f-116">[CODECAPI \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)et CODECAPI \_ AVEncCommonRateControlMode sont des propriétés d’encodeur statiques.</span><span class="sxs-lookup"><span data-stu-id="0d67f-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="0d67f-117">Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média défini sur la broche de sortie de la caméra.</span><span class="sxs-lookup"><span data-stu-id="0d67f-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d67f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d67f-118">Requirements</span></span>



| <span data-ttu-id="0d67f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d67f-119">Requirement</span></span> | <span data-ttu-id="0d67f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d67f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d67f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d67f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d67f-122">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d67f-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0d67f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d67f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d67f-124">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d67f-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0d67f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d67f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d67f-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d67f-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d67f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d67f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d67f-128">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="0d67f-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0d67f-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0d67f-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

