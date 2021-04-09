---
description: La \_ classe WMI SystemMemoryResource abstraite Win32 représente une ressource de mémoire système sur un système informatique exécutant Windows.
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Classe Win32_SystemMemoryResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861662"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="6224a-103">\_Classe SystemMemoryResource Win32</span><span class="sxs-lookup"><span data-stu-id="6224a-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="6224a-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemMemoryResource** abstraite Win32 représente une ressource de mémoire système sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="6224a-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="6224a-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6224a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6224a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6224a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6224a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6224a-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
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

## <a name="members"></a><span data-ttu-id="6224a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6224a-108">Members</span></span>

<span data-ttu-id="6224a-109">La classe **Win32 \_ SystemMemoryResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6224a-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="6224a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6224a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6224a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6224a-111">Properties</span></span>

<span data-ttu-id="6224a-112">La classe **Win32 \_ SystemMemoryResource** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6224a-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6224a-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6224a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6224a-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6224a-117">A short textual description of the object.</span></span>

<span data-ttu-id="6224a-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6224a-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-122">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6224a-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6224a-123">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6224a-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6224a-124">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="6224a-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6224a-125">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6224a-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-129">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6224a-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6224a-130">Propriété **CreationClassName** du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6224a-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="6224a-131">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6224a-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-135">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6224a-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6224a-136">Propriété de **nom** de l’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6224a-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="6224a-137">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="6224a-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-141">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6224a-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-142">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6224a-142">A textual description of the object.</span></span>

<span data-ttu-id="6224a-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="6224a-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-145">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6224a-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-147">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s mappées en mémoire DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="6224a-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-148">Adresse de fin des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="6224a-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="6224a-149">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="6224a-150">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6224a-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-152">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6224a-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-154">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6224a-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-155">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="6224a-155">Indicates when the object was installed.</span></span> <span data-ttu-id="6224a-156">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="6224a-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6224a-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6224a-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-161">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6224a-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-162">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6224a-162">Label by which the object is known.</span></span> <span data-ttu-id="6224a-163">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="6224a-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6224a-164">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-165">**De la**</span><span class="sxs-lookup"><span data-stu-id="6224a-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-166">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6224a-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-168">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s mappées en mémoire DMTF \| 001,1»)</span><span class="sxs-lookup"><span data-stu-id="6224a-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-169">Adresse de début des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="6224a-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="6224a-170">La propriété de l’identificateur de ressource matérielle doit être définie sur cette valeur pour construire la clé de ressource d’e/s mappée.</span><span class="sxs-lookup"><span data-stu-id="6224a-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="6224a-171">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="6224a-172">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6224a-173">**État**</span><span class="sxs-lookup"><span data-stu-id="6224a-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6224a-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6224a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6224a-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6224a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6224a-176">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6224a-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6224a-177">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6224a-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="6224a-178">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="6224a-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6224a-179">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="6224a-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6224a-180">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="6224a-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6224a-181">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="6224a-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6224a-182">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="6224a-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6224a-183">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="6224a-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6224a-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6224a-185">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6224a-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6224a-186">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6224a-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6224a-187">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6224a-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6224a-188">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6224a-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6224a-189">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6224a-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6224a-190">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6224a-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6224a-191">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6224a-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6224a-192">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6224a-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6224a-193">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6224a-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6224a-194">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6224a-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6224a-195">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6224a-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6224a-196">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6224a-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6224a-197">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6224a-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6224a-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6224a-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6224a-199">Notes</span><span class="sxs-lookup"><span data-stu-id="6224a-199">Remarks</span></span>

<span data-ttu-id="6224a-200">La classe **Win32 \_ SystemMemoryResource** est dérivée de [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6224a-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6224a-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6224a-201">Requirements</span></span>



| <span data-ttu-id="6224a-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6224a-202">Requirement</span></span> | <span data-ttu-id="6224a-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="6224a-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6224a-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6224a-204">Minimum supported client</span></span><br/> | <span data-ttu-id="6224a-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6224a-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6224a-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6224a-206">Minimum supported server</span></span><br/> | <span data-ttu-id="6224a-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6224a-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6224a-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6224a-208">Namespace</span></span><br/>                | <span data-ttu-id="6224a-209">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6224a-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6224a-210">MOF</span><span class="sxs-lookup"><span data-stu-id="6224a-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6224a-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6224a-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6224a-212">DLL</span><span class="sxs-lookup"><span data-stu-id="6224a-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6224a-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6224a-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6224a-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6224a-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6224a-215">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="6224a-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="6224a-216">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="6224a-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
