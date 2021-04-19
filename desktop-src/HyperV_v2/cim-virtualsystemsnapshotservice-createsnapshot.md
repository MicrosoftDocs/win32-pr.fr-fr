---
description: Crée une capture instantanée d’un système virtuel.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Méthode CreateSnapshot de la classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534656"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="75c3f-103">Méthode CreateSnapshot de la \_ classe CIM VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="75c3f-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="75c3f-104">Crée une capture instantanée d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="75c3f-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75c3f-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="75c3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75c3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c3f-107">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-108">Référence [**CIM \_ CIM**](cim-computersystem.md) au système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="75c3f-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="75c3f-109">*SnapshotSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-110">Paramètres.</span><span class="sxs-lookup"><span data-stu-id="75c3f-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="75c3f-111">*SnapshotType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-112">Type d’instantané demandé :</span><span class="sxs-lookup"><span data-stu-id="75c3f-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="75c3f-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantané complet** (2)</span><span class="sxs-lookup"><span data-stu-id="75c3f-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="75c3f-114">Capture instantanée complète du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="75c3f-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="75c3f-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Capture instantanée de disque** (3)</span><span class="sxs-lookup"><span data-stu-id="75c3f-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="75c3f-116">Capture instantanée des disques système virtuels.</span><span class="sxs-lookup"><span data-stu-id="75c3f-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="75c3f-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="75c3f-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="75c3f-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="75c3f-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="75c3f-119">*ResultingSnapshot* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-120">Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à l’instantané du système virtuel résultant.</span><span class="sxs-lookup"><span data-stu-id="75c3f-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="75c3f-121">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-122">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="75c3f-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="75c3f-123">Dans ce cas, l’instance de la [**classe CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant le nouvel instantané du système virtuel est présentée via l’Association [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) , avec la valeur de la propriété **AffectedElement** qui fait référence à la nouvelle instance de la classe **CIM \_ VirtualSystemSettingData** représentant l’instantané du système virtuel et la valeur de la **ElementEffects** définie à 5 (créer).</span><span class="sxs-lookup"><span data-stu-id="75c3f-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="75c3f-124">Ce paramètre a été en lecture/écriture dans Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="75c3f-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c3f-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75c3f-125">Return value</span></span>

<span data-ttu-id="75c3f-126">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="75c3f-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="75c3f-127">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="75c3f-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-128">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="75c3f-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-129">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="75c3f-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-130">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="75c3f-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-131">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="75c3f-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-132">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="75c3f-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-133">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="75c3f-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-134">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="75c3f-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-135">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="75c3f-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-136">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="75c3f-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="75c3f-137">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="75c3f-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75c3f-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75c3f-138">Requirements</span></span>



| <span data-ttu-id="75c3f-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75c3f-139">Requirement</span></span> | <span data-ttu-id="75c3f-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="75c3f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c3f-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75c3f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="75c3f-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="75c3f-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="75c3f-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75c3f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="75c3f-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="75c3f-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="75c3f-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75c3f-145">Namespace</span></span><br/>                | <span data-ttu-id="75c3f-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="75c3f-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="75c3f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="75c3f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75c3f-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75c3f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="75c3f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c3f-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75c3f-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75c3f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c3f-152">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="75c3f-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




