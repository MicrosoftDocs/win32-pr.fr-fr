---
title: Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: L’SHA utilise pour communiquer avec le NapAgent. | Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- NAP de l’interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322094"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="93338-106">Interface INapSystemHealthAgentBinding2</span><span class="sxs-lookup"><span data-stu-id="93338-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="93338-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="93338-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="93338-108">**INapSystemHealthAgentBinding2** fournit des méthodes que l’SHA utilise pour communiquer avec NapAgent.</span><span class="sxs-lookup"><span data-stu-id="93338-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="93338-109">Cette interface hérite de toutes les méthodes de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) et doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="93338-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="93338-110">Membres</span><span class="sxs-lookup"><span data-stu-id="93338-110">Members</span></span>

<span data-ttu-id="93338-111">L’interface **INapSystemHealthAgentBinding2** hérite de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span><span class="sxs-lookup"><span data-stu-id="93338-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="93338-112">**INapSystemHealthAgentBinding2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="93338-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="93338-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="93338-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93338-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="93338-114">Methods</span></span>

<span data-ttu-id="93338-115">L’interface **INapSystemHealthAgentBinding2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="93338-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="93338-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="93338-116">Method</span></span>                                                                                                                    | <span data-ttu-id="93338-117">Description</span><span class="sxs-lookup"><span data-stu-id="93338-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93338-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="93338-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="93338-119">Appelée par l’SHA pour déterminer l’état d’isolement du système et l’état d’isolement étendu.</span><span class="sxs-lookup"><span data-stu-id="93338-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93338-120">Notes</span><span class="sxs-lookup"><span data-stu-id="93338-120">Remarks</span></span>

<span data-ttu-id="93338-121">Toutes les API de cette interface renverront **RPC \_ E \_ Disconnected** si le NapAgent est arrêté.</span><span class="sxs-lookup"><span data-stu-id="93338-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="93338-122">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="93338-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="93338-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93338-123">Requirements</span></span>



| <span data-ttu-id="93338-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93338-124">Requirement</span></span> | <span data-ttu-id="93338-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="93338-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93338-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93338-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93338-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93338-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93338-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93338-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93338-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93338-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93338-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="93338-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="93338-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="93338-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="93338-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="93338-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93338-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93338-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="93338-134">DLL</span><span class="sxs-lookup"><span data-stu-id="93338-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93338-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93338-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="93338-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93338-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93338-137">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="93338-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="93338-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="93338-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="93338-139">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="93338-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





