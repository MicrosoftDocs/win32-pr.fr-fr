---
title: Méthode INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: Est utilisé par les agents d’intégrité pour écrire leur demande d’intégrité résultant de l’appel à INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Méthode SetSoHRequest NAP
- Méthode SetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510529"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="f65b3-106">INapSystemHealthAgentRequest :: SetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="f65b3-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="f65b3-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f65b3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f65b3-108">La méthode **INapSystemHealthAgentRequest :: SetSoHRequest** est utilisée par les agents d’intégrité pour écrire leur demande d’intégrité résultant de l’appel à [**INapSystemHealthAgentCallback :: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="f65b3-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f65b3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f65b3-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="f65b3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f65b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65b3-111">*sohRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f65b3-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65b3-112">Pointeur vers un paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="f65b3-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="f65b3-113">*cacheSohForLaterUse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f65b3-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f65b3-114">Valeur **booléenne** qui est **true** si NapAgent doit mettre en cache la [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f65b3-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65b3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f65b3-115">Return value</span></span>

<span data-ttu-id="f65b3-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="f65b3-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f65b3-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f65b3-117">Return code</span></span>                                                                                     | <span data-ttu-id="f65b3-118">Description</span><span class="sxs-lookup"><span data-stu-id="f65b3-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f65b3-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f65b3-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f65b3-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f65b3-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f65b3-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f65b3-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f65b3-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="f65b3-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f65b3-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f65b3-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f65b3-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f65b3-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f65b3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f65b3-125">Requirements</span></span>



| <span data-ttu-id="f65b3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f65b3-126">Requirement</span></span> | <span data-ttu-id="f65b3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f65b3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f65b3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f65b3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f65b3-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f65b3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f65b3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f65b3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f65b3-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f65b3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f65b3-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f65b3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f65b3-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="f65b3-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f65b3-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="f65b3-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f65b3-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f65b3-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="f65b3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f65b3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f65b3-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f65b3-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="f65b3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f65b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65b3-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="f65b3-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





