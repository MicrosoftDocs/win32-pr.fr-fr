---
title: Méthode INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: Est appelé par le NapAgent pour interroger la demande de déclaration d’intégrité de l’agent d’intégrité système.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384836"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="95d3a-106">INapSystemHealthAgentCallback :: GetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="95d3a-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="95d3a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="95d3a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="95d3a-108">La méthode **INapSystemHealthAgentCallback :: GetSoHRequest** est appelée par le NapAgent pour interroger la requête soh de l’agent d’intégrité système.</span><span class="sxs-lookup"><span data-stu-id="95d3a-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d3a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95d3a-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="95d3a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95d3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d3a-111">*demande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95d3a-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d3a-112">Pointeur COM vers un objet [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) qui identifie l’objet de requête.</span><span class="sxs-lookup"><span data-stu-id="95d3a-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d3a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95d3a-113">Return value</span></span>



| <span data-ttu-id="95d3a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="95d3a-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="95d3a-115">Description</span><span class="sxs-lookup"><span data-stu-id="95d3a-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95d3a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95d3a-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="95d3a-117">Indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="95d3a-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="95d3a-118"><dt>**HRESULT \_ à partir de \_ Win32 (RPC \_ S \_ Server \_ non disponible)**</dt></span><span class="sxs-lookup"><span data-stu-id="95d3a-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="95d3a-119">Si ce code est retourné par votre implémentation, NapAgent supprime l’algorithme SHA de la liste des transactions de hachage et vide son entrée de cache.</span><span class="sxs-lookup"><span data-stu-id="95d3a-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="95d3a-120">Quand une valeur de retour (à l’exception **\_ de HRESULT de \_ Win32 (RPC \_ S \_ Server \_ non disponible)**) est retournée par votre implémentation, le système NAP construit et retourne un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à la SHV correspondante avec les types et valeurs d’attribut suivants :</span><span class="sxs-lookup"><span data-stu-id="95d3a-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="95d3a-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="95d3a-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="95d3a-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="95d3a-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="95d3a-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <> de code d’erreur</span><span class="sxs-lookup"><span data-stu-id="95d3a-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="95d3a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="95d3a-124">Remarks</span></span>

<span data-ttu-id="95d3a-125">Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.</span><span class="sxs-lookup"><span data-stu-id="95d3a-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="95d3a-126">Cette méthode doit traiter la demande et retourner immédiatement.</span><span class="sxs-lookup"><span data-stu-id="95d3a-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="95d3a-127">Le retardement du retour de cette méthode a un impact négatif sur les performances du système et la réactivité, et peut entraîner l’expiration du délai d’autres parties du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="95d3a-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="95d3a-128">L’analyse de l’état d’intégrité ne doit pas être effectuée dans le cadre de cet appel, en particulier s’il s’agit d’un calcul intensif et prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="95d3a-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="95d3a-129">L’analyse de l’état d’intégrité et le calcul de l’SoH doivent être effectués dans un service ou un thread distinct.</span><span class="sxs-lookup"><span data-stu-id="95d3a-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="95d3a-130">La seule fonction de cette méthode consiste à définir la SoH de l’algorithme SHA et à retourner.</span><span class="sxs-lookup"><span data-stu-id="95d3a-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="95d3a-131">Si l’algorithme SHA prend beaucoup de temps pour générer une SoH, la SoH mise en cache doit être retournée au NapAgent.</span><span class="sxs-lookup"><span data-stu-id="95d3a-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="95d3a-132">S’il n’y a aucune déclaration SoH mise en cache à retourner, le SHA doit immédiatement retourner une SoH avec les valeurs et types d’attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="95d3a-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="95d3a-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="95d3a-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="95d3a-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="95d3a-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="95d3a-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  E/r [ **NAP \_ \_ non \_ mis en cache \_**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="95d3a-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="95d3a-136">Une fois la SoH générée, l’agent SHA doit appeler [**INapSystemHealthAgentBinding :: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) pour notifier le NapAgent de la modification d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="95d3a-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="95d3a-137">Le NapAgent appelle cette méthode pour interroger le SoHRequest de l’agent d’intégrité système.</span><span class="sxs-lookup"><span data-stu-id="95d3a-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="95d3a-138">L’agent SHA peut interroger l’objet [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passé pour les paramètres dont il a besoin pour calculer le SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="95d3a-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="95d3a-139">L’algorithme SHA doit définir le SoHRequest calculé sur l’objet de requête.</span><span class="sxs-lookup"><span data-stu-id="95d3a-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="95d3a-140">L’algorithme SHA ne doit pas contenir de références à l’objet de requête une fois cet appel terminé.</span><span class="sxs-lookup"><span data-stu-id="95d3a-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="95d3a-141">Lorsque cette méthode est appelée, s’il existe une SoH dans le cache de NapAgent, elle est définie sur l’objet de requête.</span><span class="sxs-lookup"><span data-stu-id="95d3a-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="95d3a-142">L’agent SHA peut l’interroger à l’aide de **GetSoHRequest**.</span><span class="sxs-lookup"><span data-stu-id="95d3a-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="95d3a-143">Si l’algorithme SHA ne définit pas une nouvelle SoH, l’algorithme mis en cache est utilisé.</span><span class="sxs-lookup"><span data-stu-id="95d3a-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="95d3a-144">Pour les Sha non liés qui sont inscrits auprès du système, le système NAP construit et envoie un SoHRequest au VALIDateur correspondant avec les types et valeurs d’attribut suivants :</span><span class="sxs-lookup"><span data-stu-id="95d3a-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="95d3a-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="95d3a-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="95d3a-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="95d3a-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="95d3a-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ non \_ initialisé**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="95d3a-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="95d3a-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95d3a-148">Requirements</span></span>



| <span data-ttu-id="95d3a-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95d3a-149">Requirement</span></span> | <span data-ttu-id="95d3a-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="95d3a-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d3a-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95d3a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="95d3a-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95d3a-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="95d3a-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95d3a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="95d3a-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95d3a-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="95d3a-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="95d3a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d3a-156"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d3a-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="95d3a-157">MIDL</span><span class="sxs-lookup"><span data-stu-id="95d3a-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95d3a-158"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95d3a-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d3a-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95d3a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d3a-160">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="95d3a-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





