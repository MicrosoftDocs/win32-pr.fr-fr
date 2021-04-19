---
description: Crée un système informatique planifié basé sur la définition d’ordinateur virtuel spécifiée.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Méthode ImportSystemDefinition de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516972"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2681c-103">Méthode ImportSystemDefinition de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="2681c-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2681c-104">Crée un système informatique planifié basé sur la définition d’ordinateur virtuel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2681c-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2681c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2681c-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2681c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2681c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2681c-107">*SystemDefinitionFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2681c-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2681c-108">Le chemin d’accès complet au fichier de définition de système (. XML ou. exp) représentant l’ordinateur virtuel qui doit être importé.</span><span class="sxs-lookup"><span data-stu-id="2681c-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="2681c-109">Le fichier de définition ne doit pas être déjà utilisé par le système hôte ou la plateforme de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="2681c-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="2681c-110">*SnapshotFolder* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2681c-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2681c-111">Le chemin d’accès complet au dossier dans lequel se trouvent les configurations d’instantanés pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2681c-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="2681c-112">Ce dossier sera recherché afin de localiser les captures instantanées référencées par la définition de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2681c-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="2681c-113">Les captures instantanées référencées introuvables à cet emplacement doivent être supprimées à l’aide de la méthode [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) , ou importées à l’aide de la méthode [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) avant de réaliser le système informatique planifié.</span><span class="sxs-lookup"><span data-stu-id="2681c-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2681c-114">*GenerateNewSystemIdentifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2681c-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2681c-115">Indique s’il faut réutiliser l’identificateur unique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2681c-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="2681c-116">Si ce paramètre a la **valeur true**, un nouvel identificateur du système est généré.</span><span class="sxs-lookup"><span data-stu-id="2681c-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="2681c-117">Si ce paramètre a la **valeur false**, l’identificateur système existant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2681c-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="2681c-118">*ImportedSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2681c-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2681c-119">Si l’opération se termine de façon synchrone, il s’agit d’une référence à un objet [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) qui représente la machine virtuelle importée.</span><span class="sxs-lookup"><span data-stu-id="2681c-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2681c-120">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2681c-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2681c-121">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2681c-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2681c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2681c-122">Return value</span></span>

<span data-ttu-id="2681c-123">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2681c-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2681c-124">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="2681c-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-125">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="2681c-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-126">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="2681c-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-127">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="2681c-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-128">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="2681c-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-129">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="2681c-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-130">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="2681c-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-131">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="2681c-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-132">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="2681c-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-133">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="2681c-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-134">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="2681c-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-135">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2681c-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-136">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="2681c-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2681c-137">**Fichier en cours d’utilisation** (32779)</span><span class="sxs-lookup"><span data-stu-id="2681c-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2681c-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2681c-138">Requirements</span></span>



| <span data-ttu-id="2681c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2681c-139">Requirement</span></span> | <span data-ttu-id="2681c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="2681c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2681c-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2681c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2681c-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2681c-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2681c-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2681c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2681c-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2681c-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2681c-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2681c-145">Namespace</span></span><br/>                | <span data-ttu-id="2681c-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2681c-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2681c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2681c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2681c-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2681c-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2681c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2681c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2681c-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2681c-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2681c-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2681c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2681c-152">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="2681c-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

