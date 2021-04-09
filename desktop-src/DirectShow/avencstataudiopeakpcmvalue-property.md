---
description: Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.
ms.assetid: 1d9a6a22-bb82-45e1-80d2-88627c90340c
title: Propriété AVEncStatAudioPeakPCMValue (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d75444631a63c946d4020fe91cdd3a980fc393
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108987"
---
# <a name="avencstataudiopeakpcmvalue-property"></a><span data-ttu-id="9c14b-103">Propriété AVEncStatAudioPeakPCMValue</span><span class="sxs-lookup"><span data-stu-id="9c14b-103">AVEncStatAudioPeakPCMValue property</span></span>

<span data-ttu-id="9c14b-104">Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.</span><span class="sxs-lookup"><span data-stu-id="9c14b-104">Returns the highest volume level that was present in the audio content.</span></span>

<span data-ttu-id="9c14b-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9c14b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9c14b-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="9c14b-106">Data type</span></span>

<span data-ttu-id="9c14b-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9c14b-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9c14b-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="9c14b-108">Property GUID</span></span>

<span data-ttu-id="9c14b-109">**CODECAPI \_ AVEncStatAudioPeakPCMValue**</span><span class="sxs-lookup"><span data-stu-id="9c14b-109">**CODECAPI\_AVEncStatAudioPeakPCMValue**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c14b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9c14b-110">Remarks</span></span>

<span data-ttu-id="9c14b-111">Cette propriété est disponible une fois l’encodage terminé.</span><span class="sxs-lookup"><span data-stu-id="9c14b-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="9c14b-112">Cette propriété s’applique uniquement à l’encodage VBR (Quality-based bit rate).</span><span class="sxs-lookup"><span data-stu-id="9c14b-112">This property applies only to quality-based variable bit rate (VBR) encoding</span></span>

## <a name="requirements"></a><span data-ttu-id="9c14b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c14b-113">Requirements</span></span>



| <span data-ttu-id="9c14b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c14b-114">Requirement</span></span> | <span data-ttu-id="9c14b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c14b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c14b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c14b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9c14b-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9c14b-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9c14b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c14b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9c14b-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9c14b-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9c14b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c14b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c14b-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c14b-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c14b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c14b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c14b-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="9c14b-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9c14b-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9c14b-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




