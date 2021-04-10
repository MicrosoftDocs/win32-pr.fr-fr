---
title: Méthode INapServerManagement SetFailureCategoryMappings (NapServerManagement. h)
description: Est utilisé pour définir les mappages de catégorie d’échec du VALIDateur.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Méthode SetFailureCategoryMappings NAP
- Méthode SetFailureCategoryMappings NAP, interface INapServerManagement
- INapServerManagement interface NAP, méthode SetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942428"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="3238a-106">INapServerManagement :: SetFailureCategoryMappings, méthode</span><span class="sxs-lookup"><span data-stu-id="3238a-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="3238a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3238a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3238a-108">La méthode **INapServerManagement :: SetFailureCategoryMappings** est utilisée pour définir les mappages de catégorie d’échec du SHV.</span><span class="sxs-lookup"><span data-stu-id="3238a-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="3238a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3238a-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="3238a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3238a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3238a-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3238a-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3238a-112">[**SystemHealthEntityId**](nap-type-constants.md) qui contient l’identificateur unique de la SHV.</span><span class="sxs-lookup"><span data-stu-id="3238a-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="3238a-113">*mappage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3238a-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3238a-114">Structure [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) qui contient les données de mappage de catégorie d’échec.</span><span class="sxs-lookup"><span data-stu-id="3238a-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3238a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3238a-115">Return value</span></span>

<span data-ttu-id="3238a-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="3238a-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3238a-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3238a-117">Return code</span></span>                                                                                     | <span data-ttu-id="3238a-118">Description</span><span class="sxs-lookup"><span data-stu-id="3238a-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3238a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3238a-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3238a-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3238a-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3238a-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3238a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3238a-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="3238a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3238a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3238a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3238a-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3238a-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3238a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3238a-125">Requirements</span></span>



| <span data-ttu-id="3238a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3238a-126">Requirement</span></span> | <span data-ttu-id="3238a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3238a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3238a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3238a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3238a-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3238a-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="3238a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3238a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3238a-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3238a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3238a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3238a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3238a-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="3238a-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="3238a-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="3238a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3238a-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3238a-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="3238a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3238a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3238a-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3238a-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="3238a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3238a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3238a-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="3238a-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





