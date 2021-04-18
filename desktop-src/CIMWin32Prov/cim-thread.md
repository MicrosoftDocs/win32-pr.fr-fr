---
description: La \_ classe de thread CIM représente la capacité d’exécuter des unités d’un processus ou d’une tâche, en parallèle. Un processus peut avoir de nombreux threads, chacun d’entre eux étant faible au processus.
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: Classe CIM_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519232"
---
# <a name="cim_thread-class"></a><span data-ttu-id="256c2-104">\_Classe de thread CIM</span><span class="sxs-lookup"><span data-stu-id="256c2-104">CIM\_Thread class</span></span>

<span data-ttu-id="256c2-105">La classe de **\_ thread CIM** représente la capacité d’exécuter des unités d’un processus ou d’une tâche, en parallèle.</span><span class="sxs-lookup"><span data-stu-id="256c2-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="256c2-106">Un processus peut avoir de nombreux threads, chacun d’entre eux étant faible au processus.</span><span class="sxs-lookup"><span data-stu-id="256c2-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="256c2-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="256c2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="256c2-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="256c2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="256c2-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="256c2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="256c2-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="256c2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="256c2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="256c2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
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
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="256c2-112">Membres</span><span class="sxs-lookup"><span data-stu-id="256c2-112">Members</span></span>

<span data-ttu-id="256c2-113">La classe de **\_ thread CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="256c2-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="256c2-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="256c2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="256c2-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="256c2-115">Properties</span></span>

<span data-ttu-id="256c2-116">La classe de **\_ thread CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="256c2-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="256c2-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="256c2-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="256c2-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-121">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="256c2-121">Short textual description of the object.</span></span>

<span data-ttu-id="256c2-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="256c2-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="256c2-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-126">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-127">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="256c2-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="256c2-128">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="256c2-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="256c2-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-132">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processus CIM**](cim-process.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-133">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="256c2-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="256c2-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-137">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processus CIM**](cim-process.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-138">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="256c2-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="256c2-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-142">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="256c2-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-143">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="256c2-143">Textual description of the object.</span></span>

<span data-ttu-id="256c2-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="256c2-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="256c2-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="256c2-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="256c2-148">Indique la condition de fonctionnement actuelle du thread.</span><span class="sxs-lookup"><span data-stu-id="256c2-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="256c2-149">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="256c2-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="256c2-150">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="256c2-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="256c2-151">**Prêt** (2)</span><span class="sxs-lookup"><span data-stu-id="256c2-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="256c2-152">**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="256c2-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="256c2-153">**Bloqué** (4)</span><span class="sxs-lookup"><span data-stu-id="256c2-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="256c2-154">**Suspendu bloqué** (5)</span><span class="sxs-lookup"><span data-stu-id="256c2-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="256c2-155">**Suspendu prêt** (6)</span><span class="sxs-lookup"><span data-stu-id="256c2-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="256c2-156">**Handle**</span><span class="sxs-lookup"><span data-stu-id="256c2-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-159">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-160">Identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="256c2-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="256c2-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-162">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="256c2-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-164">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="256c2-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-165">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="256c2-165">Date and time the object was installed.</span></span> <span data-ttu-id="256c2-166">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="256c2-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="256c2-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="256c2-168">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="256c2-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-169">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="256c2-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-171">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="256c2-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-172">Temps, en mode noyau, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="256c2-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="256c2-173">Si ces informations ne sont pas disponibles, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="256c2-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="256c2-174">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="256c2-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="256c2-175">**Nom**</span><span class="sxs-lookup"><span data-stu-id="256c2-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-178">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="256c2-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-179">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="256c2-179">Label by which the object is known.</span></span> <span data-ttu-id="256c2-180">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="256c2-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="256c2-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="256c2-182">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="256c2-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-185">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processus CIM**](cim-process.md).**OSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-186">Portée du nom de la classe de création du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="256c2-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="256c2-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-190">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processus CIM**](cim-process.md).**OSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-191">Étendue du nom du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="256c2-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-192">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="256c2-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="256c2-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="256c2-195">Urgence de l’exécution d’un thread.</span><span class="sxs-lookup"><span data-stu-id="256c2-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="256c2-196">Un thread peut avoir une priorité différente de celle de son processus propriétaire.</span><span class="sxs-lookup"><span data-stu-id="256c2-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="256c2-197">Si ces informations ne sont pas disponibles pour un thread, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="256c2-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-198">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="256c2-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-201">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processus CIM**](cim-process.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-202">Nom de la classe de création du processus de portée.</span><span class="sxs-lookup"><span data-stu-id="256c2-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-203">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="256c2-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-206">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processus CIM**](cim-process.md).**Handle**"), [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="256c2-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="256c2-207">Handle du processus d’étendue.</span><span class="sxs-lookup"><span data-stu-id="256c2-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="256c2-208">**État**</span><span class="sxs-lookup"><span data-stu-id="256c2-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="256c2-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-211">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="256c2-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-212">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="256c2-212">Current status of the object.</span></span> <span data-ttu-id="256c2-213">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="256c2-214">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="256c2-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="256c2-215">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="256c2-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="256c2-216">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="256c2-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="256c2-217">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="256c2-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="256c2-218">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="256c2-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="256c2-219">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="256c2-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="256c2-220">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="256c2-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="256c2-221">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="256c2-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="256c2-222">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="256c2-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="256c2-223">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="256c2-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="256c2-224">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="256c2-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="256c2-225">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="256c2-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="256c2-226">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="256c2-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="256c2-227">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="256c2-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="256c2-228">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="256c2-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="256c2-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="256c2-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="256c2-230">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="256c2-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="256c2-231">Temps, en mode utilisateur, en unités de nanosecondes 100.</span><span class="sxs-lookup"><span data-stu-id="256c2-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="256c2-232">Si ces informations ne sont pas disponibles, la valeur 0 (zéro) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="256c2-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="256c2-233">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="256c2-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="256c2-234">Notes</span><span class="sxs-lookup"><span data-stu-id="256c2-234">Remarks</span></span>

<span data-ttu-id="256c2-235">La classe de **\_ thread CIM** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="256c2-236">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="256c2-236">WMI does not implement this class.</span></span> <span data-ttu-id="256c2-237">Pour les classes WMI dérivées du **\_ thread CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="256c2-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="256c2-238">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="256c2-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="256c2-239">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="256c2-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="256c2-240">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="256c2-240">Requirements</span></span>



| <span data-ttu-id="256c2-241">Condition requise</span><span class="sxs-lookup"><span data-stu-id="256c2-241">Requirement</span></span> | <span data-ttu-id="256c2-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="256c2-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="256c2-243">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="256c2-243">Minimum supported client</span></span><br/> | <span data-ttu-id="256c2-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="256c2-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="256c2-245">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="256c2-245">Minimum supported server</span></span><br/> | <span data-ttu-id="256c2-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="256c2-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="256c2-247">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="256c2-247">Namespace</span></span><br/>                | <span data-ttu-id="256c2-248">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="256c2-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="256c2-249">MOF</span><span class="sxs-lookup"><span data-stu-id="256c2-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="256c2-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="256c2-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="256c2-251">DLL</span><span class="sxs-lookup"><span data-stu-id="256c2-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="256c2-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="256c2-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256c2-253">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="256c2-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256c2-254">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="256c2-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

