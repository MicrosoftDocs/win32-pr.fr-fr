---
description: Convertit une capture instantanée de collection existante en collection de points de référence. La collection d’instantanés est supprimée en tant qu’effet secondaire. Seuls les instantanés de récupération peuvent être convertis en points de référence.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Méthode ConvertToReferencePoint de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869085"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="b6895-105">Méthode ConvertToReferencePoint de la \_ classe CollectionSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="b6895-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="b6895-106">Convertit une capture instantanée de collection existante en collection de points de référence.</span><span class="sxs-lookup"><span data-stu-id="b6895-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="b6895-107">La collection d’instantanés est supprimée en tant qu’effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="b6895-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="b6895-108">Seuls les instantanés de récupération peuvent être convertis en points de référence.</span><span class="sxs-lookup"><span data-stu-id="b6895-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6895-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6895-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b6895-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6895-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6895-111">*AffectedSnapshotCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6895-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6895-112">Référence à un [**\_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) contenant la collection d’instantanés du système virtuel affectée.</span><span class="sxs-lookup"><span data-stu-id="b6895-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="b6895-113">*ResultingReferencePointCollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b6895-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6895-114">Référence à un [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) contenant la collection de points de référence du système virtuel résultant</span><span class="sxs-lookup"><span data-stu-id="b6895-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="b6895-115">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6895-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6895-116">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="b6895-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6895-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6895-117">Return value</span></span>

<span data-ttu-id="b6895-118">En cas de réussite, retourne 0 (terminé) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="b6895-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b6895-119">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="b6895-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-120">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="b6895-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-121">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="b6895-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-122">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="b6895-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-123">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="b6895-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-124">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="b6895-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-125">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="b6895-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-126">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="b6895-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-127">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="b6895-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-128">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b6895-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b6895-129">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b6895-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b6895-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6895-130">Requirements</span></span>



| <span data-ttu-id="b6895-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6895-131">Requirement</span></span> | <span data-ttu-id="b6895-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6895-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6895-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6895-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b6895-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6895-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b6895-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6895-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b6895-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b6895-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b6895-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6895-137">Namespace</span></span><br/>                | <span data-ttu-id="b6895-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6895-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6895-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b6895-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6895-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6895-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6895-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b6895-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6895-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6895-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6895-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6895-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6895-144">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="b6895-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




