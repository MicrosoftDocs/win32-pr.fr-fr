---
description: Gère la configuration des pools de ressources à l’aide de travaux.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862865"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="5528e-103">\_Classe CIM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="5528e-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="5528e-104">Gère la configuration des pools de ressources à l’aide de travaux.</span><span class="sxs-lookup"><span data-stu-id="5528e-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5528e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5528e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="5528e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5528e-106">Members</span></span>

<span data-ttu-id="5528e-107">La classe **CIM \_ ResourcePoolConfigurationService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5528e-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="5528e-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5528e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5528e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5528e-109">Methods</span></span>

<span data-ttu-id="5528e-110">La classe **CIM \_ ResourcePoolConfigurationService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5528e-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="5528e-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="5528e-111">Method</span></span>                                                                                                          | <span data-ttu-id="5528e-112">Description</span><span class="sxs-lookup"><span data-stu-id="5528e-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="5528e-113">**AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5528e-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="5528e-114">Démarre un travail pour ajouter des ressources à un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5528e-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="5528e-115">**ChangeParentResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5528e-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="5528e-116">Démarrer un travail pour modifier le pool de ressources parent d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5528e-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="5528e-117">**CreateChildResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5528e-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="5528e-118">Démarrer un travail pour créer un pool de ressources à partir d’un pool de ressources parent.</span><span class="sxs-lookup"><span data-stu-id="5528e-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="5528e-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5528e-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="5528e-120">Démarre un travail pour créer un pool de ressources racine.</span><span class="sxs-lookup"><span data-stu-id="5528e-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="5528e-121">**DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5528e-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="5528e-122">Démarrer un travail pour supprimer un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5528e-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="5528e-123">**RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5528e-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="5528e-124">Démarre un travail pour supprimer des ressources d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5528e-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="5528e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5528e-125">Requirements</span></span>



| <span data-ttu-id="5528e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5528e-126">Requirement</span></span> | <span data-ttu-id="5528e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5528e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5528e-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5528e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5528e-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5528e-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5528e-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5528e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5528e-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5528e-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5528e-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5528e-132">Namespace</span></span><br/>                | <span data-ttu-id="5528e-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5528e-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5528e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5528e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5528e-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5528e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5528e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5528e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5528e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5528e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5528e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5528e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5528e-139">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="5528e-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




