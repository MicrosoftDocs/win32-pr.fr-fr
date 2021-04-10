---
description: La \_ classe de processus CIM représente une instance unique d’un programme en cours d’exécution. Un utilisateur voit généralement un processus sous la forme d’une application ou d’une tâche.
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: Classe CIM_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950831"
---
# <a name="cim_process-class"></a><span data-ttu-id="d10a4-104">\_Classe de processus CIM</span><span class="sxs-lookup"><span data-stu-id="d10a4-104">CIM\_Process class</span></span>

<span data-ttu-id="d10a4-105">La classe de **\_ processus CIM** représente une instance unique d’un programme en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d10a4-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="d10a4-106">Un utilisateur voit généralement un processus sous la forme d’une application ou d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="d10a4-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="d10a4-107">Un processus est défini par un espace de travail des ressources mémoire et des paramètres environnementaux qui lui sont alloués.</span><span class="sxs-lookup"><span data-stu-id="d10a4-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="d10a4-108">Sur un système multitâche, l’espace de travail empêche les intrusions de ressources par d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="d10a4-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="d10a4-109">En outre, un processus peut s’exécuter en tant que threads multiples, qui s’exécutent dans le même espace de travail.</span><span class="sxs-lookup"><span data-stu-id="d10a4-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d10a4-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d10a4-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d10a4-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d10a4-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d10a4-112">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d10a4-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d10a4-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d10a4-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10a4-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d10a4-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="d10a4-115">Membres</span><span class="sxs-lookup"><span data-stu-id="d10a4-115">Members</span></span>

<span data-ttu-id="d10a4-116">La classe de **\_ processus CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d10a4-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="d10a4-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d10a4-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d10a4-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d10a4-118">Properties</span></span>

<span data-ttu-id="d10a4-119">La classe de **\_ processus CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d10a4-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d10a4-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d10a4-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-123">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-124">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d10a4-124">Short textual description of the object.</span></span>

<span data-ttu-id="d10a4-125">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-126">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d10a4-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-129">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="d10a4-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-130">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d10a4-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d10a4-131">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="d10a4-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="d10a4-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-133">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d10a4-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-135">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="d10a4-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-136">Heure à laquelle le processus a commencé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="d10a4-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-137">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d10a4-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-140">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="d10a4-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-141">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d10a4-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="d10a4-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-145">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="d10a4-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-146">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d10a4-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-147">**Description**</span><span class="sxs-lookup"><span data-stu-id="d10a4-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-150">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d10a4-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-151">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d10a4-151">Textual description of the object.</span></span>

<span data-ttu-id="d10a4-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="d10a4-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d10a4-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-156">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« état d’exécution »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-157">État de fonctionnement actuel du processus.</span><span class="sxs-lookup"><span data-stu-id="d10a4-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d10a4-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d10a4-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d10a4-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d10a4-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="d10a4-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Prêt** (2)</span><span class="sxs-lookup"><span data-stu-id="d10a4-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="d10a4-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="d10a4-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="d10a4-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqué** (4)</span><span class="sxs-lookup"><span data-stu-id="d10a4-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="d10a4-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspendu bloqué** (5)</span><span class="sxs-lookup"><span data-stu-id="d10a4-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d10a4-164">Suspendu bloqué</span><span class="sxs-lookup"><span data-stu-id="d10a4-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="d10a4-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendu prêt** (6)</span><span class="sxs-lookup"><span data-stu-id="d10a4-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d10a4-166">Suspendu prêt</span><span class="sxs-lookup"><span data-stu-id="d10a4-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="d10a4-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminé** (7)</span><span class="sxs-lookup"><span data-stu-id="d10a4-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="d10a4-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (8)</span><span class="sxs-lookup"><span data-stu-id="d10a4-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="d10a4-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Développement** (9)</span><span class="sxs-lookup"><span data-stu-id="d10a4-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d10a4-170">**Handle**</span><span class="sxs-lookup"><span data-stu-id="d10a4-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-173">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« handle »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-174">Identifie le processus.</span><span class="sxs-lookup"><span data-stu-id="d10a4-174">Identifies the process.</span></span> <span data-ttu-id="d10a4-175">Un identificateur de processus est un type de handle de processus.</span><span class="sxs-lookup"><span data-stu-id="d10a4-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d10a4-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-177">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d10a4-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-179">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d10a4-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-180">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d10a4-180">Date and time the object was installed.</span></span> <span data-ttu-id="d10a4-181">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d10a4-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d10a4-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-183">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="d10a4-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-184">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d10a4-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-186">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« heure du modèle de noyau »), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-187">Temps en mode noyau, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="d10a4-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="d10a4-188">Si ces informations ne sont pas disponibles, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d10a4-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="d10a4-189">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d10a4-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-190">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d10a4-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-193">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d10a4-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-194">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d10a4-194">Label by which the object is known.</span></span> <span data-ttu-id="d10a4-195">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d10a4-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d10a4-196">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-197">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d10a4-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-200">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système d’exploitation ")</span><span class="sxs-lookup"><span data-stu-id="d10a4-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-201">Portée du nom de la classe de création du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d10a4-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="d10a4-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-205">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système d’exploitation ")</span><span class="sxs-lookup"><span data-stu-id="d10a4-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-206">Étendue du nom du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d10a4-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-207">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="d10a4-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d10a4-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-210">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Priority »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-211">Urgence ou importance de l’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="d10a4-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="d10a4-212">Si aucune priorité n’est définie pour un processus, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d10a4-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-213">**État**</span><span class="sxs-lookup"><span data-stu-id="d10a4-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d10a4-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-216">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d10a4-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-217">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d10a4-217">Current status of the object.</span></span>

