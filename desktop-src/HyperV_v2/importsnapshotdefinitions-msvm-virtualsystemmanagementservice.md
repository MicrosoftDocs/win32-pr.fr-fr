---
description: Recherche dans le dossier spécifié les fichiers de définition d’instantané associés au système informatique planifié spécifié et crée un nouvel instantané sur le système informatique planifié pour chaque fichier de définition associé à cet emplacement.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Méthode ImportSnapshotDefinitions de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863570"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="c54c2-103">Méthode ImportSnapshotDefinitions de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="c54c2-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c54c2-104">Recherche dans le dossier spécifié les fichiers de définition d’instantané associés au système informatique planifié spécifié et crée un nouvel instantané sur le système informatique planifié pour chaque fichier de définition associé à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="c54c2-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="c54c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c54c2-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c54c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c54c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54c2-107">*PlannedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c54c2-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54c2-108">Référence à un objet [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) qui représente l’ordinateur virtuel planifié qui fait référence aux captures instantanées à importer.</span><span class="sxs-lookup"><span data-stu-id="c54c2-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-109">*SnapshotFolder* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c54c2-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54c2-110">Le chemin d’accès complet au dossier dans lequel se trouvent les configurations d’instantanés pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c54c2-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-111">*ImportedSnapshots* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c54c2-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c54c2-112">Si l’opération se termine de façon synchrone, il s’agit d’un tableau de références aux instances [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) représentant les captures instantanées qui ont été correctement importées.</span><span class="sxs-lookup"><span data-stu-id="c54c2-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c54c2-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c54c2-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c54c2-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c54c2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c54c2-115">Return value</span></span>

<span data-ttu-id="c54c2-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c54c2-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c54c2-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c54c2-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c54c2-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c54c2-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c54c2-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c54c2-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c54c2-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c54c2-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c54c2-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c54c2-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c54c2-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c54c2-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c54c2-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c54c2-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-130">**Fichier en cours d’utilisation** (32779)</span><span class="sxs-lookup"><span data-stu-id="c54c2-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c54c2-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c54c2-131">Requirements</span></span>



| <span data-ttu-id="c54c2-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c54c2-132">Requirement</span></span> | <span data-ttu-id="c54c2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c54c2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54c2-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c54c2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c54c2-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c54c2-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c54c2-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c54c2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c54c2-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c54c2-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c54c2-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c54c2-138">Namespace</span></span><br/>                | <span data-ttu-id="c54c2-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c54c2-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c54c2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c54c2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c54c2-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c54c2-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c54c2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c54c2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c54c2-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c54c2-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c54c2-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c54c2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c54c2-145">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="c54c2-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

