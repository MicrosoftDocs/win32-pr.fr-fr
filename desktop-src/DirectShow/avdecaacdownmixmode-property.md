---
description: Spécifie si un décodeur AAC utilise des équations downmix stéréo MPEG-2/MPEG-4 standard ou utilise un downmix non standard.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propriété AVDecAACDownmixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514727"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="9f093-103">Propriété AVDecAACDownmixMode</span><span class="sxs-lookup"><span data-stu-id="9f093-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="9f093-104">Spécifie si un décodeur AAC utilise des équations downmix stéréo MPEG-2/MPEG-4 standard ou utilise un downmix non standard.</span><span class="sxs-lookup"><span data-stu-id="9f093-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="9f093-105">Un exemple de downmix non standard est celui défini par ARIB document STD-B21 version 4,4.</span><span class="sxs-lookup"><span data-stu-id="9f093-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="9f093-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9f093-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9f093-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="9f093-107">Data type</span></span>

<span data-ttu-id="9f093-108">**UInt32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9f093-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="9f093-109">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="9f093-109">Property GUID</span></span>

<span data-ttu-id="9f093-110">**CODECAPI \_ AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="9f093-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="9f093-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9f093-111">Property value</span></span>

<span data-ttu-id="9f093-112">La valeur de cette propriété est un membre de l’énumération [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="9f093-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f093-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f093-113">Requirements</span></span>



| <span data-ttu-id="9f093-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f093-114">Requirement</span></span> | <span data-ttu-id="9f093-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f093-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f093-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f093-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f093-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9f093-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9f093-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f093-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f093-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9f093-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9f093-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f093-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f093-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f093-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f093-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f093-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f093-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="9f093-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9f093-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9f093-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

