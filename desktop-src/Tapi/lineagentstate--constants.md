---
description: Les \_ constantes LINEAGENTSTATE décrivent l’état d’un agent sur une adresse.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Constantes LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521752"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="995f2-103">\_Constantes LINEAGENTSTATE</span><span class="sxs-lookup"><span data-stu-id="995f2-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="995f2-104">Les **\_ constantes LINEAGENTSTATE** décrivent l’état d’un agent sur une adresse.</span><span class="sxs-lookup"><span data-stu-id="995f2-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="995f2-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="995f2-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-106">L’agent est occupé à gérer un appel acheminé à partir d’une file d’attente ACD.</span><span class="sxs-lookup"><span data-stu-id="995f2-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="995f2-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-108">L’agent est occupé à gérer un appel entrant qui n’a pas été transféré à l’agent à partir d’une file d’attente ACD dans laquelle l’agent est connecté.</span><span class="sxs-lookup"><span data-stu-id="995f2-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**</span><span class="sxs-lookup"><span data-stu-id="995f2-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-110">L’agent est occupé à gérer un autre type d’appel, tel qu’un appel personnel sortant non transféré à l’agent par un numéroteur prédictif.</span><span class="sxs-lookup"><span data-stu-id="995f2-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="995f2-111">Cette valeur peut également être utilisée lorsque l’agent est connu pour être occupé sur un appel, mais que le type d’appel est inconnu.</span><span class="sxs-lookup"><span data-stu-id="995f2-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**</span><span class="sxs-lookup"><span data-stu-id="995f2-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-113">L’agent est occupé à gérer un appel sortant, tel qu’un itinéraire à partir d’une file d’attente de numérotation prédictive.</span><span class="sxs-lookup"><span data-stu-id="995f2-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**</span><span class="sxs-lookup"><span data-stu-id="995f2-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-115">Aucun agent n’est connecté à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="995f2-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOchapy**</span><span class="sxs-lookup"><span data-stu-id="995f2-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-117">L’agent est connecté, mais il est occupé par une tâche autre que le traitement d’un appel (par exemple, en cas d’arrêt).</span><span class="sxs-lookup"><span data-stu-id="995f2-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="995f2-118">Aucun appel supplémentaire ne doit être acheminé vers l’agent.</span><span class="sxs-lookup"><span data-stu-id="995f2-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ prêt**</span><span class="sxs-lookup"><span data-stu-id="995f2-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-120">L’agent est prêt à accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="995f2-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="995f2-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-122">L’état de l’agent est inconnu et ne devient jamais connu.</span><span class="sxs-lookup"><span data-stu-id="995f2-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="995f2-123">Dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), cette condition peut également être représentée par le membre **dwAgentState** qui a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="995f2-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="995f2-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-125">L’état de l’agent est actuellement inconnu, mais peut devenir connu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="995f2-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="995f2-126">Il peut s’agir d’un état de transition lors de la première ouverture d’une ligne ou d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="995f2-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="995f2-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**</span><span class="sxs-lookup"><span data-stu-id="995f2-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="995f2-128">L’agent a terminé l’appel précédent, mais il est toujours occupé par le travail associé à cet appel.</span><span class="sxs-lookup"><span data-stu-id="995f2-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="995f2-129">L’agent ne doit pas recevoir d’appels supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="995f2-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="995f2-130">Notes</span><span class="sxs-lookup"><span data-stu-id="995f2-130">Remarks</span></span>

<span data-ttu-id="995f2-131">Les 16 bits supérieurs de cet ensemble de constantes sont réservés aux extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="995f2-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="995f2-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="995f2-132">Requirements</span></span>



| <span data-ttu-id="995f2-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="995f2-133">Requirement</span></span> | <span data-ttu-id="995f2-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="995f2-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="995f2-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="995f2-135">TAPI version</span></span><br/> | <span data-ttu-id="995f2-136">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="995f2-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="995f2-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="995f2-137">Header</span></span><br/>       | <dl> <span data-ttu-id="995f2-138"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="995f2-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




