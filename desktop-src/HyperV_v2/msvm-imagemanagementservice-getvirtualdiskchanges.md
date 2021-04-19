---
description: Récupère une liste de modifications dans la région spécifiée d’un disque virtuel depuis l’ID de Change Tracking résilient fourni ou l’ID d’instantané VHDSet.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Méthode GetVirtualDiskChanges de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521401"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="3c462-103">Méthode GetVirtualDiskChanges de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="3c462-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="3c462-104">Récupère une liste de modifications dans la région spécifiée d’un disque virtuel depuis l’ID de Change Tracking résilient fourni ou l’ID d’instantané VHDSet.</span><span class="sxs-lookup"><span data-stu-id="3c462-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c462-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c462-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3c462-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c462-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c462-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-108">Chemin d’accès complet qui spécifie l’emplacement du fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c462-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-109">*LimitId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c462-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-110">ID d’Change Tracking résilient ou ID d’instantané de définition de disque dur virtuel indiquant la ligne de base pour les modifications apportées au disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c462-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-111">*TargetSnapshotId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c462-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-112">ID d’instantané VHDSet indiquant la capture instantanée à comparer à la ligne de base lors de la détermination des modifications apportées au disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c462-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="3c462-113">Ce paramètre n’est valide que pour les fichiers de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="3c462-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-114">*ByteOffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c462-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-115">Décalage d’octet de la région du disque virtuel pour lequel interroger les modifications.</span><span class="sxs-lookup"><span data-stu-id="3c462-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-116">*ByteLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c462-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-117">Longueur en octets de la région du disque virtuel pour laquelle interroger les modifications.</span><span class="sxs-lookup"><span data-stu-id="3c462-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="3c462-118">Cette valeur doit être inférieure à la taille du disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c462-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-119">*ProcessedByteLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c462-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-120">Longueur totale en octets traitée.</span><span class="sxs-lookup"><span data-stu-id="3c462-120">The total byte length that was processed.</span></span> <span data-ttu-id="3c462-121">Cette valeur peut être inférieure ou égale à ByteLength.</span><span class="sxs-lookup"><span data-stu-id="3c462-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-122">*ChangedByteOffsets* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c462-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-123">Liste des décalages d’octets dans le disque virtuel indiquant le début de chaque plage modifiée.</span><span class="sxs-lookup"><span data-stu-id="3c462-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-124">*ChangedByteLengths* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c462-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-125">Liste des longueurs d’octets des plages modifiées dans le disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c462-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="3c462-126">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c462-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c462-127">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="3c462-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c462-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c462-128">Return value</span></span>

<span data-ttu-id="3c462-129">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c462-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3c462-130">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="3c462-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-131">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="3c462-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-132">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="3c462-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-133">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="3c462-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-134">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="3c462-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-135">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="3c462-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-136">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="3c462-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-137">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="3c462-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-138">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="3c462-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-139">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="3c462-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-140">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="3c462-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-141">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3c462-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-142">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="3c462-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3c462-143">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="3c462-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3c462-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c462-144">Requirements</span></span>



| <span data-ttu-id="3c462-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c462-145">Requirement</span></span> | <span data-ttu-id="3c462-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c462-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c462-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c462-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3c462-148">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c462-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3c462-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c462-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3c462-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c462-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3c462-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c462-151">Namespace</span></span><br/>                | <span data-ttu-id="3c462-152">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3c462-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c462-153">MOF</span><span class="sxs-lookup"><span data-stu-id="3c462-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c462-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c462-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c462-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3c462-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c462-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c462-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c462-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c462-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c462-158">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="3c462-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




