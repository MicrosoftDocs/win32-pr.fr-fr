---
description: Représente un travail créé à l’aide de la commande AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033613"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="a7872-103">\_Classe ScheduledJob Win32</span><span class="sxs-lookup"><span data-stu-id="a7872-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="a7872-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob** WMI   représente un travail créé à l’aide de la commande **at** .</span><span class="sxs-lookup"><span data-stu-id="a7872-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="a7872-105">La classe **Win32 \_ ScheduledJob** ne représente pas un travail créé à l’aide de l’Assistant tâche planifiée à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="a7872-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="a7872-106">Vous ne pouvez pas modifier une tâche créée par WMI dans l’interface utilisateur tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="a7872-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="a7872-107">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a7872-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="a7872-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a7872-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a7872-109">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="a7872-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7872-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7872-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="a7872-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a7872-111">Members</span></span>

<span data-ttu-id="a7872-112">La classe **Win32 \_ ScheduledJob** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a7872-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="a7872-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7872-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a7872-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7872-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a7872-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7872-115">Methods</span></span>

<span data-ttu-id="a7872-116">La classe **Win32 \_ ScheduledJob** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a7872-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="a7872-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="a7872-117">Method</span></span>                                                      | <span data-ttu-id="a7872-118">Description</span><span class="sxs-lookup"><span data-stu-id="a7872-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7872-119">**Créés**</span><span class="sxs-lookup"><span data-stu-id="a7872-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="a7872-120">Méthode de classe qui envoie un travail au système d’exploitation pour l’exécuter à une date et une heure futures spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a7872-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="a7872-121">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="a7872-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="a7872-122">Méthode de classe qui supprime une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="a7872-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="a7872-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a7872-123">Properties</span></span>

<span data-ttu-id="a7872-124">La classe **Win32 \_ ScheduledJob** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a7872-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7872-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a7872-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-128">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="a7872-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-129">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7872-129">A short textual description of the object.</span></span>

