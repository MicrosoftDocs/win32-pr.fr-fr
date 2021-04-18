---
description: Fournit des informations supplémentaires à utiliser avec la méthode ExportSystemDefinition de la \_ classe VirtualSystemManagementService MSVM.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Classe Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519258"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="36bed-103">MSVM \_ VirtualSystemExportSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="36bed-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="36bed-104">Fournit des informations supplémentaires à utiliser avec la méthode [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="36bed-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="36bed-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="36bed-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36bed-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36bed-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="36bed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="36bed-107">Members</span></span>

<span data-ttu-id="36bed-108">La classe **MSVM \_ VirtualSystemExportSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36bed-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="36bed-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36bed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36bed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36bed-110">Properties</span></span>

<span data-ttu-id="36bed-111">La classe **MSVM \_ VirtualSystemExportSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="36bed-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36bed-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="36bed-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-113">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="36bed-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-115">Indique l’intention d’utiliser les jeux de sauvegarde exportés.</span><span class="sxs-lookup"><span data-stu-id="36bed-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-116">Cette propriété a été ajoutée dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="36bed-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="36bed-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span><span class="sxs-lookup"><span data-stu-id="36bed-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-118">Tous les jeux de sauvegardes complets et différentiels exportés sont conservés tels quels.</span><span class="sxs-lookup"><span data-stu-id="36bed-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="36bed-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span><span class="sxs-lookup"><span data-stu-id="36bed-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-120">Les jeux de sauvegarde complète et différentielle exportés sont fusionnés pour synthétiser les jeux de sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="36bed-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="36bed-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="36bed-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36bed-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36bed-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36bed-124">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="36bed-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="36bed-125">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="36bed-125">A short description of the object.</span></span> <span data-ttu-id="36bed-126">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="36bed-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36bed-127">**CaptureLiveState**</span><span class="sxs-lookup"><span data-stu-id="36bed-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-128">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="36bed-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-130">Indique l’État à capturer si la cible de l’exportation est une machine virtuelle en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="36bed-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="36bed-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span><span class="sxs-lookup"><span data-stu-id="36bed-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-132">Aucun fichier d’état enregistré ne sera exporté pour l’ordinateur virtuel en cours d’exécution, en le plaçant dans un état de cohérence en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="36bed-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="36bed-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span><span class="sxs-lookup"><span data-stu-id="36bed-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-134">Les fichiers d’État enregistrés pour la machine virtuelle en cours d’exécution seront exportés en même temps que la configuration de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="36bed-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="36bed-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span><span class="sxs-lookup"><span data-stu-id="36bed-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-136">L’état de cohérence des applications de la machine virtuelle en cours d’exécution sera exporté.</span><span class="sxs-lookup"><span data-stu-id="36bed-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-137">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="36bed-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="36bed-138">**CopySnapshotConfiguration**</span><span class="sxs-lookup"><span data-stu-id="36bed-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-139">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="36bed-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-141">Indique les captures instantanées à exporter avec la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="36bed-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="36bed-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span><span class="sxs-lookup"><span data-stu-id="36bed-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-143">Toutes les captures instantanées sont exportées avec la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="36bed-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="36bed-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span><span class="sxs-lookup"><span data-stu-id="36bed-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-145">Aucune capture instantanée n’est exportée avec la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="36bed-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="36bed-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span><span class="sxs-lookup"><span data-stu-id="36bed-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-147">Les instantanés identifiés par la propriété **SnapshotVirtualSystem** sont exportés avec l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="36bed-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="36bed-148">Les propriétés **CopyVmStorage** et **CopyVmRuntimeInformation** sont ignorées, les informations de stockage et d’exécution sont exportées avec la machine virtuelle et tous les disques de différenciation VHD sont fusionnés dans un nouveau disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="36bed-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="36bed-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span><span class="sxs-lookup"><span data-stu-id="36bed-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="36bed-150">L’instantané identifié par la propriété **SnapshotVirtualSystem** sera exporté à des fins de sauvegarde de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="36bed-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="36bed-151">La configuration exportée utilise l’ID de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="36bed-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-152">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="36bed-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="36bed-153">**CopyVmRuntimeInformation**</span><span class="sxs-lookup"><span data-stu-id="36bed-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-154">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="36bed-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-156">Indique si les informations d’exécution de la machine virtuelle seront copiées lors de l’exportation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="36bed-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="36bed-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bed-157">Value</span></span>                                                                                | <span data-ttu-id="36bed-158">Signification</span><span class="sxs-lookup"><span data-stu-id="36bed-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36bed-159"><dt>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="36bed-160">Les informations d’exécution de la machine virtuelle seront copiées.</span><span class="sxs-lookup"><span data-stu-id="36bed-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="36bed-161"><dt>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="36bed-162">Les informations d’exécution de l’ordinateur virtuel ne seront pas copiées.</span><span class="sxs-lookup"><span data-stu-id="36bed-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36bed-163">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="36bed-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-164">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="36bed-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-166">Indique si le stockage de l’ordinateur virtuel sera copié lors de l’exportation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="36bed-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="36bed-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bed-167">Value</span></span>                                                                                | <span data-ttu-id="36bed-168">Signification</span><span class="sxs-lookup"><span data-stu-id="36bed-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="36bed-169"><dt>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="36bed-170">Le stockage de l’ordinateur virtuel sera copié.</span><span class="sxs-lookup"><span data-stu-id="36bed-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="36bed-171"><dt>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="36bed-172">Le stockage de l’ordinateur virtuel ne sera pas copié.</span><span class="sxs-lookup"><span data-stu-id="36bed-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36bed-173">**CreateVmExportSubdirectory**</span><span class="sxs-lookup"><span data-stu-id="36bed-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-174">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="36bed-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-176">Indique si un sous-répertoire avec le nom de l’ordinateur virtuel sera créé lors de l’exportation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="36bed-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="36bed-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bed-177">Value</span></span>                                                                                | <span data-ttu-id="36bed-178">Signification</span><span class="sxs-lookup"><span data-stu-id="36bed-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="36bed-179"><dt>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="36bed-180">Un sous-répertoire est créé.</span><span class="sxs-lookup"><span data-stu-id="36bed-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="36bed-181"><dt>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="36bed-182">Un sous-répertoire ne sera pas créé.</span><span class="sxs-lookup"><span data-stu-id="36bed-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36bed-183">**Description**</span><span class="sxs-lookup"><span data-stu-id="36bed-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36bed-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36bed-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36bed-186">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="36bed-186">A description of the object.</span></span> <span data-ttu-id="36bed-187">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="36bed-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36bed-188">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="36bed-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36bed-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-191">Base pour l’exportation différentielle.</span><span class="sxs-lookup"><span data-stu-id="36bed-191">Base for differential export.</span></span> <span data-ttu-id="36bed-192">Il s’agit de l’un des chemins d’accès à une instance [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente le point de référence ou le chemin d’accès à une instance [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) qui représente l’instantané à utiliser comme base pour l’exportation différentielle.</span><span class="sxs-lookup"><span data-stu-id="36bed-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="36bed-193">Si la propriété **CopySnapshotConfiguration** n’a pas la valeur 3 (**ExportOneSnapshotForBackup**), cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="36bed-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-194">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="36bed-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="36bed-195">**DisableDifferentialOfIgnoredStorage**</span><span class="sxs-lookup"><span data-stu-id="36bed-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="36bed-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-198">Indique si les disques de différenciation seront créés ou non pour le stockage ignoré pendant l’exportation.</span><span class="sxs-lookup"><span data-stu-id="36bed-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="36bed-199">Par défaut, cette valeur est définie sur false, ce qui signifie que les disques de différenciation sont créés pour le stockage qui ne va pas être copié vers la destination d’exportation.</span><span class="sxs-lookup"><span data-stu-id="36bed-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-200">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="36bed-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="36bed-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="36bed-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36bed-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36bed-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36bed-204">Nom complet de cette instance.</span><span class="sxs-lookup"><span data-stu-id="36bed-204">The display name for this instance.</span></span> <span data-ttu-id="36bed-205">En outre, le nom complet peut être utilisé comme propriété d’index pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="36bed-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="36bed-206">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36bed-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36bed-207">**ExcludedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="36bed-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-208">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="36bed-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36bed-209">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-210">Tableau d’ID d’instance [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) qui représentent les disques durs virtuels qui doivent être exclus de l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="36bed-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="36bed-211">Si au moins un des ID fournis n’est pas un disque dur virtuel attaché valide, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="36bed-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="36bed-212">Les disques durs virtuels référencés par cette propriété peuvent provenir de la machine virtuelle et/ou de l’un de ses instantanés.</span><span class="sxs-lookup"><span data-stu-id="36bed-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="36bed-213">L’exclusion de disques durs virtuels n’est pas prise en charge lorsque la propriété **CopySnapshotConfiguration** est définie sur 0 (ExportAllSnapshots).</span><span class="sxs-lookup"><span data-stu-id="36bed-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="36bed-214">Notez que l’ID d’instance RASD pour les disques durs virtuels représente l’emplacement auquel ils sont attachés, et l’exclusion de cet ID exclut tous les disques durs virtuels attachés à cet emplacement dans l’arborescence des captures instantanées de la machine virtuelle, quelle que soit la chaîne de disque dur virtuel valide.</span><span class="sxs-lookup"><span data-stu-id="36bed-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-215">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="36bed-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="36bed-216">**ExportForLiveMigration**</span><span class="sxs-lookup"><span data-stu-id="36bed-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-217">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="36bed-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-218">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-219">Indique si la machine virtuelle exportée est destinée à être utilisée dans la migration dynamique.</span><span class="sxs-lookup"><span data-stu-id="36bed-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="36bed-220">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="36bed-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="36bed-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="36bed-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36bed-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36bed-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36bed-224">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="36bed-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="36bed-225">Dans l’étendue de l’espace de noms d’instanciation, identifie de manière opaque et unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="36bed-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="36bed-226">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36bed-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36bed-227">**SnapshotVirtualSystem**</span><span class="sxs-lookup"><span data-stu-id="36bed-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36bed-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36bed-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36bed-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36bed-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="36bed-230">Chemin d’accès à une instance [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente l’instantané à exporter avec l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="36bed-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="36bed-231">Si la propriété **CopySnapshotConfiguration** n’a pas la valeur 2 (ExportOneSnapshot), cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="36bed-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36bed-232">Notes</span><span class="sxs-lookup"><span data-stu-id="36bed-232">Remarks</span></span>

<span data-ttu-id="36bed-233">L’accès à la classe **MSVM \_ VirtualSystemExportSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="36bed-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="36bed-234">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="36bed-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="36bed-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36bed-235">Requirements</span></span>



| <span data-ttu-id="36bed-236">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36bed-236">Requirement</span></span> | <span data-ttu-id="36bed-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bed-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bed-238">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36bed-238">Minimum supported client</span></span><br/> | <span data-ttu-id="36bed-239">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36bed-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="36bed-240">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36bed-240">Minimum supported server</span></span><br/> | <span data-ttu-id="36bed-241">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36bed-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36bed-242">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36bed-242">Namespace</span></span><br/>                | <span data-ttu-id="36bed-243">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="36bed-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="36bed-244">MOF</span><span class="sxs-lookup"><span data-stu-id="36bed-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36bed-245"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36bed-246">DLL</span><span class="sxs-lookup"><span data-stu-id="36bed-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36bed-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36bed-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36bed-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36bed-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bed-249">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="36bed-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="36bed-250">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="36bed-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="36bed-251">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="36bed-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

