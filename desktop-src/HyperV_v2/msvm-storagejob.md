---
description: Représente un travail d’opération de stockage créé par le service de gestion d’images Microsoft Hyper-V.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869082"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="172ce-103">MSVM \_ StorageJob, classe</span><span class="sxs-lookup"><span data-stu-id="172ce-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="172ce-104">Représente un travail d’opération de stockage créé par le service de gestion d’images Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="172ce-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="172ce-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="172ce-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="172ce-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="172ce-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="172ce-107">Membres</span><span class="sxs-lookup"><span data-stu-id="172ce-107">Members</span></span>

<span data-ttu-id="172ce-108">La classe **MSVM \_ StorageJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="172ce-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="172ce-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="172ce-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="172ce-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="172ce-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="172ce-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="172ce-111">Methods</span></span>

<span data-ttu-id="172ce-112">La classe **MSVM \_ StorageJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="172ce-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="172ce-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="172ce-113">Method</span></span>                                                           | <span data-ttu-id="172ce-114">Description</span><span class="sxs-lookup"><span data-stu-id="172ce-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="172ce-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="172ce-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="172ce-116">Récupère l’erreur qui décrit la raison de l’échec du travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="172ce-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="172ce-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="172ce-118">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="172ce-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="172ce-119">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une ou plusieurs instances d' **\_ erreur MSVM** sont retournées.</span><span class="sxs-lookup"><span data-stu-id="172ce-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="172ce-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="172ce-120">**KillJob**</span></span>                                                      | <span data-ttu-id="172ce-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="172ce-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="172ce-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="172ce-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="172ce-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="172ce-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="172ce-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="172ce-124">Properties</span></span>

