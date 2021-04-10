---
title: Méthode INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Inscrit un SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Méthode RegisterSystemHealthValidator NAP
- Méthode RegisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, méthode RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200591"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="b1bb4-106">INapServerManagement :: RegisterSystemHealthValidator, méthode</span><span class="sxs-lookup"><span data-stu-id="b1bb4-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="b1bb4-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b1bb4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b1bb4-108">La méthode **INapServerManagement :: RegisterSystemHealthValidator** inscrit un SHV.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bb4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1bb4-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="b1bb4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1bb4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bb4-111">*validateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1bb4-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bb4-112">Pointeur vers une structure [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription SHV.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="b1bb4-113">*validatorClsid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1bb4-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bb4-114">Pointeur vers le CLSID de la classe COM qui implémente l’interface [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .</span><span class="sxs-lookup"><span data-stu-id="b1bb4-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bb4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1bb4-115">Return value</span></span>

<span data-ttu-id="b1bb4-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b1bb4-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b1bb4-117">Return code</span></span>                                                                                            | <span data-ttu-id="b1bb4-118">Description</span><span class="sxs-lookup"><span data-stu-id="b1bb4-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1bb4-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="b1bb4-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b1bb4-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="b1bb4-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b1bb4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="b1bb4-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b1bb4-125"><dt>**\_ID en \_ conflit NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="b1bb4-126">L’ID SHV est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="b1bb4-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1bb4-127">Requirements</span></span>



| <span data-ttu-id="b1bb4-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1bb4-128">Requirement</span></span> | <span data-ttu-id="b1bb4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1bb4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bb4-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1bb4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bb4-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1bb4-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="b1bb4-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1bb4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bb4-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1bb4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1bb4-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1bb4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1bb4-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1bb4-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="b1bb4-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1bb4-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1bb4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b1bb4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1bb4-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1bb4-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="b1bb4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1bb4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bb4-141">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="b1bb4-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





