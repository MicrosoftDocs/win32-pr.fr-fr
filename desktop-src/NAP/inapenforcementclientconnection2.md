---
title: Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Autoriser la gestion des connexions clientes. | Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- NAP de l’interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869742"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="e4ac0-106">Interface INapEnforcementClientConnection2</span><span class="sxs-lookup"><span data-stu-id="e4ac0-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="e4ac0-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4ac0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e4ac0-108">**INapEnforcementClientConnection2** fournit des méthodes qui permettent la gestion des connexions clientes.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="e4ac0-109">Cette interface hérite de toutes les méthodes de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) et doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="e4ac0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e4ac0-110">Members</span></span>

<span data-ttu-id="e4ac0-111">L’interface **INapEnforcementClientConnection2** hérite de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e4ac0-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="e4ac0-112">**INapEnforcementClientConnection2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4ac0-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="e4ac0-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4ac0-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4ac0-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4ac0-114">Methods</span></span>

<span data-ttu-id="e4ac0-115">L’interface **INapEnforcementClientConnection2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="e4ac0-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="e4ac0-116">Method</span></span>                                                                                                              | <span data-ttu-id="e4ac0-117">Description</span><span class="sxs-lookup"><span data-stu-id="e4ac0-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="e4ac0-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="e4ac0-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="e4ac0-119">Permet d’obtenir les ID des validateurs d’intégrité du client.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="e4ac0-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e4ac0-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="e4ac0-121">Utilisé pour obtenir les informations d’isolation pour le client.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="e4ac0-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="e4ac0-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="e4ac0-123">Utilisé par NapAgent pour définir les ID SHV installés pour le client.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="e4ac0-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e4ac0-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="e4ac0-125">Utilisé par NapAgent pour définir les informations d’isolation pour le client.</span><span class="sxs-lookup"><span data-stu-id="e4ac0-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4ac0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4ac0-126">Requirements</span></span>



| <span data-ttu-id="e4ac0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4ac0-127">Requirement</span></span> | <span data-ttu-id="e4ac0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4ac0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ac0-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4ac0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ac0-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4ac0-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4ac0-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4ac0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ac0-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4ac0-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4ac0-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4ac0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4ac0-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4ac0-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4ac0-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="e4ac0-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4ac0-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4ac0-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4ac0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e4ac0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4ac0-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4ac0-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e4ac0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4ac0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ac0-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e4ac0-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="e4ac0-141">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="e4ac0-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e4ac0-142">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="e4ac0-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





