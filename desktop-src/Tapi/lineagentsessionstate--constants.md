---
description: Les \_ constantes LINEAGENTSESSIONSTATE décrivent les différents États de session de l’agent.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Constantes LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525463"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="4c3c8-103">\_Constantes LINEAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="4c3c8-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="4c3c8-104">Les **\_ constantes LINEAGENTSESSIONSTATE** décrivent les différents États de session de l’agent.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="4c3c8-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**</span><span class="sxs-lookup"><span data-stu-id="4c3c8-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4c3c8-106">L’agent est occupé à gérer un appel.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c3c8-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**</span><span class="sxs-lookup"><span data-stu-id="4c3c8-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4c3c8-108">L’agent est occupé à gérer l’encapsulation de l’appel.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c3c8-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="4c3c8-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4c3c8-110">La session de l’agent s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c3c8-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOchapy**</span><span class="sxs-lookup"><span data-stu-id="4c3c8-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4c3c8-112">L’agent est connecté, mais il est occupé par une tâche autre que le traitement d’un appel (par exemple, en cas d’arrêt).</span><span class="sxs-lookup"><span data-stu-id="4c3c8-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="4c3c8-113">Aucun appel supplémentaire ne doit être acheminé vers l’agent.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c3c8-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ prêt**</span><span class="sxs-lookup"><span data-stu-id="4c3c8-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4c3c8-115">L’agent est prêt à accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c3c8-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ libéré**</span><span class="sxs-lookup"><span data-stu-id="4c3c8-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4c3c8-117">La session de l’agent a été libérée.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c3c8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c3c8-118">Requirements</span></span>



| <span data-ttu-id="4c3c8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c3c8-119">Requirement</span></span> | <span data-ttu-id="4c3c8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c3c8-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4c3c8-121">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="4c3c8-121">TAPI version</span></span><br/> | <span data-ttu-id="4c3c8-122">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="4c3c8-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4c3c8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c3c8-123">Header</span></span><br/>       | <dl> <span data-ttu-id="4c3c8-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c3c8-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




