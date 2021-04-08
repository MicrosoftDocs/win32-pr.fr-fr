---
description: Spécifie comment le décodeur reproduit un double audio mono.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Propriété AVDecAudioDualMonoReproMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747084"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="aed21-103">Propriété AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="aed21-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="aed21-104">Spécifie comment le décodeur reproduit un double audio mono.</span><span class="sxs-lookup"><span data-stu-id="aed21-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="aed21-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aed21-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="aed21-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="aed21-106">Data type</span></span>

<span data-ttu-id="aed21-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aed21-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aed21-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="aed21-108">Property GUID</span></span>

<span data-ttu-id="aed21-109">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="aed21-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="aed21-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aed21-110">Property value</span></span>

<span data-ttu-id="aed21-111">La valeur de cette propriété est un membre de l’énumération [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .</span><span class="sxs-lookup"><span data-stu-id="aed21-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="aed21-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aed21-112">Remarks</span></span>

<span data-ttu-id="aed21-113">Cette propriété s’applique uniquement lorsque le flux de bits d’entrée du décodeur contient du son double mono.</span><span class="sxs-lookup"><span data-stu-id="aed21-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="aed21-114">Pour tester cette condition, récupérez la valeur de la propriété [AVDecAudioDualMono](avdecaudiodualmono-property.md) .</span><span class="sxs-lookup"><span data-stu-id="aed21-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="aed21-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aed21-115">Requirements</span></span>



| <span data-ttu-id="aed21-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aed21-116">Requirement</span></span> | <span data-ttu-id="aed21-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aed21-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aed21-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aed21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aed21-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="aed21-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aed21-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aed21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aed21-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="aed21-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aed21-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="aed21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed21-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed21-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed21-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aed21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed21-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="aed21-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aed21-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="aed21-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




