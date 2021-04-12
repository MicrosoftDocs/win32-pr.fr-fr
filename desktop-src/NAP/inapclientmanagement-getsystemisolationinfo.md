---
title: Méthode INapClientManagement GetSystemIsolationInfo (NapManagement. h)
description: Récupère des informations sur l’état d’isolement du NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Méthode GetSystemIsolationInfo NAP
- Méthode GetSystemIsolationInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385016"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="e89dd-106">INapClientManagement :: GetSystemIsolationInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="e89dd-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="e89dd-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e89dd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e89dd-108">La méthode **GetSystemIsolationInfo** récupère les informations sur l’état d’isolement du NapClient.</span><span class="sxs-lookup"><span data-stu-id="e89dd-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="e89dd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e89dd-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="e89dd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e89dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e89dd-111">*isolationInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e89dd-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e89dd-112">Pointeur vers un pointeur vers une structure [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) qui contient les informations d’état d’isolement.</span><span class="sxs-lookup"><span data-stu-id="e89dd-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="e89dd-113">*unknownConnections* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e89dd-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e89dd-114">Pointeur vers un indicateur qui indique si l’une des connexions est dans un état inconnu.</span><span class="sxs-lookup"><span data-stu-id="e89dd-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="e89dd-115">Si l’un d’eux est, l’indicateur a la valeur **true**; Sinon, l’indicateur a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="e89dd-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e89dd-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e89dd-116">Return value</span></span>

<span data-ttu-id="e89dd-117">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="e89dd-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="e89dd-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e89dd-118">Return code</span></span>                                                                                         | <span data-ttu-id="e89dd-119">Description</span><span class="sxs-lookup"><span data-stu-id="e89dd-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e89dd-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="e89dd-121">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e89dd-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e89dd-122"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="e89dd-123">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e89dd-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e89dd-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="e89dd-125">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e89dd-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e89dd-126"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e89dd-127">NapAgent n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e89dd-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="e89dd-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e89dd-128">Remarks</span></span>

<span data-ttu-id="e89dd-129">Les informations d’isolation récupérées ne reflètent pas les États inconnus.</span><span class="sxs-lookup"><span data-stu-id="e89dd-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="e89dd-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e89dd-130">Requirements</span></span>



| <span data-ttu-id="e89dd-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e89dd-131">Requirement</span></span> | <span data-ttu-id="e89dd-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e89dd-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e89dd-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e89dd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e89dd-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e89dd-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e89dd-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e89dd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e89dd-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e89dd-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e89dd-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="e89dd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e89dd-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="e89dd-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="e89dd-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e89dd-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="e89dd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e89dd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e89dd-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="e89dd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e89dd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89dd-144">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="e89dd-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





