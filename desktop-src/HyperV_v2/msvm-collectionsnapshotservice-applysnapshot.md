---
description: Applique une collection d’instantanés à la collection de systèmes d’ordinateurs virtuels.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Méthode ApplySnapshot de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514423"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="e90c6-103">Méthode ApplySnapshot de la \_ classe CollectionSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="e90c6-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="e90c6-104">Applique une collection d’instantanés à la collection de systèmes d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="e90c6-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e90c6-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e90c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e90c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90c6-107">*SnapshotCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e90c6-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90c6-108">Référence à une [**\_ collection CIM**](cim-collection.md) qui représente la collection d’instantanés à appliquer.</span><span class="sxs-lookup"><span data-stu-id="e90c6-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="e90c6-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e90c6-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e90c6-110">Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e90c6-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="e90c6-111">Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e90c6-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90c6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e90c6-112">Return value</span></span>

<span data-ttu-id="e90c6-113">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="e90c6-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e90c6-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e90c6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e90c6-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="e90c6-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="e90c6-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="e90c6-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="e90c6-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-120">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="e90c6-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e90c6-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="e90c6-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-123">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e90c6-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e90c6-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e90c6-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e90c6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e90c6-125">Requirements</span></span>



| <span data-ttu-id="e90c6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e90c6-126">Requirement</span></span> | <span data-ttu-id="e90c6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e90c6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90c6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e90c6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e90c6-129">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e90c6-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e90c6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e90c6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e90c6-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e90c6-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e90c6-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e90c6-132">Namespace</span></span><br/>                | <span data-ttu-id="e90c6-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e90c6-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e90c6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e90c6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e90c6-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e90c6-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e90c6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e90c6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90c6-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e90c6-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e90c6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e90c6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90c6-139">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="e90c6-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