<span data-ttu-id="172ce-125">La classe **MSVM \_ StorageJob** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="172ce-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="172ce-126">**Annulable**</span><span class="sxs-lookup"><span data-stu-id="172ce-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="172ce-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-129">Indique si le travail peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="172ce-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="172ce-130">La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.</span><span class="sxs-lookup"><span data-stu-id="172ce-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="172ce-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-134">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="172ce-134">A short description of the object.</span></span> <span data-ttu-id="172ce-135">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-136">**Enfant**</span><span class="sxs-lookup"><span data-stu-id="172ce-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-139">En cas d’échec de l’opération asynchrone, cette propriété contient le chemin d’accès complet de l’enfant du disque dur virtuel affecté par cette opération.</span><span class="sxs-lookup"><span data-stu-id="172ce-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="172ce-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-143">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="172ce-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="172ce-144">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="172ce-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="172ce-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-146">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="172ce-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="172ce-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-149">Spécifie si le travail doit être automatiquement supprimé à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="172ce-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="172ce-150">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-151">**Description**</span><span class="sxs-lookup"><span data-stu-id="172ce-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-154">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="172ce-154">A description of the object.</span></span> <span data-ttu-id="172ce-155">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="172ce-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-157">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-159">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="172ce-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="172ce-160">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="172ce-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="172ce-161">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-163">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-165">La durée d’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="172ce-166">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="172ce-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-170">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="172ce-170">A display name for the object.</span></span> <span data-ttu-id="172ce-171">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="172ce-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-173">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-175">Code d’erreur spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="172ce-175">A vendor-specific error code.</span></span> <span data-ttu-id="172ce-176">La valeur doit être égale à zéro si le travail s’est terminé sans erreur.</span><span class="sxs-lookup"><span data-stu-id="172ce-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="172ce-177">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="172ce-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-181">Chaîne qui contient la description de l’erreur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="172ce-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="172ce-182">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="172ce-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="172ce-186">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)</span><span class="sxs-lookup"><span data-stu-id="172ce-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="172ce-187">Description résumée de l’erreur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="172ce-187">A summary description of the error, if present.</span></span> <span data-ttu-id="172ce-188">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="172ce-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-192">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="172ce-192">The current health of the element.</span></span> <span data-ttu-id="172ce-193">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="172ce-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="172ce-194">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="172ce-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="172ce-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="172ce-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="172ce-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-197">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-199">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="172ce-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="172ce-200">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="172ce-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-204">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="172ce-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="172ce-205">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-206">**JobCompletionStatusCode**</span><span class="sxs-lookup"><span data-stu-id="172ce-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="172ce-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-209">Code **HRESULT** qui décrit l’état d’achèvement de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="172ce-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-210">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="172ce-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-211">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="172ce-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-213">Nombre de fois où la tâche doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="172ce-213">The number of times that the job should be run.</span></span> <span data-ttu-id="172ce-214">La valeur 1 indique que le travail n’est pas récurrent, tandis que toute valeur différente de zéro indique une limite au nombre de fois où le travail se reproduira.</span><span class="sxs-lookup"><span data-stu-id="172ce-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="172ce-215">La valeur zéro indique qu’il n’y a pas de limite au nombre de fois où le travail peut être traité, mais qu’il se termine une fois que le **UntilTime** a été atteint ou lorsque le travail est arrêté manuellement.</span><span class="sxs-lookup"><span data-stu-id="172ce-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="172ce-216">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="172ce-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-218">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-220">État opérationnel d’un travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-220">The operational state of a job.</span></span> <span data-ttu-id="172ce-221">Il peut également indiquer des transitions entre ces États, par exemple 6 (arrêt) et 3 (à partir de).</span><span class="sxs-lookup"><span data-stu-id="172ce-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="172ce-222">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="172ce-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="172ce-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="172ce-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="172ce-224">Signification</span><span class="sxs-lookup"><span data-stu-id="172ce-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="172ce-225"><dt>**Nouveau**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="172ce-226">Le travail n’a jamais été démarré.</span><span class="sxs-lookup"><span data-stu-id="172ce-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="172ce-227">À <dt>**partir**</dt> du <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="172ce-228">Le travail passe des États « nouveau », « suspendu » ou « service » à l’État « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="172ce-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="172ce-229"><dt>**En cours d’exécution**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="172ce-230">La tâche est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="172ce-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="172ce-231"><dt>**Suspendu**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="172ce-232">La tâche est arrêtée, mais elle peut être redémarrée de manière transparente.</span><span class="sxs-lookup"><span data-stu-id="172ce-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="172ce-233"><dt>**Arrêt**</dt> de <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="172ce-234">Le travail passe à l’état « terminé », « terminé » ou « mort ».</span><span class="sxs-lookup"><span data-stu-id="172ce-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="172ce-235"><dt>**Terminé**</dt> le <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="172ce-236">Le travail s’est terminé normalement.</span><span class="sxs-lookup"><span data-stu-id="172ce-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="172ce-237"><dt>**Terminé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="172ce-238">La tâche a été arrêtée par une demande de modification d’État « Terminate ».</span><span class="sxs-lookup"><span data-stu-id="172ce-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="172ce-239">Le travail et tous ses processus sous-jacents sont terminés et peuvent être redémarrés uniquement en tant que nouveau travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="172ce-240">L’exigence de redémarrage du travail uniquement en tant que nouveau travail est spécifique à un travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="172ce-241"><dt>**Abattu**</dt> le <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="172ce-242">La tâche a été arrêtée par une demande de modification d’État « Kill ».</span><span class="sxs-lookup"><span data-stu-id="172ce-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="172ce-243">Les processus sous-jacents peuvent toujours être en cours d’exécution et un nettoyage peut être nécessaire pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="172ce-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="172ce-244"><dt>**Exception**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="172ce-245">La tâche est dans un état anormal qui peut indiquer une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="172ce-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="172ce-246">L’état réel du travail peut être disponible par le biais d’objets spécifiques à un travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="172ce-247"><dt>**Service**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="172ce-248">La tâche est dans un état spécifique au fournisseur qui prend en charge la découverte de problèmes, la résolution, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="172ce-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="172ce-249"><dt>**DMTF réservé**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="172ce-250">Réservé.</span><span class="sxs-lookup"><span data-stu-id="172ce-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="172ce-251"><dt> **Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="172ce-252">Réservé.</span><span class="sxs-lookup"><span data-stu-id="172ce-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="172ce-253">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="172ce-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-256">Chaîne qui représente l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="172ce-256">A string that represents the job status.</span></span> <span data-ttu-id="172ce-257">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="172ce-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-259">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-261">Type d’opération asynchrone faisant l’objet d’un suivi par cette instance de **MSVM \_ StorageJob**.</span><span class="sxs-lookup"><span data-stu-id="172ce-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="172ce-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="172ce-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="172ce-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**Création d’un disque dur virtuel** (1)</span><span class="sxs-lookup"><span data-stu-id="172ce-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-264">Création d’une image de disque dur virtuel (VHD).</span><span class="sxs-lookup"><span data-stu-id="172ce-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="172ce-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Création de disquette** (2)</span><span class="sxs-lookup"><span data-stu-id="172ce-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-266">Création d’une image de disquette virtuelle (VFD).</span><span class="sxs-lookup"><span data-stu-id="172ce-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="172ce-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compactage** (3)</span><span class="sxs-lookup"><span data-stu-id="172ce-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-268">Compactage de la taille d’une image de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="172ce-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="172ce-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span><span class="sxs-lookup"><span data-stu-id="172ce-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-270">Extension de la taille d’une image de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="172ce-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="172ce-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Fusion** (5)</span><span class="sxs-lookup"><span data-stu-id="172ce-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-272">Fusion de plusieurs images VHD en une seule image.</span><span class="sxs-lookup"><span data-stu-id="172ce-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="172ce-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span><span class="sxs-lookup"><span data-stu-id="172ce-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-274">Conversion du type d’une image de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="172ce-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="172ce-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Montage en boucle** (7)</span><span class="sxs-lookup"><span data-stu-id="172ce-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-276">Montage du disque dur virtuel sur la partition parente</span><span class="sxs-lookup"><span data-stu-id="172ce-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="172ce-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Récupération d’informations sur VHD** (8)</span><span class="sxs-lookup"><span data-stu-id="172ce-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="172ce-278">Montage du disque dur virtuel sur le système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="172ce-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="172ce-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Valider l’image VHD** (9)</span><span class="sxs-lookup"><span data-stu-id="172ce-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="172ce-280">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-281">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-283">Indique si les heures représentées dans les propriétés **RunStartInterval** et **UntilTime** représentent des heures locales ou des heures UTC.</span><span class="sxs-lookup"><span data-stu-id="172ce-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="172ce-284">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="172ce-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Heure locale** (1)</span><span class="sxs-lookup"><span data-stu-id="172ce-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Heure UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="172ce-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="172ce-287">**Nom**</span><span class="sxs-lookup"><span data-stu-id="172ce-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-290">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="172ce-290">The label by which the object is known.</span></span> <span data-ttu-id="172ce-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-292">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="172ce-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-295">Utilisateur qui est averti en cas d’achèvement ou d’échec d’un travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="172ce-296">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-297">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="172ce-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-298">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-300">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="172ce-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="172ce-301">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="172ce-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="172ce-302">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="172ce-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-304">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="172ce-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-306">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="172ce-306">The current statuses of the object.</span></span> <span data-ttu-id="172ce-307">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-308">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="172ce-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-311">Chaîne qui décrit l’action de récupération lorsque la propriété **RecoveryAction** de l’instance a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="172ce-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="172ce-312">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-313">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="172ce-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-316">Utilisateur qui a envoyé le travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-316">The user who submitted the job.</span></span> <span data-ttu-id="172ce-317">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-318">**Parent**</span><span class="sxs-lookup"><span data-stu-id="172ce-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-321">En cas d’échec de l’opération asynchrone, cette propriété contient le chemin d’accès du fichier au parent du disque dur virtuel affecté par cette opération.</span><span class="sxs-lookup"><span data-stu-id="172ce-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="172ce-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-323">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="172ce-325">Qualificateurs : **MinValue** (0), **MaxValue** (100), **unités** (« percent »)</span><span class="sxs-lookup"><span data-stu-id="172ce-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="172ce-326">Pourcentage d’achèvement du travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-326">The completion percentage of the job.</span></span> <span data-ttu-id="172ce-327">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-328">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="172ce-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-329">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-331">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="172ce-331">Provides high level status information.</span></span> <span data-ttu-id="172ce-332">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="172ce-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="172ce-333">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="172ce-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="172ce-334">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-335">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="172ce-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-336">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="172ce-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-338">Importance de l’exécution d’un travail.</span><span class="sxs-lookup"><span data-stu-id="172ce-338">The importance of a job's execution.</span></span> <span data-ttu-id="172ce-339">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-340">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="172ce-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-341">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="172ce-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-343">Décrit l’action de récupération à entreprendre pour un travail qui n’a pas été exécuté avec succès.</span><span class="sxs-lookup"><span data-stu-id="172ce-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="172ce-344">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="172ce-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="172ce-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="172ce-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Ne pas continuer** (2)</span><span class="sxs-lookup"><span data-stu-id="172ce-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuer avec la tâche suivante** (3)</span><span class="sxs-lookup"><span data-stu-id="172ce-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Travail de réexécution** (4)</span><span class="sxs-lookup"><span data-stu-id="172ce-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Exécuter la tâche de récupération** (5)</span><span class="sxs-lookup"><span data-stu-id="172ce-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="172ce-351">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="172ce-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-352">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="172ce-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="172ce-354">Qualificateurs : **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="172ce-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="172ce-355">Jour du mois sur lequel le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="172ce-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="172ce-356">Il existe différentes interprétations pour cette propriété, en fonction de la valeur de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="172ce-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="172ce-357">Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est positif, **RunDay** définit le jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="172ce-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="172ce-358">Par exemple, si **RunDayOfWeek** est égal à 0 et que **RunDay** est égal à 12, la tâche est traitée le 12 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="172ce-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="172ce-359">Quand **RunDayOfWeek** a la valeur 0 et que **RunDay** est négatif, **RunDay** définit le nombre de jours avant le dernier jour du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="172ce-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="172ce-360">1 indique le dernier jour du mois, 2 indique un jour avant le dernier jour du mois, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="172ce-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="172ce-361">Par exemple, si **RunDayOfWeek** est égal à 0 et **RunDay** la valeur 1, la tâche est traitée le dernier jour du mois.</span><span class="sxs-lookup"><span data-stu-id="172ce-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="172ce-362">Quand **RunDayOfWeek** n’est pas égal à 0, **RunDayOfWeek** est le jour de la semaine où le travail sera traité, par rapport à **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="172ce-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="172ce-363">Par exemple, si **RunDay** est 15 et **RunDayOfWeek** est 7 (+ samedi), le travail sera traité le premier samedi, le ou après le 15 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="172ce-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="172ce-364">Si **RunDay** est 20 et **RunDayOfWeek** est 7 (samedi), la tâche est traitée le premier samedi le ou avant le 20 <sup>ème</sup> jour du mois.</span><span class="sxs-lookup"><span data-stu-id="172ce-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="172ce-365">Si **RunDay** est 1 et que **RunDayOfWeek** est 1 (dimanche), la tâche est traitée le dernier dimanche du mois.</span><span class="sxs-lookup"><span data-stu-id="172ce-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="172ce-366">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-367">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="172ce-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-368">Type de données : **sint8**</span><span class="sxs-lookup"><span data-stu-id="172ce-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-370">Entier positif ou négatif utilisé conjointement avec **RunDay** pour indiquer le jour de la semaine ou du mois où le travail est traité.</span><span class="sxs-lookup"><span data-stu-id="172ce-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="172ce-371">Pour plus d’informations, consultez la description de la propriété **RunDay** .</span><span class="sxs-lookup"><span data-stu-id="172ce-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="172ce-372">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="172ce-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="172ce-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="172ce-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="172ce-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="172ce-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="172ce-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="172ce-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="172ce-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="172ce-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Dimanche** (1)</span><span class="sxs-lookup"><span data-stu-id="172ce-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lundi** (2)</span><span class="sxs-lookup"><span data-stu-id="172ce-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Mardi** (3)</span><span class="sxs-lookup"><span data-stu-id="172ce-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="172ce-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jeudi** (5)</span><span class="sxs-lookup"><span data-stu-id="172ce-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Vendredi** (6)</span><span class="sxs-lookup"><span data-stu-id="172ce-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Samedi** (7)</span><span class="sxs-lookup"><span data-stu-id="172ce-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="172ce-388">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="172ce-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-389">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="172ce-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-391">Mois pendant lequel le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="172ce-391">The month during which the job should be processed.</span></span> <span data-ttu-id="172ce-392">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="172ce-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janvier** (0)</span><span class="sxs-lookup"><span data-stu-id="172ce-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Février** (1)</span><span class="sxs-lookup"><span data-stu-id="172ce-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Mars** (2)</span><span class="sxs-lookup"><span data-stu-id="172ce-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Avril** (3)</span><span class="sxs-lookup"><span data-stu-id="172ce-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mai** (4)</span><span class="sxs-lookup"><span data-stu-id="172ce-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Juin** (5)</span><span class="sxs-lookup"><span data-stu-id="172ce-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Juillet** (6)</span><span class="sxs-lookup"><span data-stu-id="172ce-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Août** (7)</span><span class="sxs-lookup"><span data-stu-id="172ce-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septembre** (8)</span><span class="sxs-lookup"><span data-stu-id="172ce-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octobre** (9)</span><span class="sxs-lookup"><span data-stu-id="172ce-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)</span><span class="sxs-lookup"><span data-stu-id="172ce-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="172ce-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Décembre** (11)</span><span class="sxs-lookup"><span data-stu-id="172ce-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="172ce-405">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="172ce-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-406">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-408">Intervalle de temps après minuit lorsque le travail doit être traité.</span><span class="sxs-lookup"><span data-stu-id="172ce-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="172ce-409">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-410">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-411">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-413">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-415">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-417">Heure de début de la tâche.</span><span class="sxs-lookup"><span data-stu-id="172ce-417">The time that the job began.</span></span> <span data-ttu-id="172ce-418">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-419">**État**</span><span class="sxs-lookup"><span data-stu-id="172ce-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="172ce-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-422">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="172ce-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="172ce-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-424">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="172ce-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="172ce-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-426">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="172ce-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="172ce-427">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="172ce-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-428">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="172ce-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-429">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-431">Durée, en minutes, pendant laquelle le travail est conservé une fois qu’il a fini de s’exécuter, soit à l’issue ou à l’échec de cette exécution.</span><span class="sxs-lookup"><span data-stu-id="172ce-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="172ce-432">Le travail doit rester en présence pendant un certain temps, quelle que soit la valeur de la propriété **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="172ce-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="172ce-433">La valeur par défaut est cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="172ce-433">The default is five minutes.</span></span> <span data-ttu-id="172ce-434">Cette propriété est héritée de la [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85))et est toujours définie sur 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="172ce-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="172ce-435">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="172ce-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-436">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-438">Heure de la dernière modification de l’état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="172ce-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="172ce-439">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="172ce-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-440">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="172ce-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-441">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-443">Heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="172ce-443">The time that the job was submitted.</span></span> <span data-ttu-id="172ce-444">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="172ce-445">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="172ce-446">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="172ce-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="172ce-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="172ce-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="172ce-448">Heure à laquelle le travail n’est pas valide ou doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="172ce-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="172ce-449">Cette propriété est héritée de la [**\_ tâche CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="172ce-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="172ce-450">Notes</span><span class="sxs-lookup"><span data-stu-id="172ce-450">Remarks</span></span>

<span data-ttu-id="172ce-451">L’accès à la classe **MSVM \_ StorageJob** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="172ce-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="172ce-452">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="172ce-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="172ce-453">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="172ce-453">Requirements</span></span>



| <span data-ttu-id="172ce-454">Condition requise</span><span class="sxs-lookup"><span data-stu-id="172ce-454">Requirement</span></span> | <span data-ttu-id="172ce-455">Valeur</span><span class="sxs-lookup"><span data-stu-id="172ce-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="172ce-456">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="172ce-456">Minimum supported client</span></span><br/> | <span data-ttu-id="172ce-457">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="172ce-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="172ce-458">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="172ce-458">Minimum supported server</span></span><br/> | <span data-ttu-id="172ce-459">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="172ce-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="172ce-460">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="172ce-460">Namespace</span></span><br/>                | <span data-ttu-id="172ce-461">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="172ce-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="172ce-462">MOF</span><span class="sxs-lookup"><span data-stu-id="172ce-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="172ce-463"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="172ce-464">DLL</span><span class="sxs-lookup"><span data-stu-id="172ce-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="172ce-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="172ce-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="172ce-466">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="172ce-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172ce-467">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="172ce-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="172ce-468">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="172ce-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="172ce-469">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="172ce-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

