---
title: Méthode INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: Est appelé si un SoHRequest a été interrogé à partir de l’algorithme SHA, mais que la réponse n’a jamais été renvoyée.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Méthode NotifyOrphanedSoHRequest NAP
- Méthode NotifyOrphanedSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385191"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="0f359-106">INapSystemHealthAgentCallback :: NotifyOrphanedSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="0f359-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="0f359-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0f359-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0f359-108">La méthode **INapSystemHealthAgentCallback :: NotifyOrphanedSoHRequest** est appelée si un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a été interrogé à partir de l’algorithme SHA, mais que la réponse n’a jamais été renvoyée.</span><span class="sxs-lookup"><span data-stu-id="0f359-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f359-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f359-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="0f359-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f359-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f359-111">*CorrelationId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f359-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f359-112">Pointeur vers la structure d’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique qui identifie le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)orphelin.</span><span class="sxs-lookup"><span data-stu-id="0f359-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f359-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f359-113">Return value</span></span>

<span data-ttu-id="0f359-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0f359-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0f359-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0f359-115">Return code</span></span>                                                                          | <span data-ttu-id="0f359-116">Description</span><span class="sxs-lookup"><span data-stu-id="0f359-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="0f359-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f359-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0f359-118">Indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0f359-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f359-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0f359-119">Remarks</span></span>

<span data-ttu-id="0f359-120">Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.</span><span class="sxs-lookup"><span data-stu-id="0f359-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="0f359-121">Cette méthode peut être appelée par le système dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="0f359-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="0f359-122">Un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) n’a pas pu être envoyé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0f359-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="0f359-123">Un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a été envoyé sur le réseau, mais aucun **SoHResponse** n’a été renvoyé, c.-à-d. que l’application a dépassé le délai d’attente ou qu’il n’y avait pas de validateur de validateur correspondant côté serveur.</span><span class="sxs-lookup"><span data-stu-id="0f359-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="0f359-124">La connexion s’est arrêtée ou un enforceur est passé hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0f359-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="0f359-125">Comme il ne s’agit que d’une notification de meilleur effort, il ne doit pas compter sur ces informations pour nettoyer l’État.</span><span class="sxs-lookup"><span data-stu-id="0f359-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="0f359-126">Il existe plusieurs situations dans lesquelles un SHA ne sera pas notifié :</span><span class="sxs-lookup"><span data-stu-id="0f359-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="0f359-127">En cas de dysfonctionnement d’un application, autrement dit, il n’avertit pas l’SHA lorsque l’état de la connexion est inactif.</span><span class="sxs-lookup"><span data-stu-id="0f359-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="0f359-128">Si une application se bloque.</span><span class="sxs-lookup"><span data-stu-id="0f359-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="0f359-129">Dans les conditions d’erreur, par exemple, la mémoire NapAgent est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0f359-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="0f359-130">Les agents d’intégrité du service peuvent obtenir des notifications erronées lorsqu’ils se lient pour la première fois au NapAgent, par exemple, si un échange SoH est en cours d’exécution lorsque la liaison SHA est terminée, puis expire.</span><span class="sxs-lookup"><span data-stu-id="0f359-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f359-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f359-131">Requirements</span></span>



| <span data-ttu-id="0f359-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f359-132">Requirement</span></span> | <span data-ttu-id="0f359-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f359-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f359-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f359-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0f359-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f359-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0f359-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f359-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0f359-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f359-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0f359-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f359-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f359-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f359-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f359-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="0f359-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f359-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f359-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f359-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f359-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f359-143">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="0f359-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





