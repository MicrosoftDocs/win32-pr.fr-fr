---
title: Interface INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: Sont déclarés par le système et implémentés par l’enregistreur SHA afin que le NapAgent puisse communiquer avec l’algorithme SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- NAP de l’interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518100"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="75086-105">Interface INapSystemHealthAgentCallback</span><span class="sxs-lookup"><span data-stu-id="75086-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="75086-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="75086-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="75086-107">L’interface **INapSystemHealthAgentCallback** fournit des méthodes de rappel qui sont déclarées par le système et implémentées par l’enregistreur SHA afin que le NapAgent puisse communiquer avec l’algorithme SHA.</span><span class="sxs-lookup"><span data-stu-id="75086-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="75086-108">Membres</span><span class="sxs-lookup"><span data-stu-id="75086-108">Members</span></span>

<span data-ttu-id="75086-109">L’interface **INapSystemHealthAgentCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="75086-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="75086-110">**INapSystemHealthAgentCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="75086-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="75086-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="75086-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="75086-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="75086-112">Methods</span></span>

<span data-ttu-id="75086-113">L’interface **INapSystemHealthAgentCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="75086-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="75086-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="75086-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="75086-115">Description</span><span class="sxs-lookup"><span data-stu-id="75086-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75086-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span><span class="sxs-lookup"><span data-stu-id="75086-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="75086-117">Utilisé par l’algorithme SHA pour comparer le SoHs.</span><span class="sxs-lookup"><span data-stu-id="75086-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="75086-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="75086-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="75086-119">Appelé par NapAgent pour déterminer l’état de l’agent SHA.</span><span class="sxs-lookup"><span data-stu-id="75086-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="75086-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="75086-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="75086-121">Appelée par NapAgent pour interroger la demande de déclaration d’intégrité de l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="75086-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="75086-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="75086-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="75086-123">Appelé si une requête SoH a été interrogée à partir de l’agent SHA, mais que la réponse n’a jamais été renvoyée.</span><span class="sxs-lookup"><span data-stu-id="75086-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="75086-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span><span class="sxs-lookup"><span data-stu-id="75086-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="75086-125">Appelée par NapAgent pour indiquer que l’état d’isolement système ou l’heure de fin de la période d’essai a changé.</span><span class="sxs-lookup"><span data-stu-id="75086-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="75086-126">**INapSystemHealthAgentCallback ::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="75086-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="75086-127">Appelé lorsque NapAgent reçoit une réponse SoH destinée à cet agent d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="75086-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="75086-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75086-128">Requirements</span></span>



| <span data-ttu-id="75086-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75086-129">Requirement</span></span> | <span data-ttu-id="75086-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="75086-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75086-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75086-131">Minimum supported client</span></span><br/> | <span data-ttu-id="75086-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75086-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75086-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75086-133">Minimum supported server</span></span><br/> | <span data-ttu-id="75086-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75086-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="75086-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="75086-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="75086-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="75086-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="75086-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="75086-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75086-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75086-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75086-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75086-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75086-140">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="75086-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="75086-141">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="75086-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

