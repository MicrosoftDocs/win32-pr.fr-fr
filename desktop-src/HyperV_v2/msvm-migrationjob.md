---
description: Cette classe représente un travail d’opération de migration créé pour le stockage ou la migration du système virtuel par le service de migration de système virtuel.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517617"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="10b96-103">MSVM \_ MigrationJob, classe</span><span class="sxs-lookup"><span data-stu-id="10b96-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="10b96-104">Cette classe représente un travail d’opération de migration créé pour le stockage ou la migration du système virtuel par le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="10b96-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="10b96-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="10b96-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b96-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10b96-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="10b96-107">Membres</span><span class="sxs-lookup"><span data-stu-id="10b96-107">Members</span></span>

<span data-ttu-id="10b96-108">La classe **MSVM \_ MigrationJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="10b96-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="10b96-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="10b96-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="10b96-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="10b96-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10b96-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="10b96-111">Methods</span></span>

<span data-ttu-id="10b96-112">La classe **MSVM \_ MigrationJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="10b96-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="10b96-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="10b96-113">Method</span></span>                                                             | <span data-ttu-id="10b96-114">Description</span><span class="sxs-lookup"><span data-stu-id="10b96-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10b96-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="10b96-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="10b96-116">Récupère l’objet d’erreur pour la tâche de migration, s’il en existe une.</span><span class="sxs-lookup"><span data-stu-id="10b96-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="10b96-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="10b96-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="10b96-118">Récupère les objets d’erreur pour la tâche de migration, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="10b96-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="10b96-119">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="10b96-119">**KillJob**</span></span>                                                        | <span data-ttu-id="10b96-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="10b96-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="10b96-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="10b96-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="10b96-122">Demande que l’état de la tâche de migration passe à l’état spécifié.</span><span class="sxs-lookup"><span data-stu-id="10b96-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10b96-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="10b96-123">Properties</span></span>

