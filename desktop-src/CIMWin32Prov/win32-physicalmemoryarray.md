---
description: Le \_ PhysicalMemoryArray Win32&\# 160 ; La classe WMI représente des détails sur la mémoire physique du système informatique. Cela comprend le nombre de périphériques de mémoire, la capacité de mémoire disponible et le type de mémoire&\# 8212 ; par exemple, la mémoire système ou vidéo.
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950856"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="d8f03-104">\_Classe PhysicalMemoryArray Win32</span><span class="sxs-lookup"><span data-stu-id="d8f03-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="d8f03-105">La [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ PhysicalMemoryArray Win32** représente des détails sur la mémoire physique du système informatique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="d8f03-106">Cela comprend le nombre de périphériques de mémoire, la capacité de mémoire disponible et le type de mémoire, par exemple la mémoire système ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="d8f03-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="d8f03-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d8f03-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d8f03-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d8f03-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f03-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8f03-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="d8f03-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d8f03-110">Members</span></span>

<span data-ttu-id="d8f03-111">La classe **Win32 \_ PhysicalMemoryArray** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8f03-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="d8f03-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8f03-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d8f03-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8f03-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d8f03-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8f03-114">Methods</span></span>

<span data-ttu-id="d8f03-115">La classe **Win32 \_ PhysicalMemoryArray** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d8f03-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="d8f03-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="d8f03-116">Method</span></span>           | <span data-ttu-id="d8f03-117">Description</span><span class="sxs-lookup"><span data-stu-id="d8f03-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="d8f03-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="d8f03-118">**IsCompatible**</span></span> | <span data-ttu-id="d8f03-119">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d8f03-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d8f03-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8f03-120">Properties</span></span>

<span data-ttu-id="d8f03-121">La classe **Win32 \_ PhysicalMemoryArray** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8f03-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8f03-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8f03-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-125">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-126">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="d8f03-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="d8f03-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-128">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d8f03-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-131">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d8f03-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-132">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d8f03-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d8f03-133">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d8f03-134">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-135">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="d8f03-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-136">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d8f03-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-138">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-139">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d8f03-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="d8f03-140">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-141">**Description**</span><span class="sxs-lookup"><span data-stu-id="d8f03-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-144">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d8f03-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-145">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8f03-145">Description of the object.</span></span>

<span data-ttu-id="d8f03-146">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-147">**Height**</span><span class="sxs-lookup"><span data-stu-id="d8f03-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-148">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d8f03-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-150">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-151">Hauteur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d8f03-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="d8f03-152">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-153">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="d8f03-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-154">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8f03-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-156">Si la **valeur est true**, un package physique peut être échangé à chaud (s’il est possible de remplacer l’élément par un autre physiquement, mais équivalent, alors que le package qui le contient a une alimentation qui lui est appliquée, est « on »).</span><span class="sxs-lookup"><span data-stu-id="d8f03-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="d8f03-157">Par exemple, un package de lecteur de disque inséré à l’aide de connecteurs SCA est amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d8f03-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="d8f03-158">Tous les packages pouvant être échangés à chaud sont par nature amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="d8f03-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="d8f03-159">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d8f03-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-161">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d8f03-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-163">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d8f03-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-164">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8f03-164">Date and time the object was installed.</span></span> <span data-ttu-id="d8f03-165">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d8f03-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d8f03-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-167">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="d8f03-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f03-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-170">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 16 \| location")</span><span class="sxs-lookup"><span data-stu-id="d8f03-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-171">Emplacement physique du tableau de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d8f03-171">Physical location of the memory array.</span></span>

<span data-ttu-id="d8f03-172">Cette valeur provient du membre d' **emplacement** de la structure du tableau de la **mémoire physique** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d8f03-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d8f03-173">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="d8f03-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8f03-174">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d8f03-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8f03-175">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d8f03-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="d8f03-176">**Carte système ou carte mère** (3)</span><span class="sxs-lookup"><span data-stu-id="d8f03-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-177">**Carte d’extension ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="d8f03-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-178">**Carte complémentaire EISA** (5)</span><span class="sxs-lookup"><span data-stu-id="d8f03-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-179">**Carte complémentaire PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="d8f03-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-180">**Carte complémentaire MCA** (7)</span><span class="sxs-lookup"><span data-stu-id="d8f03-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-181">**Carte complémentaire PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="d8f03-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-182">**Carte complémentaire propriétaire** (9)</span><span class="sxs-lookup"><span data-stu-id="d8f03-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="d8f03-183">**NuBus** (10)</span><span class="sxs-lookup"><span data-stu-id="d8f03-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-184">**Carte complémentaire PC-98/C20** (11)</span><span class="sxs-lookup"><span data-stu-id="d8f03-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-185">**Carte complémentaire PC-98/C24** (12)</span><span class="sxs-lookup"><span data-stu-id="d8f03-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-186">**Carte complémentaire PC-98/E** (13)</span><span class="sxs-lookup"><span data-stu-id="d8f03-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="d8f03-187">**Carte complémentaire PC-98/bus local** (14)</span><span class="sxs-lookup"><span data-stu-id="d8f03-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8f03-188">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="d8f03-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-191">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d8f03-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-192">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="d8f03-193">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="d8f03-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-195">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d8f03-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-197">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 16 \| Capacity maximum")</span><span class="sxs-lookup"><span data-stu-id="d8f03-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-198">Utilisez la propriété **MaxCapacityEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="d8f03-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="d8f03-199">Cette valeur provient du membre **capacité maximale** de la structure du tableau de la **mémoire physique** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d8f03-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d8f03-200">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Taille maximale de la mémoire (en octets) qui est installée pour ce tableau de mémoire spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="d8f03-201">Si la taille est inconnue, la propriété reçoit la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d8f03-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-202">**MaxCapacityEx**</span><span class="sxs-lookup"><span data-stu-id="d8f03-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-203">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8f03-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-205">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« SMBIOS \| type 16 \| Extended maximum Capacity »), [**Units**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-206">Taille maximale de mémoire (en kilo-octets) à installer pour ce tableau de mémoire spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="d8f03-207">Si la taille est inconnue, la propriété reçoit la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d8f03-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="d8f03-208">Cette valeur provient du membre **capacité maximale étendue** de la structure du tableau de la **mémoire physique** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d8f03-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d8f03-209">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d8f03-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-210">**MemoryDevices**</span><span class="sxs-lookup"><span data-stu-id="d8f03-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f03-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-213">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 16 \| Number of Memory Devices")</span><span class="sxs-lookup"><span data-stu-id="d8f03-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-214">Nombre d’emplacements physiques ou de sockets disponibles dans ce tableau de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d8f03-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="d8f03-215">Cette valeur provient du **nombre d’unités de mémoire** membre de la structure du tableau de la **mémoire physique** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d8f03-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-216">**MemoryErrorCorrection**</span><span class="sxs-lookup"><span data-stu-id="d8f03-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-217">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f03-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-219">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 16 \| Memory error correction")</span><span class="sxs-lookup"><span data-stu-id="d8f03-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-220">Type de correction d’erreur utilisé par le tableau de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d8f03-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="d8f03-221">Cette valeur provient du membre de **Correction d’erreur de mémoire** de la structure du tableau de la **mémoire physique** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d8f03-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d8f03-222">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="d8f03-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8f03-223">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d8f03-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8f03-224">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d8f03-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d8f03-225">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="d8f03-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="d8f03-226">**Parité** (4)</span><span class="sxs-lookup"><span data-stu-id="d8f03-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="d8f03-227">**ECC sur un bit** (5)</span><span class="sxs-lookup"><span data-stu-id="d8f03-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="d8f03-228">**ECC multi-bits** (6)</span><span class="sxs-lookup"><span data-stu-id="d8f03-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="d8f03-229">**CRC** (7)</span><span class="sxs-lookup"><span data-stu-id="d8f03-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8f03-230">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="d8f03-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-233">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d8f03-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-234">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="d8f03-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="d8f03-235">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-236">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d8f03-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-239">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d8f03-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-240">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d8f03-240">Label by which the object is known.</span></span> <span data-ttu-id="d8f03-241">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d8f03-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d8f03-242">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d8f03-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-246">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="d8f03-247">Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="d8f03-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="d8f03-248">Notez que si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété est **null** et les données de code-barres utilisées comme clé de classe, dans la propriété Tag.</span><span class="sxs-lookup"><span data-stu-id="d8f03-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="d8f03-249">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-250">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="d8f03-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-253">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d8f03-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-254">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="d8f03-255">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-256">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="d8f03-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-257">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8f03-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-259">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="d8f03-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="d8f03-260">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-261">**Bande**</span><span class="sxs-lookup"><span data-stu-id="d8f03-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-262">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8f03-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-264">Si la **valeur est true**, un package physique est amovible (s’il est conçu pour être pris dans et hors du conteneur physique dans lequel il est normalement trouvé, sans altérer la fonction de l’empaquetage global).</span><span class="sxs-lookup"><span data-stu-id="d8f03-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="d8f03-265">Un package peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="d8f03-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="d8f03-266">Si l’alimentation peut être « activée » et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d8f03-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="d8f03-267">Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas d’un package de lecteur de disque inséré à l’aide de connecteurs SCA.</span><span class="sxs-lookup"><span data-stu-id="d8f03-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="d8f03-268">Toutefois, cette dernière peut être permutée à chaud.</span><span class="sxs-lookup"><span data-stu-id="d8f03-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="d8f03-269">L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante.</span><span class="sxs-lookup"><span data-stu-id="d8f03-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="d8f03-270">La suppression de ces composants affecterait la fonction de l’ensemble de l’empaquetage ou est impossible en raison de l’intégration étroite du package.</span><span class="sxs-lookup"><span data-stu-id="d8f03-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="d8f03-271">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-272">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="d8f03-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-273">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8f03-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-275">Si la **valeur est true**, ce composant de média physique peut être remplacé par un autre physiquement différent.</span><span class="sxs-lookup"><span data-stu-id="d8f03-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="d8f03-276">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="d8f03-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="d8f03-277">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="d8f03-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="d8f03-278">Un autre exemple est un package d’alimentation monté sur des rails coulissants.</span><span class="sxs-lookup"><span data-stu-id="d8f03-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="d8f03-279">Tous les packages amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="d8f03-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="d8f03-280">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-281">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d8f03-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-284">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d8f03-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-285">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d8f03-286">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-287">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="d8f03-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-290">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d8f03-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-291">Numéro de point de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="d8f03-292">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-293">**État**</span><span class="sxs-lookup"><span data-stu-id="d8f03-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-296">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d8f03-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-297">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8f03-297">Current status of the object.</span></span> <span data-ttu-id="d8f03-298">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="d8f03-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d8f03-299">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="d8f03-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d8f03-300">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="d8f03-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d8f03-301">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="d8f03-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d8f03-302">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="d8f03-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d8f03-303">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d8f03-304">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8f03-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d8f03-305">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d8f03-306">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d8f03-307">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8f03-308">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d8f03-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d8f03-309">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d8f03-310">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d8f03-311">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d8f03-312">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d8f03-313">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d8f03-314">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d8f03-315">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d8f03-316">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8f03-317">**Tag**</span><span class="sxs-lookup"><span data-stu-id="d8f03-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-320">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d8f03-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-321">Identificateur unique du tableau de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="d8f03-322">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="d8f03-323">Exemple : « tableau de mémoire physique 1 »</span><span class="sxs-lookup"><span data-stu-id="d8f03-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-324">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="d8f03-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-325">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8f03-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-327">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 16 \| use")</span><span class="sxs-lookup"><span data-stu-id="d8f03-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-328">Utilisation de la mémoire dans le système informatique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="d8f03-329">Cette valeur provient du membre **use** de la structure de la **mémoire physique** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d8f03-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d8f03-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="d8f03-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8f03-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d8f03-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8f03-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d8f03-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="d8f03-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**Mémoire système** (3)</span><span class="sxs-lookup"><span data-stu-id="d8f03-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="d8f03-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Mémoire vidéo** (4)</span><span class="sxs-lookup"><span data-stu-id="d8f03-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="d8f03-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Mémoire flash** (5)</span><span class="sxs-lookup"><span data-stu-id="d8f03-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="d8f03-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**RAM non volatile** (6)</span><span class="sxs-lookup"><span data-stu-id="d8f03-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d8f03-337">RAM non volatile</span><span class="sxs-lookup"><span data-stu-id="d8f03-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="d8f03-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Mémoire cache** (7)</span><span class="sxs-lookup"><span data-stu-id="d8f03-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8f03-339">**Version**</span><span class="sxs-lookup"><span data-stu-id="d8f03-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8f03-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-342">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d8f03-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-343">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d8f03-343">Version of the physical element.</span></span>

<span data-ttu-id="d8f03-344">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-345">**Poids**</span><span class="sxs-lookup"><span data-stu-id="d8f03-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-346">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d8f03-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-348">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-349">Poids du package physique en livres.</span><span class="sxs-lookup"><span data-stu-id="d8f03-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="d8f03-350">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8f03-351">**Width**</span><span class="sxs-lookup"><span data-stu-id="d8f03-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8f03-352">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d8f03-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8f03-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8f03-354">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d8f03-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d8f03-355">Largeur du package physique en pouces.</span><span class="sxs-lookup"><span data-stu-id="d8f03-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="d8f03-356">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8f03-357">Notes</span><span class="sxs-lookup"><span data-stu-id="d8f03-357">Remarks</span></span>

<span data-ttu-id="d8f03-358">La classe **Win32 \_ PhysicalMemoryArray** est dérivée de [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d8f03-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d8f03-359">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8f03-359">Examples</span></span>

<span data-ttu-id="d8f03-360">L’exemple PowerShell suivant récupère le nombre d’emplacements de mémoire et la quantité de mémoire installée sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="d8f03-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="d8f03-361">L’exemple de code VBScript suivant retourne des informations sur la mémoire physique installée sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d8f03-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d8f03-362">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8f03-362">Requirements</span></span>



| <span data-ttu-id="d8f03-363">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8f03-363">Requirement</span></span> | <span data-ttu-id="d8f03-364">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8f03-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f03-365">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8f03-365">Minimum supported client</span></span><br/> | <span data-ttu-id="d8f03-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8f03-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8f03-367">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8f03-367">Minimum supported server</span></span><br/> | <span data-ttu-id="d8f03-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8f03-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8f03-369">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8f03-369">Namespace</span></span><br/>                | <span data-ttu-id="d8f03-370">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d8f03-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8f03-371">MOF</span><span class="sxs-lookup"><span data-stu-id="d8f03-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8f03-372"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8f03-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8f03-373">DLL</span><span class="sxs-lookup"><span data-stu-id="d8f03-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8f03-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8f03-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f03-375">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8f03-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f03-376">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="d8f03-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="d8f03-377">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="d8f03-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d8f03-378">**\_MemoryArrayLocation Win32**</span><span class="sxs-lookup"><span data-stu-id="d8f03-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 
