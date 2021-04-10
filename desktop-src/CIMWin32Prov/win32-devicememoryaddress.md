---
description: La \_ classe WMI DeviceMemoryAddress WMI représente une adresse mémoire de l’appareil sur un système informatique exécutant Windows.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Classe Win32_DeviceMemoryAddress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950761"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="9c824-103">\_Classe DeviceMemoryAddress Win32</span><span class="sxs-lookup"><span data-stu-id="9c824-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="9c824-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceMemoryAddress** WMI représente une adresse mémoire de l’appareil sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="9c824-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="9c824-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9c824-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9c824-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9c824-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c824-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c824-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="9c824-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9c824-108">Members</span></span>

<span data-ttu-id="9c824-109">La classe **Win32 \_ DeviceMemoryAddress** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9c824-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="9c824-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9c824-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c824-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9c824-111">Properties</span></span>

<span data-ttu-id="9c824-112">La classe **Win32 \_ DeviceMemoryAddress** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9c824-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c824-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9c824-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="9c824-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-117">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="9c824-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="9c824-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c824-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c824-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c824-123">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9c824-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9c824-124">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9c824-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="9c824-125">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c824-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-129">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9c824-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9c824-130">Nom de la classe de création de système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9c824-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="9c824-131">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9c824-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-135">Qualificateurs : [**propagé**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c824-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c824-136">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9c824-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="9c824-137">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c824-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-141">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9c824-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-142">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9c824-142">Description of the object.</span></span>

<span data-ttu-id="9c824-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="9c824-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-145">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c824-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s mappées en mémoire DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="9c824-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-148">Adresse de fin des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9c824-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="9c824-149">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="9c824-150">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9c824-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9c824-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-152">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c824-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-154">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="9c824-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-155">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9c824-155">Date and time the object was installed.</span></span> <span data-ttu-id="9c824-156">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="9c824-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9c824-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-158">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="9c824-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-161">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| indicateurs de \| \_ descripteur de ressource partielle win32api SystemStructures cm \_ \_ \| »)</span><span class="sxs-lookup"><span data-stu-id="9c824-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-162">Caractéristiques de la ressource mémoire sur le système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="9c824-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="9c824-163">Les valeurs sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="9c824-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="9c824-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span><span class="sxs-lookup"><span data-stu-id="9c824-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-165">La mémoire peut être à la fois en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="9c824-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="9c824-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span><span class="sxs-lookup"><span data-stu-id="9c824-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-167">La mémoire est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9c824-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="9c824-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span><span class="sxs-lookup"><span data-stu-id="9c824-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-169">La mémoire ne peut être écrite qu’en écriture.</span><span class="sxs-lookup"><span data-stu-id="9c824-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="9c824-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** (« prefetchable »)</span><span class="sxs-lookup"><span data-stu-id="9c824-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-171">Un bloc de mémoire est copié à partir de la mémoire principale dans une mémoire tampon de petite taille gérée par le chipset de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9c824-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="9c824-172">Les opérations de lecture répétées à partir de la même partie de la mémoire sont plus rapides avec la mémoire prérécupérée.</span><span class="sxs-lookup"><span data-stu-id="9c824-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="9c824-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** (« CombinedWrite »)</span><span class="sxs-lookup"><span data-stu-id="9c824-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-174">TBD</span><span class="sxs-lookup"><span data-stu-id="9c824-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="9c824-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** (« Type24 »)</span><span class="sxs-lookup"><span data-stu-id="9c824-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-176">TBD</span><span class="sxs-lookup"><span data-stu-id="9c824-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="9c824-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** (« cacheable »)</span><span class="sxs-lookup"><span data-stu-id="9c824-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-178">TBD</span><span class="sxs-lookup"><span data-stu-id="9c824-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="9c824-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** (« WindowDecode »)</span><span class="sxs-lookup"><span data-stu-id="9c824-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-180">TBD</span><span class="sxs-lookup"><span data-stu-id="9c824-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="9c824-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** (« bar »)</span><span class="sxs-lookup"><span data-stu-id="9c824-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="9c824-182">TBD</span><span class="sxs-lookup"><span data-stu-id="9c824-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9c824-183">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9c824-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-186">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9c824-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-187">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9c824-187">Label by which the object is known.</span></span> <span data-ttu-id="9c824-188">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="9c824-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9c824-189">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-190">**De la**</span><span class="sxs-lookup"><span data-stu-id="9c824-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-191">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c824-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-193">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MappingStrings"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s mappées en mémoire DMTF \| 001,1»)</span><span class="sxs-lookup"><span data-stu-id="9c824-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-194">Adresse de départ des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9c824-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="9c824-195">La propriété de l’identificateur de ressource matérielle doit être définie sur cette valeur pour construire la clé de ressource d’e/s mappée.</span><span class="sxs-lookup"><span data-stu-id="9c824-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="9c824-196">Cette propriété est héritée de la [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="9c824-197">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9c824-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9c824-198">**État**</span><span class="sxs-lookup"><span data-stu-id="9c824-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c824-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9c824-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c824-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c824-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c824-201">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9c824-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9c824-202">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9c824-202">Current status of the object.</span></span> <span data-ttu-id="9c824-203">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="9c824-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9c824-204">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="9c824-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9c824-205">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="9c824-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9c824-206">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="9c824-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9c824-207">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="9c824-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9c824-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9c824-209">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9c824-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9c824-210">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="9c824-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9c824-211">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="9c824-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9c824-212">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9c824-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9c824-213">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="9c824-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9c824-214">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9c824-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9c824-215">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9c824-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9c824-216">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9c824-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9c824-217">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="9c824-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9c824-218">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="9c824-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9c824-219">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="9c824-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9c824-220">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="9c824-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9c824-221">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="9c824-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9c824-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9c824-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9c824-223">Notes</span><span class="sxs-lookup"><span data-stu-id="9c824-223">Remarks</span></span>

<span data-ttu-id="9c824-224">La classe **Win32 \_ DeviceMemoryAddress** est dérivée de [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="9c824-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c824-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c824-225">Requirements</span></span>



| <span data-ttu-id="9c824-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c824-226">Requirement</span></span> | <span data-ttu-id="9c824-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c824-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c824-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c824-228">Minimum supported client</span></span><br/> | <span data-ttu-id="9c824-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c824-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9c824-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c824-230">Minimum supported server</span></span><br/> | <span data-ttu-id="9c824-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c824-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9c824-232">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9c824-232">Namespace</span></span><br/>                | <span data-ttu-id="9c824-233">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9c824-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9c824-234">MOF</span><span class="sxs-lookup"><span data-stu-id="9c824-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c824-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c824-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c824-236">DLL</span><span class="sxs-lookup"><span data-stu-id="9c824-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c824-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c824-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c824-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c824-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c824-239">**\_SystemMemoryResource Win32**</span><span class="sxs-lookup"><span data-stu-id="9c824-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="9c824-240">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="9c824-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