<span data-ttu-id="a7872-130">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-131">**Commande**</span><span class="sxs-lookup"><span data-stu-id="a7872-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-134">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures \| [**de gestion de réseau at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**")</span><span class="sxs-lookup"><span data-stu-id="a7872-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-135">Nom de la commande, du programme de traitement par lots ou du fichier binaire (et des arguments de ligne de commande) que le service de planification utilise pour appeler le travail.</span><span class="sxs-lookup"><span data-stu-id="a7872-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="a7872-136">Exemple : "**Defrag** **/q/f**"</span><span class="sxs-lookup"><span data-stu-id="a7872-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="a7872-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="a7872-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7872-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-140">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**»)</span><span class="sxs-lookup"><span data-stu-id="a7872-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-141">Jours du mois où la tâche est planifiée pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a7872-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="a7872-142">Si un travail est planifié pour s’exécuter sur plusieurs jours du mois, ces valeurs peuvent être jointes dans un ou logique.</span><span class="sxs-lookup"><span data-stu-id="a7872-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="a7872-143">Par exemple, si un travail doit s’exécuter le 1er et le 16 de chaque mois, la valeur de la propriété **DaysOfMonth** est 1 ou 32768.</span><span class="sxs-lookup"><span data-stu-id="a7872-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="a7872-144"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a7872-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-145">premier</span><span class="sxs-lookup"><span data-stu-id="a7872-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="a7872-146"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a7872-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-147">2</span><span class="sxs-lookup"><span data-stu-id="a7872-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="a7872-148"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="a7872-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-149">3e</span><span class="sxs-lookup"><span data-stu-id="a7872-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="a7872-150"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="a7872-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-151">4e</span><span class="sxs-lookup"><span data-stu-id="a7872-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="a7872-152"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="a7872-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-153">5e</span><span class="sxs-lookup"><span data-stu-id="a7872-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="a7872-154"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="a7872-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-155">6e</span><span class="sxs-lookup"><span data-stu-id="a7872-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="a7872-156"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="a7872-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-157">7e</span><span class="sxs-lookup"><span data-stu-id="a7872-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="a7872-158"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="a7872-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-159">8e</span><span class="sxs-lookup"><span data-stu-id="a7872-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="a7872-160"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="a7872-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-161">9e</span><span class="sxs-lookup"><span data-stu-id="a7872-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="a7872-162"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="a7872-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-163">Palmarè</span><span class="sxs-lookup"><span data-stu-id="a7872-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="a7872-164"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="a7872-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-165">11th</span><span class="sxs-lookup"><span data-stu-id="a7872-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="a7872-166"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="a7872-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-167">12th</span><span class="sxs-lookup"><span data-stu-id="a7872-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="a7872-168"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="a7872-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-169">13th</span><span class="sxs-lookup"><span data-stu-id="a7872-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="a7872-170"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="a7872-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-171">14e</span><span class="sxs-lookup"><span data-stu-id="a7872-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="a7872-172"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="a7872-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-173">15</span><span class="sxs-lookup"><span data-stu-id="a7872-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="a7872-174"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="a7872-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-175">16</span><span class="sxs-lookup"><span data-stu-id="a7872-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="a7872-176"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="a7872-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-177">septième</span><span class="sxs-lookup"><span data-stu-id="a7872-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="a7872-178"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="a7872-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-179">18e</span><span class="sxs-lookup"><span data-stu-id="a7872-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="a7872-180"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="a7872-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-181">dix</span><span class="sxs-lookup"><span data-stu-id="a7872-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="a7872-182"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="a7872-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-183">vingtième</span><span class="sxs-lookup"><span data-stu-id="a7872-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="a7872-184"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="a7872-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-185">21st</span><span class="sxs-lookup"><span data-stu-id="a7872-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="a7872-186"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="a7872-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-187">22nd</span><span class="sxs-lookup"><span data-stu-id="a7872-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="a7872-188"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="a7872-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-189">23rd</span><span class="sxs-lookup"><span data-stu-id="a7872-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="a7872-190"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="a7872-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-191">24</span><span class="sxs-lookup"><span data-stu-id="a7872-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="a7872-192"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="a7872-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-193">vingt</span><span class="sxs-lookup"><span data-stu-id="a7872-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="a7872-194"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="a7872-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-195">26</span><span class="sxs-lookup"><span data-stu-id="a7872-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="a7872-196"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="a7872-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-197">27</span><span class="sxs-lookup"><span data-stu-id="a7872-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="a7872-198"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="a7872-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-199">28</span><span class="sxs-lookup"><span data-stu-id="a7872-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="a7872-200"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="a7872-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-201">29</span><span class="sxs-lookup"><span data-stu-id="a7872-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="a7872-202"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="a7872-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-203">30e</span><span class="sxs-lookup"><span data-stu-id="a7872-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="a7872-204"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="a7872-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="a7872-205">31</span><span class="sxs-lookup"><span data-stu-id="a7872-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a7872-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="a7872-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7872-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-209">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| structures de gestion \| [**de réseau at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")</span><span class="sxs-lookup"><span data-stu-id="a7872-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-210">Jours de la semaine où un travail est planifié pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a7872-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="a7872-211">Si un travail est planifié pour s’exécuter plusieurs jours de la semaine, les valeurs peuvent être jointes dans un ou logique.</span><span class="sxs-lookup"><span data-stu-id="a7872-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="a7872-212">Par exemple, si un travail est planifié pour s’exécuter le lundi, le mercredi et le vendredi, la valeur de la propriété **DaysOfWeek** est 1, 4 ou 16.</span><span class="sxs-lookup"><span data-stu-id="a7872-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="a7872-213">**Lundi** (1)</span><span class="sxs-lookup"><span data-stu-id="a7872-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="a7872-214">**Mardi** (2)</span><span class="sxs-lookup"><span data-stu-id="a7872-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="a7872-215">**Mercredi** (4)</span><span class="sxs-lookup"><span data-stu-id="a7872-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="a7872-216">**Jeudi** (8)</span><span class="sxs-lookup"><span data-stu-id="a7872-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="a7872-217">**Vendredi** (16)</span><span class="sxs-lookup"><span data-stu-id="a7872-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="a7872-218">**Samedi** (32)</span><span class="sxs-lookup"><span data-stu-id="a7872-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="a7872-219">**Dimanche** (64)</span><span class="sxs-lookup"><span data-stu-id="a7872-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7872-220">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7872-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-223">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a7872-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-224">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7872-224">A textual description of the object.</span></span>

