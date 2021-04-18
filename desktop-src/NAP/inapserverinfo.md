---
title: Interface INapServerInfo (NapServerManagement. h)
description: Les clients de gestion (par exemple, les fournisseurs WMI ou les outils en ligne de commande) utilisent pour interroger l’état du système de serveur NAP.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- NAP de l’interface INapServerInfo
- INapServerInfo interface NAP, Description
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509327"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="2b325-105">Interface INapServerInfo</span><span class="sxs-lookup"><span data-stu-id="2b325-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="2b325-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2b325-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2b325-107">**INapServerInfo** fournit des méthodes utilisées par les clients de gestion (par exemple, les fournisseurs WMI ou les outils en ligne de commande) pour interroger l’état du système de serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="2b325-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="2b325-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2b325-108">Members</span></span>

<span data-ttu-id="2b325-109">L’interface **INapServerInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2b325-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2b325-110">**INapServerInfo** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b325-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="2b325-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2b325-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b325-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2b325-112">Methods</span></span>

<span data-ttu-id="2b325-113">L’interface **INapServerInfo** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2b325-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="2b325-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="2b325-114">Method</span></span>                                                                                                                   | <span data-ttu-id="2b325-115">Description</span><span class="sxs-lookup"><span data-stu-id="2b325-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="2b325-116">**INapServerInfo::GetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="2b325-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="2b325-117">Récupère les mappages de catégorie d’échec pour un VALIDateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2b325-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="2b325-118">**INapServerInfo::GetNapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="2b325-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="2b325-119">Récupère des informations sur le serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="2b325-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="2b325-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span><span class="sxs-lookup"><span data-stu-id="2b325-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="2b325-121">Récupère une liste des validateurs d’intégrité inscrits.</span><span class="sxs-lookup"><span data-stu-id="2b325-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2b325-122">Notes</span><span class="sxs-lookup"><span data-stu-id="2b325-122">Remarks</span></span>

<span data-ttu-id="2b325-123">Ces méthodes fournissent uniquement des informations statiques sur le serveur NAP et ses composants sur le système.</span><span class="sxs-lookup"><span data-stu-id="2b325-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b325-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b325-124">Requirements</span></span>



| <span data-ttu-id="2b325-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b325-125">Requirement</span></span> | <span data-ttu-id="2b325-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b325-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b325-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b325-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b325-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b325-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="2b325-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b325-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b325-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b325-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b325-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b325-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b325-132"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b325-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b325-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="2b325-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b325-134"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b325-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2b325-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2b325-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b325-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b325-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="2b325-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b325-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b325-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="2b325-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2b325-139">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="2b325-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

