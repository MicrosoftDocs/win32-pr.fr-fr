---
description: Représente un service qui peut créer, appliquer et supprimer des instantanés de systèmes virtuels.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: Classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869282"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="64253-103">\_Classe CIM VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="64253-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="64253-104">Représente un service qui peut créer, appliquer et supprimer des instantanés de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="64253-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="64253-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64253-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="64253-106">Membres</span><span class="sxs-lookup"><span data-stu-id="64253-106">Members</span></span>

<span data-ttu-id="64253-107">La classe **CIM \_ VirtualSystemSnapshotService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="64253-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="64253-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="64253-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="64253-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="64253-109">Methods</span></span>

<span data-ttu-id="64253-110">La classe **CIM \_ VirtualSystemSnapshotService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="64253-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="64253-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="64253-111">Method</span></span>                                                                      | <span data-ttu-id="64253-112">Description</span><span class="sxs-lookup"><span data-stu-id="64253-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64253-113">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="64253-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="64253-114">Applique un instantané de système virtuel au système virtuel sur le système virtuel source.</span><span class="sxs-lookup"><span data-stu-id="64253-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="64253-115">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="64253-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="64253-116">Crée une capture instantanée d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="64253-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="64253-117">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="64253-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="64253-118">Supprime un instantané du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="64253-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="64253-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64253-119">Requirements</span></span>



| <span data-ttu-id="64253-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64253-120">Requirement</span></span> | <span data-ttu-id="64253-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="64253-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64253-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64253-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64253-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="64253-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="64253-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64253-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64253-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64253-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="64253-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="64253-126">Namespace</span></span><br/>                | <span data-ttu-id="64253-127">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="64253-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64253-128">MOF</span><span class="sxs-lookup"><span data-stu-id="64253-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64253-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64253-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64253-130">DLL</span><span class="sxs-lookup"><span data-stu-id="64253-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64253-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64253-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64253-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64253-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64253-133">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="64253-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




