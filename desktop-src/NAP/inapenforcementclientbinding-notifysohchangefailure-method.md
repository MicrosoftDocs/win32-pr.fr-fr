---
title: Méthode INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient. h)
description: Est utilisé par le client de mise en œuvre pour informer NapAgent qu’il n’a pas pu traiter un NotifySoHChange INapEnforcementClientCallback précédent.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Méthode NotifySoHChangeFailure NAP
- Méthode NotifySoHChangeFailure NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode NotifySoHChangeFailure
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467006"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="fcc70-106">INapEnforcementClientBinding :: NotifySoHChangeFailure, méthode</span><span class="sxs-lookup"><span data-stu-id="fcc70-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="fcc70-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fcc70-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fcc70-108">La méthode **INapEnforcementClientBinding :: NotifySoHChangeFailure** est utilisée par le client de mise en œuvre pour informer le NapAgent qu’il n’a pas pu traiter un [**INapEnforcementClientCallback :: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)précédent.</span><span class="sxs-lookup"><span data-stu-id="fcc70-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc70-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcc70-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="fcc70-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcc70-110">Parameters</span></span>

<span data-ttu-id="fcc70-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fcc70-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fcc70-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcc70-112">Return value</span></span>

<span data-ttu-id="fcc70-113">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="fcc70-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fcc70-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fcc70-114">Return code</span></span>                                                                                             | <span data-ttu-id="fcc70-115">Description</span><span class="sxs-lookup"><span data-stu-id="fcc70-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fcc70-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="fcc70-117">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="fcc70-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="fcc70-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="fcc70-119">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="fcc70-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fcc70-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="fcc70-121">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="fcc70-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fcc70-122"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="fcc70-123">L’application n’a pas été précédemment initialisée.</span><span class="sxs-lookup"><span data-stu-id="fcc70-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="fcc70-124">Notes</span><span class="sxs-lookup"><span data-stu-id="fcc70-124">Remarks</span></span>

<span data-ttu-id="fcc70-125">À la suite de cette méthode, l’appel de NapAgent tente d’appliquer la modification de SoH ultérieurement en appelant [**INapEnforcementClientCallback :: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc70-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="fcc70-126">Une fois que le client de contrainte a appelé [**INapEnforcementClientBinding :: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), il doit ensuite appliquer la modification, ce qui signifie qu’aucune défaillance n’est gérée par le NapAgent après ce point.</span><span class="sxs-lookup"><span data-stu-id="fcc70-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="fcc70-127">Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc70-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc70-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcc70-128">Requirements</span></span>



| <span data-ttu-id="fcc70-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcc70-129">Requirement</span></span> | <span data-ttu-id="fcc70-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcc70-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc70-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcc70-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc70-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcc70-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fcc70-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcc70-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc70-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcc70-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fcc70-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcc70-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcc70-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcc70-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="fcc70-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fcc70-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fcc70-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fcc70-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcc70-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fcc70-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcc70-141">See also</span></span>

<dl> <span data-ttu-id="fcc70-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fcc70-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="fcc70-143">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="fcc70-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="fcc70-144">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="fcc70-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="fcc70-145">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="fcc70-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





