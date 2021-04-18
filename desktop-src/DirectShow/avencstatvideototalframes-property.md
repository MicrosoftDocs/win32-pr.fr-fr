---
description: Retourne le nombre de trames vidéo reçues par l’encodeur.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propriété AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512857"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="d8fa5-103">Propriété AVEncStatVideoTotalFrames</span><span class="sxs-lookup"><span data-stu-id="d8fa5-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="d8fa5-104">Retourne le nombre de trames vidéo reçues par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="d8fa5-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="d8fa5-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d8fa5-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d8fa5-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="d8fa5-106">Data type</span></span>

<span data-ttu-id="d8fa5-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d8fa5-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d8fa5-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="d8fa5-108">Property GUID</span></span>

<span data-ttu-id="d8fa5-109">**CODECAPI \_ AVEncStatVideoTotalFrames**</span><span class="sxs-lookup"><span data-stu-id="d8fa5-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fa5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d8fa5-110">Remarks</span></span>

<span data-ttu-id="d8fa5-111">Cette propriété est disponible une fois l’encodage terminé.</span><span class="sxs-lookup"><span data-stu-id="d8fa5-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="d8fa5-112">La valeur de cette propriété est le nombre total de trames envoyées à l’encodeur, y compris les frames qui ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="d8fa5-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="d8fa5-113">Pour obtenir le nombre de frames encodés, lisez la propriété [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d8fa5-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8fa5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8fa5-114">Requirements</span></span>



| <span data-ttu-id="d8fa5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8fa5-115">Requirement</span></span> | <span data-ttu-id="d8fa5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8fa5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fa5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8fa5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d8fa5-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8fa5-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d8fa5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8fa5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d8fa5-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8fa5-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d8fa5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8fa5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8fa5-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8fa5-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8fa5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8fa5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fa5-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="d8fa5-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d8fa5-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d8fa5-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




