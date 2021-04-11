---
title: Méthode INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Récupère des informations sur les Sha enregistrés.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Méthode GetRegisteredSystemHealthAgents NAP
- Méthode GetRegisteredSystemHealthAgents NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942430"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a><span data-ttu-id="18454-106">INapClientManagement :: GetRegisteredSystemHealthAgents, méthode</span><span class="sxs-lookup"><span data-stu-id="18454-106">INapClientManagement::GetRegisteredSystemHealthAgents method</span></span>

> [!Note]  
> <span data-ttu-id="18454-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="18454-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="18454-108">La méthode **GetRegisteredSystemHealthAgents** récupère des informations sur l’intégrité des données inscrite.</span><span class="sxs-lookup"><span data-stu-id="18454-108">The **GetRegisteredSystemHealthAgents** method retrieves information about the registered SHAs.</span></span>

## <a name="syntax"></a><span data-ttu-id="18454-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18454-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a><span data-ttu-id="18454-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18454-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18454-111">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18454-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18454-112">Pointeur vers un [**SystemHealthEntityCount**](nap-datatypes.md) qui décrit le nombre de Sha inscrits.</span><span class="sxs-lookup"><span data-stu-id="18454-112">A pointer to a [**SystemHealthEntityCount**](nap-datatypes.md) that describes the number of registered SHAs.</span></span>

</dd> <dt>

<span data-ttu-id="18454-113">*agents* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18454-113">*agents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18454-114">Pointeur vers un tableau de structures [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui décrivent les Sha inscrits.</span><span class="sxs-lookup"><span data-stu-id="18454-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered SHAs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18454-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18454-115">Return value</span></span>

<span data-ttu-id="18454-116">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="18454-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="18454-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="18454-117">Return code</span></span>                                                                                         | <span data-ttu-id="18454-118">Description</span><span class="sxs-lookup"><span data-stu-id="18454-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="18454-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="18454-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="18454-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="18454-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="18454-121"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="18454-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="18454-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="18454-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="18454-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="18454-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="18454-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="18454-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="18454-125"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="18454-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="18454-126">NapAgent n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="18454-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="18454-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18454-127">Requirements</span></span>



| <span data-ttu-id="18454-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18454-128">Requirement</span></span> | <span data-ttu-id="18454-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="18454-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18454-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18454-130">Minimum supported client</span></span><br/> | <span data-ttu-id="18454-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18454-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="18454-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18454-132">Minimum supported server</span></span><br/> | <span data-ttu-id="18454-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18454-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18454-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="18454-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="18454-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="18454-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="18454-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="18454-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18454-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18454-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="18454-138">DLL</span><span class="sxs-lookup"><span data-stu-id="18454-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18454-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18454-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="18454-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18454-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18454-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="18454-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





