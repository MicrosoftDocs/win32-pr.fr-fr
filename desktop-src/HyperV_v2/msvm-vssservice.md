---
description: Représente le service VSS invité. Elle est utilisée pour interroger les informations du cluster invité à partir de l’hôte Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318085"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="0e346-104">MSVM \_ VssService, classe</span><span class="sxs-lookup"><span data-stu-id="0e346-104">Msvm\_VssService class</span></span>

<span data-ttu-id="0e346-105">Représente le service VSS invité.</span><span class="sxs-lookup"><span data-stu-id="0e346-105">Represents the guest VSS service.</span></span> <span data-ttu-id="0e346-106">Elle est utilisée pour interroger les informations du cluster invité à partir de l’hôte Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0e346-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="0e346-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e346-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e346-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e346-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="0e346-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0e346-109">Members</span></span>

<span data-ttu-id="0e346-110">La classe **MSVM \_ VssService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e346-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="0e346-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e346-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0e346-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e346-112">Methods</span></span>

<span data-ttu-id="0e346-113">La classe **MSVM \_ VssService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e346-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="0e346-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e346-114">Method</span></span>                                                                               | <span data-ttu-id="0e346-115">Description</span><span class="sxs-lookup"><span data-stu-id="0e346-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="0e346-116">**QueryGuestClusterInformation**</span><span class="sxs-lookup"><span data-stu-id="0e346-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="0e346-117">Interrogation des informations de cluster à partir de l’hôte Hyper-V vers l’invité.</span><span class="sxs-lookup"><span data-stu-id="0e346-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0e346-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e346-118">Requirements</span></span>



| <span data-ttu-id="0e346-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e346-119">Requirement</span></span> | <span data-ttu-id="0e346-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e346-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e346-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e346-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e346-122">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e346-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0e346-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e346-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e346-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0e346-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0e346-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e346-125">Namespace</span></span><br/>                | <span data-ttu-id="0e346-126">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e346-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e346-127">MOF</span><span class="sxs-lookup"><span data-stu-id="0e346-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e346-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e346-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e346-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0e346-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e346-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e346-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e346-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e346-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e346-132">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="0e346-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




