---
title: Méthode INapSystemHealthAgentRequest GetCacheSoHFlag (NapSystemHealthAgent. h)
description: Est utilisé uniquement par NapAgent.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Méthode GetCacheSoHFlag NAP
- Méthode GetCacheSoHFlag NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetCacheSoHFlag
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509002"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="5e2f0-106">INapSystemHealthAgentRequest :: GetCacheSoHFlag, méthode</span><span class="sxs-lookup"><span data-stu-id="5e2f0-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="5e2f0-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5e2f0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e2f0-108">La méthode **INapSystemHealthAgentRequest :: GetCacheSoHFlag** est utilisée uniquement par le NapAgent.</span><span class="sxs-lookup"><span data-stu-id="5e2f0-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2f0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e2f0-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="5e2f0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e2f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2f0-111">*cacheSohForLaterUse*</span><span class="sxs-lookup"><span data-stu-id="5e2f0-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="5e2f0-112">Valeur **booléenne** qui est **true** si NapAgent doit mettre en cache la [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5e2f0-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2f0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e2f0-113">Return value</span></span>

<span data-ttu-id="5e2f0-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="5e2f0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5e2f0-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5e2f0-115">Return code</span></span>                                                                                     | <span data-ttu-id="5e2f0-116">Description</span><span class="sxs-lookup"><span data-stu-id="5e2f0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e2f0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5e2f0-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5e2f0-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5e2f0-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5e2f0-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="5e2f0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5e2f0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5e2f0-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5e2f0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5e2f0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e2f0-123">Requirements</span></span>



| <span data-ttu-id="5e2f0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e2f0-124">Requirement</span></span> | <span data-ttu-id="5e2f0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e2f0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2f0-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e2f0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2f0-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e2f0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e2f0-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e2f0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2f0-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e2f0-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e2f0-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e2f0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e2f0-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f0-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e2f0-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="5e2f0-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e2f0-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f0-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e2f0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5e2f0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e2f0-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f0-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="5e2f0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e2f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2f0-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="5e2f0-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





