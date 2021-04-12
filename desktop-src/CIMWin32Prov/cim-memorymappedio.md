---
description: La \_ classe CIM MemoryMappedIO représente l’architecture d’ordinateur des e/s mappées en mémoire. Cette classe résout les ressources de mémoire et d’e/s de port.
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: Classe CIM_MemoryMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033726"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="40c78-104">\_Classe CIM MemoryMappedIO</span><span class="sxs-lookup"><span data-stu-id="40c78-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="40c78-105">La classe **CIM \_ MemoryMappedIO** représente l’architecture d’ordinateur des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="40c78-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="40c78-106">Cette classe résout les ressources de mémoire et d’e/s de port.</span><span class="sxs-lookup"><span data-stu-id="40c78-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40c78-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="40c78-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="40c78-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="40c78-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="40c78-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="40c78-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="40c78-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="40c78-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c78-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40c78-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="40c78-112">Membres</span><span class="sxs-lookup"><span data-stu-id="40c78-112">Members</span></span>

<span data-ttu-id="40c78-113">La classe **CIM \_ MemoryMappedIO** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="40c78-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="40c78-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40c78-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40c78-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40c78-115">Properties</span></span>

<span data-ttu-id="40c78-116">La classe **CIM \_ MemoryMappedIO** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="40c78-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40c78-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="40c78-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="40c78-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="40c78-121">A short textual description of the object.</span></span>

<span data-ttu-id="40c78-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40c78-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="40c78-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-126">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40c78-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40c78-127">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="40c78-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="40c78-128">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="40c78-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="40c78-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="40c78-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-132">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="40c78-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="40c78-133">Propriété **CreationClassName** du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="40c78-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="40c78-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="40c78-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-137">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40c78-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40c78-138">Propriété de **nom** de l’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="40c78-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="40c78-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="40c78-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-142">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="40c78-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-143">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="40c78-143">A textual description of the object.</span></span>

<span data-ttu-id="40c78-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40c78-145">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="40c78-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-146">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40c78-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s mappées en mémoire DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="40c78-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-149">Adresse de fin des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="40c78-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="40c78-150">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40c78-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="40c78-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40c78-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-152">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="40c78-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-154">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="40c78-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-155">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="40c78-155">Indicates when the object was installed.</span></span> <span data-ttu-id="40c78-156">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="40c78-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="40c78-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40c78-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="40c78-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-161">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="40c78-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-162">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="40c78-162">Label by which the object is known.</span></span> <span data-ttu-id="40c78-163">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="40c78-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="40c78-164">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40c78-165">**De la**</span><span class="sxs-lookup"><span data-stu-id="40c78-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-166">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40c78-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-168">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s mappées en mémoire DMTF \| 001,1»)</span><span class="sxs-lookup"><span data-stu-id="40c78-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-169">Adresse de début des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="40c78-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="40c78-170">La propriété de l’identificateur de ressource matérielle doit être définie sur cette valeur pour construire la clé de ressource d’e/s mappée.</span><span class="sxs-lookup"><span data-stu-id="40c78-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="40c78-171">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40c78-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="40c78-172">**État**</span><span class="sxs-lookup"><span data-stu-id="40c78-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40c78-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40c78-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40c78-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40c78-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40c78-175">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="40c78-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="40c78-176">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="40c78-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="40c78-177">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="40c78-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="40c78-178">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="40c78-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="40c78-179">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="40c78-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="40c78-180">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="40c78-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="40c78-181">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="40c78-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="40c78-182">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="40c78-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="40c78-183">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="40c78-184">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="40c78-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="40c78-185">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="40c78-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="40c78-186">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="40c78-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40c78-187">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="40c78-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40c78-188">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="40c78-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="40c78-189">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="40c78-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="40c78-190">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="40c78-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="40c78-191">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="40c78-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="40c78-192">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="40c78-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="40c78-193">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="40c78-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="40c78-194">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="40c78-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="40c78-195">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="40c78-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="40c78-196">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="40c78-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="40c78-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="40c78-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="40c78-198">Notes</span><span class="sxs-lookup"><span data-stu-id="40c78-198">Remarks</span></span>

<span data-ttu-id="40c78-199">La classe **CIM \_ MemoryMappedIO** est dérivée de [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="40c78-200">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="40c78-200">WMI does not implement this class.</span></span> <span data-ttu-id="40c78-201">Pour les classes dérivées de **CIM \_ MemoryMappedIO**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="40c78-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="40c78-202">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="40c78-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="40c78-203">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="40c78-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c78-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40c78-204">Requirements</span></span>



| <span data-ttu-id="40c78-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40c78-205">Requirement</span></span> | <span data-ttu-id="40c78-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="40c78-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40c78-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c78-207">Minimum supported client</span></span><br/> | <span data-ttu-id="40c78-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40c78-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40c78-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c78-209">Minimum supported server</span></span><br/> | <span data-ttu-id="40c78-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40c78-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40c78-211">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="40c78-211">Namespace</span></span><br/>                | <span data-ttu-id="40c78-212">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="40c78-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40c78-213">MOF</span><span class="sxs-lookup"><span data-stu-id="40c78-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40c78-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40c78-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40c78-215">DLL</span><span class="sxs-lookup"><span data-stu-id="40c78-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40c78-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40c78-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c78-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40c78-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c78-218">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="40c78-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

