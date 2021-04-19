---
description: Les \_ constantes d’indicateur de bit LINEDIALTONEMODE décrivent différents types de tonalités. Une tonalité spéciale comporte généralement une signification particulière (comme avec le message en attente).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Constantes LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539563"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="8d7e5-104">\_Constantes LINEDIALTONEMODE</span><span class="sxs-lookup"><span data-stu-id="8d7e5-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="8d7e5-105">Les constantes d’indicateur de bit **LINEDIALTONEMODE \_** décrivent différents types de tonalités.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="8d7e5-106">Une tonalité spéciale comporte généralement une signification particulière (comme avec le message en attente).</span><span class="sxs-lookup"><span data-stu-id="8d7e5-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="8d7e5-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ externe**</span><span class="sxs-lookup"><span data-stu-id="8d7e5-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d7e5-108">Il s’agit d’une tonalité externe (réseau public).</span><span class="sxs-lookup"><span data-stu-id="8d7e5-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d7e5-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interne**</span><span class="sxs-lookup"><span data-stu-id="8d7e5-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d7e5-110">Il s’agit d’une tonalité interne, comme dans un PBX.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d7e5-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="8d7e5-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d7e5-112">Il s’agit d’une tonalité normale, qui est généralement une tonalité continue.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d7e5-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ spécial**</span><span class="sxs-lookup"><span data-stu-id="8d7e5-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d7e5-114">Il s’agit d’une tonalité spéciale indiquant qu’une certaine condition (connue par le commutateur ou le réseau) est actuellement en vigueur.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="8d7e5-115">Les tonalités spéciales utilisent généralement un ton interrompu.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="8d7e5-116">Comme avec une tonalité normale, cela indique que le commutateur est prêt à recevoir le numéro à composer.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d7e5-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="8d7e5-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d7e5-118">Le mode de tonalité n’est pas disponible et ne devient pas connu.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d7e5-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="8d7e5-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d7e5-120">Le mode de tonalité n’est pas actuellement connu, mais peut devenir connu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d7e5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8d7e5-121">Remarks</span></span>

<span data-ttu-id="8d7e5-122">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="8d7e5-123">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="8d7e5-124">Les **\_ constantes LINEDIALTONEMODE** sont utilisées dans la structure de données [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pour un appel dans l’état de la tonalité.</span><span class="sxs-lookup"><span data-stu-id="8d7e5-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d7e5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d7e5-125">Requirements</span></span>



| <span data-ttu-id="8d7e5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d7e5-126">Requirement</span></span> | <span data-ttu-id="8d7e5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d7e5-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8d7e5-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8d7e5-128">TAPI version</span></span><br/> | <span data-ttu-id="8d7e5-129">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8d7e5-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8d7e5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d7e5-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8d7e5-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d7e5-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




