---
description: Élément logique qui représente une unité de travail à exécuter, par exemple un script ou un travail d’impression. Un travail est différent d’un processus, car un travail peut être planifié ou mis en file d’attente, et son exécution n’est pas limitée à un seul système.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Classe CIM_Job (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952524"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="15e2e-104">Classe CIM_Job (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="15e2e-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="15e2e-105">Élément logique qui représente une unité de travail à exécuter, par exemple un script ou un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="15e2e-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="15e2e-106">Un travail est différent d’un processus, car un travail peut être planifié ou mis en file d’attente, et son exécution n’est pas limitée à un seul système.</span><span class="sxs-lookup"><span data-stu-id="15e2e-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e2e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15e2e-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
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
};
```

## <a name="members"></a><span data-ttu-id="15e2e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="15e2e-108">Members</span></span>

<span data-ttu-id="15e2e-109">La classe de **\_ tâche CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="15e2e-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="15e2e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="15e2e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="15e2e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15e2e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15e2e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="15e2e-112">Methods</span></span>

<span data-ttu-id="15e2e-113">La classe de **\_ tâche CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="15e2e-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="15e2e-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="15e2e-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="15e2e-115">Description</span><span class="sxs-lookup"><span data-stu-id="15e2e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="15e2e-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span><span class="sxs-lookup"><span data-stu-id="15e2e-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="15e2e-117">Cette méthode est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-117">This method is deprecated.</span></span> <span data-ttu-id="15e2e-118">Utilisez à la place la méthode <strong>RequestStateChange</strong> .</span><span class="sxs-lookup"><span data-stu-id="15e2e-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="15e2e-119">Description déconseillée : ferme un travail.</span><span class="sxs-lookup"><span data-stu-id="15e2e-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="15e2e-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15e2e-120">Properties</span></span>

<span data-ttu-id="15e2e-121">La classe de **\_ tâche CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="15e2e-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15e2e-122">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="15e2e-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="15e2e-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-125">**True** pour supprimer le travail une fois l’opération terminée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="15e2e-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="15e2e-126">Cette propriété ne supprime pas les travaux qui se terminent avant que cette propriété ait la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="15e2e-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="15e2e-127">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-130">Durée d’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="15e2e-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="15e2e-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15e2e-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-134">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**ErrorDescription**»)</span><span class="sxs-lookup"><span data-stu-id="15e2e-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-135">Code d’erreur spécifique au fournisseur qui capture les informations de traitement des tâches récurrentes.</span><span class="sxs-lookup"><span data-stu-id="15e2e-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="15e2e-136">La valeur doit être égale à zéro si le travail s’est terminé sans erreur.</span><span class="sxs-lookup"><span data-stu-id="15e2e-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="15e2e-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15e2e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-140">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="15e2e-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-141">Chaîne de forme libre qui contient une description du code d’erreur correspondant dans la propriété **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="15e2e-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-142">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="15e2e-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15e2e-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-145">Nombre de fois où le travail est exécuté.</span><span class="sxs-lookup"><span data-stu-id="15e2e-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-146">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="15e2e-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15e2e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-149">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**»)</span><span class="sxs-lookup"><span data-stu-id="15e2e-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-150">Chaîne de forme libre qui représente l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="15e2e-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-151">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-152">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15e2e-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-154">Indique si les heures dans les propriétés **RunStartInterval** et **UntilTime** représentent des heures locales ou des heures UTC.</span><span class="sxs-lookup"><span data-stu-id="15e2e-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="15e2e-155">**Heure locale** (1)</span><span class="sxs-lookup"><span data-stu-id="15e2e-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="15e2e-156">**Heure UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="15e2e-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15e2e-157">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="15e2e-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15e2e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-160">Utilisateur à notifier lorsqu’un travail se termine ou échoue.</span><span class="sxs-lookup"><span data-stu-id="15e2e-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-161">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="15e2e-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15e2e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-164">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-165">Chaîne qui décrit l’action de récupération lorsque la propriété **RecoveryAction** est **autre** (« 1 »).</span><span class="sxs-lookup"><span data-stu-id="15e2e-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-166">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="15e2e-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15e2e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-169">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")</span><span class="sxs-lookup"><span data-stu-id="15e2e-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-170">L’utilisateur qui a envoyé le travail, ou le nom du service ou de la méthode qui a demandé le travail.</span><span class="sxs-lookup"><span data-stu-id="15e2e-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="15e2e-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15e2e-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-174">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« percent »), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **punitif** (« percent »)</span><span class="sxs-lookup"><span data-stu-id="15e2e-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-175">Pourcentage de la tâche qui est terminé.</span><span class="sxs-lookup"><span data-stu-id="15e2e-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="15e2e-176">La valeur « 101 » n’est pas définie et ne sera pas autorisée dans la prochaine révision majeure de la spécification.</span><span class="sxs-lookup"><span data-stu-id="15e2e-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="15e2e-177">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="15e2e-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-178">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15e2e-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-180">Importance du travail.</span><span class="sxs-lookup"><span data-stu-id="15e2e-180">The importance of the job.</span></span> <span data-ttu-id="15e2e-181">Plus le numéro est faible, plus la priorité est élevée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-182">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="15e2e-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-183">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15e2e-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-185">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**OtherRecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-186">Décrit l’action de récupération à entreprendre en cas d’échec d’une tâche d’exécution.</span><span class="sxs-lookup"><span data-stu-id="15e2e-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15e2e-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="15e2e-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="15e2e-188">Il est inconnu de l’action de récupération à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="15e2e-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15e2e-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="15e2e-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="15e2e-190">L’action de récupération sera spécifiée dans la propriété **OtherRecoveryAction** .</span><span class="sxs-lookup"><span data-stu-id="15e2e-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="15e2e-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Ne pas continuer** (2)</span><span class="sxs-lookup"><span data-stu-id="15e2e-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="15e2e-192">Arrêtez l’exécution du travail et mettez à jour son état de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="15e2e-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuer avec la tâche suivante** (3)</span><span class="sxs-lookup"><span data-stu-id="15e2e-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="15e2e-194">Passez à la tâche suivante dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="15e2e-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="15e2e-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Travail de réexécution** (4)</span><span class="sxs-lookup"><span data-stu-id="15e2e-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="15e2e-196">La tâche doit être réexécutée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="15e2e-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Exécuter la tâche de récupération** (5)</span><span class="sxs-lookup"><span data-stu-id="15e2e-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="15e2e-198">Exécutez le travail associé à l’aide de la relation **RecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="15e2e-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="15e2e-199">Notez que la tâche de récupération doit déjà se trouver dans la file d’attente à partir de laquelle elle sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="15e2e-200">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="15e2e-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-201">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="15e2e-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-203">Qualificateurs : [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Job CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-204">Entier utilisé conjointement avec la propriété **RunDayOfWeek** pour indiquer le jour de traitement du travail ; ou, si **RunDayOfWeek** est défini sur zéro, **RunDay** indique le jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="15e2e-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="15e2e-205">Si **RunDay** est un entier négatif, il spécifie un jour relatif à la fin du mois, ou si **RunDay** est un entier positif, il spécifie un jour par rapport au début du mois.</span><span class="sxs-lookup"><span data-stu-id="15e2e-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-206">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="15e2e-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-207">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="15e2e-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-209">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-210">Entier utilisé conjointement avec la propriété **RunDay** pour indiquer le jour de traitement du travail ; ou, si **RunDayOfWeek** est défini sur zéro, **RunDay** indique le jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="15e2e-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="15e2e-211">**-Samedi** (-7)</span><span class="sxs-lookup"><span data-stu-id="15e2e-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="15e2e-212">**-Vendredi** (-6)</span><span class="sxs-lookup"><span data-stu-id="15e2e-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="15e2e-213">**-Jeudi** (-5)</span><span class="sxs-lookup"><span data-stu-id="15e2e-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="15e2e-214">**-Mercredi** (-4)</span><span class="sxs-lookup"><span data-stu-id="15e2e-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="15e2e-215">**-Mardi** (-3)</span><span class="sxs-lookup"><span data-stu-id="15e2e-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="15e2e-216">**-Lundi** (-2)</span><span class="sxs-lookup"><span data-stu-id="15e2e-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="15e2e-217">**-Dimanche** (-1)</span><span class="sxs-lookup"><span data-stu-id="15e2e-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="15e2e-218">**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="15e2e-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="15e2e-219">**Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="15e2e-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="15e2e-220">**Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="15e2e-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="15e2e-221">**Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="15e2e-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="15e2e-222">**Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="15e2e-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="15e2e-223">**Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="15e2e-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="15e2e-224">**Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="15e2e-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="15e2e-225">**Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="15e2e-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15e2e-226">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="15e2e-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-227">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="15e2e-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-228">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-229">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-230">Mois de traitement du travail.</span><span class="sxs-lookup"><span data-stu-id="15e2e-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="15e2e-231">**Janvier** (0)</span><span class="sxs-lookup"><span data-stu-id="15e2e-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="15e2e-232">**Février** (1)</span><span class="sxs-lookup"><span data-stu-id="15e2e-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="15e2e-233">**Mars** (2)</span><span class="sxs-lookup"><span data-stu-id="15e2e-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="15e2e-234">**Avril** (3)</span><span class="sxs-lookup"><span data-stu-id="15e2e-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="15e2e-235">**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="15e2e-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="15e2e-236">**Juin** (5)</span><span class="sxs-lookup"><span data-stu-id="15e2e-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="15e2e-237">**Juillet** (6)</span><span class="sxs-lookup"><span data-stu-id="15e2e-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="15e2e-238">**Août** (7)</span><span class="sxs-lookup"><span data-stu-id="15e2e-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="15e2e-239">**Septembre** (8)</span><span class="sxs-lookup"><span data-stu-id="15e2e-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="15e2e-240">**Octobre** (9)</span><span class="sxs-lookup"><span data-stu-id="15e2e-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="15e2e-241">**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="15e2e-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="15e2e-242">**Décembre** (11)</span><span class="sxs-lookup"><span data-stu-id="15e2e-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15e2e-243">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="15e2e-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-244">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-245">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-246">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-247">Intervalle de temps après minuit lorsque le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="15e2e-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="15e2e-248">Par exemple, « 00000000020000.000000:000 » indique que le travail est exécuté à l’heure ou après deux heures, heure locale ou heure UTC (UTC est spécifiée avec la propriété **LocalOrUtcTime** ).</span><span class="sxs-lookup"><span data-stu-id="15e2e-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-249">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-250">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-251">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-252">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) («**\_ tâche CIM**.**RunMonth**», «**\_ tâche CIM**.**RunDay**», «**\_ tâche CIM**.**RunDayOfWeek**», «**\_ tâche CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="15e2e-253">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-253">This property is deprecated.</span></span> <span data-ttu-id="15e2e-254">Au lieu de cela, nous vous recommandons d’utiliser les propriétés **RunMonth**, **RunDay**, **RunDayOfWeek** et **RunStartInterval** .</span><span class="sxs-lookup"><span data-stu-id="15e2e-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="15e2e-255">Heure à laquelle le travail en cours est planifié pour démarrer.</span><span class="sxs-lookup"><span data-stu-id="15e2e-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="15e2e-256">Cette heure peut être représentée par une date et une heure ou par un intervalle relatif à l’heure à laquelle la propriété est demandée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="15e2e-257">La valeur zéro indique que le travail est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="15e2e-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-259">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-261">Heure à laquelle le travail a démarré.</span><span class="sxs-lookup"><span data-stu-id="15e2e-261">The time when the job started.</span></span> <span data-ttu-id="15e2e-262">Cette heure peut être représentée par une date et une heure ou par un intervalle relatif à l’heure à laquelle la propriété est demandée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-263">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="15e2e-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-264">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15e2e-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-266">Heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="15e2e-266">The time when the job was submitted.</span></span> <span data-ttu-id="15e2e-267">La valeur tous les zéros indique que l’élément parent n’est pas capable de signaler une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="15e2e-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="15e2e-268">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15e2e-269">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15e2e-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-270">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="15e2e-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15e2e-271">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**\_ tâche CIM**.**LocalOrUtcTime**")</span><span class="sxs-lookup"><span data-stu-id="15e2e-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="15e2e-272">Heure après laquelle le travail devient non valide ou doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="15e2e-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="15e2e-273">L’heure peut être représentée par une date et une heure ou par un intervalle relatif à l’heure à laquelle cette propriété est demandée.</span><span class="sxs-lookup"><span data-stu-id="15e2e-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="15e2e-274">La valeur tous les neuf indique que le travail peut s’exécuter indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="15e2e-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15e2e-275">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15e2e-275">Requirements</span></span>



| <span data-ttu-id="15e2e-276">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15e2e-276">Requirement</span></span> | <span data-ttu-id="15e2e-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="15e2e-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e2e-278">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15e2e-278">Minimum supported client</span></span><br/> | <span data-ttu-id="15e2e-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15e2e-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15e2e-280">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15e2e-280">Minimum supported server</span></span><br/> | <span data-ttu-id="15e2e-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15e2e-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15e2e-282">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="15e2e-282">Namespace</span></span><br/>                | <span data-ttu-id="15e2e-283">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="15e2e-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15e2e-284">MOF</span><span class="sxs-lookup"><span data-stu-id="15e2e-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15e2e-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15e2e-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15e2e-286">DLL</span><span class="sxs-lookup"><span data-stu-id="15e2e-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e2e-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15e2e-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15e2e-288">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15e2e-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e2e-289">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="15e2e-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

