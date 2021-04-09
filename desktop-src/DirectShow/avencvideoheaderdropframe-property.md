---
description: Spécifie la valeur de l’indicateur de frame de dépôt dans l’en-tête groupe d’images (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propriété AVEncVideoHeaderDropFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846738"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="dbe89-103">Propriété AVEncVideoHeaderDropFrame</span><span class="sxs-lookup"><span data-stu-id="dbe89-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="dbe89-104">Spécifie la valeur de l’indicateur de frame de dépôt dans l’en-tête groupe d’images (GOP).</span><span class="sxs-lookup"><span data-stu-id="dbe89-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="dbe89-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dbe89-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="dbe89-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="dbe89-106">Data type</span></span>

<span data-ttu-id="dbe89-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="dbe89-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="dbe89-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="dbe89-108">Property GUID</span></span>

<span data-ttu-id="dbe89-109">**CODECAPI \_ AVEncVideoHeaderDropFrame**</span><span class="sxs-lookup"><span data-stu-id="dbe89-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="dbe89-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dbe89-110">Property value</span></span>

<span data-ttu-id="dbe89-111">La valeur de cette propriété peut être 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="dbe89-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe89-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dbe89-112">Remarks</span></span>

<span data-ttu-id="dbe89-113">Le mode de trame déroulant est utilisé dans la vidéo NTSC pour corriger l’écart entre la vidéo, 29,97 images par seconde, et l’affichage du code de temps, qui est de 30 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="dbe89-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="dbe89-114">En mode Drop Frame, les numéros de trame 00 et 01 sont ignorés au début de chaque minute, à l’exception des minutes, même les multiples de dix (00, 10, 20, etc.).</span><span class="sxs-lookup"><span data-stu-id="dbe89-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="dbe89-115">Seuls les numéros de frame dans le code d’heure sont supprimés. aucun frame réel n’est supprimé.</span><span class="sxs-lookup"><span data-stu-id="dbe89-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe89-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbe89-116">Requirements</span></span>



| <span data-ttu-id="dbe89-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbe89-117">Requirement</span></span> | <span data-ttu-id="dbe89-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe89-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe89-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe89-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe89-120">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="dbe89-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="dbe89-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe89-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe89-122">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="dbe89-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="dbe89-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbe89-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe89-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe89-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe89-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe89-126">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="dbe89-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="dbe89-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="dbe89-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




