---
title: Interface INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: SHA utilise pour communiquer et coordonner le traitement avec le système NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- NAP de l’interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508526"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="a8bdc-105">Interface INapSystemHealthAgentRequest</span><span class="sxs-lookup"><span data-stu-id="a8bdc-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="a8bdc-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a8bdc-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a8bdc-107">L’interface **INapSystemHealthAgentRequest** fournit des méthodes que SHA utilise pour communiquer et coordonner le traitement avec le système NAP.</span><span class="sxs-lookup"><span data-stu-id="a8bdc-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="a8bdc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a8bdc-108">Members</span></span>

<span data-ttu-id="a8bdc-109">L’interface **INapSystemHealthAgentRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a8bdc-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8bdc-110">**INapSystemHealthAgentRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a8bdc-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="a8bdc-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8bdc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8bdc-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8bdc-112">Methods</span></span>

<span data-ttu-id="a8bdc-113">L’interface **INapSystemHealthAgentRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a8bdc-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="a8bdc-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="a8bdc-114">Method</span></span>                                                                                                                     | <span data-ttu-id="a8bdc-115">Description</span><span class="sxs-lookup"><span data-stu-id="a8bdc-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8bdc-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span><span class="sxs-lookup"><span data-stu-id="a8bdc-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="a8bdc-117">Utilisé uniquement par NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a8bdc-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="a8bdc-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="a8bdc-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="a8bdc-119">Utilisé par les agents d’intégrité système pour corréler SoHs et [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="a8bdc-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="a8bdc-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="a8bdc-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="a8bdc-121">Utilisé par les Sha pour récupérer les SoHs précédemment mis en cache par le NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a8bdc-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="a8bdc-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="a8bdc-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="a8bdc-123">Utilisé par l’agent d’intégrité pour récupérer son [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="a8bdc-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="a8bdc-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="a8bdc-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="a8bdc-125">Utilisé par les agents d’intégrité système pour enregistrer l’ID de corrélation.</span><span class="sxs-lookup"><span data-stu-id="a8bdc-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="a8bdc-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="a8bdc-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="a8bdc-127">Utilisé par les agents d’intégrité pour écrire leur demande d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="a8bdc-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="a8bdc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8bdc-128">Requirements</span></span>



| <span data-ttu-id="a8bdc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8bdc-129">Requirement</span></span> | <span data-ttu-id="a8bdc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8bdc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bdc-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8bdc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a8bdc-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8bdc-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8bdc-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8bdc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a8bdc-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8bdc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8bdc-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8bdc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8bdc-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bdc-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8bdc-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="a8bdc-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8bdc-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8bdc-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8bdc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a8bdc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8bdc-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8bdc-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="a8bdc-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8bdc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bdc-142">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="a8bdc-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a8bdc-143">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="a8bdc-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

