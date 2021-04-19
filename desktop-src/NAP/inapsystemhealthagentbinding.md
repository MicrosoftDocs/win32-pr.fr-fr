---
title: Interface INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: L’SHA utilise pour communiquer avec le NapAgent. | Interface INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- NAP de l’interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525848"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="19210-106">Interface INapSystemHealthAgentBinding</span><span class="sxs-lookup"><span data-stu-id="19210-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="19210-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="19210-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19210-108">**INapSystemHealthAgentBinding** fournit des méthodes que l’SHA utilise pour communiquer avec NapAgent.</span><span class="sxs-lookup"><span data-stu-id="19210-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="19210-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="19210-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="19210-110">Membres</span><span class="sxs-lookup"><span data-stu-id="19210-110">Members</span></span>

<span data-ttu-id="19210-111">L’interface **INapSystemHealthAgentBinding** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="19210-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="19210-112">**INapSystemHealthAgentBinding** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="19210-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="19210-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19210-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="19210-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19210-114">Methods</span></span>

<span data-ttu-id="19210-115">L’interface **INapSystemHealthAgentBinding** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="19210-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="19210-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="19210-116">Method</span></span>                                                                                                                     | <span data-ttu-id="19210-117">Description</span><span class="sxs-lookup"><span data-stu-id="19210-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19210-118">**INapSystemHealthAgentBinding::FlushCache**</span><span class="sxs-lookup"><span data-stu-id="19210-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="19210-119">Appelée par un SHA pour vider son cache SoH.</span><span class="sxs-lookup"><span data-stu-id="19210-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="19210-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="19210-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="19210-121">Appelée par l’SHA pour déterminer l’état de l’isolation du système.</span><span class="sxs-lookup"><span data-stu-id="19210-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="19210-122">**INapSystemHealthAgentBinding :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="19210-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="19210-123">Initialise l’algorithme SHA et lie l’algorithme SHA au service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="19210-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="19210-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="19210-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="19210-125">Appelée par l’SHA lorsque leur SoH change.</span><span class="sxs-lookup"><span data-stu-id="19210-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="19210-126">**INapSystemHealthAgentBinding :: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="19210-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="19210-127">Appelée par l’agent de niveau de l’agent pour obliger le NapAgent à libérer toutes ses références aux pointeurs SHA COM.</span><span class="sxs-lookup"><span data-stu-id="19210-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19210-128">Notes</span><span class="sxs-lookup"><span data-stu-id="19210-128">Remarks</span></span>

<span data-ttu-id="19210-129">Toutes les API de cette interface renverront **RPC \_ E \_ Disconnected** si le NapAgent est arrêté.</span><span class="sxs-lookup"><span data-stu-id="19210-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="19210-130">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="19210-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="19210-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19210-131">Requirements</span></span>



| <span data-ttu-id="19210-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19210-132">Requirement</span></span> | <span data-ttu-id="19210-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="19210-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19210-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19210-134">Minimum supported client</span></span><br/> | <span data-ttu-id="19210-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19210-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="19210-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19210-136">Minimum supported server</span></span><br/> | <span data-ttu-id="19210-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19210-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="19210-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="19210-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="19210-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="19210-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="19210-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="19210-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19210-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19210-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="19210-142">DLL</span><span class="sxs-lookup"><span data-stu-id="19210-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19210-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19210-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="19210-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19210-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19210-145">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="19210-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="19210-146">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="19210-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

