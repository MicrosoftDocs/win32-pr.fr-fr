---
description: Représente une unité de travail et est utilisé pour suivre la progression des opérations asynchrones.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529289"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="c1da3-103">MSVM \_ ConcreteJob, classe</span><span class="sxs-lookup"><span data-stu-id="c1da3-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="c1da3-104">Version concrète du travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-104">A concrete version of job.</span></span> <span data-ttu-id="c1da3-105">Cette classe représente une unité de travail générique et instantiatable, telle qu’un traitement par lots ou un travail d’impression, et est spécifiquement utilisée dans Hyper-V pour suivre la progression des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="c1da3-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="c1da3-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c1da3-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1da3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1da3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="c1da3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c1da3-108">Members</span></span>

<span data-ttu-id="c1da3-109">La classe **MSVM \_ ConcreteJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c1da3-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="c1da3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1da3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1da3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c1da3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1da3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1da3-112">Methods</span></span>

<span data-ttu-id="c1da3-113">La classe **MSVM \_ ConcreteJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c1da3-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="c1da3-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="c1da3-114">Method</span></span>                                                            | <span data-ttu-id="c1da3-115">Description</span><span class="sxs-lookup"><span data-stu-id="c1da3-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="c1da3-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="c1da3-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="c1da3-117">Récupère l’objet d’erreur pour le travail, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="c1da3-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="c1da3-118">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="c1da3-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="c1da3-119">Récupère les objets d’erreur pour le travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c1da3-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="c1da3-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="c1da3-120">**KillJob**</span></span>                                                       | <span data-ttu-id="c1da3-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c1da3-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="c1da3-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c1da3-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="c1da3-123">Demande que l’état du travail passe à l’état spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1da3-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c1da3-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c1da3-124">Properties</span></span>

