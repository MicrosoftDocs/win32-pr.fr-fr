---
title: Méthode INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Annule l’inscription d’un SHA auprès du système NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Méthode UnregisterSystemHealthAgent NAP
- Méthode UnregisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509118"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="43242-106">INapClientManagement :: UnregisterSystemHealthAgent, méthode</span><span class="sxs-lookup"><span data-stu-id="43242-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="43242-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="43242-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="43242-108">La méthode **UnregisterSystemHealthAgent** annule l’inscription d’un SHA auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="43242-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="43242-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43242-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="43242-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43242-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43242-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43242-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43242-112">[**SystemHealthEntityId**](nap-datatypes.md) qui identifie l’agent d’intégrité système dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="43242-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43242-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43242-113">Return value</span></span>

<span data-ttu-id="43242-114">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="43242-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="43242-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="43242-115">Return code</span></span>                                                                                         | <span data-ttu-id="43242-116">Description</span><span class="sxs-lookup"><span data-stu-id="43242-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="43242-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43242-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="43242-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="43242-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="43242-119"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="43242-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="43242-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="43242-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="43242-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="43242-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="43242-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="43242-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="43242-123"><dt>**la protection NAP est \_ \_ toujours \_ liée**</dt></span><span class="sxs-lookup"><span data-stu-id="43242-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="43242-124">L’algorithme SHA reste lié et ne peut pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="43242-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="43242-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43242-125">Requirements</span></span>



| <span data-ttu-id="43242-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43242-126">Requirement</span></span> | <span data-ttu-id="43242-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="43242-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43242-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43242-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43242-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43242-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="43242-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43242-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43242-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43242-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="43242-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="43242-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="43242-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="43242-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="43242-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="43242-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43242-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43242-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="43242-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43242-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43242-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43242-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="43242-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43242-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43242-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="43242-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





