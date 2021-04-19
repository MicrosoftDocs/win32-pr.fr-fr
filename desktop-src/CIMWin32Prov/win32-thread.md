---
description: Le \_ thread Win32&\# 8194 ; La classe WMI représente un thread d’exécution.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Classe Win32_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515176"
---
# <a name="win32_thread-class"></a><span data-ttu-id="91d91-103">\_Classe de thread Win32</span><span class="sxs-lookup"><span data-stu-id="91d91-103">Win32\_Thread class</span></span>

<span data-ttu-id="91d91-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) du **\_ thread Win32** représente un thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="91d91-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="91d91-105">Lorsqu’un processus doit avoir un thread d’exécution, le processus peut créer d’autres threads pour exécuter des tâches en parallèle.</span><span class="sxs-lookup"><span data-stu-id="91d91-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="91d91-106">Les threads partagent l’environnement de processus, de sorte que plusieurs threads sous le même processus utilisent moins de mémoire que le même nombre de processus.</span><span class="sxs-lookup"><span data-stu-id="91d91-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="91d91-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="91d91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="91d91-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="91d91-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d91-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91d91-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="91d91-110">Membres</span><span class="sxs-lookup"><span data-stu-id="91d91-110">Members</span></span>

<span data-ttu-id="91d91-111">La classe de **\_ thread Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="91d91-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="91d91-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91d91-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91d91-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91d91-113">Properties</span></span>

<span data-ttu-id="91d91-114">La classe de **\_ thread Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="91d91-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91d91-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="91d91-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-118">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="91d91-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-119">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91d91-119">Short description of the object.</span></span>

<span data-ttu-id="91d91-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91d91-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-124">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91d91-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d91-125">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="91d91-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="91d91-126">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="91d91-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="91d91-127">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-128">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91d91-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-131">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**\_ processus CIM**](cim-process.md).**CSCreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91d91-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d91-132">Nom de la classe de création du système d’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="91d91-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="91d91-133">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="91d91-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-137">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**\_ processus CIM**](cim-process.md).**CSName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91d91-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d91-138">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="91d91-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="91d91-139">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-140">**Description**</span><span class="sxs-lookup"><span data-stu-id="91d91-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-143">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="91d91-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-144">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91d91-144">Description of the object.</span></span>

