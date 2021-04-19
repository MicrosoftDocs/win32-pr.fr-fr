---
description: Décrit un service de point de référence de système virtuel.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106542087"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="94c8c-103">MSVM \_ VirtualSystemReferencePointService, classe</span><span class="sxs-lookup"><span data-stu-id="94c8c-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="94c8c-104">Décrit un service de point de référence de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="94c8c-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="94c8c-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="94c8c-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94c8c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="94c8c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="94c8c-107">Members</span></span>

<span data-ttu-id="94c8c-108">La classe **MSVM \_ VirtualSystemReferencePointService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="94c8c-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="94c8c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94c8c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94c8c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94c8c-110">Methods</span></span>

<span data-ttu-id="94c8c-111">La classe **MSVM \_ VirtualSystemReferencePointService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="94c8c-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="94c8c-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="94c8c-112">Method</span></span>                                                                                                       | <span data-ttu-id="94c8c-113">Description</span><span class="sxs-lookup"><span data-stu-id="94c8c-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="94c8c-114">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="94c8c-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="94c8c-115">Crée un point de référence d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="94c8c-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="94c8c-116">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="94c8c-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="94c8c-117">Supprime le point de référence spécifié.</span><span class="sxs-lookup"><span data-stu-id="94c8c-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="94c8c-118">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="94c8c-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="94c8c-119">Exporte le point de référence du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="94c8c-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="94c8c-120">**ImportReferencePointMetadata**</span><span class="sxs-lookup"><span data-stu-id="94c8c-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="94c8c-121">Importe les métadonnées de point de référence du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="94c8c-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="94c8c-122">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="94c8c-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="94c8c-123">Supprime le journal de données associé au point de référence.</span><span class="sxs-lookup"><span data-stu-id="94c8c-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="94c8c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94c8c-124">Requirements</span></span>



| <span data-ttu-id="94c8c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94c8c-125">Requirement</span></span> | <span data-ttu-id="94c8c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="94c8c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94c8c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94c8c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="94c8c-128">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94c8c-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="94c8c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94c8c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="94c8c-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="94c8c-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="94c8c-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="94c8c-131">Namespace</span></span><br/>                | <span data-ttu-id="94c8c-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="94c8c-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="94c8c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="94c8c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94c8c-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94c8c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94c8c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="94c8c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94c8c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94c8c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94c8c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94c8c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c8c-138">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="94c8c-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




