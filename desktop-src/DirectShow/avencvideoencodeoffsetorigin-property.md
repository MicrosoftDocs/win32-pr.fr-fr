---
description: Spécifie les angles gauche et supérieur du rectangle de découpage, si la vidéo est rognée.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propriété AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108986"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="d6ac2-103">Propriété AVEncVideoEncodeOffsetOrigin</span><span class="sxs-lookup"><span data-stu-id="d6ac2-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="d6ac2-104">Spécifie les angles gauche et supérieur du rectangle de découpage, si la vidéo est rognée.</span><span class="sxs-lookup"><span data-stu-id="d6ac2-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="d6ac2-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d6ac2-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6ac2-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="d6ac2-106">Data type</span></span>

<span data-ttu-id="d6ac2-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d6ac2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d6ac2-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="d6ac2-108">Property GUID</span></span>

<span data-ttu-id="d6ac2-109">**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**</span><span class="sxs-lookup"><span data-stu-id="d6ac2-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="d6ac2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d6ac2-110">Property value</span></span>

<span data-ttu-id="d6ac2-111">Les 16 bits supérieurs de la valeur contiennent le décalage par rapport au bord gauche du frame d’entrée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d6ac2-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="d6ac2-112">Les 16 bits inférieurs contiennent le décalage par rapport au bord supérieur du frame d’entrée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d6ac2-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6ac2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d6ac2-113">Remarks</span></span>

<span data-ttu-id="d6ac2-114">Les applications peuvent définir cette propriété pour rogner la vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d6ac2-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="d6ac2-115">Utilisez la propriété [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) pour spécifier la largeur et la hauteur du rectangle de découpage.</span><span class="sxs-lookup"><span data-stu-id="d6ac2-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ac2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6ac2-116">Requirements</span></span>



| <span data-ttu-id="d6ac2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6ac2-117">Requirement</span></span> | <span data-ttu-id="d6ac2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6ac2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ac2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6ac2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ac2-120">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6ac2-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d6ac2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6ac2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ac2-122">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6ac2-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d6ac2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6ac2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ac2-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6ac2-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6ac2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6ac2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ac2-126">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="d6ac2-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d6ac2-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d6ac2-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