<span data-ttu-id="91d91-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-146">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="91d91-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-147">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91d91-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-149">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| performance data structures performance \| [**\_ \_ type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="91d91-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-150">Durée totale d’exécution, en millisecondes, accordée à ce thread depuis sa création.</span><span class="sxs-lookup"><span data-stu-id="91d91-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="91d91-151">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="91d91-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91d91-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91d91-155">Condition de fonctionnement actuelle du thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="91d91-156">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91d91-157">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="91d91-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91d91-158">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="91d91-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="91d91-159">**Prêt** (2)</span><span class="sxs-lookup"><span data-stu-id="91d91-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="91d91-160">**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="91d91-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="91d91-161">**Bloqué** (4)</span><span class="sxs-lookup"><span data-stu-id="91d91-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="91d91-162">**Suspendu bloqué** (5)</span><span class="sxs-lookup"><span data-stu-id="91d91-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="91d91-163">**Suspendu prêt** (6)</span><span class="sxs-lookup"><span data-stu-id="91d91-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91d91-164">**Handle**</span><span class="sxs-lookup"><span data-stu-id="91d91-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-167">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Tool Help structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")</span><span class="sxs-lookup"><span data-stu-id="91d91-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-168">Handle vers un thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-168">Handle to a thread.</span></span> <span data-ttu-id="91d91-169">Par défaut, le descripteur dispose de droits d’accès complets.</span><span class="sxs-lookup"><span data-stu-id="91d91-169">The handle has full access rights by default.</span></span> <span data-ttu-id="91d91-170">Avec l’accès de sécurité approprié, le handle peut être utilisé dans toute fonction qui accepte un handle de thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="91d91-171">En fonction de l’indicateur d’héritage spécifié lors de sa création, ce handle peut être hérité par les processus enfants.</span><span class="sxs-lookup"><span data-stu-id="91d91-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="91d91-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="91d91-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-173">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="91d91-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-175">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="91d91-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-176">L’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="91d91-176">Object was installed.</span></span> <span data-ttu-id="91d91-177">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="91d91-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="91d91-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-179">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="91d91-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-180">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91d91-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-182">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| données de performance structures de données \| [**perf \_ \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanosecondes")</span><span class="sxs-lookup"><span data-stu-id="91d91-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-183">Temps en mode noyau, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="91d91-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="91d91-184">Si ces informations ne sont pas disponibles, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="91d91-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="91d91-185">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-186">**Nom**</span><span class="sxs-lookup"><span data-stu-id="91d91-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-189">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="91d91-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-190">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="91d91-190">Label by which the object is known.</span></span> <span data-ttu-id="91d91-191">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="91d91-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="91d91-192">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-193">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91d91-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-196">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**\_ processus CIM**](cim-process.md).**OSCreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91d91-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d91-197">Nom de la classe de création du système d’exploitation d’étendue.</span><span class="sxs-lookup"><span data-stu-id="91d91-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="91d91-198">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="91d91-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-202">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**\_ processus CIM**](cim-process.md).**OSName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91d91-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d91-203">Nom du système d’exploitation de portée.</span><span class="sxs-lookup"><span data-stu-id="91d91-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="91d91-204">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-205">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="91d91-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-206">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d91-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-208">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (« Priority »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Tool structures Help structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri »)</span><span class="sxs-lookup"><span data-stu-id="91d91-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-209">Priorité dynamique du thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="91d91-210">Chaque thread a une priorité dynamique que le planificateur utilise pour déterminer le thread à exécuter.</span><span class="sxs-lookup"><span data-stu-id="91d91-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="91d91-211">Initialement, la priorité dynamique d’un thread est identique à sa priorité de base.</span><span class="sxs-lookup"><span data-stu-id="91d91-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="91d91-212">Le système peut augmenter et diminuer la priorité dynamique pour s’assurer qu’il est réactif (garantissant qu’aucun thread n’est privé pour le temps processeur).</span><span class="sxs-lookup"><span data-stu-id="91d91-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="91d91-213">Le système n’augmente pas la priorité des threads avec un niveau de priorité de base compris entre 16 et 31.</span><span class="sxs-lookup"><span data-stu-id="91d91-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="91d91-214">Seuls les threads dont la priorité de base est comprise entre 0 et 15 reçoivent une priorité dynamique.</span><span class="sxs-lookup"><span data-stu-id="91d91-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="91d91-215">Des valeurs plus élevées indiquent des priorités plus élevées.</span><span class="sxs-lookup"><span data-stu-id="91d91-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="91d91-216">**PriorityBase**</span><span class="sxs-lookup"><span data-stu-id="91d91-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-217">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d91-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-219">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| performance data structures \| [**perf \_ \_ type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase")</span><span class="sxs-lookup"><span data-stu-id="91d91-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-220">Priorité de base actuelle d’un thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-220">Current base priority of a thread.</span></span> <span data-ttu-id="91d91-221">Le système d’exploitation peut augmenter la priorité dynamique du thread au-dessus de la priorité de base si le thread gère l’entrée d’utilisateur, ou le réduire vers la priorité de base si le thread devient lié au calcul.</span><span class="sxs-lookup"><span data-stu-id="91d91-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="91d91-222">La valeur de la propriété **PriorityBase** peut être comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="91d91-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="91d91-223">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91d91-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-226">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**\_ processus CIM**](cim-process.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91d91-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91d91-227">Valeur de la propriété de processus d’étendue **CreationClassName** .</span><span class="sxs-lookup"><span data-stu-id="91d91-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="91d91-228">Cette propriété est héritée [**du \_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="91d91-229">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="91d91-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-232">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagée**](../wmisdk/standard-qualifiers.md) ("[**\_ processus CIM**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures d’aide de l’outil win32api \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")</span><span class="sxs-lookup"><span data-stu-id="91d91-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-233">Processus qui a créé le thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-233">Process that created the thread.</span></span> <span data-ttu-id="91d91-234">Le contenu de cette propriété peut être utilisé par les éléments de l’interface de programmation d’applications (API) Windows.</span><span class="sxs-lookup"><span data-stu-id="91d91-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="91d91-235">**StartAddress**</span><span class="sxs-lookup"><span data-stu-id="91d91-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-236">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d91-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-238">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WIn32API \| thread Object \| LPTHREAD \_ Start \_ routine \| lpStartAddress »)</span><span class="sxs-lookup"><span data-stu-id="91d91-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-239">Adresse de début du thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-239">Starting address of the thread.</span></span> <span data-ttu-id="91d91-240">Étant donné que toute application disposant d’un accès approprié au thread peut modifier le contexte du thread, cette valeur peut uniquement être une approximation de l’adresse de début du thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="91d91-241">**État**</span><span class="sxs-lookup"><span data-stu-id="91d91-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91d91-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-244">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="91d91-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-245">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91d91-245">Current status of the object.</span></span> <span data-ttu-id="91d91-246">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="91d91-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="91d91-247">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="91d91-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="91d91-248">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="91d91-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="91d91-249">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="91d91-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="91d91-250">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="91d91-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="91d91-251">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="91d91-252">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="91d91-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="91d91-253">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="91d91-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="91d91-254">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="91d91-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91d91-255">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="91d91-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91d91-256">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="91d91-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="91d91-257">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="91d91-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="91d91-258">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="91d91-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="91d91-259">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="91d91-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="91d91-260">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="91d91-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="91d91-261">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="91d91-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="91d91-262">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="91d91-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="91d91-263">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="91d91-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="91d91-264">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="91d91-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91d91-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="91d91-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-266">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d91-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-268">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| État du thread win32api »)</span><span class="sxs-lookup"><span data-stu-id="91d91-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-269">État d’exécution actuel du thread.</span><span class="sxs-lookup"><span data-stu-id="91d91-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="91d91-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialisé** (0)</span><span class="sxs-lookup"><span data-stu-id="91d91-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-271">Initialisé : il est reconnu par le micronoyau.</span><span class="sxs-lookup"><span data-stu-id="91d91-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="91d91-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Prêt** (1)</span><span class="sxs-lookup"><span data-stu-id="91d91-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-273">Ready : il est prêt à s’exécuter sur le processeur disponible suivant.</span><span class="sxs-lookup"><span data-stu-id="91d91-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="91d91-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (2)</span><span class="sxs-lookup"><span data-stu-id="91d91-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-275">En cours d’exécution, il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="91d91-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="91d91-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Veille** (3)</span><span class="sxs-lookup"><span data-stu-id="91d91-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-277">STANDBY : il est sur le point de s’exécuter, un seul thread peut être dans cet État à la fois.</span><span class="sxs-lookup"><span data-stu-id="91d91-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="91d91-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminé** (4)</span><span class="sxs-lookup"><span data-stu-id="91d91-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-279">Terminé : l’exécution est terminée.</span><span class="sxs-lookup"><span data-stu-id="91d91-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="91d91-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>En **attente** (5)</span><span class="sxs-lookup"><span data-stu-id="91d91-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-281">En attente : il n’est pas prêt pour le processeur, lorsque vous êtes prêt, il est replanifié.</span><span class="sxs-lookup"><span data-stu-id="91d91-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="91d91-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span><span class="sxs-lookup"><span data-stu-id="91d91-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-283">Transition : le thread attend des ressources autres que le processeur.</span><span class="sxs-lookup"><span data-stu-id="91d91-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91d91-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (7)</span><span class="sxs-lookup"><span data-stu-id="91d91-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-285">Inconnu : l’état du thread est inconnu.</span><span class="sxs-lookup"><span data-stu-id="91d91-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91d91-286">**ThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="91d91-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-287">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91d91-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-289">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« raison de l' \| attente du thread win32api »)</span><span class="sxs-lookup"><span data-stu-id="91d91-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-290">Raison pour laquelle le thread est en attente.</span><span class="sxs-lookup"><span data-stu-id="91d91-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="91d91-291">Cette valeur est valide uniquement si le membre **ThreadState** a la valeur transition (6).</span><span class="sxs-lookup"><span data-stu-id="91d91-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="91d91-292">Les paires d’événements permettent la communication avec les sous-systèmes protégés.</span><span class="sxs-lookup"><span data-stu-id="91d91-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="91d91-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Exécutif** (0)</span><span class="sxs-lookup"><span data-stu-id="91d91-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="91d91-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span><span class="sxs-lookup"><span data-stu-id="91d91-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="91d91-295">FreePage</span><span class="sxs-lookup"><span data-stu-id="91d91-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="91d91-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Page** (2)</span><span class="sxs-lookup"><span data-stu-id="91d91-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="91d91-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span><span class="sxs-lookup"><span data-stu-id="91d91-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="91d91-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span><span class="sxs-lookup"><span data-stu-id="91d91-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="91d91-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span><span class="sxs-lookup"><span data-stu-id="91d91-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="91d91-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Page** (6)</span><span class="sxs-lookup"><span data-stu-id="91d91-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="91d91-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span><span class="sxs-lookup"><span data-stu-id="91d91-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="91d91-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span><span class="sxs-lookup"><span data-stu-id="91d91-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="91d91-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Page** (9)</span><span class="sxs-lookup"><span data-stu-id="91d91-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="91d91-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span><span class="sxs-lookup"><span data-stu-id="91d91-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="91d91-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span><span class="sxs-lookup"><span data-stu-id="91d91-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="91d91-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span><span class="sxs-lookup"><span data-stu-id="91d91-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="91d91-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Page** (13)</span><span class="sxs-lookup"><span data-stu-id="91d91-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="91d91-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span><span class="sxs-lookup"><span data-stu-id="91d91-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="91d91-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span><span class="sxs-lookup"><span data-stu-id="91d91-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="91d91-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span><span class="sxs-lookup"><span data-stu-id="91d91-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="91d91-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span><span class="sxs-lookup"><span data-stu-id="91d91-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="91d91-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span><span class="sxs-lookup"><span data-stu-id="91d91-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="91d91-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**Du pageout.** (19)</span><span class="sxs-lookup"><span data-stu-id="91d91-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91d91-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (20)</span><span class="sxs-lookup"><span data-stu-id="91d91-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91d91-315">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="91d91-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d91-316">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91d91-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91d91-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91d91-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d91-318">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| données de performance structures de données \| [**perf \_ \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanosecondes")</span><span class="sxs-lookup"><span data-stu-id="91d91-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="91d91-319">Temps en mode utilisateur, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="91d91-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="91d91-320">Si ces informations ne sont pas disponibles, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="91d91-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="91d91-321">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91d91-322">Notes</span><span class="sxs-lookup"><span data-stu-id="91d91-322">Remarks</span></span>

<span data-ttu-id="91d91-323">La classe de **\_ thread Win32** est dérivée du [**\_ thread CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="91d91-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="91d91-324">**Vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="91d91-324">**Overview**</span></span>

<span data-ttu-id="91d91-325">Pour une analyse quotidienne quotidienne, il est généralement peu utile d’avoir une liste détaillée des threads et leurs propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="91d91-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="91d91-326">Les ordinateurs créent et suppriment des milliers de threads au cours d’une journée, et peu de ces créations ou suppressions sont significatives pour toute personne, mais le développeur qui a écrit le logiciel.</span><span class="sxs-lookup"><span data-stu-id="91d91-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="91d91-327">Toutefois, lorsque vous résolvez les problèmes liés à une application, le suivi des threads individuels d’un processus vous permet d’identifier le moment où les threads sont créés et le moment où ils sont détruits.</span><span class="sxs-lookup"><span data-stu-id="91d91-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="91d91-328">Étant donné que les threads créés mais non détruits entraînent des fuites de mémoire, le suivi des threads individuels peut être utile pour les techniciens du support technique.</span><span class="sxs-lookup"><span data-stu-id="91d91-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="91d91-329">De même, l’identification des priorités des threads peut aider à identifier les threads qui, en s’exécutant à une priorité anormalement élevée, prétendent les cycles processeur requis par d’autres threads et d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="91d91-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="91d91-330">**Utilisation du \_ thread Win32**</span><span class="sxs-lookup"><span data-stu-id="91d91-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="91d91-331">Comme impliqué dans le bloc de syntaxe précédent, la classe de **\_ thread Win32** ne signale pas le nom du processus sous lequel chaque thread s’exécute.</span><span class="sxs-lookup"><span data-stu-id="91d91-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="91d91-332">Au lieu de cela, il signale l’ID du processus sous lequel le thread s’exécute.</span><span class="sxs-lookup"><span data-stu-id="91d91-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="91d91-333">Pour retourner le nom d’un processus et une liste de tous ses threads, votre script doit :</span><span class="sxs-lookup"><span data-stu-id="91d91-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="91d91-334">Connectez-vous à la classe de [**\_ processus Win32**](win32-process.md) et retournez la liste des processus et leurs ID de processus.</span><span class="sxs-lookup"><span data-stu-id="91d91-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="91d91-335">Stockez temporairement ces informations dans un objet de tableau ou de dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="91d91-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="91d91-336">Pour chaque ID de processus, retournez la liste des threads de ce processus, puis affichez le nom du processus et la liste des threads.</span><span class="sxs-lookup"><span data-stu-id="91d91-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="91d91-337">Exemples</span><span class="sxs-lookup"><span data-stu-id="91d91-337">Examples</span></span>

<span data-ttu-id="91d91-338">L’exemple VBScript suivant surveille les threads en cours d’exécution sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="91d91-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="91d91-339">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91d91-339">Requirements</span></span>



| <span data-ttu-id="91d91-340">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91d91-340">Requirement</span></span> | <span data-ttu-id="91d91-341">Valeur</span><span class="sxs-lookup"><span data-stu-id="91d91-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91d91-342">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d91-342">Minimum supported client</span></span><br/> | <span data-ttu-id="91d91-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91d91-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91d91-344">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d91-344">Minimum supported server</span></span><br/> | <span data-ttu-id="91d91-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91d91-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91d91-346">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91d91-346">Namespace</span></span><br/>                | <span data-ttu-id="91d91-347">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="91d91-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91d91-348">MOF</span><span class="sxs-lookup"><span data-stu-id="91d91-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91d91-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91d91-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91d91-350">DLL</span><span class="sxs-lookup"><span data-stu-id="91d91-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d91-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91d91-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d91-352">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91d91-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d91-353">**\_Thread CIM**</span><span class="sxs-lookup"><span data-stu-id="91d91-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="91d91-354">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="91d91-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
