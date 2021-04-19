---
description: Cette classe représente un travail d’exportation de point de référence de collection.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535696"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="eaed7-103">MSVM \_ CollectionReferencePointExportJob, classe</span><span class="sxs-lookup"><span data-stu-id="eaed7-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="eaed7-104">Cette classe représente un travail d’exportation de point de référence de collection.</span><span class="sxs-lookup"><span data-stu-id="eaed7-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="eaed7-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eaed7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaed7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaed7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="eaed7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="eaed7-107">Members</span></span>

<span data-ttu-id="eaed7-108">La classe **MSVM \_ CollectionReferencePointExportJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eaed7-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="eaed7-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eaed7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="eaed7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eaed7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eaed7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eaed7-111">Methods</span></span>

<span data-ttu-id="eaed7-112">La classe **MSVM \_ CollectionReferencePointExportJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eaed7-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="eaed7-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="eaed7-113">Method</span></span>                                                                                  | <span data-ttu-id="eaed7-114">Description</span><span class="sxs-lookup"><span data-stu-id="eaed7-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="eaed7-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="eaed7-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="eaed7-116">Récupère une erreur.</span><span class="sxs-lookup"><span data-stu-id="eaed7-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="eaed7-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="eaed7-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="eaed7-118">Récupère des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="eaed7-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="eaed7-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="eaed7-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="eaed7-120">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="eaed7-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="eaed7-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eaed7-121">Properties</span></span>

<span data-ttu-id="eaed7-122">La classe **MSVM \_ CollectionReferencePointExportJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eaed7-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eaed7-123">**BaseReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="eaed7-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaed7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-126">GUID du point de référence de collection utilisé comme base dans le exportoperation.</span><span class="sxs-lookup"><span data-stu-id="eaed7-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-127">**Annulable**</span><span class="sxs-lookup"><span data-stu-id="eaed7-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaed7-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-130">Indique si le travail peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="eaed7-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="eaed7-131">La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.</span><span class="sxs-lookup"><span data-stu-id="eaed7-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-132">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="eaed7-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaed7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-135">GUID du groupe de machines virtuelles pour lequel les fichiers journaux wereexported.</span><span class="sxs-lookup"><span data-stu-id="eaed7-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="eaed7-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaed7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-139">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="eaed7-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-140">Contient une description résumée des erreurs.</span><span class="sxs-lookup"><span data-stu-id="eaed7-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-141">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="eaed7-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaed7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-144">Emplacement d’exportation.</span><span class="sxs-lookup"><span data-stu-id="eaed7-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-145">**ExportedConfigFilePaths**</span><span class="sxs-lookup"><span data-stu-id="eaed7-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-146">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaed7-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-148">Chemin d’accès du fichier de configuration de l’ordinateur virtuel exporté.</span><span class="sxs-lookup"><span data-stu-id="eaed7-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-149">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="eaed7-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-150">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaed7-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-152">ID d’instance des disques virtuels pour lesquels les fichiers journaux ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="eaed7-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-153">**ExportedGuestStateFilePaths**</span><span class="sxs-lookup"><span data-stu-id="eaed7-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-154">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaed7-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-156">Chemin d’accès du fichier d’État invité de l’ordinateur virtuel exporté.</span><span class="sxs-lookup"><span data-stu-id="eaed7-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="eaed7-157">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="eaed7-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="eaed7-158">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="eaed7-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-159">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaed7-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-161">Chemins des fichiers journaux qui ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="eaed7-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-162">**ExportedRuntimeFilePaths**</span><span class="sxs-lookup"><span data-stu-id="eaed7-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-163">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaed7-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-165">Chemin d’accès du fichier d’état d’exécution de l’ordinateur virtuel exporté.</span><span class="sxs-lookup"><span data-stu-id="eaed7-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-166">**ReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="eaed7-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaed7-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-169">GUID du point de référence de collection qui est exporté.</span><span class="sxs-lookup"><span data-stu-id="eaed7-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="eaed7-170">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="eaed7-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaed7-171">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="eaed7-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eaed7-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaed7-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eaed7-173">GUID des machines virtuelles pour lesquelles l’opération d’exportation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="eaed7-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eaed7-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaed7-174">Requirements</span></span>



| <span data-ttu-id="eaed7-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaed7-175">Requirement</span></span> | <span data-ttu-id="eaed7-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaed7-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaed7-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaed7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="eaed7-178">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaed7-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eaed7-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaed7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="eaed7-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eaed7-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eaed7-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eaed7-181">Namespace</span></span><br/>                | <span data-ttu-id="eaed7-182">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="eaed7-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eaed7-183">MOF</span><span class="sxs-lookup"><span data-stu-id="eaed7-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaed7-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaed7-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaed7-185">DLL</span><span class="sxs-lookup"><span data-stu-id="eaed7-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaed7-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eaed7-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eaed7-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaed7-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaed7-188">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="eaed7-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

