---
description: Service pour créer, détruire et exporter des points de référence.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543673"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="cd2b9-103">MSVM \_ CollectionReferencePointService, classe</span><span class="sxs-lookup"><span data-stu-id="cd2b9-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="cd2b9-104">Service pour créer, détruire et exporter des points de référence</span><span class="sxs-lookup"><span data-stu-id="cd2b9-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="cd2b9-105">de collections de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-105">of virtual system collections.</span></span>

<span data-ttu-id="cd2b9-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd2b9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="cd2b9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cd2b9-108">Members</span></span>

<span data-ttu-id="cd2b9-109">La classe **MSVM \_ CollectionReferencePointService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cd2b9-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="cd2b9-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd2b9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd2b9-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd2b9-111">Methods</span></span>

<span data-ttu-id="cd2b9-112">La classe **MSVM \_ CollectionReferencePointService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="cd2b9-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="cd2b9-113">Method</span></span>                                                                                      | <span data-ttu-id="cd2b9-114">Description</span><span class="sxs-lookup"><span data-stu-id="cd2b9-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd2b9-115">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="cd2b9-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="cd2b9-116">Crée un point de référence d’une collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="cd2b9-117">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="cd2b9-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="cd2b9-118">Détruit une collection de points de référence existante.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="cd2b9-119">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres points de référence qui dépendent de la collection de points de référence affectés.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="cd2b9-120">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="cd2b9-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="cd2b9-121">Exporte une collection de points de référence dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="cd2b9-122">La collection de points de référence, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="cd2b9-123">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="cd2b9-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="cd2b9-124">Supprime le journal de données associé au point de référence.</span><span class="sxs-lookup"><span data-stu-id="cd2b9-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="cd2b9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd2b9-125">Requirements</span></span>



| <span data-ttu-id="cd2b9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd2b9-126">Requirement</span></span> | <span data-ttu-id="cd2b9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd2b9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2b9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd2b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2b9-129">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd2b9-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cd2b9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd2b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2b9-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cd2b9-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cd2b9-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd2b9-132">Namespace</span></span><br/>                | <span data-ttu-id="cd2b9-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd2b9-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd2b9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cd2b9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd2b9-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd2b9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd2b9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd2b9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd2b9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd2b9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd2b9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd2b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2b9-139">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="cd2b9-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




