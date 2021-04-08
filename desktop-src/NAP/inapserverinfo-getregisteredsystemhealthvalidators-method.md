---
title: Méthode INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement. h)
description: Récupère une liste des validateurs d’intégrité inscrits.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Méthode GetRegisteredSystemHealthValidators NAP
- Méthode GetRegisteredSystemHealthValidators NAP, interface INapServerInfo
- INapServerInfo interface NAP, méthode GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033127"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="4c12b-106">INapServerInfo :: GetRegisteredSystemHealthValidators, méthode</span><span class="sxs-lookup"><span data-stu-id="4c12b-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="4c12b-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="4c12b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4c12b-108">La méthode **INapServerInfo :: GetRegisteredSystemHealthValidators** récupère une liste des validateurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="4c12b-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c12b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c12b-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="4c12b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c12b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c12b-111">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c12b-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c12b-112">Pointeur vers un [**SystemHealthEntityCount**](nap-type-constants.md) qui contient le nombre de validateurs d’intégrité du système inscrits.</span><span class="sxs-lookup"><span data-stu-id="4c12b-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="4c12b-113">*validateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c12b-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c12b-114">Pointeur vers un pointeur vers une structure [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription SHV.</span><span class="sxs-lookup"><span data-stu-id="4c12b-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="4c12b-115">*validatorClsids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c12b-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c12b-116">Pointeur vers un tableau d’ID pour les validateurs d’intégrité inscrits.</span><span class="sxs-lookup"><span data-stu-id="4c12b-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c12b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c12b-117">Return value</span></span>

<span data-ttu-id="4c12b-118">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="4c12b-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4c12b-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4c12b-119">Return code</span></span>                                                                                     | <span data-ttu-id="4c12b-120">Description</span><span class="sxs-lookup"><span data-stu-id="4c12b-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c12b-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c12b-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4c12b-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4c12b-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4c12b-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4c12b-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4c12b-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="4c12b-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4c12b-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4c12b-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4c12b-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="4c12b-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c12b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c12b-127">Requirements</span></span>



| <span data-ttu-id="4c12b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c12b-128">Requirement</span></span> | <span data-ttu-id="4c12b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c12b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c12b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c12b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c12b-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c12b-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="4c12b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c12b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c12b-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c12b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4c12b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c12b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c12b-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c12b-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c12b-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="4c12b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c12b-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c12b-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="4c12b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4c12b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c12b-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c12b-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="4c12b-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c12b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c12b-141">**NapComponentRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="4c12b-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="4c12b-142">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="4c12b-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





