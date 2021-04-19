---
description: Représente un travail d’opération de service de fichiers invité.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Classe Msvm_CopyFileToGuestJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533961"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="366f1-103">MSVM \_ CopyFileToGuestJob, classe</span><span class="sxs-lookup"><span data-stu-id="366f1-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="366f1-104">Représente un travail d’opération de service de fichiers invité.</span><span class="sxs-lookup"><span data-stu-id="366f1-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="366f1-105">Cette classe dérive de [**MSVM \_ GuestFileService**](msvm-guestfileservice.md).</span><span class="sxs-lookup"><span data-stu-id="366f1-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="366f1-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="366f1-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="366f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="366f1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="366f1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="366f1-108">Members</span></span>

<span data-ttu-id="366f1-109">La classe **MSVM \_ CopyFileToGuestJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="366f1-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="366f1-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="366f1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="366f1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="366f1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="366f1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="366f1-112">Methods</span></span>

<span data-ttu-id="366f1-113">La classe **MSVM \_ CopyFileToGuestJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="366f1-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="366f1-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="366f1-114">Method</span></span>                                                                   | <span data-ttu-id="366f1-115">Description</span><span class="sxs-lookup"><span data-stu-id="366f1-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="366f1-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="366f1-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="366f1-117">Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="366f1-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="366f1-118">**GetError**</span><span class="sxs-lookup"><span data-stu-id="366f1-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="366f1-119">Récupère l’objet d’erreur pour le travail.</span><span class="sxs-lookup"><span data-stu-id="366f1-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="366f1-120">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="366f1-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="366f1-121">Récupère les objets d’erreur pour le travail.</span><span class="sxs-lookup"><span data-stu-id="366f1-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="366f1-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="366f1-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="366f1-123">Modifie l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="366f1-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="366f1-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="366f1-124">**StartService**</span></span>                                                         | <span data-ttu-id="366f1-125">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="366f1-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="366f1-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="366f1-126">**StopService**</span></span>                                                          | <span data-ttu-id="366f1-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="366f1-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="366f1-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="366f1-128">Properties</span></span>

<span data-ttu-id="366f1-129">La classe **MSVM \_ CopyFileToGuestJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="366f1-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="366f1-130">**Annulable**</span><span class="sxs-lookup"><span data-stu-id="366f1-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="366f1-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-133">Indique si le travail peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="366f1-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="366f1-134">La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.</span><span class="sxs-lookup"><span data-stu-id="366f1-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="366f1-135">Si la **valeur est true**, la tâche peut être annulée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="366f1-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="366f1-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="366f1-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-139">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="366f1-139">Short textual description of the object.</span></span> <span data-ttu-id="366f1-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="366f1-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="366f1-141">**CopyFileToGuestSettingData**</span><span class="sxs-lookup"><span data-stu-id="366f1-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-142">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="366f1-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="366f1-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-144">Définition des données utilisées pour copier un fichier.</span><span class="sxs-lookup"><span data-stu-id="366f1-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="366f1-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="366f1-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-148">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="366f1-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="366f1-149">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="366f1-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="366f1-150">**Description**</span><span class="sxs-lookup"><span data-stu-id="366f1-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-153">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="366f1-153">Textual description of the object.</span></span> <span data-ttu-id="366f1-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="366f1-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="366f1-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="366f1-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="366f1-158">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="366f1-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="366f1-159">Description résumée de l’erreur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="366f1-159">A summary description of the error, if present.</span></span> <span data-ttu-id="366f1-160">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="366f1-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="366f1-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="366f1-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-162">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="366f1-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-164">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="366f1-164">Date and time the object was installed.</span></span> <span data-ttu-id="366f1-165">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="366f1-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="366f1-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="366f1-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="366f1-167">**Nom**</span><span class="sxs-lookup"><span data-stu-id="366f1-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-170">Identificateur unique du service qui fournit également une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="366f1-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="366f1-171">Pour plus d’informations sur les fonctionnalités, consultez la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="366f1-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="366f1-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="366f1-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="366f1-173">**Cours**</span><span class="sxs-lookup"><span data-stu-id="366f1-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-174">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="366f1-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-176">Si la **valeur est true**, le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="366f1-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="366f1-177">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="366f1-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-180">Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="366f1-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="366f1-181">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="366f1-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="366f1-182">**Automatique**</span><span class="sxs-lookup"><span data-stu-id="366f1-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="366f1-183">**Opération**</span><span class="sxs-lookup"><span data-stu-id="366f1-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="366f1-184">**État**</span><span class="sxs-lookup"><span data-stu-id="366f1-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-187">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="366f1-187">Current status of the object.</span></span> <span data-ttu-id="366f1-188">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="366f1-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="366f1-189">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="366f1-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="366f1-190">**OK**</span><span class="sxs-lookup"><span data-stu-id="366f1-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="366f1-191">**Erreurs**</span><span class="sxs-lookup"><span data-stu-id="366f1-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="366f1-192">**Détérioré**</span><span class="sxs-lookup"><span data-stu-id="366f1-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="366f1-193">**Connue**</span><span class="sxs-lookup"><span data-stu-id="366f1-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="366f1-194">**« Échec prévu »**</span><span class="sxs-lookup"><span data-stu-id="366f1-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="366f1-195">**Démarr**</span><span class="sxs-lookup"><span data-stu-id="366f1-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="366f1-196">**Arrêt**</span><span class="sxs-lookup"><span data-stu-id="366f1-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="366f1-197">**Services**</span><span class="sxs-lookup"><span data-stu-id="366f1-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="366f1-198">**Trop sollicité**</span><span class="sxs-lookup"><span data-stu-id="366f1-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="366f1-199">**« Non récupéré »**</span><span class="sxs-lookup"><span data-stu-id="366f1-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="366f1-200">**« Aucun contact »**</span><span class="sxs-lookup"><span data-stu-id="366f1-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="366f1-201">**« Comm. perdue »**</span><span class="sxs-lookup"><span data-stu-id="366f1-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="366f1-202">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="366f1-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-205">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="366f1-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="366f1-206">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="366f1-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-209">Nom du système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="366f1-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="366f1-210">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="366f1-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="366f1-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="366f1-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="366f1-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="366f1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="366f1-213">GUID du système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="366f1-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="366f1-214">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="366f1-214">Requirements</span></span>



| <span data-ttu-id="366f1-215">Condition requise</span><span class="sxs-lookup"><span data-stu-id="366f1-215">Requirement</span></span> | <span data-ttu-id="366f1-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="366f1-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="366f1-217">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="366f1-217">Minimum supported client</span></span><br/> | <span data-ttu-id="366f1-218">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="366f1-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="366f1-219">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="366f1-219">Minimum supported server</span></span><br/> | <span data-ttu-id="366f1-220">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="366f1-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="366f1-221">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="366f1-221">Namespace</span></span><br/>                | <span data-ttu-id="366f1-222">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="366f1-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="366f1-223">MOF</span><span class="sxs-lookup"><span data-stu-id="366f1-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="366f1-224"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="366f1-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="366f1-225">DLL</span><span class="sxs-lookup"><span data-stu-id="366f1-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="366f1-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="366f1-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="366f1-227">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="366f1-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366f1-228">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="366f1-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="366f1-229">**MSVM \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="366f1-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="366f1-230">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="366f1-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

