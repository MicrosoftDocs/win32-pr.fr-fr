---
description: Crée un nouvel \_ objet CIM CollectionOfMSEs.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Méthode DefineCollection de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530721"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="63e53-103">Méthode DefineCollection de la \_ classe CollectionManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="63e53-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="63e53-104">Crée un nouvel objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="63e53-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63e53-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="63e53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63e53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e53-107">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63e53-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e53-108">Nom de la nouvelle collection.</span><span class="sxs-lookup"><span data-stu-id="63e53-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="63e53-109">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63e53-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e53-110">ID de la nouvelle collection.</span><span class="sxs-lookup"><span data-stu-id="63e53-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="63e53-111">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63e53-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e53-112">Type de la nouvelle collection.</span><span class="sxs-lookup"><span data-stu-id="63e53-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="63e53-113">**Collection de systèmes virtuels** (0)</span><span class="sxs-lookup"><span data-stu-id="63e53-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="63e53-114">**Collection de collections** (1)</span><span class="sxs-lookup"><span data-stu-id="63e53-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="63e53-115">*DefinedCollection* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="63e53-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63e53-116">Référence aux objets qui définissent la collection.</span><span class="sxs-lookup"><span data-stu-id="63e53-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="63e53-117">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="63e53-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63e53-118">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="63e53-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e53-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63e53-119">Return value</span></span>

<span data-ttu-id="63e53-120">En cas de réussite, retourne 0 ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="63e53-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="63e53-121">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="63e53-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="63e53-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-123">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="63e53-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-124">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="63e53-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-125">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="63e53-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-126">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="63e53-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-127">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="63e53-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-128">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="63e53-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-129">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="63e53-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-130">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="63e53-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-131">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="63e53-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-132">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="63e53-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-133">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="63e53-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="63e53-134">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="63e53-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="63e53-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63e53-135">Requirements</span></span>



| <span data-ttu-id="63e53-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63e53-136">Requirement</span></span> | <span data-ttu-id="63e53-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="63e53-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e53-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63e53-138">Minimum supported client</span></span><br/> | <span data-ttu-id="63e53-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63e53-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="63e53-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63e53-140">Minimum supported server</span></span><br/> | <span data-ttu-id="63e53-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="63e53-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="63e53-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63e53-142">Namespace</span></span><br/>                | <span data-ttu-id="63e53-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="63e53-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="63e53-144">MOF</span><span class="sxs-lookup"><span data-stu-id="63e53-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63e53-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63e53-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63e53-146">DLL</span><span class="sxs-lookup"><span data-stu-id="63e53-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e53-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63e53-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="63e53-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63e53-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e53-149">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="63e53-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




