---
title: Méthode INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Récupère des informations sur l’état d’isolement et l’état d’isolement étendu du NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Méthode GetSystemIsolationInfoEx NAP
- Méthode GetSystemIsolationInfoEx NAP, interface INapClientManagement2
- INapClientManagement2 interface NAP, méthode GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032658"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="7e530-106">INapClientManagement2 :: GetSystemIsolationInfoEx, méthode</span><span class="sxs-lookup"><span data-stu-id="7e530-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="7e530-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7e530-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7e530-108">La méthode **GetSystemIsolationInfoEx** récupère les informations relatives à l’état d’isolement et à l’état d’isolement étendu du NapClient.</span><span class="sxs-lookup"><span data-stu-id="7e530-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e530-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e530-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="7e530-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e530-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e530-111">*isolationInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e530-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e530-112">Pointeur vers un pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient les informations d’état d’isolement.</span><span class="sxs-lookup"><span data-stu-id="7e530-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="7e530-113">*unknownConnections* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e530-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e530-114">Pointeur vers une valeur BOOLÉENNE qui est **true** si l’une des connexions est dans un état inconnu et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7e530-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e530-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e530-115">Return value</span></span>

<span data-ttu-id="7e530-116">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="7e530-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="7e530-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7e530-117">Return code</span></span>                                                                                         | <span data-ttu-id="7e530-118">Description</span><span class="sxs-lookup"><span data-stu-id="7e530-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e530-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="7e530-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7e530-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7e530-121"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="7e530-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="7e530-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7e530-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="7e530-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7e530-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7e530-125"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7e530-126">NapAgent n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7e530-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="7e530-127">Notes</span><span class="sxs-lookup"><span data-stu-id="7e530-127">Remarks</span></span>

<span data-ttu-id="7e530-128">Les informations d’isolation récupérées ne reflètent pas les États inconnus.</span><span class="sxs-lookup"><span data-stu-id="7e530-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="7e530-129">L’algorithme SHA doit libérer la structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) en appelant [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="7e530-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e530-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e530-130">Requirements</span></span>



| <span data-ttu-id="7e530-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e530-131">Requirement</span></span> | <span data-ttu-id="7e530-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e530-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e530-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e530-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7e530-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e530-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e530-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e530-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7e530-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e530-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7e530-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e530-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e530-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e530-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="7e530-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e530-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="7e530-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7e530-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e530-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e530-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="7e530-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e530-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e530-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="7e530-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





