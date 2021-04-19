---
description: Spécifie la largeur et la hauteur de la vidéo encodée, si la vidéo est rognée.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propriété AVEncVideoEncodeDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514707"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="31638-103">Propriété AVEncVideoEncodeDimension</span><span class="sxs-lookup"><span data-stu-id="31638-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="31638-104">Spécifie la largeur et la hauteur de la vidéo encodée, si la vidéo est rognée.</span><span class="sxs-lookup"><span data-stu-id="31638-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="31638-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="31638-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="31638-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="31638-106">Data type</span></span>

<span data-ttu-id="31638-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="31638-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="31638-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="31638-108">Property GUID</span></span>

<span data-ttu-id="31638-109">**CODECAPI \_ AVEncVideoEncodeDimension**</span><span class="sxs-lookup"><span data-stu-id="31638-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="31638-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="31638-110">Property value</span></span>

<span data-ttu-id="31638-111">Les 16 bits supérieurs de la valeur contiennent la largeur en pixels, et les 16 bits inférieurs contiennent la hauteur en pixels.</span><span class="sxs-lookup"><span data-stu-id="31638-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="31638-112">Notes</span><span class="sxs-lookup"><span data-stu-id="31638-112">Remarks</span></span>

<span data-ttu-id="31638-113">Les applications peuvent définir cette propriété pour rogner la vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31638-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="31638-114">La taille spécifiée doit être inférieure à la taille des images vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31638-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="31638-115">Utilisez la propriété [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) pour spécifier les angles gauche et supérieur du rectangle de découpage.</span><span class="sxs-lookup"><span data-stu-id="31638-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="31638-116">Les encodeurs peuvent retourner cette propriété en tant que fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="31638-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="31638-117">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="31638-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="31638-118">Pour les encodeurs de caméra UVC 1,5, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="31638-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="31638-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31638-119">Requirements</span></span>



| <span data-ttu-id="31638-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31638-120">Requirement</span></span> | <span data-ttu-id="31638-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="31638-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31638-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31638-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31638-123">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="31638-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="31638-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31638-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31638-125">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="31638-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="31638-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="31638-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31638-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="31638-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31638-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31638-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31638-129">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="31638-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="31638-130">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="31638-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

