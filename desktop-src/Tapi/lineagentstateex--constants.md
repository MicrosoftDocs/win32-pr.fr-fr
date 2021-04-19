---
description: Les \_ constantes LINEAGENTSTATEEX décrivent l’état d’un agent sur une adresse.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Constantes LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541743"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="31b5a-103">\_Constantes LINEAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="31b5a-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="31b5a-104">Les **\_ constantes LINEAGENTSTATEEX** décrivent l’état d’un agent sur une adresse.</span><span class="sxs-lookup"><span data-stu-id="31b5a-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="31b5a-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="31b5a-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-106">L’agent est occupé à gérer un appel acheminé à partir d’une file d’attente ACD.</span><span class="sxs-lookup"><span data-stu-id="31b5a-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b5a-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="31b5a-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-108">L’agent est occupé à gérer un appel entrant qui n’a pas été transféré à l’agent à partir d’une file d’attente ACD dans laquelle l’agent est connecté.</span><span class="sxs-lookup"><span data-stu-id="31b5a-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b5a-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**</span><span class="sxs-lookup"><span data-stu-id="31b5a-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-110">L’agent est occupé à gérer un appel sortant, tel qu’un itinéraire à partir d’une file d’attente de numérotation prédictive.</span><span class="sxs-lookup"><span data-stu-id="31b5a-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b5a-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOchapy**</span><span class="sxs-lookup"><span data-stu-id="31b5a-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-112">L’agent est connecté, mais il est occupé par une tâche autre que le traitement d’un appel (par exemple, en cas d’arrêt).</span><span class="sxs-lookup"><span data-stu-id="31b5a-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="31b5a-113">Aucun appel supplémentaire ne doit être acheminé vers l’agent.</span><span class="sxs-lookup"><span data-stu-id="31b5a-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b5a-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ prêt**</span><span class="sxs-lookup"><span data-stu-id="31b5a-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-115">L’agent est prêt à accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="31b5a-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b5a-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ libéré**</span><span class="sxs-lookup"><span data-stu-id="31b5a-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-117">L’agent a été libéré, probablement parce qu’il a été déconnecté.</span><span class="sxs-lookup"><span data-stu-id="31b5a-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b5a-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="31b5a-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b5a-119">L’état de l’agent est actuellement inconnu, mais peut devenir connu ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="31b5a-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="31b5a-120">Il peut s’agir d’un état de transition lors de la première ouverture d’une ligne ou d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="31b5a-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31b5a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31b5a-121">Requirements</span></span>



| <span data-ttu-id="31b5a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31b5a-122">Requirement</span></span> | <span data-ttu-id="31b5a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="31b5a-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="31b5a-124">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="31b5a-124">TAPI version</span></span><br/> | <span data-ttu-id="31b5a-125">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="31b5a-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="31b5a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="31b5a-126">Header</span></span><br/>       | <dl> <span data-ttu-id="31b5a-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b5a-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




