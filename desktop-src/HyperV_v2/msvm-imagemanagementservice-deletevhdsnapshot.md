---
description: Supprime une entrée de capture instantanée de disque dur virtuel dans un fichier de définition de VHD.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Méthode DeleteVHDSnapshot de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514458"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="c5db7-103">Méthode DeleteVHDSnapshot de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="c5db7-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="c5db7-104">Supprime une entrée de capture instantanée de disque dur virtuel dans un fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="c5db7-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5db7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5db7-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c5db7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5db7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5db7-107">*VHDSetPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5db7-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5db7-108">Chaîne contenant le chemin d’accès au fichier de l’ensemble de disques durs virtuels contenant l’instantané en question.</span><span class="sxs-lookup"><span data-stu-id="c5db7-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="c5db7-109">*SnapshotId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5db7-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5db7-110">GUID représentant l’ID d’instantané de l’entrée de capture instantanée de disque dur virtuel à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c5db7-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="c5db7-111">*PersistReferenceSnapshot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5db7-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5db7-112">Indique si un enregistrement d’instantané de référence uniquement doit être rendu persistant après la suppression de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="c5db7-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="c5db7-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c5db7-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5db7-114">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="c5db7-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5db7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5db7-115">Return value</span></span>

<span data-ttu-id="c5db7-116">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5db7-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c5db7-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c5db7-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c5db7-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c5db7-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c5db7-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c5db7-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c5db7-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c5db7-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c5db7-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c5db7-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c5db7-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c5db7-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c5db7-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c5db7-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c5db7-130">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="c5db7-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c5db7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5db7-131">Requirements</span></span>



| <span data-ttu-id="c5db7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5db7-132">Requirement</span></span> | <span data-ttu-id="c5db7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5db7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5db7-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5db7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c5db7-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5db7-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c5db7-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5db7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c5db7-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c5db7-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c5db7-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c5db7-138">Namespace</span></span><br/>                | <span data-ttu-id="c5db7-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5db7-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5db7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c5db7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5db7-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5db7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5db7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c5db7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5db7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5db7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5db7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5db7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5db7-145">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="c5db7-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




