---
description: Représente un service qui contrôle la migration des systèmes virtuels entre les systèmes hôtes. Cette classe vérifie également si une migration en attente est susceptible de se dérouler correctement.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864573"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="431ec-104">\_Classe CIM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="431ec-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="431ec-105">Représente un service qui contrôle la migration des systèmes virtuels entre les systèmes hôtes.</span><span class="sxs-lookup"><span data-stu-id="431ec-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="431ec-106">Cette classe vérifie également si une migration en attente est susceptible de se dérouler correctement.</span><span class="sxs-lookup"><span data-stu-id="431ec-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="431ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="431ec-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="431ec-108">Membres</span><span class="sxs-lookup"><span data-stu-id="431ec-108">Members</span></span>

<span data-ttu-id="431ec-109">La classe **CIM \_ VirtualSystemMigrationService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="431ec-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="431ec-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="431ec-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="431ec-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="431ec-111">Methods</span></span>

<span data-ttu-id="431ec-112">La classe **CIM \_ VirtualSystemMigrationService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="431ec-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="431ec-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="431ec-113">Method</span></span>                                                                                                                     | <span data-ttu-id="431ec-114">Description</span><span class="sxs-lookup"><span data-stu-id="431ec-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="431ec-115">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="431ec-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="431ec-116">Vérifie si la migration d’un système virtuel en attente vers un ordinateur hôte est susceptible d’être effectuée.</span><span class="sxs-lookup"><span data-stu-id="431ec-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="431ec-117">**CheckVirtualSystemIsMigratableToSystem**</span><span class="sxs-lookup"><span data-stu-id="431ec-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="431ec-118">Vérifie si la migration d’un système virtuel en attente vers un système est susceptible d’être effectuée.</span><span class="sxs-lookup"><span data-stu-id="431ec-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="431ec-119">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="431ec-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="431ec-120">Migre un système virtuel vers un ordinateur hôte cible.</span><span class="sxs-lookup"><span data-stu-id="431ec-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="431ec-121">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="431ec-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="431ec-122">Migre un système virtuel vers le système cible.</span><span class="sxs-lookup"><span data-stu-id="431ec-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="431ec-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="431ec-123">Requirements</span></span>



| <span data-ttu-id="431ec-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="431ec-124">Requirement</span></span> | <span data-ttu-id="431ec-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="431ec-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431ec-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="431ec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="431ec-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="431ec-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="431ec-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="431ec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="431ec-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="431ec-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="431ec-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="431ec-130">Namespace</span></span><br/>                | <span data-ttu-id="431ec-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="431ec-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="431ec-132">MOF</span><span class="sxs-lookup"><span data-stu-id="431ec-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="431ec-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="431ec-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="431ec-134">DLL</span><span class="sxs-lookup"><span data-stu-id="431ec-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431ec-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="431ec-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="431ec-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="431ec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431ec-137">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="431ec-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




