---
description: Retourne le nombre de trames vidéo qui ont été encodées.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propriété AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109371"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="4485f-103">Propriété AVEncStatVideoCodedFrames</span><span class="sxs-lookup"><span data-stu-id="4485f-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="4485f-104">Retourne le nombre de trames vidéo qui ont été encodées.</span><span class="sxs-lookup"><span data-stu-id="4485f-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="4485f-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4485f-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4485f-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="4485f-106">Data type</span></span>

<span data-ttu-id="4485f-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="4485f-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4485f-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="4485f-108">Property GUID</span></span>

<span data-ttu-id="4485f-109">**CODECAPI \_ AVEncStatVideoCodedFrames**</span><span class="sxs-lookup"><span data-stu-id="4485f-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="4485f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4485f-110">Remarks</span></span>

<span data-ttu-id="4485f-111">Cette propriété est disponible une fois l’encodage terminé.</span><span class="sxs-lookup"><span data-stu-id="4485f-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="4485f-112">La valeur de cette propriété est égale à la propriété [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) moins le nombre de frames supprimés.</span><span class="sxs-lookup"><span data-stu-id="4485f-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="4485f-113">L’encodeur peut supprimer des frames pour rester dans les limites de la vitesse de transmission spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4485f-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="4485f-114">Elle peut également supprimer des frames à la fin du flux (consultez la propriété [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="4485f-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="4485f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4485f-115">Requirements</span></span>



| <span data-ttu-id="4485f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4485f-116">Requirement</span></span> | <span data-ttu-id="4485f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4485f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4485f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4485f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4485f-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4485f-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4485f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4485f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4485f-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4485f-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4485f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4485f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4485f-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4485f-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4485f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4485f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4485f-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="4485f-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4485f-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="4485f-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