<span data-ttu-id="a7872-225">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-226">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-227">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7872-229">Durée d’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="a7872-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="a7872-230">Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7872-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-232">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-234">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="a7872-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-235">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="a7872-235">Indicates when the object was installed.</span></span> <span data-ttu-id="a7872-236">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="a7872-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a7872-237">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-238">**InteractWithDesktop**</span><span class="sxs-lookup"><span data-stu-id="a7872-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-239">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7872-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-241">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de gestion de réseau win32api \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **Job non \_ interactive**")</span><span class="sxs-lookup"><span data-stu-id="a7872-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-242">Le travail spécifié est interactif, ce qui signifie qu’un utilisateur peut fournir une entrée à une tâche planifiée pendant son exécution.</span><span class="sxs-lookup"><span data-stu-id="a7872-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="a7872-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="a7872-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-244">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7872-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-246">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**»)</span><span class="sxs-lookup"><span data-stu-id="a7872-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-247">Numéro d’identification du travail.</span><span class="sxs-lookup"><span data-stu-id="a7872-247">Identifying number of the job.</span></span> <span data-ttu-id="a7872-248">Elle est utilisée par les méthodes comme handle d’une tâche planifiée sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a7872-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="a7872-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="a7872-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-252">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures de gestion \| de réseau à l’indicateur d'[**\_ énumération du**](/windows/win32/api/lmat/ns-lmat-at_enum) \|  \| **travail \_ Exec \_ Error**")</span><span class="sxs-lookup"><span data-stu-id="a7872-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-253">État de l’exécution lors de la dernière planification de l’exécution de ce travail.</span><span class="sxs-lookup"><span data-stu-id="a7872-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="a7872-254">**Succès** (« réussite »)</span><span class="sxs-lookup"><span data-stu-id="a7872-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="a7872-255">**Échec** (« échec »)</span><span class="sxs-lookup"><span data-stu-id="a7872-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7872-256">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a7872-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-259">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a7872-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-260">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="a7872-260">Label by which the object is known.</span></span> <span data-ttu-id="a7872-261">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="a7872-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a7872-262">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-263">**Notifier**</span><span class="sxs-lookup"><span data-stu-id="a7872-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7872-266">L’utilisateur est averti en cas d’achèvement ou d’échec de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a7872-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="a7872-267">Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-268">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="a7872-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7872-271">Utilisateur qui a envoyé le travail.</span><span class="sxs-lookup"><span data-stu-id="a7872-271">User who submitted the job.</span></span>

<span data-ttu-id="a7872-272">Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-273">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="a7872-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-274">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7872-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7872-276">Importance de l’exécution d’un travail.</span><span class="sxs-lookup"><span data-stu-id="a7872-276">Importance of a job's execution.</span></span>

