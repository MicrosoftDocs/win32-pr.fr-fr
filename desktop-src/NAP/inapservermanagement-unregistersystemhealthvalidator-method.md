---
title: Méthode INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: Permet d’annuler l’inscription d’un SHV auprès du serveur NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Méthode UnregisterSystemHealthValidator NAP
- Méthode UnregisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, méthode UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509142"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="17956-106">INapServerManagement :: UnregisterSystemHealthValidator, méthode</span><span class="sxs-lookup"><span data-stu-id="17956-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="17956-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="17956-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="17956-108">La méthode **INapServerManagement :: UnregisterSystemHealthValidator** est utilisée pour annuler l’inscription d’un SHV auprès du serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="17956-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="17956-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17956-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="17956-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17956-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17956-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17956-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17956-112">[**SystemHealthEntityId**](nap-type-constants.md) qui contient l’identificateur unique de la SHV dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="17956-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17956-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17956-113">Return value</span></span>

<span data-ttu-id="17956-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="17956-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="17956-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="17956-115">Return code</span></span>                                                                                     | <span data-ttu-id="17956-116">Description</span><span class="sxs-lookup"><span data-stu-id="17956-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="17956-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17956-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="17956-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="17956-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="17956-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="17956-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="17956-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="17956-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="17956-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="17956-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="17956-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="17956-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17956-123">Notes</span><span class="sxs-lookup"><span data-stu-id="17956-123">Remarks</span></span>

<span data-ttu-id="17956-124">Si des appels asynchrones sont en attente sur le SHV, ils seront terminés plus tard et seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="17956-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="17956-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17956-125">Requirements</span></span>



| <span data-ttu-id="17956-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17956-126">Requirement</span></span> | <span data-ttu-id="17956-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="17956-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17956-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17956-128">Minimum supported client</span></span><br/> | <span data-ttu-id="17956-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17956-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="17956-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17956-130">Minimum supported server</span></span><br/> | <span data-ttu-id="17956-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17956-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17956-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="17956-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="17956-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="17956-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="17956-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="17956-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17956-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17956-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="17956-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17956-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17956-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17956-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="17956-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17956-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17956-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="17956-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





