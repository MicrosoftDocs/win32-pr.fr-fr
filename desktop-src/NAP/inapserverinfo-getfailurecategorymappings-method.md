---
title: Méthode INapServerInfo GetFailureCategoryMappings (NapServerManagement. h)
description: Récupère les mappages de catégorie d’échec pour un SHA ou un VALIDateur spécifié.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Méthode GetFailureCategoryMappings NAP
- Méthode GetFailureCategoryMappings NAP, interface INapServerInfo
- INapServerInfo interface NAP, méthode GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467058"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="a4756-106">INapServerInfo :: GetFailureCategoryMappings, méthode</span><span class="sxs-lookup"><span data-stu-id="a4756-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="a4756-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a4756-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a4756-108">La méthode **INapServerInfo :: GetFailureCategoryMappings** récupère les mappages de catégorie d’échec pour un SHA ou un validateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4756-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4756-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4756-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="a4756-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4756-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4756-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4756-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4756-112">[**SystemHealthEntityId**](nap-type-constants.md) qui contient l’identificateur unique de l’agent SHA ou du SHV.</span><span class="sxs-lookup"><span data-stu-id="a4756-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="a4756-113">*mappage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a4756-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4756-114">Pointeur vers un [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) qui contient les données de mappage.</span><span class="sxs-lookup"><span data-stu-id="a4756-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4756-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4756-115">Return value</span></span>

<span data-ttu-id="a4756-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="a4756-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a4756-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a4756-117">Return code</span></span>                                                                                     | <span data-ttu-id="a4756-118">Description</span><span class="sxs-lookup"><span data-stu-id="a4756-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a4756-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4756-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a4756-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="a4756-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a4756-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a4756-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a4756-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="a4756-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a4756-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a4756-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a4756-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a4756-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a4756-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4756-125">Requirements</span></span>



| <span data-ttu-id="a4756-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4756-126">Requirement</span></span> | <span data-ttu-id="a4756-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4756-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4756-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4756-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a4756-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4756-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="a4756-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4756-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a4756-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4756-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a4756-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4756-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4756-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4756-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4756-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="a4756-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4756-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4756-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="a4756-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a4756-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4756-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4756-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="a4756-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4756-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4756-139">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="a4756-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





