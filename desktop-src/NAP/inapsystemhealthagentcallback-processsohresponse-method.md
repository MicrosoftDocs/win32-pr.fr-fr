---
title: Méthode INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: Est appelé lorsque le NapAgent reçoit un SoHResponse destiné à cet agent d’intégrité.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Méthode ProcessSoHResponse NAP
- Méthode ProcessSoHResponse NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942268"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="cf662-106">INapSystemHealthAgentCallback ::P méthode rocessSoHResponse</span><span class="sxs-lookup"><span data-stu-id="cf662-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="cf662-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="cf662-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cf662-108">La méthode **INapSystemHealthAgentCallback ::P rocesssohresponse** est appelée quand le NapAgent reçoit un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destiné à cet agent d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="cf662-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf662-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf662-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="cf662-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf662-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf662-111">*demande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf662-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf662-112">Pointeur COM vers un objet [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) qui identifie l’objet de requête.</span><span class="sxs-lookup"><span data-stu-id="cf662-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf662-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf662-113">Return value</span></span>

<span data-ttu-id="cf662-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="cf662-114">This method can return one of these values.</span></span>



| <span data-ttu-id="cf662-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cf662-115">Return code</span></span>                                                                                            | <span data-ttu-id="cf662-116">Description</span><span class="sxs-lookup"><span data-stu-id="cf662-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf662-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf662-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="cf662-118">Indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cf662-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="cf662-119"><dt>**\_paquet NAP E \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf662-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="cf662-120">Retourné par cette implémentation si le format de la réponse n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="cf662-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf662-121">Notes</span><span class="sxs-lookup"><span data-stu-id="cf662-121">Remarks</span></span>

<span data-ttu-id="cf662-122">Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.</span><span class="sxs-lookup"><span data-stu-id="cf662-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="cf662-123">Quand le NapAgent reçoit un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destiné à cet agent d’intégrité, il appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cf662-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="cf662-124">L’agent d’intégrité doit interroger le SoHResponse à partir de l’objet de requête.</span><span class="sxs-lookup"><span data-stu-id="cf662-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="cf662-125">Elle ne doit pas contenir de références à l’objet de requête une fois cet appel terminé.</span><span class="sxs-lookup"><span data-stu-id="cf662-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="cf662-126">La méthode **INapSystemHealthAgentCallback ::P rocesssohresponse** ne doit pas être bloquée.</span><span class="sxs-lookup"><span data-stu-id="cf662-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="cf662-127">Si un traitement de correction est requis, toute implémentation de **ProcessSoHResponse** doit démarrer un nouveau thread pour effectuer un traitement de correction.</span><span class="sxs-lookup"><span data-stu-id="cf662-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="cf662-128">NapAgent doit appeler [**INapSystemHealthAgentCallBack :: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) pour déterminer l’état de correction de l’algorithme SHA.</span><span class="sxs-lookup"><span data-stu-id="cf662-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="cf662-129">Cette méthode doit retourner **le \_ paquet NAP E \_ non valide \_** si le format de la réponse n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="cf662-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf662-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf662-130">Requirements</span></span>



| <span data-ttu-id="cf662-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf662-131">Requirement</span></span> | <span data-ttu-id="cf662-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf662-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf662-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf662-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cf662-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf662-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf662-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf662-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cf662-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf662-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf662-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf662-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf662-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf662-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf662-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="cf662-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf662-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf662-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf662-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf662-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf662-142">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="cf662-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





