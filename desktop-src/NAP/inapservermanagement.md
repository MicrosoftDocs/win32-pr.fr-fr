---
title: Interface INapServerManagement (NapServerManagement. h)
description: Sont utilisés pour gérer le serveur NAP.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- NAP de l’interface INapServerManagement
- INapServerManagement interface NAP, Description
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104146"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="41d68-105">Interface INapServerManagement</span><span class="sxs-lookup"><span data-stu-id="41d68-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="41d68-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="41d68-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="41d68-107">**INapServerManagement** fournit les méthodes utilisées pour gérer le serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="41d68-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="41d68-108">Membres</span><span class="sxs-lookup"><span data-stu-id="41d68-108">Members</span></span>

<span data-ttu-id="41d68-109">L’interface **INapServerManagement** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="41d68-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="41d68-110">**INapServerManagement** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="41d68-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="41d68-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="41d68-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="41d68-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="41d68-112">Methods</span></span>

<span data-ttu-id="41d68-113">L’interface **INapServerManagement** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="41d68-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="41d68-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="41d68-114">Method</span></span>                                                                                                                       | <span data-ttu-id="41d68-115">Description</span><span class="sxs-lookup"><span data-stu-id="41d68-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="41d68-116">**INapServerManagement::RegisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="41d68-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="41d68-117">Inscrit un SHV.</span><span class="sxs-lookup"><span data-stu-id="41d68-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="41d68-118">**INapServerManagement::SetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="41d68-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="41d68-119">Définit les mappages de catégorie d’échec du VALIDateur.</span><span class="sxs-lookup"><span data-stu-id="41d68-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="41d68-120">**INapServerManagement::UnregisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="41d68-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="41d68-121">Annule l’inscription d’un validateur de l’intégrité du serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="41d68-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="41d68-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41d68-122">Requirements</span></span>



| <span data-ttu-id="41d68-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41d68-123">Requirement</span></span> | <span data-ttu-id="41d68-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="41d68-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d68-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d68-125">Minimum supported client</span></span><br/> | <span data-ttu-id="41d68-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d68-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="41d68-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d68-127">Minimum supported server</span></span><br/> | <span data-ttu-id="41d68-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41d68-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41d68-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="41d68-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="41d68-130"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d68-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="41d68-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="41d68-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41d68-132"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41d68-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="41d68-133">DLL</span><span class="sxs-lookup"><span data-stu-id="41d68-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d68-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d68-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="41d68-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41d68-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d68-136">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="41d68-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="41d68-137">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="41d68-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

