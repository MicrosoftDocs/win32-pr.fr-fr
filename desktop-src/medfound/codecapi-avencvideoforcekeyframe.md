---
description: Force l’encodeur à coder le frame suivant comme une image clé.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512914"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="25edd-103">CODECAPI \_ propriété AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="25edd-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="25edd-104">Force l’encodeur à coder le frame suivant comme une image clé.</span><span class="sxs-lookup"><span data-stu-id="25edd-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="25edd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="25edd-105">Data type</span></span>

<span data-ttu-id="25edd-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="25edd-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="25edd-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="25edd-107">Property GUID</span></span>

<span data-ttu-id="25edd-108">**CODECAPI \_ AVEncVideoForceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="25edd-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="25edd-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="25edd-109">Property value</span></span>

<span data-ttu-id="25edd-110">Si la valeur est différente de zéro, l’encodeur encode le frame suivant comme une image clé.</span><span class="sxs-lookup"><span data-stu-id="25edd-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="25edd-111">Si la valeur est égale à zéro, l’encodeur choisit s’il faut encoder le frame suivant comme une image clé.</span><span class="sxs-lookup"><span data-stu-id="25edd-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="25edd-112">Cette propriété s’applique au frame suivant que l’encodeur reçoit comme entrée.</span><span class="sxs-lookup"><span data-stu-id="25edd-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="25edd-113">Pour une transformation de Media Foundation (MFT), il s’agit du frame suivant qui est passé à la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) .</span><span class="sxs-lookup"><span data-stu-id="25edd-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="25edd-114">Le paramètre se réinitialise à zéro après le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="25edd-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="25edd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="25edd-115">Remarks</span></span>

<span data-ttu-id="25edd-116">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="25edd-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25edd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25edd-117">Requirements</span></span>



| <span data-ttu-id="25edd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25edd-118">Requirement</span></span> | <span data-ttu-id="25edd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="25edd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25edd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25edd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25edd-121">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="25edd-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="25edd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25edd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25edd-123">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="25edd-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="25edd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="25edd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="25edd-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="25edd-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25edd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25edd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25edd-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25edd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="25edd-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="25edd-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

