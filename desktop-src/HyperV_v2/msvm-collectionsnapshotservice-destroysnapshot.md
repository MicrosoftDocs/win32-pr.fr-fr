---
description: Détruit un instantané existant de la collection de systèmes virtuels. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Méthode DestroySnapshot de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527815"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="f33a9-104">Méthode DestroySnapshot de la \_ classe CollectionSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="f33a9-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="f33a9-105">Détruit un instantané existant de la collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="f33a9-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="f33a9-106">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.</span><span class="sxs-lookup"><span data-stu-id="f33a9-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33a9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f33a9-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f33a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f33a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33a9-109">*AffectedSnapshotCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f33a9-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33a9-110">Référence à une [**\_ collection CIM**](cim-collection.md) qui décrit la collection d’instantanés de système virtuel affectée.</span><span class="sxs-lookup"><span data-stu-id="f33a9-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="f33a9-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f33a9-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f33a9-112">Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f33a9-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="f33a9-113">Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="f33a9-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33a9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f33a9-114">Return value</span></span>

<span data-ttu-id="f33a9-115">En cas de réussite, retourne 0 (terminé) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="f33a9-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f33a9-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="f33a9-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f33a9-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="f33a9-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="f33a9-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="f33a9-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="f33a9-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-122">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="f33a9-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f33a9-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="f33a9-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f33a9-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f33a9-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f33a9-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f33a9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f33a9-127">Requirements</span></span>



| <span data-ttu-id="f33a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f33a9-128">Requirement</span></span> | <span data-ttu-id="f33a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f33a9-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33a9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f33a9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f33a9-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f33a9-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f33a9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f33a9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f33a9-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f33a9-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f33a9-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f33a9-134">Namespace</span></span><br/>                | <span data-ttu-id="f33a9-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f33a9-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f33a9-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f33a9-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f33a9-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f33a9-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f33a9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f33a9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33a9-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f33a9-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f33a9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f33a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33a9-141">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="f33a9-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




