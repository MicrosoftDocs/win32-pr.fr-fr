---
title: Méthode INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: Est utilisé par le NapAgent pour informer le client de contrainte des modifications de déclaration d’intégrité.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Méthode NotifySoHChange NAP
- Méthode NotifySoHChange NAP, interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, méthode NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106432"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="e2519-106">INapEnforcementClientCallback :: NotifySoHChange, méthode</span><span class="sxs-lookup"><span data-stu-id="e2519-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="e2519-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2519-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e2519-108">La méthode de rappel **INapEnforcementClientCallback :: NotifySoHChange** est utilisée par le NapAgent pour informer le client de contrainte des modifications de SOH.</span><span class="sxs-lookup"><span data-stu-id="e2519-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2519-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2519-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="e2519-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2519-110">Parameters</span></span>

<span data-ttu-id="e2519-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e2519-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2519-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2519-112">Return value</span></span>

<span data-ttu-id="e2519-113">Cette méthode de rappel doit retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="e2519-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="e2519-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e2519-114">Return code</span></span>                                                                                                | <span data-ttu-id="e2519-115">Description</span><span class="sxs-lookup"><span data-stu-id="e2519-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2519-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2519-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e2519-117">Retourne cette valeur si l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e2519-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="e2519-118"><dt>**\_serveur RPC \_ S \_ non disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="e2519-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="e2519-119">Si cette valeur est retournée, l’application est supprimée de la liste de l’algorithme de hachage des transactions et l’entrée de cache NapAgent correspondante est vidée.</span><span class="sxs-lookup"><span data-stu-id="e2519-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="e2519-120">L’algorithme SHA défaillant peut alors se réinitialiser avec NapAgent.</span><span class="sxs-lookup"><span data-stu-id="e2519-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2519-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e2519-121">Remarks</span></span>

<span data-ttu-id="e2519-122">L’achèvement de la correction du système est un événement de modification de l’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="e2519-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="e2519-123">Cela signifie que vous devez appeler **NotifySoHChange** quand une notification [**INapSystemHealthAgentCallback :: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indique que le client est corrigé.</span><span class="sxs-lookup"><span data-stu-id="e2519-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="e2519-124">Lorsqu’un client est résolu, le membre d' **État** de la structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) retournée par **GetFixupInfo** a la valeur **fixupStateSuccess**.</span><span class="sxs-lookup"><span data-stu-id="e2519-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="e2519-125">Après avoir été appelé par le NapAgent via ce rappel, l’agent d’application doit ensuite appeler [**INapEnforcementClientBinding :: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) pour récupérer la nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="e2519-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="e2519-126">Cet appel peut être effectué sur le même thread que **INapEnforcementClientCallback :: NotifySoHChange**.</span><span class="sxs-lookup"><span data-stu-id="e2519-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2519-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2519-127">Requirements</span></span>



| <span data-ttu-id="e2519-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2519-128">Requirement</span></span> | <span data-ttu-id="e2519-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2519-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2519-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2519-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2519-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2519-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2519-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2519-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2519-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2519-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2519-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2519-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2519-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2519-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2519-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="e2519-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2519-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2519-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2519-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2519-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2519-139">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="e2519-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





