---
title: Interface INapClientManagement2 (NapManagement. h)
description: Fournit des méthodes pour la gestion des clients NAP. | Interface INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- NAP de l’interface INapClientManagement2
- INapClientManagement2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043056"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="21464-106">Interface INapClientManagement2</span><span class="sxs-lookup"><span data-stu-id="21464-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="21464-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="21464-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="21464-108">L’interface **INapClientManagement2** fournit des méthodes pour la gestion des clients NAP.</span><span class="sxs-lookup"><span data-stu-id="21464-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="21464-109">Cette interface hérite de toutes les méthodes de [**INapClientManagement**](inapclientmanagement.md) et doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="21464-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="21464-110">Membres</span><span class="sxs-lookup"><span data-stu-id="21464-110">Members</span></span>

<span data-ttu-id="21464-111">L’interface **INapClientManagement2** hérite de [**INapClientManagement**](inapclientmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="21464-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="21464-112">**INapClientManagement2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="21464-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="21464-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="21464-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21464-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="21464-114">Methods</span></span>

<span data-ttu-id="21464-115">L’interface **INapClientManagement2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="21464-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="21464-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="21464-116">Method</span></span>                                                                                                    | <span data-ttu-id="21464-117">Description</span><span class="sxs-lookup"><span data-stu-id="21464-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21464-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="21464-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="21464-119">Récupère les informations relatives à l’état d’isolement et à l’état d’isolement étendu du client NAP.</span><span class="sxs-lookup"><span data-stu-id="21464-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21464-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21464-120">Requirements</span></span>



| <span data-ttu-id="21464-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21464-121">Requirement</span></span> | <span data-ttu-id="21464-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="21464-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="21464-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21464-123">Minimum supported client</span></span><br/> | <span data-ttu-id="21464-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21464-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="21464-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21464-125">Minimum supported server</span></span><br/> | <span data-ttu-id="21464-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21464-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="21464-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="21464-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="21464-128"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="21464-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="21464-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="21464-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21464-130"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21464-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="21464-131">DLL</span><span class="sxs-lookup"><span data-stu-id="21464-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21464-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21464-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="21464-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21464-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21464-134">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="21464-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="21464-135">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="21464-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="21464-136">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="21464-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





