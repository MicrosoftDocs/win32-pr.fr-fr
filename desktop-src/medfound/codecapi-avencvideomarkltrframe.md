---
description: Marque le frame actuel comme un cadre LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524628"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="aeef1-103">CODECAPI \_ propriété AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="aeef1-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="aeef1-104">Marque le frame actuel comme un cadre LTR.</span><span class="sxs-lookup"><span data-stu-id="aeef1-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="aeef1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="aeef1-105">Data type</span></span>

<span data-ttu-id="aeef1-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="aeef1-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aeef1-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="aeef1-107">Property GUID</span></span>

<span data-ttu-id="aeef1-108">**CODECAPI \_ AVEncVideoMarkLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="aeef1-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="aeef1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="aeef1-109">Remarks</span></span>

<span data-ttu-id="aeef1-110">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="aeef1-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="aeef1-111">La valeur de ce contrôle est la valeur de la syntaxe H. 264 *LongTermFramIdx* associée au frame actuel.</span><span class="sxs-lookup"><span data-stu-id="aeef1-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="aeef1-112">Si le frame actuel n’est pas dans la couche de base, par exemple, l’élément de syntaxe *temporal \_ ID* n’est pas égal à 0, cette propriété s’applique au frame de couche de base suivant dans l’ordre de codage.</span><span class="sxs-lookup"><span data-stu-id="aeef1-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="aeef1-113">Cette propriété ne doit pas être appelée si un appel en attente pour marquer un frame LTR a été émis à l’aide de la \_ propriété CODECAPI AVEncVideoMarkLTRFrame et que l’encodeur n’a pas encore marqué un frame comme LTR.</span><span class="sxs-lookup"><span data-stu-id="aeef1-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="aeef1-114">En d’autres termes, l’encodeur ne doit pas faire remonter les \_ demandes CODECAPI AVEncVideoMarkLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="aeef1-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="aeef1-115">Si une \_ demande CODECAPI AVEncVideoMarkLTRFrame est soumise alors qu’une autre \_ demande de AVEncVideoMarkLTRFrame CODECAPI est toujours en attente, la demande plus ancienne doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="aeef1-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="aeef1-116">La \_ propriété CODECAPI AVEncVideoMarkLTRFrame est dynamique et peut être définie au cours de la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="aeef1-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeef1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aeef1-117">Requirements</span></span>



| <span data-ttu-id="aeef1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aeef1-118">Requirement</span></span> | <span data-ttu-id="aeef1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aeef1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aeef1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aeef1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aeef1-121">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aeef1-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="aeef1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aeef1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aeef1-123">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aeef1-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="aeef1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="aeef1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeef1-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeef1-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeef1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeef1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeef1-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aeef1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




