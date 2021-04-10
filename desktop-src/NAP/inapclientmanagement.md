---
title: Interface INapClientManagement (NapManagement. h)
description: Fournit des méthodes pour la gestion des clients NAP. | Interface INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- NAP de l’interface INapClientManagement
- INapClientManagement interface NAP, Description
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953694"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="5341c-106">Interface INapClientManagement</span><span class="sxs-lookup"><span data-stu-id="5341c-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="5341c-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5341c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5341c-108">L’interface **INapClientManagement** fournit des méthodes pour la gestion des clients NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="5341c-109">[**INapClientManagement2**](inapclientmanagement2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="5341c-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="5341c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5341c-110">Members</span></span>

<span data-ttu-id="5341c-111">L’interface **INapClientManagement** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5341c-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5341c-112">**INapClientManagement** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5341c-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="5341c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5341c-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5341c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5341c-114">Methods</span></span>

<span data-ttu-id="5341c-115">L’interface **INapClientManagement** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5341c-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="5341c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="5341c-116">Method</span></span>                                                                                                                | <span data-ttu-id="5341c-117">Description</span><span class="sxs-lookup"><span data-stu-id="5341c-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="5341c-118">**INapClientManagement::GetNapClientInfo**</span><span class="sxs-lookup"><span data-stu-id="5341c-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="5341c-119">Récupère des informations sur un client NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="5341c-120">**INapClientManagement::GetRegisteredEnforcementClients**</span><span class="sxs-lookup"><span data-stu-id="5341c-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="5341c-121">Récupère des informations sur les clients de mise en œuvre inscrits.</span><span class="sxs-lookup"><span data-stu-id="5341c-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="5341c-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span><span class="sxs-lookup"><span data-stu-id="5341c-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="5341c-123">Récupérez des informations sur un SHA inscrit.</span><span class="sxs-lookup"><span data-stu-id="5341c-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="5341c-124">**INapClientManagement::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="5341c-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="5341c-125">Récupère des informations sur l’état d’isolement du client NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="5341c-126">**INapClientManagement::RegisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="5341c-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="5341c-127">Inscrit un client de mise en œuvre auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="5341c-128">**INapClientManagement::RegisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="5341c-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="5341c-129">Inscrit un SHA auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="5341c-130">**INapClientManagement::UnregisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="5341c-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="5341c-131">Annule l’inscription d’un client de contrainte auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="5341c-132">**INapClientManagement::UnregisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="5341c-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="5341c-133">Annule l’inscription d’un SHA auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="5341c-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="5341c-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5341c-134">Requirements</span></span>



| <span data-ttu-id="5341c-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5341c-135">Requirement</span></span> | <span data-ttu-id="5341c-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5341c-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5341c-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5341c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5341c-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5341c-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5341c-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5341c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5341c-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5341c-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5341c-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="5341c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5341c-142"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="5341c-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="5341c-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="5341c-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5341c-144"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5341c-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="5341c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5341c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5341c-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5341c-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="5341c-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5341c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5341c-148">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="5341c-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5341c-149">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="5341c-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