<span data-ttu-id="a7872-277">Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-278">**RunRepeatedly**</span><span class="sxs-lookup"><span data-stu-id="a7872-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-279">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a7872-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-281">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures \| [**de gestion de réseau at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **\_ fonctionnent \_ régulièrement**")</span><span class="sxs-lookup"><span data-stu-id="a7872-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-282">La tâche planifiée s’exécute de manière répétée les jours où la tâche est planifiée.</span><span class="sxs-lookup"><span data-stu-id="a7872-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="a7872-283">Si la **valeur est false**, la tâche est exécutée une fois.</span><span class="sxs-lookup"><span data-stu-id="a7872-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="a7872-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-285">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-287">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures de gestion de réseau win32api \| [**au JobTime \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| ")</span><span class="sxs-lookup"><span data-stu-id="a7872-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-288">Heure UTC d’exécution du travail, sous la forme «AAAAMMJJHHMMSS. MMMMMM (+-) OOO», où « AAAAMMJJ » doit être remplacé par « \* \* \* \* \* \* \* \* ».</span><span class="sxs-lookup"><span data-stu-id="a7872-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="a7872-289">Le remplacement est nécessaire, car le service de planification autorise uniquement la configuration des tâches à exécuter une seule fois, ou une exécution le jour du mois ou de la semaine.</span><span class="sxs-lookup"><span data-stu-id="a7872-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="a7872-290">Une tâche ne peut pas être exécutée à une date spécifique.</span><span class="sxs-lookup"><span data-stu-id="a7872-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="a7872-291">La section « (+-) OOO » de la valeur de la propriété **StartTime** est le décalage actuel pour la traduction de l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="a7872-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="a7872-292">Le biais correspond à la différence entre l’heure UTC et l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="a7872-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="a7872-293">Pour calculer le décalage pour votre fuseau horaire, multipliez le nombre d’heures d’avance ou de retard de l’heure de Greenwich (GMT) par 60 (utilisez un nombre positif comme nombre d’heures avant l’heure GMT et un nombre négatif si votre fuseau horaire est situé en arrière-plan GMT).</span><span class="sxs-lookup"><span data-stu-id="a7872-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="a7872-294">Ajoutez un 60 supplémentaire à votre calcul si votre fuseau horaire utilise l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="a7872-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="a7872-295">Par exemple, le fuseau horaire Pacifique est de huit heures après l’heure GMT. par conséquent, le décalage est égal à-420 (-8 \* 60 + 60) lorsque l’heure d’été est utilisée et-480 (-8 \* 60) lorsque l’heure d’été n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="a7872-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="a7872-296">Vous pouvez également déterminer la valeur du décalage en interrogeant la propriété Bias de la classe [**Win32 \_ TimeZone**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="a7872-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="a7872-297">Par exemple : « \* \* \* \* \* \* \* \* 123000.000000-420 » spécifie 14,30 (2:30 P.M.) PST avec l’heure d’été en vigueur.</span><span class="sxs-lookup"><span data-stu-id="a7872-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="a7872-298">**État**</span><span class="sxs-lookup"><span data-stu-id="a7872-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a7872-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7872-301">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a7872-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a7872-302">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7872-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="a7872-303">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="a7872-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a7872-304">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="a7872-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a7872-305">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="a7872-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a7872-306">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="a7872-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a7872-307">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="a7872-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a7872-308">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="a7872-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a7872-309">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a7872-310">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7872-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a7872-311">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="a7872-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a7872-312">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="a7872-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a7872-313">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="a7872-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7872-314">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="a7872-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a7872-315">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="a7872-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a7872-316">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="a7872-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a7872-317">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="a7872-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a7872-318">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="a7872-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a7872-319">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="a7872-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a7872-320">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="a7872-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a7872-321">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="a7872-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a7872-322">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="a7872-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7872-323">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="a7872-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-324">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7872-326">Heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="a7872-326">Time that the job was submitted.</span></span>

<span data-ttu-id="a7872-327">Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7872-328">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7872-329">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7872-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7872-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a7872-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7872-331">Heure à laquelle le travail n’est pas valide ou doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="a7872-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="a7872-332">Cette propriété est héritée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7872-333">Notes</span><span class="sxs-lookup"><span data-stu-id="a7872-333">Remarks</span></span>

<span data-ttu-id="a7872-334">Chaque travail planifié sur le service de planification est stocké de façon permanente (le planificateur peut démarrer un travail après un redémarrage) et est exécuté à l’heure et au jour spécifiés de la semaine ou du mois.</span><span class="sxs-lookup"><span data-stu-id="a7872-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="a7872-335">Si l’ordinateur n’est pas actif ou si le service planifié n’est pas en cours d’exécution à l’heure de travail spécifiée, le service de planification exécute le travail spécifié le jour suivant à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a7872-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="a7872-336">Les travaux sont planifiés en fonction du temps universel coordonné (UTC, Universal Time Coordinated) avec décalage de décalage par rapport à l’heure GMT (Greenwich Mean Time), ce qui signifie qu’un travail peut être spécifié à l’aide de n’importe quel fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="a7872-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="a7872-337">La **classe \_ ScheduledJob Win32** retourne l’heure locale avec décalage UTC lors de l’énumération d’un objet et convertit en heure locale lors de la création de nouveaux travaux.</span><span class="sxs-lookup"><span data-stu-id="a7872-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="a7872-338">Par exemple, un travail spécifié pour s’exécuter sur un ordinateur de Boston à 10:30 h 00.</span><span class="sxs-lookup"><span data-stu-id="a7872-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="a7872-339">Le lundi heure du Pacifique sera planifié pour s’exécuter en local à 1:30 h 00</span><span class="sxs-lookup"><span data-stu-id="a7872-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="a7872-340">Mardi est.</span><span class="sxs-lookup"><span data-stu-id="a7872-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="a7872-341">Un client doit prendre en compte si l’heure d’été est en cours d’exécution sur l’ordinateur local, et si c’est le cas, soustraire un décalage de 60 minutes à partir de l’offset UTC.</span><span class="sxs-lookup"><span data-stu-id="a7872-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="a7872-342">La classe **Win32 \_ ScheduledJob** est dérivée de la [**\_ tâche CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="a7872-343">Vous devez être membre du groupe administrateurs pour créer une tâche planifiée à l’aide de cette classe.</span><span class="sxs-lookup"><span data-stu-id="a7872-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="a7872-344">La classe **Win32 \_ ScheduledJob** utilise en interne le protocole at, qui est lié à la désapprobation à partir de Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a7872-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="a7872-345">Dans un premier temps, le protocole AT est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="a7872-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="a7872-346">Si le protocole est désactivé, par exemple, l’appel de la méthode [**Create**](create-method-in-class-win32-scheduledjob.md) sur un objet **Win32 \_ ScheduledJob** échoue avec l’erreur 0x8.</span><span class="sxs-lookup"><span data-stu-id="a7872-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="a7872-347">Vous pouvez réactiver le protocole AT en ajoutant l’entrée de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="a7872-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="a7872-348">Vous devrez peut-être redémarrer l’ordinateur pour que le paramètre soit effectif.</span><span class="sxs-lookup"><span data-stu-id="a7872-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="a7872-349">Étant donné que **Win32 \_ ScheduledJob** est basé sur l’API Win32 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , vous ne pouvez pas utiliser cette classe conjointement avec l’planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a7872-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="a7872-350">Si vous souhaitez utiliser Planificateur de tâches, utilisez l’API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a7872-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="a7872-351">Pour plus d’informations, consultez la [référence planificateur de tâches](../taskschd/task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a7872-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7872-352">Exemples</span><span class="sxs-lookup"><span data-stu-id="a7872-352">Examples</span></span>

<span data-ttu-id="a7872-353">L’exemple de code VBScript suivant planifie l’exécution de Notepad.exe de manière interactive à 1:25 par l’heure de l’ordinateur local tous les mercredis.</span><span class="sxs-lookup"><span data-stu-id="a7872-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="a7872-354">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7872-354">Requirements</span></span>



| <span data-ttu-id="a7872-355">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7872-355">Requirement</span></span> | <span data-ttu-id="a7872-356">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7872-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7872-357">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7872-357">Minimum supported client</span></span><br/> | <span data-ttu-id="a7872-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7872-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7872-359">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7872-359">Minimum supported server</span></span><br/> | <span data-ttu-id="a7872-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7872-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7872-361">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7872-361">Namespace</span></span><br/>                | <span data-ttu-id="a7872-362">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a7872-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7872-363">MOF</span><span class="sxs-lookup"><span data-stu-id="a7872-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7872-364"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7872-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7872-365">DLL</span><span class="sxs-lookup"><span data-stu-id="a7872-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7872-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7872-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7872-367">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7872-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7872-368">**\_Travail CIM**</span><span class="sxs-lookup"><span data-stu-id="a7872-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="a7872-369">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a7872-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a7872-370">Tâches WMI : tâches planifiées</span><span class="sxs-lookup"><span data-stu-id="a7872-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
