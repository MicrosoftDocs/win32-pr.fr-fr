---
title: Méthode INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: Est utilisé par l’agent d’intégrité pour récupérer son objet BLOB SoHResponse lorsque le NapAgent appelle INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Méthode GetSoHResponse NAP
- Méthode GetSoHResponse NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103293"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="5a65f-106">INapSystemHealthAgentRequest :: GetSoHResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="5a65f-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="5a65f-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5a65f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5a65f-108">La méthode **INapSystemHealthAgentRequest :: GetSoHResponse** est utilisée par l’agent d’intégrité pour récupérer son objet BLOB SoHResponse lorsque le NapAgent appelle [**INapSystemHealthAgentCallback ::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span><span class="sxs-lookup"><span data-stu-id="5a65f-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a65f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a65f-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="5a65f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a65f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a65f-111">*sohResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a65f-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a65f-112">Pointeur vers un pointeur vers un paquet [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="5a65f-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="5a65f-113">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a65f-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a65f-114">Pointeur vers un indicateur qui active la correction par l’algorithme SHA si le bit [**shaFixup**](nap-type-constants.md) est défini ; sinon, la correction est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5a65f-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="5a65f-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5a65f-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="5a65f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="5a65f-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="5a65f-117"><dt>**shaFixup**</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="5a65f-118">L’algorithme SHA est supposé effectuer la correction en fonction de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5a65f-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="5a65f-119">Si cet indicateur n’est pas défini, l’agent SHA ne doit pas effectuer de correction même si le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique qu’il n’est pas sain.</span><span class="sxs-lookup"><span data-stu-id="5a65f-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a65f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a65f-120">Return value</span></span>

<span data-ttu-id="5a65f-121">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="5a65f-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5a65f-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5a65f-122">Return code</span></span>                                                                                     | <span data-ttu-id="5a65f-123">Description</span><span class="sxs-lookup"><span data-stu-id="5a65f-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a65f-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5a65f-125">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5a65f-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5a65f-126"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5a65f-127">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="5a65f-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5a65f-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5a65f-129">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5a65f-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a65f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a65f-130">Requirements</span></span>



| <span data-ttu-id="5a65f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a65f-131">Requirement</span></span> | <span data-ttu-id="5a65f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a65f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a65f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a65f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5a65f-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a65f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5a65f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a65f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5a65f-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a65f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5a65f-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a65f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a65f-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a65f-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="5a65f-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a65f-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="5a65f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5a65f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a65f-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a65f-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="5a65f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a65f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a65f-144">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="5a65f-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





