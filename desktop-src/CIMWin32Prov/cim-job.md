---
description: La \_ classe de tâche CIM représente une unité de travail pour un système, par exemple un travail d’impression. Un travail est différent d’un processus, car un travail peut être planifié.
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: CIM_Job, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110839"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="17b03-104">CIM_Job, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="17b03-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="17b03-105">La classe de **\_ tâche CIM** représente une unité de travail pour un système, par exemple un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="17b03-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="17b03-106">Un travail est différent d’un processus, car un travail peut être planifié.</span><span class="sxs-lookup"><span data-stu-id="17b03-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17b03-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="17b03-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17b03-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="17b03-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17b03-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="17b03-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="17b03-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="17b03-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b03-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17b03-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="17b03-112">Membres</span><span class="sxs-lookup"><span data-stu-id="17b03-112">Members</span></span>

<span data-ttu-id="17b03-113">La classe de **\_ tâche CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17b03-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="17b03-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17b03-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17b03-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17b03-115">Properties</span></span>

<span data-ttu-id="17b03-116">La classe de **\_ tâche CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="17b03-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17b03-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="17b03-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b03-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="17b03-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="17b03-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="17b03-121">A short textual description of the object.</span></span>

<span data-ttu-id="17b03-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17b03-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="17b03-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b03-126">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="17b03-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="17b03-127">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="17b03-127">A textual description of the object.</span></span>

<span data-ttu-id="17b03-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17b03-129">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-132">Durée d’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="17b03-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="17b03-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-134">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b03-136">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="17b03-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="17b03-137">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="17b03-137">Indicates when the object was installed.</span></span> <span data-ttu-id="17b03-138">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="17b03-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="17b03-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17b03-140">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="17b03-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-143">Chaîne de forme libre qui représente l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="17b03-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="17b03-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b03-147">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="17b03-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="17b03-148">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="17b03-148">Label by which the object is known.</span></span> <span data-ttu-id="17b03-149">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="17b03-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="17b03-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17b03-151">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="17b03-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-154">L’utilisateur est averti en cas d’achèvement ou d’échec de la tâche.</span><span class="sxs-lookup"><span data-stu-id="17b03-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-155">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="17b03-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-158">Utilisateur qui a envoyé le travail.</span><span class="sxs-lookup"><span data-stu-id="17b03-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-159">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="17b03-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17b03-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-162">Importance de l’exécution d’un travail.</span><span class="sxs-lookup"><span data-stu-id="17b03-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-164">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-166">Heure de début de la tâche.</span><span class="sxs-lookup"><span data-stu-id="17b03-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-167">**État**</span><span class="sxs-lookup"><span data-stu-id="17b03-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17b03-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b03-170">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="17b03-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="17b03-171">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="17b03-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="17b03-172">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="17b03-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="17b03-173">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="17b03-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="17b03-174">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="17b03-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="17b03-175">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="17b03-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="17b03-176">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="17b03-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="17b03-177">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="17b03-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="17b03-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="17b03-179">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="17b03-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="17b03-180">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="17b03-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="17b03-181">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="17b03-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="17b03-182">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="17b03-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17b03-183">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="17b03-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="17b03-184">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="17b03-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="17b03-185">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="17b03-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="17b03-186">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="17b03-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="17b03-187">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="17b03-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="17b03-188">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="17b03-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="17b03-189">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="17b03-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="17b03-190">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="17b03-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="17b03-191">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="17b03-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17b03-192">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="17b03-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-193">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-195">Heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="17b03-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="17b03-196">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b03-197">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17b03-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17b03-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17b03-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17b03-199">Heure à laquelle le travail n’est pas valide ou doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="17b03-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17b03-200">Notes</span><span class="sxs-lookup"><span data-stu-id="17b03-200">Remarks</span></span>

<span data-ttu-id="17b03-201">La classe de **\_ tâche CIM** est dérivée de la [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="17b03-202">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="17b03-202">WMI does not implement this class.</span></span> <span data-ttu-id="17b03-203">Pour les classes dérivées de la **\_ tâche CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17b03-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="17b03-204">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="17b03-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17b03-205">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="17b03-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b03-206">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17b03-206">Requirements</span></span>



| <span data-ttu-id="17b03-207">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17b03-207">Requirement</span></span> | <span data-ttu-id="17b03-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="17b03-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b03-209">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17b03-209">Minimum supported client</span></span><br/> | <span data-ttu-id="17b03-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17b03-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17b03-211">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17b03-211">Minimum supported server</span></span><br/> | <span data-ttu-id="17b03-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17b03-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17b03-213">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="17b03-213">Namespace</span></span><br/>                | <span data-ttu-id="17b03-214">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="17b03-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17b03-215">MOF</span><span class="sxs-lookup"><span data-stu-id="17b03-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17b03-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17b03-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17b03-217">DLL</span><span class="sxs-lookup"><span data-stu-id="17b03-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b03-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b03-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b03-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17b03-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b03-220">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="17b03-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

