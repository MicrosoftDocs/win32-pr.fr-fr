---
description: Crée une capture instantanée d’une collection de systèmes virtuels.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Méthode CreateSnapshot de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755156"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="8981b-103">Méthode CreateSnapshot de la \_ classe CollectionSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="8981b-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="8981b-104">Crée une capture instantanée d’une collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="8981b-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8981b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8981b-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8981b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8981b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8981b-107">*Collection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8981b-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8981b-108">Référence à une [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) qui décrit la collection de systèmes virtuels affectés.</span><span class="sxs-lookup"><span data-stu-id="8981b-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="8981b-109">*SnapshotSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8981b-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8981b-110">Contient les paramètres.</span><span class="sxs-lookup"><span data-stu-id="8981b-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="8981b-111">*SnapshotType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8981b-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8981b-112">Type d’instantané demandé :</span><span class="sxs-lookup"><span data-stu-id="8981b-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8981b-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8981b-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="8981b-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Instantané standard** (1)</span><span class="sxs-lookup"><span data-stu-id="8981b-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8981b-115">Instantané standard du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="8981b-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="8981b-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Instantané de récupération** (2)</span><span class="sxs-lookup"><span data-stu-id="8981b-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8981b-117">Instantané pour les scénarios de récupération, y compris la réplication de basculement et la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8981b-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8981b-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8981b-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="8981b-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8981b-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8981b-120">*ResultingSnapshotCollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8981b-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8981b-121">En cas de réussite, retourne une référence de [**\_ collection CIM**](cim-collection.md) contenant l’instantané du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="8981b-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="8981b-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8981b-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8981b-123">Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8981b-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="8981b-124">Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="8981b-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8981b-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8981b-125">Return value</span></span>

<span data-ttu-id="8981b-126">En cas de réussite, retourne 0 (terminé) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="8981b-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8981b-127">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="8981b-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-128">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="8981b-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-129">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="8981b-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-130">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="8981b-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-131">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="8981b-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-132">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="8981b-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-133">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="8981b-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-134">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8981b-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-135">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="8981b-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-136">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8981b-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8981b-137">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8981b-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8981b-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8981b-138">Requirements</span></span>



| <span data-ttu-id="8981b-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8981b-139">Requirement</span></span> | <span data-ttu-id="8981b-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="8981b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8981b-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8981b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8981b-142">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8981b-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8981b-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8981b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8981b-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8981b-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8981b-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8981b-145">Namespace</span></span><br/>                | <span data-ttu-id="8981b-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8981b-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8981b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8981b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8981b-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8981b-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8981b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8981b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8981b-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8981b-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8981b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8981b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8981b-152">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="8981b-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




