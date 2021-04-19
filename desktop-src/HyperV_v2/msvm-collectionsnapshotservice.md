---
description: Service permettant de créer, de détruire et d’exporter la collection de captures instantanées de systèmes virtuels.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524571"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="caeea-103">MSVM \_ CollectionSnapshotService, classe</span><span class="sxs-lookup"><span data-stu-id="caeea-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="caeea-104">Service permettant de créer, de détruire et d’exporter la collection de captures instantanées de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="caeea-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="caeea-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="caeea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="caeea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caeea-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="caeea-107">Membres</span><span class="sxs-lookup"><span data-stu-id="caeea-107">Members</span></span>

<span data-ttu-id="caeea-108">La classe **MSVM \_ CollectionSnapshotService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="caeea-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="caeea-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="caeea-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="caeea-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="caeea-110">Methods</span></span>

<span data-ttu-id="caeea-111">La classe **MSVM \_ CollectionSnapshotService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="caeea-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="caeea-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="caeea-112">Method</span></span>                                                                                    | <span data-ttu-id="caeea-113">Description</span><span class="sxs-lookup"><span data-stu-id="caeea-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caeea-114">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="caeea-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="caeea-115">Applique une collection d’instantanés à la collection de systèmes d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="caeea-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="caeea-116">**ConvertToReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="caeea-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="caeea-117">Convertit une capture instantanée de collection existante en collection de points de référence.</span><span class="sxs-lookup"><span data-stu-id="caeea-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="caeea-118">La collection d’instantanés est supprimée en tant qu’effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="caeea-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="caeea-119">Seuls les instantanés de récupération peuvent être convertis en points de référence.</span><span class="sxs-lookup"><span data-stu-id="caeea-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="caeea-120">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="caeea-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="caeea-121">Crée une capture instantanée d’une collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="caeea-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="caeea-122">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="caeea-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="caeea-123">Détruisez un instantané existant de la collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="caeea-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="caeea-124">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.</span><span class="sxs-lookup"><span data-stu-id="caeea-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="caeea-125">**Temps**</span><span class="sxs-lookup"><span data-stu-id="caeea-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="caeea-126">Exporte une collection d’instantanés de systèmes d’ordinateurs virtuels dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="caeea-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="caeea-127">La collection d’instantanés, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="caeea-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="caeea-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caeea-128">Requirements</span></span>



| <span data-ttu-id="caeea-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caeea-129">Requirement</span></span> | <span data-ttu-id="caeea-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="caeea-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caeea-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caeea-131">Minimum supported client</span></span><br/> | <span data-ttu-id="caeea-132">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caeea-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="caeea-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caeea-133">Minimum supported server</span></span><br/> | <span data-ttu-id="caeea-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="caeea-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="caeea-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="caeea-135">Namespace</span></span><br/>                | <span data-ttu-id="caeea-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="caeea-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="caeea-137">MOF</span><span class="sxs-lookup"><span data-stu-id="caeea-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caeea-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="caeea-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="caeea-139">DLL</span><span class="sxs-lookup"><span data-stu-id="caeea-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caeea-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="caeea-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="caeea-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caeea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caeea-142">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="caeea-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




