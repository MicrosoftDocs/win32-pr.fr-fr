---
description: Cette classe représente un travail d’exportation de point de référence système virtuel.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530453"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="ba9b1-103">MSVM \_ VirtualSystemReferencePointExportJob, classe</span><span class="sxs-lookup"><span data-stu-id="ba9b1-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="ba9b1-104">Cette classe représente un travail d’exportation de point de référence système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="ba9b1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba9b1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba9b1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="ba9b1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ba9b1-107">Members</span></span>

<span data-ttu-id="ba9b1-108">La classe **MSVM \_ VirtualSystemReferencePointExportJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba9b1-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="ba9b1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ba9b1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ba9b1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba9b1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ba9b1-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ba9b1-111">Methods</span></span>

<span data-ttu-id="ba9b1-112">La classe **MSVM \_ VirtualSystemReferencePointExportJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="ba9b1-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="ba9b1-113">Method</span></span>                                                                                     | <span data-ttu-id="ba9b1-114">Description</span><span class="sxs-lookup"><span data-stu-id="ba9b1-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="ba9b1-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="ba9b1-116">Récupère l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="ba9b1-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="ba9b1-118">Récupère des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="ba9b1-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="ba9b1-120">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="ba9b1-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba9b1-121">Properties</span></span>

<span data-ttu-id="ba9b1-122">La classe **MSVM \_ VirtualSystemReferencePointExportJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba9b1-123">**BaseReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-126">GUID du point de référence utilisé comme base dans l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-127">**Annulable**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-130">Indique si le travail peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="ba9b1-131">La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-135">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="ba9b1-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-136">Contient une description résumée des erreurs.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-137">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-140">Emplacement d’exportation.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-141">**ExportedConfigFilePath**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-144">Chemin d’accès du fichier de configuration exporté.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-145">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-146">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-148">ID d’instance des disques virtuels pour lesquels les fichiers journaux ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-149">**ExportedGuestStateFilePath**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-152">Chemin d’accès du fichier d’État invité exporté.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="ba9b1-153">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ba9b1-154">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-155">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-157">Chemins des fichiers journaux qui ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-158">**ExportedRuntimeFilePath**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-161">Chemin d’accès du fichier d’état d’exécution exporté.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-162">**ReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-165">GUID du point de référence exporté.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b1-166">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba9b1-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba9b1-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba9b1-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba9b1-169">GUID de l’ordinateur virtuel pour lequel les fichiers journaux ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="ba9b1-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba9b1-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba9b1-170">Requirements</span></span>



| <span data-ttu-id="ba9b1-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba9b1-171">Requirement</span></span> | <span data-ttu-id="ba9b1-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba9b1-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b1-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba9b1-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ba9b1-174">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba9b1-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ba9b1-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba9b1-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ba9b1-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba9b1-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ba9b1-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ba9b1-177">Namespace</span></span><br/>                | <span data-ttu-id="ba9b1-178">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba9b1-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ba9b1-179">MOF</span><span class="sxs-lookup"><span data-stu-id="ba9b1-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba9b1-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba9b1-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba9b1-181">DLL</span><span class="sxs-lookup"><span data-stu-id="ba9b1-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba9b1-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba9b1-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba9b1-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba9b1-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba9b1-184">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="ba9b1-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