<span data-ttu-id="10b96-124">La classe **MSVM \_ MigrationJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="10b96-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10b96-125">**Annulable**</span><span class="sxs-lookup"><span data-stu-id="10b96-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="10b96-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-128">Indique si le travail peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="10b96-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="10b96-129">La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.</span><span class="sxs-lookup"><span data-stu-id="10b96-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="10b96-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-133">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="10b96-133">A short description of the object.</span></span> <span data-ttu-id="10b96-134">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-135">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="10b96-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-136">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-138">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="10b96-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="10b96-139">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="10b96-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="10b96-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-141">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="10b96-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="10b96-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-144">Spécifie si le travail doit être automatiquement supprimé à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="10b96-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="10b96-145">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="10b96-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-149">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="10b96-149">A description of the object.</span></span> <span data-ttu-id="10b96-150">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-151">**DestinationHost**</span><span class="sxs-lookup"><span data-stu-id="10b96-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-154">Nom d’hôte de la plateforme de virtualisation de destination vers laquelle le système virtuel migre.</span><span class="sxs-lookup"><span data-stu-id="10b96-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="10b96-155">Il s’agit d’une **valeur null** pour la migration du stockage.</span><span class="sxs-lookup"><span data-stu-id="10b96-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="10b96-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-159">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="10b96-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="10b96-160">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="10b96-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="10b96-161">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-163">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-165">Intervalle de temps pendant lequel le travail s’est exécuté, ou durée totale d’exécution si le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="10b96-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="10b96-166">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="10b96-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-170">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="10b96-170">A display name for the object.</span></span> <span data-ttu-id="10b96-171">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="10b96-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-173">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-175">Code d’erreur spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="10b96-175">A vendor-specific error code.</span></span> <span data-ttu-id="10b96-176">La valeur doit être égale à zéro si le travail s’est terminé sans erreur.</span><span class="sxs-lookup"><span data-stu-id="10b96-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="10b96-177">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="10b96-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-181">Chaîne qui contient la description de l’erreur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="10b96-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="10b96-182">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="10b96-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10b96-186">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="10b96-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="10b96-187">Description résumée de l’erreur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="10b96-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="10b96-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-189">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-191">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="10b96-191">The current health of the element.</span></span> <span data-ttu-id="10b96-192">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="10b96-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="10b96-193">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="10b96-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="10b96-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="10b96-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10b96-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-196">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-198">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="10b96-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="10b96-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="10b96-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10b96-203">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="10b96-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="10b96-204">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="10b96-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="10b96-205">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="10b96-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-206">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="10b96-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10b96-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-209">Nombre de fois où la tâche doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="10b96-209">The number of times that the job should be run.</span></span> <span data-ttu-id="10b96-210">La valeur 1 indique que le travail n’est pas récurrent, tandis que toute valeur différente de zéro indique une limite au nombre de fois où le travail se reproduira.</span><span class="sxs-lookup"><span data-stu-id="10b96-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="10b96-211">La valeur zéro indique qu’il n’y a pas de limite au nombre de fois où le travail peut être traité, mais qu’il se termine une fois que le **UntilTime** a été atteint ou lorsque le travail est arrêté manuellement.</span><span class="sxs-lookup"><span data-stu-id="10b96-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="10b96-212">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="10b96-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-214">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-216">**JobState** est une énumération entière qui indique l’état opérationnel d’un travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="10b96-217">Il peut également indiquer des transitions entre ces États, par exemple « arrêt » et « démarrage ».</span><span class="sxs-lookup"><span data-stu-id="10b96-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="10b96-218">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="10b96-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="10b96-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b96-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="10b96-220">Signification</span><span class="sxs-lookup"><span data-stu-id="10b96-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="10b96-221"><dt>**Nouveau**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="10b96-222">Le travail n’a jamais été démarré.</span><span class="sxs-lookup"><span data-stu-id="10b96-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="10b96-223">À <dt>**partir**</dt> du <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="10b96-224">Le travail passe des États 2 (nouveau), 5 (suspendu) ou 11 (service) à l’État 4 (en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="10b96-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="10b96-225"><dt>**En cours d’exécution**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="10b96-226">La tâche est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="10b96-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="10b96-227"><dt>**Suspendu**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="10b96-228">La tâche est arrêtée, mais elle peut être redémarrée de manière transparente.</span><span class="sxs-lookup"><span data-stu-id="10b96-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="10b96-229"><dt>**Arrêt**</dt> de <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="10b96-230">Le travail passe à un État 7 (terminé), 8 (terminé) ou 9 (abattu).</span><span class="sxs-lookup"><span data-stu-id="10b96-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="10b96-231"><dt>**Terminé**</dt> le <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="10b96-232">Le travail s’est terminé normalement.</span><span class="sxs-lookup"><span data-stu-id="10b96-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="10b96-233"><dt>**Terminé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="10b96-234">La tâche a été arrêtée par une demande de modification d’État « Terminate ».</span><span class="sxs-lookup"><span data-stu-id="10b96-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="10b96-235">Le travail et tous ses processus sous-jacents sont terminés et peuvent être redémarrés uniquement en tant que nouveau travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="10b96-236">L’exigence de redémarrage du travail uniquement en tant que nouveau travail est spécifique à un travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="10b96-237"><dt>**Abattu**</dt> le <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="10b96-238">La tâche a été arrêtée par une demande de modification d’État « Kill ».</span><span class="sxs-lookup"><span data-stu-id="10b96-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="10b96-239">Les processus sous-jacents peuvent toujours être en cours d’exécution et un nettoyage peut être nécessaire pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="10b96-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="10b96-240"><dt>**Exception**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="10b96-241">La tâche est dans un état anormal qui peut indiquer une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="10b96-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="10b96-242">L’état réel du travail peut être disponible par le biais d’objets spécifiques à un travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="10b96-243"><dt>**Service**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="10b96-244">La tâche est dans un état spécifique au fournisseur qui prend en charge la découverte de problèmes, la résolution, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="10b96-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="10b96-245"><dt>**DMTF réservé**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="10b96-246">Réservé.</span><span class="sxs-lookup"><span data-stu-id="10b96-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="10b96-247"><dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="10b96-248">Réservé.</span><span class="sxs-lookup"><span data-stu-id="10b96-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="10b96-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="10b96-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-252">Chaîne qui représente l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="10b96-252">A string that represents the job status.</span></span> <span data-ttu-id="10b96-253">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="10b96-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-255">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-257">Indique le type de travail faisant l’objet d’un suivi par cet objet.</span><span class="sxs-lookup"><span data-stu-id="10b96-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10b96-258">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="10b96-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="10b96-259">**Création d’une machine virtuelle distante** (300)</span><span class="sxs-lookup"><span data-stu-id="10b96-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="10b96-260">**Vérification de la compatibilité des machines virtuelles** (301)</span><span class="sxs-lookup"><span data-stu-id="10b96-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="10b96-261">**Vérification de la compatibilité des ordinateurs virtuels et du stockage** (302)</span><span class="sxs-lookup"><span data-stu-id="10b96-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="10b96-262">**Vérification** de la compatibilité du stockage (303)</span><span class="sxs-lookup"><span data-stu-id="10b96-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="10b96-263">**Vérification** de la migration du stockage (304)</span><span class="sxs-lookup"><span data-stu-id="10b96-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="10b96-264">**Déplacement de la machine virtuelle** (305)</span><span class="sxs-lookup"><span data-stu-id="10b96-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="10b96-265">**Déplacement de l’ordinateur virtuel et du stockage** (306)</span><span class="sxs-lookup"><span data-stu-id="10b96-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="10b96-266">**Déplacement du stockage** (307)</span><span class="sxs-lookup"><span data-stu-id="10b96-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10b96-267">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-268">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-270">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="10b96-271">Indique si les heures représentées dans les propriétés **RunStartInterval** et **UntilTime** représentent des heures locales ou des heures UTC.</span><span class="sxs-lookup"><span data-stu-id="10b96-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="10b96-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Heure locale** (1)</span><span class="sxs-lookup"><span data-stu-id="10b96-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Heure UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="10b96-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10b96-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="10b96-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-275">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10b96-277">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span><span class="sxs-lookup"><span data-stu-id="10b96-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="10b96-278">Type de migration représenté par cet objet de traitement.</span><span class="sxs-lookup"><span data-stu-id="10b96-278">The migration type represented by this job object.</span></span> <span data-ttu-id="10b96-279">Il s’agira de l’une des valeurs définies pour la propriété **MigrationType** de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="10b96-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-280">**Nom**</span><span class="sxs-lookup"><span data-stu-id="10b96-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10b96-283">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="10b96-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="10b96-284">Nom complet de cette instance d’un travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-284">The display name for this instance of a job.</span></span> <span data-ttu-id="10b96-285">En outre, le nom complet peut être utilisé en tant que propriété pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="10b96-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="10b96-286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-287">**NewResourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="10b96-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-288">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="10b96-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10b96-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-290">Pour une migration dynamique, elle est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="10b96-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="10b96-291">Pour une migration de stockage, si la **valeur est null**, aucun disque dur virtuel (VHD) de la machine virtuelle ne sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="10b96-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="10b96-292">Sinon, elle contient un tableau d’instances incorporées de la classe [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) qui représentent les disques durs virtuels à déplacer.</span><span class="sxs-lookup"><span data-stu-id="10b96-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="10b96-293">La propriété de **connexion** de ces instances spécifie l’emplacement de destination du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="10b96-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-294">**NewSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="10b96-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-297">Pour une migration dynamique, elle est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="10b96-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="10b96-298">Pour une migration de stockage, si la **valeur est null**, les racines de données de l’ordinateur virtuel ne sont pas déplacées.</span><span class="sxs-lookup"><span data-stu-id="10b96-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="10b96-299">Sinon, elle contient une instance incorporée de la [**classe MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , où les propriétés **ExternalDataRoot**, **SnapshotDataRoot** et **SwapFileDataRoot** spécifient les nouvelles racines de données.</span><span class="sxs-lookup"><span data-stu-id="10b96-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-300">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="10b96-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-303">Utilisateur qui est averti en cas d’achèvement ou d’échec d’un travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="10b96-304">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-305">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="10b96-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-306">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-308">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="10b96-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="10b96-309">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="10b96-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="10b96-310">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="10b96-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-312">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10b96-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-314">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="10b96-314">The current statuses of the object.</span></span> <span data-ttu-id="10b96-315">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="10b96-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-316">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="10b96-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-319">Chaîne qui décrit l’action de récupération lorsque la propriété **RecoveryAction** de l’instance a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="10b96-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="10b96-320">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-321">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="10b96-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-324">Utilisateur qui a envoyé le travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-324">The user who submitted the job.</span></span> <span data-ttu-id="10b96-325">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="10b96-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-327">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10b96-329">Qualificateurs : **MinValue** (0), **MaxValue** (100), **unités** (« percent »)</span><span class="sxs-lookup"><span data-stu-id="10b96-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="10b96-330">Pourcentage d’achèvement du travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-330">The completion percentage of the job.</span></span> <span data-ttu-id="10b96-331">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-332">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="10b96-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-333">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-335">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="10b96-335">Provides high level status information.</span></span> <span data-ttu-id="10b96-336">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="10b96-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="10b96-337">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="10b96-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="10b96-338">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="10b96-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-339">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="10b96-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-340">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10b96-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-342">Importance de l’exécution d’un travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-342">The importance of a job's execution.</span></span> <span data-ttu-id="10b96-343">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-344">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="10b96-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-345">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10b96-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-347">Décrit l’action de récupération à entreprendre pour un travail qui n’a pas réussi à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="10b96-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="10b96-348">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="10b96-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="10b96-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="10b96-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Ne pas continuer** (2)</span><span class="sxs-lookup"><span data-stu-id="10b96-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuer avec la tâche suivante** (3)</span><span class="sxs-lookup"><span data-stu-id="10b96-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Travail de réexécution** (4)</span><span class="sxs-lookup"><span data-stu-id="10b96-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Exécuter la tâche de récupération** (5)</span><span class="sxs-lookup"><span data-stu-id="10b96-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10b96-355">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="10b96-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-356">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="10b96-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10b96-358">Qualificateurs : **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="10b96-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="10b96-359">Jour du mois sur lequel le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="10b96-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="10b96-360">Il existe différentes interprétations pour cette propriété, en fonction de la valeur de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="10b96-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="10b96-361">Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est positif, **RunDay** définit le jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="10b96-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="10b96-362">Par exemple, si **RunDayOfWeek** est égal à 0 et que **RunDay** est égal à 12, la tâche est traitée le 12 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="10b96-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="10b96-363">Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est négatif, **RunDay** définit le nombre de jours avant le dernier jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="10b96-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="10b96-364">1 indique le dernier jour du mois, 2 indique un jour avant le dernier jour du mois, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="10b96-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="10b96-365">Par exemple, si **RunDayOfWeek** est égal à 0 et **RunDay** la valeur 1, la tâche est traitée le dernier jour du mois.</span><span class="sxs-lookup"><span data-stu-id="10b96-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="10b96-366">Quand **RunDayOfWeek** n’est pas égal à 0, **RunDayOfWeek** est le jour de la semaine où le travail sera traité, par rapport à **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="10b96-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="10b96-367">Par exemple, si **RunDay** est 15 et **RunDayOfWeek** est 7 (+ samedi), le travail sera traité le premier samedi, le ou après le 15 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="10b96-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="10b96-368">Si **RunDay** est 20 et **RunDayOfWeek** est 7 (samedi), la tâche est traitée le premier samedi le ou avant le 20 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="10b96-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="10b96-369">Si **RunDay** est 1 et que **RunDayOfWeek** est 1 (dimanche), la tâche est traitée le dernier dimanche du mois.</span><span class="sxs-lookup"><span data-stu-id="10b96-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="10b96-370">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-371">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="10b96-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-372">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="10b96-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-374">Entier positif ou négatif utilisé conjointement avec **RunDay** pour indiquer le jour de la semaine ou du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="10b96-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="10b96-375">Pour plus d’informations, consultez la description de la propriété **RunDay** .</span><span class="sxs-lookup"><span data-stu-id="10b96-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="10b96-376">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="10b96-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="10b96-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="10b96-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="10b96-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="10b96-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="10b96-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="10b96-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="10b96-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="10b96-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="10b96-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="10b96-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="10b96-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="10b96-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="10b96-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="10b96-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="10b96-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10b96-392">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="10b96-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-393">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="10b96-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-395">Mois pendant lequel le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="10b96-395">The month during which the job should be processed.</span></span> <span data-ttu-id="10b96-396">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="10b96-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janvier** (0)</span><span class="sxs-lookup"><span data-stu-id="10b96-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Février** (1)</span><span class="sxs-lookup"><span data-stu-id="10b96-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Mars** (2)</span><span class="sxs-lookup"><span data-stu-id="10b96-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Avril** (3)</span><span class="sxs-lookup"><span data-stu-id="10b96-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="10b96-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juin** (5)</span><span class="sxs-lookup"><span data-stu-id="10b96-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Juillet** (6)</span><span class="sxs-lookup"><span data-stu-id="10b96-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Août** (7)</span><span class="sxs-lookup"><span data-stu-id="10b96-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septembre** (8)</span><span class="sxs-lookup"><span data-stu-id="10b96-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octobre** (9)</span><span class="sxs-lookup"><span data-stu-id="10b96-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="10b96-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="10b96-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Décembre** (11)</span><span class="sxs-lookup"><span data-stu-id="10b96-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10b96-409">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="10b96-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-410">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-412">Intervalle de temps après minuit lorsque le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="10b96-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="10b96-413">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-414">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-415">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-417">Heure de début planifiée pour le travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="10b96-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="10b96-418">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-420">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-422">Heure de début de la tâche.</span><span class="sxs-lookup"><span data-stu-id="10b96-422">The time that the job began.</span></span> <span data-ttu-id="10b96-423">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-424">**État**</span><span class="sxs-lookup"><span data-stu-id="10b96-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-425">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-427">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="10b96-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-428">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="10b96-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-429">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="10b96-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10b96-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-431">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="10b96-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="10b96-432">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="10b96-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="10b96-433">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="10b96-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-434">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-436">Durée, en minutes, pendant laquelle le travail est conservé une fois qu’il a fini de s’exécuter, soit à l’issue ou à l’échec de cette exécution.</span><span class="sxs-lookup"><span data-stu-id="10b96-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="10b96-437">Le travail doit rester en présence pendant un certain temps, quelle que soit la valeur de la propriété **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="10b96-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="10b96-438">La valeur par défaut est cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="10b96-438">The default is five minutes.</span></span> <span data-ttu-id="10b96-439">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85))et est toujours définie sur 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="10b96-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="10b96-440">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="10b96-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-441">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-443">Date ou heure de la dernière modification de l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="10b96-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="10b96-444">Si l’état de la tâche n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="10b96-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="10b96-445">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="10b96-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="10b96-446">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="10b96-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-447">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="10b96-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-448">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-450">Heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="10b96-450">The time that the job was submitted.</span></span> <span data-ttu-id="10b96-451">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-452">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-453">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10b96-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-455">Heure à laquelle le travail n’est pas valide ou doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="10b96-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="10b96-456">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="10b96-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="10b96-457">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="10b96-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10b96-458">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10b96-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10b96-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10b96-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10b96-460">Nom unique du système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="10b96-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10b96-461">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10b96-461">Requirements</span></span>



| <span data-ttu-id="10b96-462">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10b96-462">Requirement</span></span> | <span data-ttu-id="10b96-463">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b96-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b96-464">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10b96-464">Minimum supported client</span></span><br/> | <span data-ttu-id="10b96-465">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10b96-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="10b96-466">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10b96-466">Minimum supported server</span></span><br/> | <span data-ttu-id="10b96-467">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10b96-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10b96-468">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="10b96-468">Namespace</span></span><br/>                | <span data-ttu-id="10b96-469">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="10b96-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="10b96-470">MOF</span><span class="sxs-lookup"><span data-stu-id="10b96-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10b96-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10b96-472">DLL</span><span class="sxs-lookup"><span data-stu-id="10b96-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10b96-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10b96-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