<span data-ttu-id="d10a4-218">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d10a4-219">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d10a4-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d10a4-220">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d10a4-221">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d10a4-222">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d10a4-223">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d10a4-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d10a4-224">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d10a4-225">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d10a4-226">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d10a4-227">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d10a4-228">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d10a4-229">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d10a4-230">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d10a4-231">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d10a4-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="d10a4-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-233">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d10a4-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-235">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date d’arrêt")</span><span class="sxs-lookup"><span data-stu-id="d10a4-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-236">Heure à laquelle le processus a été arrêté ou arrêté.</span><span class="sxs-lookup"><span data-stu-id="d10a4-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-237">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="d10a4-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-238">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d10a4-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-240">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« temps mode utilisateur »), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-241">Heure en mode utilisateur, en unités de nanosecondes 100.</span><span class="sxs-lookup"><span data-stu-id="d10a4-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="d10a4-242">Si ces informations ne sont pas disponibles, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d10a4-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="d10a4-243">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d10a4-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d10a4-244">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="d10a4-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10a4-245">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d10a4-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d10a4-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10a4-247">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« taille de la plage de travail »), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« octets »)</span><span class="sxs-lookup"><span data-stu-id="d10a4-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d10a4-248">Quantité de mémoire, en octets, qu’un processus doit exécuter efficacement pour un système d’exploitation qui utilise la gestion de la mémoire basée sur les pages.</span><span class="sxs-lookup"><span data-stu-id="d10a4-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="d10a4-249">Si le système ne dispose pas de suffisamment de mémoire (inférieure à la taille de la plage de travail), une surcharge se produit.</span><span class="sxs-lookup"><span data-stu-id="d10a4-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="d10a4-250">Si la taille de la plage de travail n’est pas connue, utilisez la **valeur null** ou 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d10a4-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="d10a4-251">Si vous fournissez des données de jeu de travail, vous pouvez surveiller les informations pour comprendre les besoins en mémoire en constante évolution d’un processus.</span><span class="sxs-lookup"><span data-stu-id="d10a4-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="d10a4-252">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d10a4-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d10a4-253">Notes</span><span class="sxs-lookup"><span data-stu-id="d10a4-253">Remarks</span></span>

<span data-ttu-id="d10a4-254">La classe de **\_ processus CIM** est dérivée de la [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="d10a4-255">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d10a4-255">WMI does not implement this class.</span></span> <span data-ttu-id="d10a4-256">Pour les classes WMI dérivées du **\_ processus CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d10a4-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d10a4-257">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d10a4-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d10a4-258">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d10a4-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10a4-259">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d10a4-259">Requirements</span></span>



| <span data-ttu-id="d10a4-260">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d10a4-260">Requirement</span></span> | <span data-ttu-id="d10a4-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="d10a4-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d10a4-262">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d10a4-262">Minimum supported client</span></span><br/> | <span data-ttu-id="d10a4-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d10a4-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d10a4-264">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d10a4-264">Minimum supported server</span></span><br/> | <span data-ttu-id="d10a4-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d10a4-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d10a4-266">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d10a4-266">Namespace</span></span><br/>                | <span data-ttu-id="d10a4-267">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d10a4-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d10a4-268">MOF</span><span class="sxs-lookup"><span data-stu-id="d10a4-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d10a4-269"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d10a4-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d10a4-270">DLL</span><span class="sxs-lookup"><span data-stu-id="d10a4-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d10a4-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d10a4-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10a4-272">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d10a4-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10a4-273">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d10a4-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

