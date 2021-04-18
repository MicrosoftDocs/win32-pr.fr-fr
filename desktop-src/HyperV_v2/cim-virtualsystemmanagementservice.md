---
description: Représente un service qui gère des systèmes virtuels.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: Classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519871"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="76021-103">\_Classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="76021-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="76021-104">Représente un service qui gère des systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="76021-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="76021-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76021-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="76021-106">Membres</span><span class="sxs-lookup"><span data-stu-id="76021-106">Members</span></span>

<span data-ttu-id="76021-107">La classe **CIM \_ VirtualSystemManagementService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76021-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="76021-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76021-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="76021-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76021-109">Methods</span></span>

<span data-ttu-id="76021-110">La classe **CIM \_ VirtualSystemManagementService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="76021-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="76021-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="76021-111">Method</span></span>                                                                                      | <span data-ttu-id="76021-112">Description</span><span class="sxs-lookup"><span data-stu-id="76021-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="76021-113">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="76021-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="76021-114">Ajoute des ressources à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="76021-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="76021-115">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="76021-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="76021-116">Définit un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="76021-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="76021-117">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="76021-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="76021-118">Supprime un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="76021-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="76021-119">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="76021-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="76021-120">Modifie les paramètres de ressource virtuelle pour une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="76021-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="76021-121">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="76021-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="76021-122">Modifie les paramètres du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="76021-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="76021-123">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="76021-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="76021-124">Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="76021-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="76021-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76021-125">Requirements</span></span>



| <span data-ttu-id="76021-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76021-126">Requirement</span></span> | <span data-ttu-id="76021-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="76021-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76021-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76021-128">Minimum supported client</span></span><br/> | <span data-ttu-id="76021-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="76021-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="76021-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76021-130">Minimum supported server</span></span><br/> | <span data-ttu-id="76021-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76021-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="76021-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76021-132">Namespace</span></span><br/>                | <span data-ttu-id="76021-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="76021-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76021-134">MOF</span><span class="sxs-lookup"><span data-stu-id="76021-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76021-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76021-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76021-136">DLL</span><span class="sxs-lookup"><span data-stu-id="76021-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76021-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76021-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76021-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76021-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76021-139">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="76021-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