<span data-ttu-id="c1da3-125">La classe **MSVM \_ ConcreteJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1da3-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1da3-126">**Annulable**</span><span class="sxs-lookup"><span data-stu-id="c1da3-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c1da3-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-129">Indique si le travail peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="c1da3-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="c1da3-130">La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.</span><span class="sxs-lookup"><span data-stu-id="c1da3-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c1da3-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-134">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c1da3-134">A short description of the object.</span></span> <span data-ttu-id="c1da3-135">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c1da3-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-139">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c1da3-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c1da3-140">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c1da3-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c1da3-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-142">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="c1da3-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c1da3-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-145">Spécifie si le travail doit être automatiquement supprimé à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c1da3-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="c1da3-146">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-147">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1da3-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-150">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="c1da3-150">A description of the object.</span></span> <span data-ttu-id="c1da3-151">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c1da3-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-155">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c1da3-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c1da3-156">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c1da3-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c1da3-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-158">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-159">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-161">Intervalle de temps pendant lequel le travail s’est exécuté, ou durée totale d’exécution si le travail est terminé.</span><span class="sxs-lookup"><span data-stu-id="c1da3-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="c1da3-162">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c1da3-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-166">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c1da3-166">A display name for the object.</span></span> <span data-ttu-id="c1da3-167">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c1da3-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-169">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-171">Code d’erreur spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c1da3-171">A vendor-specific error code.</span></span> <span data-ttu-id="c1da3-172">La valeur doit être égale à zéro si le travail s’est terminé sans erreur.</span><span class="sxs-lookup"><span data-stu-id="c1da3-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="c1da3-173">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c1da3-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-177">Chaîne qui contient la description de l’erreur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c1da3-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="c1da3-178">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="c1da3-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-182">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="c1da3-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-183">Description résumée de l’erreur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c1da3-183">A summary description of the error, if present.</span></span> <span data-ttu-id="c1da3-184">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c1da3-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-186">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-188">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c1da3-188">The current health of the element.</span></span> <span data-ttu-id="c1da3-189">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="c1da3-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c1da3-190">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="c1da3-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c1da3-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="c1da3-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c1da3-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-193">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-195">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c1da3-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c1da3-196">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1da3-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-200">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="c1da3-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-201">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c1da3-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c1da3-202">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c1da3-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-203">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="c1da3-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-204">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1da3-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-206">Nombre de fois où la tâche doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="c1da3-206">The number of times that the job should be run.</span></span> <span data-ttu-id="c1da3-207">La valeur 1 indique que le travail n’est pas récurrent, tandis que toute valeur différente de zéro indique une limite au nombre de fois où le travail se reproduira.</span><span class="sxs-lookup"><span data-stu-id="c1da3-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="c1da3-208">La valeur zéro indique qu’il n’y a pas de limite au nombre de fois où le travail peut être traité, mais qu’il se termine une fois que le **UntilTime** a été atteint ou lorsque le travail est arrêté manuellement.</span><span class="sxs-lookup"><span data-stu-id="c1da3-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="c1da3-209">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="c1da3-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-213">**JobState** est une énumération entière qui indique l’état opérationnel d’un travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="c1da3-214">Il peut également indiquer des transitions entre ces États, par exemple « arrêt » et « démarrage ».</span><span class="sxs-lookup"><span data-stu-id="c1da3-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="c1da3-215">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1da3-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="c1da3-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1da3-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="c1da3-217">Signification</span><span class="sxs-lookup"><span data-stu-id="c1da3-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="c1da3-218"><dt>**Nouveau**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="c1da3-219">Le travail n’a jamais été démarré.</span><span class="sxs-lookup"><span data-stu-id="c1da3-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="c1da3-220">À <dt>**partir**</dt> du <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="c1da3-221">Le travail passe des États 2 (nouveau), 5 (suspendu) ou 11 (service) à l’État 4 (en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="c1da3-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="c1da3-222"><dt>**En cours d’exécution**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="c1da3-223">La tâche est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="c1da3-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="c1da3-224"><dt>**Suspendu**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="c1da3-225">La tâche est arrêtée, mais elle peut être redémarrée de manière transparente.</span><span class="sxs-lookup"><span data-stu-id="c1da3-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="c1da3-226"><dt>**Arrêt**</dt> de <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="c1da3-227">Le travail passe à un État 7 (terminé), 8 (terminé) ou 9 (abattu).</span><span class="sxs-lookup"><span data-stu-id="c1da3-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="c1da3-228"><dt>**Terminé**</dt> le <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="c1da3-229">Le travail s’est terminé normalement.</span><span class="sxs-lookup"><span data-stu-id="c1da3-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="c1da3-230"><dt>**Terminé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="c1da3-231">La tâche a été arrêtée par une demande de modification d’État « Terminate ».</span><span class="sxs-lookup"><span data-stu-id="c1da3-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="c1da3-232">Le travail et tous ses processus sous-jacents sont terminés et peuvent être redémarrés uniquement en tant que nouveau travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="c1da3-233">L’exigence de redémarrage du travail uniquement en cas de nouveau travail est spécifique à un travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="c1da3-234"><dt>**Abattu**</dt> le <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="c1da3-235">La tâche a été arrêtée par une demande de modification d’État « Kill ».</span><span class="sxs-lookup"><span data-stu-id="c1da3-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="c1da3-236">Les processus sous-jacents peuvent toujours être en cours d’exécution et un nettoyage peut être nécessaire pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="c1da3-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="c1da3-237"><dt>**Exception**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="c1da3-238">La tâche est dans un état anormal qui peut indiquer une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c1da3-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="c1da3-239">L’état réel du travail peut être disponible par le biais d’objets spécifiques à un travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="c1da3-240"><dt>**Service**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="c1da3-241">La tâche est dans un état spécifique au fournisseur qui prend en charge la découverte de problèmes, la résolution, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="c1da3-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c1da3-242"><dt>**DMTF réservé**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="c1da3-243">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c1da3-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="c1da3-244"><dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="c1da3-245">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c1da3-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="c1da3-246">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="c1da3-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-249">Chaîne qui représente l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c1da3-249">A string that represents the job status.</span></span> <span data-ttu-id="c1da3-250">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="c1da3-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-252">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-254">Indique le type de travail faisant l’objet d’un suivi par cet objet.</span><span class="sxs-lookup"><span data-stu-id="c1da3-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c1da3-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c1da3-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Définir la machine virtuelle** (1)</span><span class="sxs-lookup"><span data-stu-id="c1da3-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modifier la machine virtuelle** (2)</span><span class="sxs-lookup"><span data-stu-id="c1da3-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Détruire l’ordinateur virtuel** (3)</span><span class="sxs-lookup"><span data-stu-id="c1da3-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="c1da3-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modifier les paramètres du service de gestion** (4)</span><span class="sxs-lookup"><span data-stu-id="c1da3-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialiser la machine virtuelle** (10)</span><span class="sxs-lookup"><span data-stu-id="c1da3-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**En attente de démarrage de la machine virtuelle** (11)</span><span class="sxs-lookup"><span data-stu-id="c1da3-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Démarrer la machine virtuelle** (12)</span><span class="sxs-lookup"><span data-stu-id="c1da3-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Mettre hors tension la machine virtuelle** (13)</span><span class="sxs-lookup"><span data-stu-id="c1da3-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Enregistrer l’ordinateur virtuel** (14)</span><span class="sxs-lookup"><span data-stu-id="c1da3-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restaurer la machine virtuelle** (15)</span><span class="sxs-lookup"><span data-stu-id="c1da3-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Arrêter la machine virtuelle** (16)</span><span class="sxs-lookup"><span data-stu-id="c1da3-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Suspendre la machine virtuelle** (26)</span><span class="sxs-lookup"><span data-stu-id="c1da3-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Reprendre la machine virtuelle** (27)</span><span class="sxs-lookup"><span data-stu-id="c1da3-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Réinitialiser l’ordinateur virtuel** (28)</span><span class="sxs-lookup"><span data-stu-id="c1da3-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Redémarrer la machine virtuelle** (29)</span><span class="sxs-lookup"><span data-stu-id="c1da3-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="c1da3-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Ajouter des ressources de machine virtuelle** (30)</span><span class="sxs-lookup"><span data-stu-id="c1da3-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="c1da3-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modifier les ressources des machines virtuelles** (31)</span><span class="sxs-lookup"><span data-stu-id="c1da3-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="c1da3-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Supprimer des ressources de machine virtuelle** (32)</span><span class="sxs-lookup"><span data-stu-id="c1da3-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="c1da3-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Demander la mémoire initiale de l’ordinateur virtuel** (40)</span><span class="sxs-lookup"><span data-stu-id="c1da3-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Ajouter de la mémoire à la machine virtuelle** (41)</span><span class="sxs-lookup"><span data-stu-id="c1da3-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Supprimer la mémoire de l’ordinateur virtuel** (42)</span><span class="sxs-lookup"><span data-stu-id="c1da3-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="c1da3-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Fusion de disques VHD** (50)</span><span class="sxs-lookup"><span data-stu-id="c1da3-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Créer un instantané VSS à l’intérieur d’une machine virtuelle** (51)</span><span class="sxs-lookup"><span data-stu-id="c1da3-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="c1da3-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Obtient les données des paramètres d’importation** (60)</span><span class="sxs-lookup"><span data-stu-id="c1da3-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Importer l’ordinateur virtuel** (61)</span><span class="sxs-lookup"><span data-stu-id="c1da3-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Exporter l’ordinateur virtuel** (62)</span><span class="sxs-lookup"><span data-stu-id="c1da3-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="c1da3-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Inscrire la configuration** (63)</span><span class="sxs-lookup"><span data-stu-id="c1da3-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="c1da3-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Annuler l’inscription** de la Configuration (64)</span><span class="sxs-lookup"><span data-stu-id="c1da3-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Machine virtuelle d’instantané** (70)</span><span class="sxs-lookup"><span data-stu-id="c1da3-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="c1da3-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Appliquer la capture instantanée d’ordinateur virtuel** (71)</span><span class="sxs-lookup"><span data-stu-id="c1da3-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="c1da3-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Supprimer la capture instantanée d’ordinateur virtuel** (72)</span><span class="sxs-lookup"><span data-stu-id="c1da3-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="c1da3-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>Effacer l’état de l’instantané de l' **ordinateur virtuel** (73)</span><span class="sxs-lookup"><span data-stu-id="c1da3-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="c1da3-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Ajouter des ressources à un pool de ressources** (80)</span><span class="sxs-lookup"><span data-stu-id="c1da3-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="c1da3-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Supprimer des ressources d’un pool de ressources** (81)</span><span class="sxs-lookup"><span data-stu-id="c1da3-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="c1da3-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modifier les paramètres du serveur de réplication** (90)</span><span class="sxs-lookup"><span data-stu-id="c1da3-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="c1da3-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Créer une relation de réplication** (91)</span><span class="sxs-lookup"><span data-stu-id="c1da3-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="c1da3-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modifier les paramètres de relation de réplication** (92)</span><span class="sxs-lookup"><span data-stu-id="c1da3-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="c1da3-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Supprimer la relation de réplication** (93)</span><span class="sxs-lookup"><span data-stu-id="c1da3-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="c1da3-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Démarrer la réplication initiale en bande** (94)</span><span class="sxs-lookup"><span data-stu-id="c1da3-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="c1da3-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Importation de réplication** (95)</span><span class="sxs-lookup"><span data-stu-id="c1da3-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="c1da3-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Modifier l’état de la réplication** (96)</span><span class="sxs-lookup"><span data-stu-id="c1da3-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="c1da3-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Lancer le basculement** (97)</span><span class="sxs-lookup"><span data-stu-id="c1da3-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="c1da3-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Rétablir le basculement** (98)</span><span class="sxs-lookup"><span data-stu-id="c1da3-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="c1da3-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Valider le basculement** (99)</span><span class="sxs-lookup"><span data-stu-id="c1da3-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="c1da3-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Réplication synchronisée Inititate** (100)</span><span class="sxs-lookup"><span data-stu-id="c1da3-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="c1da3-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Annuler la réplication synchronisée** (101)</span><span class="sxs-lookup"><span data-stu-id="c1da3-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="c1da3-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initier un réplica de test** (102)</span><span class="sxs-lookup"><span data-stu-id="c1da3-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="c1da3-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Supprimer le réplica de test** (103)</span><span class="sxs-lookup"><span data-stu-id="c1da3-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="c1da3-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Réplication inverse** (104)</span><span class="sxs-lookup"><span data-stu-id="c1da3-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="c1da3-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Delta d’envoi de réplication** (105)</span><span class="sxs-lookup"><span data-stu-id="c1da3-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="c1da3-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Delta de réception de réplication** (106)</span><span class="sxs-lookup"><span data-stu-id="c1da3-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="c1da3-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronisation** (107)</span><span class="sxs-lookup"><span data-stu-id="c1da3-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="c1da3-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Appliquer le journal des modifications** (108)</span><span class="sxs-lookup"><span data-stu-id="c1da3-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="c1da3-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Arrêter la réplication initiale** (109)</span><span class="sxs-lookup"><span data-stu-id="c1da3-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="c1da3-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Arrêter la resynchronisation** (110)</span><span class="sxs-lookup"><span data-stu-id="c1da3-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="c1da3-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Obtient les statistiques des réplicas** (111)</span><span class="sxs-lookup"><span data-stu-id="c1da3-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="c1da3-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Préparer le vérificateur de cohérence** (112)</span><span class="sxs-lookup"><span data-stu-id="c1da3-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="c1da3-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Vérificateur de cohérence** (113)</span><span class="sxs-lookup"><span data-stu-id="c1da3-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="c1da3-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Arrêter le vérificateur de cohérence** (114)</span><span class="sxs-lookup"><span data-stu-id="c1da3-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="c1da3-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Tester la connexion de réplication** (115)</span><span class="sxs-lookup"><span data-stu-id="c1da3-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="c1da3-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Envoi du réplica initial** (116)</span><span class="sxs-lookup"><span data-stu-id="c1da3-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="c1da3-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Démarrer la réplication initiale de resynchronisation** (117)</span><span class="sxs-lookup"><span data-stu-id="c1da3-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="c1da3-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Démarrer l’exportation de la réplication initiale** (118)</span><span class="sxs-lookup"><span data-stu-id="c1da3-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="c1da3-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Réinitialiser les statistiques des réplicas** (119)</span><span class="sxs-lookup"><span data-stu-id="c1da3-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="c1da3-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Appliquer des deltas enregistrés** (120)</span><span class="sxs-lookup"><span data-stu-id="c1da3-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="c1da3-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronisation de la réplication étendue** (121)</span><span class="sxs-lookup"><span data-stu-id="c1da3-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="c1da3-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Lecture** de la configuration du réplica de Test (122)</span><span class="sxs-lookup"><span data-stu-id="c1da3-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="c1da3-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Changer le mode de réplication en principal** (123)</span><span class="sxs-lookup"><span data-stu-id="c1da3-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="c1da3-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Lancer la restauration automatique** (124)</span><span class="sxs-lookup"><span data-stu-id="c1da3-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="c1da3-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Mettre à jour le jeu de disques** (125)</span><span class="sxs-lookup"><span data-stu-id="c1da3-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-326">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="c1da3-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Définir le commutateur Ethernet** (130)</span><span class="sxs-lookup"><span data-stu-id="c1da3-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="c1da3-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modifier les paramètres du commutateur Ethernet** (131)</span><span class="sxs-lookup"><span data-stu-id="c1da3-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="c1da3-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Détruire le commutateur Ethernet** (132)</span><span class="sxs-lookup"><span data-stu-id="c1da3-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="c1da3-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Ajouter des ressources de commutateur Ethernet** (133)</span><span class="sxs-lookup"><span data-stu-id="c1da3-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="c1da3-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modifier les ressources de commutateur Ethernet** (134)</span><span class="sxs-lookup"><span data-stu-id="c1da3-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="c1da3-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Supprimer des ressources de commutateur Ethernet** (135)</span><span class="sxs-lookup"><span data-stu-id="c1da3-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Valider l’ordinateur virtuel planifié** (140)</span><span class="sxs-lookup"><span data-stu-id="c1da3-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Réalisation d’une machine virtuelle** (141)</span><span class="sxs-lookup"><span data-stu-id="c1da3-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="c1da3-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Création d’un pool de ressources** (150)</span><span class="sxs-lookup"><span data-stu-id="c1da3-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="c1da3-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Modification des ressources parentes d’un pool de ressources** (151)</span><span class="sxs-lookup"><span data-stu-id="c1da3-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="c1da3-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Modification des paramètres non Alloction d’un pool de ressources** (152)</span><span class="sxs-lookup"><span data-stu-id="c1da3-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="c1da3-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Suppression d’un pool de ressources** (153)</span><span class="sxs-lookup"><span data-stu-id="c1da3-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="c1da3-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Activer REMOTEFX GPU** (160)</span><span class="sxs-lookup"><span data-stu-id="c1da3-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="c1da3-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Désactiver REMOTEFX GPU** (161)</span><span class="sxs-lookup"><span data-stu-id="c1da3-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="c1da3-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modifier les paramètres du service 3D** (162)</span><span class="sxs-lookup"><span data-stu-id="c1da3-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-342">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="c1da3-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Sauvegarder l’ordinateur virtuel** (170)</span><span class="sxs-lookup"><span data-stu-id="c1da3-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="c1da3-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Interface de service invité** (180)</span><span class="sxs-lookup"><span data-stu-id="c1da3-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-345">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="c1da3-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Interroger les informations du cluster invité** (181)</span><span class="sxs-lookup"><span data-stu-id="c1da3-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-347">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="c1da3-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Définir la collection** (190)</span><span class="sxs-lookup"><span data-stu-id="c1da3-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-349">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="c1da3-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Détruire la collection** (191)</span><span class="sxs-lookup"><span data-stu-id="c1da3-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-351">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="c1da3-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Renommer la collection** (192)</span><span class="sxs-lookup"><span data-stu-id="c1da3-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-353">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="c1da3-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Ajouter un membre à la collection** (193)</span><span class="sxs-lookup"><span data-stu-id="c1da3-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-355">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="c1da3-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Supprimer un membre d’une collection** (194)</span><span class="sxs-lookup"><span data-stu-id="c1da3-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-357">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="c1da3-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Ajouter un paramètre au regroupement** (195)</span><span class="sxs-lookup"><span data-stu-id="c1da3-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-359">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="c1da3-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Supprimer le paramètre de la collection** (196)</span><span class="sxs-lookup"><span data-stu-id="c1da3-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-361">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="c1da3-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modifier le paramètre du regroupement** (197)</span><span class="sxs-lookup"><span data-stu-id="c1da3-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-363">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="c1da3-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Collection d’instantanés** (198)</span><span class="sxs-lookup"><span data-stu-id="c1da3-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-365">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="c1da3-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convertir un instantané en point de référence** (200)</span><span class="sxs-lookup"><span data-stu-id="c1da3-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-367">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="c1da3-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Créer un point de référence** (201)</span><span class="sxs-lookup"><span data-stu-id="c1da3-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-369">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="c1da3-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Supprimer le point de référence** (202)</span><span class="sxs-lookup"><span data-stu-id="c1da3-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-371">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="c1da3-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Exporter le point de référence** (203)</span><span class="sxs-lookup"><span data-stu-id="c1da3-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-373">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="c1da3-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Supprimer les données associées du point de référence** (204)</span><span class="sxs-lookup"><span data-stu-id="c1da3-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-375">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="c1da3-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Créer un point de référence sur la collection** (205)</span><span class="sxs-lookup"><span data-stu-id="c1da3-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-377">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="c1da3-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Exporter le point de référence sur la collection** (206)</span><span class="sxs-lookup"><span data-stu-id="c1da3-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-379">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="c1da3-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Supprimer les données associées du point de référence sur la collection** (207)</span><span class="sxs-lookup"><span data-stu-id="c1da3-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-381">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="c1da3-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Supprimer le point de référence sur la collection** (208)</span><span class="sxs-lookup"><span data-stu-id="c1da3-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-383">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="c1da3-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Importer les métadonnées de point de référence** (209)</span><span class="sxs-lookup"><span data-stu-id="c1da3-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-385">Valeur ajoutée dans Windows 10 en tant que **point de référence de nettoyage**.</span><span class="sxs-lookup"><span data-stu-id="c1da3-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="c1da3-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Monter ou démonter un appareil attribuable** (260)</span><span class="sxs-lookup"><span data-stu-id="c1da3-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="c1da3-387">Valeur ajoutée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c1da3-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c1da3-388">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-389">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-391">Indique si les heures représentées dans les propriétés **RunStartInterval** et **UntilTime** représentent des heures locales ou des heures UTC.</span><span class="sxs-lookup"><span data-stu-id="c1da3-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="c1da3-392">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="c1da3-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Heure locale** (1)</span><span class="sxs-lookup"><span data-stu-id="c1da3-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Heure UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="c1da3-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1da3-395">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c1da3-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-396">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-398">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="c1da3-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-399">Nom complet de cette instance d’un travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-399">The display name for this instance of a job.</span></span> <span data-ttu-id="c1da3-400">En outre, le nom complet peut être utilisé en tant que propriété pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="c1da3-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="c1da3-401">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-402">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="c1da3-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-405">Utilisateur qui est averti en cas d’achèvement ou d’échec d’un travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="c1da3-406">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-407">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c1da3-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-408">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-410">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c1da3-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c1da3-411">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c1da3-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c1da3-412">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c1da3-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-414">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-416">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c1da3-416">The current statuses of the object.</span></span> <span data-ttu-id="c1da3-417">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="c1da3-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-418">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="c1da3-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-419">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-421">Chaîne qui décrit l’action de récupération lorsque la propriété **RecoveryAction** de l’instance a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="c1da3-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="c1da3-422">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-423">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="c1da3-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-426">Utilisateur qui a envoyé le travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-426">The user who submitted the job.</span></span> <span data-ttu-id="c1da3-427">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="c1da3-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-429">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-431">Qualificateurs : **MinValue** (0), **MaxValue** (100), **unités** (« percent »)</span><span class="sxs-lookup"><span data-stu-id="c1da3-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-432">Pourcentage d’achèvement du travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-432">The completion percentage of the job.</span></span> <span data-ttu-id="c1da3-433">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-434">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c1da3-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-435">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-437">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="c1da3-437">Provides high level status information.</span></span> <span data-ttu-id="c1da3-438">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="c1da3-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c1da3-439">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c1da3-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c1da3-440">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c1da3-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-441">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="c1da3-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-442">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1da3-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-444">Importance de l’exécution d’un travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-444">The importance of a job's execution.</span></span> <span data-ttu-id="c1da3-445">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-446">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="c1da3-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-447">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1da3-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-449">Décrit l’action de récupération à entreprendre pour un travail qui n’a pas été exécuté avec succès.</span><span class="sxs-lookup"><span data-stu-id="c1da3-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="c1da3-450">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="c1da3-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c1da3-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c1da3-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Ne pas continuer** (2)</span><span class="sxs-lookup"><span data-stu-id="c1da3-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuer avec la tâche suivante** (3)</span><span class="sxs-lookup"><span data-stu-id="c1da3-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Travail de réexécution** (4)</span><span class="sxs-lookup"><span data-stu-id="c1da3-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Exécuter la tâche de récupération** (5)</span><span class="sxs-lookup"><span data-stu-id="c1da3-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1da3-457">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="c1da3-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-458">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="c1da3-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-460">Qualificateurs : **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="c1da3-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-461">Jour du mois sur lequel le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="c1da3-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="c1da3-462">Il existe différentes interprétations pour cette propriété, en fonction de la valeur de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="c1da3-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="c1da3-463">Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est positif, **RunDay** définit le jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="c1da3-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="c1da3-464">Par exemple, si **RunDayOfWeek** est égal à 0 et que **RunDay** est égal à 12, la tâche est traitée le 12 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="c1da3-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="c1da3-465">Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est négatif, **RunDay** définit le nombre de jours avant le dernier jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="c1da3-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="c1da3-466">1 indique le dernier jour du mois, 2 indique un jour avant le dernier jour du mois, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c1da3-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="c1da3-467">Par exemple, si **RunDayOfWeek** est égal à 0 et **RunDay** la valeur 1, la tâche est traitée le dernier jour du mois.</span><span class="sxs-lookup"><span data-stu-id="c1da3-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="c1da3-468">Quand **RunDayOfWeek** n’est pas égal à 0, **RunDayOfWeek** est le jour de la semaine où le travail sera traité, par rapport à **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="c1da3-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="c1da3-469">Par exemple, si **RunDay** est 15 et **RunDayOfWeek** est 7 (+ samedi), le travail sera traité le premier samedi, le ou après le 15 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="c1da3-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="c1da3-470">Si **RunDay** est 20 et **RunDayOfWeek** est 7 (samedi), la tâche est traitée le premier samedi le ou avant le 20 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="c1da3-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="c1da3-471">Si **RunDay** est 1 et que **RunDayOfWeek** est 1 (dimanche), la tâche est traitée le dernier dimanche du mois.</span><span class="sxs-lookup"><span data-stu-id="c1da3-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="c1da3-472">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-473">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="c1da3-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-474">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="c1da3-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-476">Entier positif ou négatif utilisé conjointement avec **RunDay** pour indiquer le jour de la semaine ou du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="c1da3-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="c1da3-477">Pour plus d’informations, consultez la description de la propriété **RunDay** .</span><span class="sxs-lookup"><span data-stu-id="c1da3-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="c1da3-478">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="c1da3-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="c1da3-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="c1da3-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="c1da3-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="c1da3-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="c1da3-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="c1da3-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="c1da3-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="c1da3-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="c1da3-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="c1da3-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="c1da3-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="c1da3-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="c1da3-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="c1da3-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="c1da3-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1da3-494">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="c1da3-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-495">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="c1da3-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-496">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-497">Mois pendant lequel le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="c1da3-497">The month during which the job should be processed.</span></span> <span data-ttu-id="c1da3-498">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="c1da3-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janvier** (0)</span><span class="sxs-lookup"><span data-stu-id="c1da3-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Février** (1)</span><span class="sxs-lookup"><span data-stu-id="c1da3-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Mars** (2)</span><span class="sxs-lookup"><span data-stu-id="c1da3-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Avril** (3)</span><span class="sxs-lookup"><span data-stu-id="c1da3-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="c1da3-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juin** (5)</span><span class="sxs-lookup"><span data-stu-id="c1da3-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Juillet** (6)</span><span class="sxs-lookup"><span data-stu-id="c1da3-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Août** (7)</span><span class="sxs-lookup"><span data-stu-id="c1da3-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septembre** (8)</span><span class="sxs-lookup"><span data-stu-id="c1da3-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octobre** (9)</span><span class="sxs-lookup"><span data-stu-id="c1da3-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="c1da3-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Décembre** (11)</span><span class="sxs-lookup"><span data-stu-id="c1da3-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1da3-511">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="c1da3-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-512">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-514">Intervalle de temps après minuit lorsque le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="c1da3-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="c1da3-515">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-516">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-517">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-518">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-519">Heure de début planifiée pour le travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c1da3-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="c1da3-520">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-522">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-523">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-524">Heure de début de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c1da3-524">The time that the job began.</span></span> <span data-ttu-id="c1da3-525">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-526">**État**</span><span class="sxs-lookup"><span data-stu-id="c1da3-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-527">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1da3-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-528">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-529">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c1da3-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c1da3-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-531">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c1da3-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-532">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-533">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c1da3-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c1da3-534">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="c1da3-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-535">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="c1da3-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-536">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-537">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-538">Durée, en minutes, pendant laquelle le travail est conservé une fois qu’il a fini de s’exécuter, soit à l’issue ou à l’échec de cette exécution.</span><span class="sxs-lookup"><span data-stu-id="c1da3-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="c1da3-539">Le travail doit rester en présence pendant un certain temps, quelle que soit la valeur de la propriété **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="c1da3-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="c1da3-540">La valeur par défaut est cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="c1da3-540">The default is five minutes.</span></span> <span data-ttu-id="c1da3-541">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85))et est toujours définie sur 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="c1da3-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c1da3-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-543">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-544">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-545">Date ou heure de la dernière modification de l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="c1da3-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="c1da3-546">Si l’état de la tâche n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="c1da3-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="c1da3-547">Si une modification d’État a été demandée mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c1da3-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="c1da3-548">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1da3-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-549">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="c1da3-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-550">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-551">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-552">Heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="c1da3-552">The time that the job was submitted.</span></span> <span data-ttu-id="c1da3-553">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="c1da3-554">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1da3-555">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1da3-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1da3-556">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c1da3-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1da3-557">Heure à laquelle le travail n’est pas valide ou doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="c1da3-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="c1da3-558">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="c1da3-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1da3-559">Notes</span><span class="sxs-lookup"><span data-stu-id="c1da3-559">Remarks</span></span>

<span data-ttu-id="c1da3-560">L’accès à la classe **MSVM \_ ConcreteJob** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="c1da3-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c1da3-561">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c1da3-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1da3-562">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1da3-562">Requirements</span></span>



| <span data-ttu-id="c1da3-563">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1da3-563">Requirement</span></span> | <span data-ttu-id="c1da3-564">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1da3-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1da3-565">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1da3-565">Minimum supported client</span></span><br/> | <span data-ttu-id="c1da3-566">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1da3-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1da3-567">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1da3-567">Minimum supported server</span></span><br/> | <span data-ttu-id="c1da3-568">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1da3-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1da3-569">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1da3-569">Namespace</span></span><br/>                | <span data-ttu-id="c1da3-570">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1da3-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1da3-571">MOF</span><span class="sxs-lookup"><span data-stu-id="c1da3-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1da3-572"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1da3-573">DLL</span><span class="sxs-lookup"><span data-stu-id="c1da3-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1da3-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1da3-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1da3-575">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1da3-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1da3-576">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="c1da3-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="c1da3-577">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1da3-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c1da3-578">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="c1da3-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

