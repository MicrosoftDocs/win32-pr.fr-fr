---
description: Retourne le nombre moyen de bits par seconde de l’audio encodé.
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: Propriété AVEncStatAudioAverageBPS (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76bcf1ca7b3ee74ae406ebd71f85988a4d13313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033536"
---
# <a name="avencstataudioaveragebps-property"></a><span data-ttu-id="89ddf-103">Propriété AVEncStatAudioAverageBPS</span><span class="sxs-lookup"><span data-stu-id="89ddf-103">AVEncStatAudioAverageBPS property</span></span>

<span data-ttu-id="89ddf-104">Retourne le nombre moyen de bits par seconde de l’audio encodé.</span><span class="sxs-lookup"><span data-stu-id="89ddf-104">Returns the average bits per second of the encoded audio.</span></span>

<span data-ttu-id="89ddf-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="89ddf-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="89ddf-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="89ddf-106">Data type</span></span>

<span data-ttu-id="89ddf-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="89ddf-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="89ddf-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="89ddf-108">Property GUID</span></span>

<span data-ttu-id="89ddf-109">**CODECAPI \_ AVEncStatAudioAverageBPS**</span><span class="sxs-lookup"><span data-stu-id="89ddf-109">**CODECAPI\_AVEncStatAudioAverageBPS**</span></span>

## <a name="remarks"></a><span data-ttu-id="89ddf-110">Notes</span><span class="sxs-lookup"><span data-stu-id="89ddf-110">Remarks</span></span>

<span data-ttu-id="89ddf-111">Cette propriété est disponible une fois l’encodage terminé.</span><span class="sxs-lookup"><span data-stu-id="89ddf-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="89ddf-112">Cette propriété s’applique uniquement à l’encodage VBR (Quality-based bit rate).</span><span class="sxs-lookup"><span data-stu-id="89ddf-112">This property applies only to quality-based variable bit rate (VBR) encoding</span></span>

## <a name="requirements"></a><span data-ttu-id="89ddf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89ddf-113">Requirements</span></span>



| <span data-ttu-id="89ddf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89ddf-114">Requirement</span></span> | <span data-ttu-id="89ddf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="89ddf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89ddf-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89ddf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="89ddf-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="89ddf-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="89ddf-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89ddf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="89ddf-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="89ddf-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="89ddf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="89ddf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="89ddf-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89ddf-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89ddf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89ddf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ddf-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="89ddf-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="89ddf-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="89ddf-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




