---
title: INapEnforcementClientBinding Initialize, méthode (NapEnforcementClient. h)
description: Démarre automatiquement le service NapAgent.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464830"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="6f2a1-106">INapEnforcementClientBinding :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="6f2a1-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="6f2a1-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6f2a1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6f2a1-108">La méthode **INapEnforcementClientBinding :: Initialize** démarre automatiquement le service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2a1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f2a1-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="6f2a1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f2a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f2a1-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f2a1-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f2a1-112">[**EnforcementEntityId**](nap-datatypes.md) qui identifie le client de mise en œuvre et sa version.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="6f2a1-113">*rappel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f2a1-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f2a1-114">Pointeur COM vers une interface [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) utilisée par le NapAgent pour rappeler les clients de mise en œuvre avec Notify/Process.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="6f2a1-115">Le NapAgent contient une référence à l’objet associé à cette interface jusqu’à ce que [**INapEnforcementClientBinding :: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f2a1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f2a1-116">Return value</span></span>

<span data-ttu-id="6f2a1-117">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6f2a1-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6f2a1-118">Return code</span></span>                                                                                                         | <span data-ttu-id="6f2a1-119">Description</span><span class="sxs-lookup"><span data-stu-id="6f2a1-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f2a1-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="6f2a1-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6f2a1-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="6f2a1-123">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="6f2a1-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="6f2a1-125">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="6f2a1-126"><dt>**HRESULT (erreur \_ déjà \_ initialisée)**</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="6f2a1-127">Si l’application d’application a été précédemment initialisée, ce code d’erreur est retourné.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="6f2a1-128"><dt>**NAP \_ E \_ non \_ inscrit**</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="6f2a1-129">Si l’application n’a pas été inscrite précédemment, ce code d’erreur est retourné.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6f2a1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="6f2a1-130">Remarks</span></span>

<span data-ttu-id="6f2a1-131">Le client de contrainte doit appeler la méthode **INapEnforcementClientBinding :: Initialize** avant d’appeler toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="6f2a1-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f2a1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f2a1-132">Requirements</span></span>



| <span data-ttu-id="6f2a1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f2a1-133">Requirement</span></span> | <span data-ttu-id="6f2a1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f2a1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f2a1-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f2a1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6f2a1-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f2a1-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6f2a1-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f2a1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6f2a1-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f2a1-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6f2a1-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f2a1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f2a1-140"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f2a1-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="6f2a1-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f2a1-142"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="6f2a1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6f2a1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f2a1-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="6f2a1-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f2a1-145">See also</span></span>

<dl> <span data-ttu-id="6f2a1-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6f2a1-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="6f2a1-147">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="6f2a1-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="6f2a1-148">**INapEnforcementClientBinding :: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="6f2a1-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





