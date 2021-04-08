---
title: Méthode INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: Est utilisé par le client de mise en œuvre pour récupérer une requête SoH pour une connexion particulière.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941919"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="7a18a-106">INapEnforcementClientBinding :: GetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="7a18a-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="7a18a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a18a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7a18a-108">La méthode **INapEnforcementClientBinding :: GetSoHRequest** est utilisée par le client de mise en œuvre pour récupérer une requête SOH pour une connexion particulière.</span><span class="sxs-lookup"><span data-stu-id="7a18a-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a18a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a18a-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="7a18a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a18a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a18a-111">*connexion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a18a-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a18a-112">Pointeur COM vers une interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="7a18a-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="7a18a-113">NapAgent ne contient pas de références à l’objet associé à cette interface une fois la méthode terminée.</span><span class="sxs-lookup"><span data-stu-id="7a18a-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="7a18a-114">*retriggerHint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7a18a-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a18a-115">Pointeur vers un **booléen** qui indique si la connexion doit être redéclenchée.</span><span class="sxs-lookup"><span data-stu-id="7a18a-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="7a18a-116">Elle a la **valeur true** si le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a changé depuis le dernier appel à cette fonction ou si [**ProbationTime**](nap-datatypes.md) a expiré.</span><span class="sxs-lookup"><span data-stu-id="7a18a-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="7a18a-117">Sinon, la **valeur false** est retournée.</span><span class="sxs-lookup"><span data-stu-id="7a18a-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a18a-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a18a-118">Return value</span></span>

<span data-ttu-id="7a18a-119">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="7a18a-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7a18a-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7a18a-120">Return code</span></span>                                                                                             | <span data-ttu-id="7a18a-121">Description</span><span class="sxs-lookup"><span data-stu-id="7a18a-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a18a-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="7a18a-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7a18a-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="7a18a-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="7a18a-125">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="7a18a-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7a18a-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="7a18a-127">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7a18a-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7a18a-128"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="7a18a-129">L’application n’a pas été précédemment initialisée.</span><span class="sxs-lookup"><span data-stu-id="7a18a-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="7a18a-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7a18a-130">Remarks</span></span>

<span data-ttu-id="7a18a-131">NapAgent définit [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) sur l’objet de connexion.</span><span class="sxs-lookup"><span data-stu-id="7a18a-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="7a18a-132">Si une [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) était en attente sur cette connexion, elle est ignorée et les Sha sont avertis du **SoHRequests** orphelin.</span><span class="sxs-lookup"><span data-stu-id="7a18a-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="7a18a-133">Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="7a18a-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a18a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a18a-134">Requirements</span></span>



| <span data-ttu-id="7a18a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a18a-135">Requirement</span></span> | <span data-ttu-id="7a18a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a18a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a18a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a18a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7a18a-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a18a-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7a18a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a18a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7a18a-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a18a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7a18a-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a18a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a18a-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a18a-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="7a18a-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a18a-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7a18a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7a18a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a18a-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7a18a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a18a-147">See also</span></span>

<dl> <span data-ttu-id="7a18a-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="7a18a-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="7a18a-149">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="7a18a-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





