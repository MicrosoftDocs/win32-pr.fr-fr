---
title: Méthode INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Récupère des informations sur les clients de mise en œuvre inscrits.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Méthode GetRegisteredEnforcementClients NAP
- Méthode GetRegisteredEnforcementClients NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466043"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="8f578-106">INapClientManagement :: GetRegisteredEnforcementClients, méthode</span><span class="sxs-lookup"><span data-stu-id="8f578-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="8f578-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8f578-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8f578-108">La méthode **GetRegisteredEnforcementClients** récupère des informations sur les clients de mise en œuvre inscrits.</span><span class="sxs-lookup"><span data-stu-id="8f578-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f578-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f578-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="8f578-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f578-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f578-111">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8f578-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f578-112">Pointeur vers un [**EnforcementEntityCount**](nap-datatypes.md) qui contient le nombre de clients de mise en œuvre inscrits.</span><span class="sxs-lookup"><span data-stu-id="8f578-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="8f578-113">*application* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8f578-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f578-114">Pointeur vers un tableau de structures [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui décrivent les clients de mise en œuvre inscrits.</span><span class="sxs-lookup"><span data-stu-id="8f578-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f578-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f578-115">Return value</span></span>

<span data-ttu-id="8f578-116">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8f578-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="8f578-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8f578-117">Return code</span></span>                                                                                         | <span data-ttu-id="8f578-118">Description</span><span class="sxs-lookup"><span data-stu-id="8f578-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f578-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="8f578-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8f578-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8f578-121"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="8f578-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8f578-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8f578-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="8f578-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8f578-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8f578-125"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8f578-126">NapAgent n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8f578-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="8f578-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f578-127">Requirements</span></span>



| <span data-ttu-id="8f578-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f578-128">Requirement</span></span> | <span data-ttu-id="8f578-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f578-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f578-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f578-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8f578-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f578-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8f578-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f578-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8f578-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f578-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8f578-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f578-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f578-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f578-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="8f578-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f578-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="8f578-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8f578-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f578-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f578-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="8f578-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f578-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f578-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="8f578-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





