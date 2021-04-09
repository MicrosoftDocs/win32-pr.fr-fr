---
title: Méthode INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Peut être utilisé par les SoHs de récupération d’intégrité du NapAgent précédemment mis en cache par le.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033186"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="01d5c-106">INapSystemHealthAgentRequest :: GetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="01d5c-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="01d5c-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="01d5c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="01d5c-108">La méthode **INapSystemHealthAgentRequest :: GetSoHRequest** peut être utilisée par les SoHs de récupération d’intégrité des précédemment mises en cache par NapAgent.</span><span class="sxs-lookup"><span data-stu-id="01d5c-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d5c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01d5c-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="01d5c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01d5c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d5c-111">*sohRequest* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="01d5c-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01d5c-112">Pointeur vers un pointeur vers un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="01d5c-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d5c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01d5c-113">Return value</span></span>

<span data-ttu-id="01d5c-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="01d5c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="01d5c-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="01d5c-115">Return code</span></span>                                                                                            | <span data-ttu-id="01d5c-116">Description</span><span class="sxs-lookup"><span data-stu-id="01d5c-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01d5c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="01d5c-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="01d5c-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="01d5c-119"><dt>**E/r NAP \_ \_ non \_ mis en cache \_**</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="01d5c-120">SoH introuvable ; NapAgent n’a pas de copie mise en cache.</span><span class="sxs-lookup"><span data-stu-id="01d5c-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="01d5c-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="01d5c-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="01d5c-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="01d5c-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="01d5c-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="01d5c-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="01d5c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01d5c-125">Requirements</span></span>



| <span data-ttu-id="01d5c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01d5c-126">Requirement</span></span> | <span data-ttu-id="01d5c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="01d5c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d5c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01d5c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="01d5c-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01d5c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="01d5c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01d5c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="01d5c-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01d5c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="01d5c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="01d5c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d5c-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="01d5c-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="01d5c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01d5c-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="01d5c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="01d5c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d5c-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d5c-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="01d5c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d5c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d5c-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="01d5c-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





