---
title: INapEnforcementClientBinding méthode Uninitialize (NapEnforcementClient. h)
description: Conclut le service NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Uninitialize la méthode NAP
- Uninitialize Method NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Uninitialize, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512617"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="3827b-106">INapEnforcementClientBinding :: Uninitialize, méthode</span><span class="sxs-lookup"><span data-stu-id="3827b-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="3827b-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3827b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3827b-108">La méthode **INapEnforcementClientBinding :: Uninitialize** conclut le service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="3827b-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3827b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3827b-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="3827b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3827b-110">Parameters</span></span>

<span data-ttu-id="3827b-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3827b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3827b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3827b-112">Return value</span></span>

<span data-ttu-id="3827b-113">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="3827b-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3827b-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3827b-114">Return code</span></span>                                                                                     | <span data-ttu-id="3827b-115">Description</span><span class="sxs-lookup"><span data-stu-id="3827b-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3827b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3827b-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3827b-117">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3827b-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="3827b-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3827b-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3827b-119">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="3827b-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3827b-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3827b-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3827b-121">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3827b-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3827b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3827b-122">Remarks</span></span>

<span data-ttu-id="3827b-123">NapAgent bloque le traitement jusqu’à ce que tous les appels existants sur les interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) et [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) soient terminés.</span><span class="sxs-lookup"><span data-stu-id="3827b-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="3827b-124">À la fin de cet appel, NapAgent libère toutes ses références sur les pointeurs COM du client de mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="3827b-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="3827b-125">Avant que cette fonction soit appelée, l’application doit appeler [**INapEnforcementClientBinding :: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) sur toutes ses connexions actives, afin que l’SHA puisse être averti si l’un de leurs SoH-Requests était orphelin.</span><span class="sxs-lookup"><span data-stu-id="3827b-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="3827b-126">Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="3827b-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3827b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3827b-127">Requirements</span></span>



| <span data-ttu-id="3827b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3827b-128">Requirement</span></span> | <span data-ttu-id="3827b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3827b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3827b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3827b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3827b-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3827b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3827b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3827b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3827b-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3827b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3827b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="3827b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3827b-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3827b-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3827b-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="3827b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3827b-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3827b-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3827b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3827b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3827b-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3827b-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3827b-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3827b-140">See also</span></span>

<dl> <span data-ttu-id="3827b-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3827b-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="3827b-142">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="3827b-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="3827b-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="3827b-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="3827b-144">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="3827b-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





