---
description: Gère les collections sur l’hôte Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760497"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="53878-103">MSVM \_ CollectionManagementService, classe</span><span class="sxs-lookup"><span data-stu-id="53878-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="53878-104">Gère les collections sur l’hôte Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="53878-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="53878-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="53878-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53878-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53878-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="53878-107">Membres</span><span class="sxs-lookup"><span data-stu-id="53878-107">Members</span></span>

<span data-ttu-id="53878-108">La classe **MSVM \_ CollectionManagementService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53878-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="53878-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53878-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="53878-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53878-110">Methods</span></span>

<span data-ttu-id="53878-111">La classe **MSVM \_ CollectionManagementService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="53878-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="53878-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="53878-112">Method</span></span>                                                                          | <span data-ttu-id="53878-113">Description</span><span class="sxs-lookup"><span data-stu-id="53878-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53878-114">**AddMember**</span><span class="sxs-lookup"><span data-stu-id="53878-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="53878-115">Ajoute le propriété ManagedElement spécifié en tant que membre de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="53878-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="53878-116">**DefineCollection**</span><span class="sxs-lookup"><span data-stu-id="53878-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="53878-117">Crée un nouvel objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="53878-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="53878-118">**DestroyCollection**</span><span class="sxs-lookup"><span data-stu-id="53878-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="53878-119">Supprime l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="53878-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="53878-120">**RemoveMember**</span><span class="sxs-lookup"><span data-stu-id="53878-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="53878-121">Supprime le propriété ManagedElement spécifié en tant que membre de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="53878-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="53878-122">**RemoveMemberById**</span><span class="sxs-lookup"><span data-stu-id="53878-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="53878-123">Supprime le propriété ManagedElement spécifié en tant que membre de l’élément [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) avec l’identificateur donné.</span><span class="sxs-lookup"><span data-stu-id="53878-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="53878-124">Cela échoue même si l’objet avec cet identificateur n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="53878-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="53878-125">**RenameCollection**</span><span class="sxs-lookup"><span data-stu-id="53878-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="53878-126">Met à jour le ElementName de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="53878-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="53878-127">**StartService**</span><span class="sxs-lookup"><span data-stu-id="53878-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="53878-128">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="53878-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="53878-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="53878-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="53878-130">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="53878-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="53878-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53878-131">Requirements</span></span>



| <span data-ttu-id="53878-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53878-132">Requirement</span></span> | <span data-ttu-id="53878-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="53878-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53878-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53878-134">Minimum supported client</span></span><br/> | <span data-ttu-id="53878-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53878-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="53878-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53878-136">Minimum supported server</span></span><br/> | <span data-ttu-id="53878-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="53878-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="53878-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53878-138">Namespace</span></span><br/>                | <span data-ttu-id="53878-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="53878-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53878-140">MOF</span><span class="sxs-lookup"><span data-stu-id="53878-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53878-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53878-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53878-142">DLL</span><span class="sxs-lookup"><span data-stu-id="53878-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53878-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53878-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53878-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53878-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53878-145">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="53878-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




