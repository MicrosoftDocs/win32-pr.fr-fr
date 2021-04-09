---
description: La \_ classe CIM PhysicalMemory représente des périphériques mémoire de bas niveau, tels que les SIMM, les DIMMs, les puces mémoire brutes, etc.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861534"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="85faf-103">\_Classe CIM PhysicalMemory</span><span class="sxs-lookup"><span data-stu-id="85faf-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="85faf-104">La classe **CIM \_ PhysicalMemory** représente des périphériques mémoire de bas niveau, tels que les SIMM, les DIMMs, les puces mémoire brutes, etc.</span><span class="sxs-lookup"><span data-stu-id="85faf-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85faf-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="85faf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="85faf-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="85faf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="85faf-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="85faf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="85faf-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="85faf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85faf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85faf-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="85faf-110">Membres</span><span class="sxs-lookup"><span data-stu-id="85faf-110">Members</span></span>

<span data-ttu-id="85faf-111">La classe **CIM \_ PhysicalMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="85faf-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="85faf-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="85faf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85faf-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="85faf-113">Properties</span></span>

<span data-ttu-id="85faf-114">La classe **CIM \_ PhysicalMemory** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="85faf-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85faf-115">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="85faf-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="85faf-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-119">Étiquette Banque dans laquelle se trouve la mémoire.</span><span class="sxs-lookup"><span data-stu-id="85faf-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="85faf-120">Par exemple, « Bank 0 » ou « Bank A ».</span><span class="sxs-lookup"><span data-stu-id="85faf-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="85faf-121">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="85faf-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-122">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85faf-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-124">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="85faf-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-125">Capacité totale de la mémoire physique, en octets.</span><span class="sxs-lookup"><span data-stu-id="85faf-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="85faf-126">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="85faf-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-127">**Caption**</span><span class="sxs-lookup"><span data-stu-id="85faf-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-130">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="85faf-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-131">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="85faf-131">Short textual description of the object.</span></span>

<span data-ttu-id="85faf-132">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85faf-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-136">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85faf-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-137">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="85faf-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="85faf-138">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="85faf-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="85faf-139">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="85faf-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85faf-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="85faf-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-144">Largeur des données de la mémoire physique, en bits.</span><span class="sxs-lookup"><span data-stu-id="85faf-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="85faf-145">Une largeur de données de 0 (zéro), et une largeur totale de 8, indique que la mémoire est utilisée uniquement pour fournir des bits de correction d’erreur.</span><span class="sxs-lookup"><span data-stu-id="85faf-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="85faf-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="85faf-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-149">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="85faf-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-150">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="85faf-150">Textual description of the object.</span></span>

<span data-ttu-id="85faf-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-152">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="85faf-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85faf-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-155">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="85faf-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-156">Facteur de forme d’implémentation pour la puce.</span><span class="sxs-lookup"><span data-stu-id="85faf-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="85faf-157">Par exemple, des valeurs telles que SIMM, TSOP ou PGA peuvent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="85faf-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="85faf-158">Cette propriété est héritée de la [**\_ puce CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="85faf-159">0</span><span class="sxs-lookup"><span data-stu-id="85faf-159">0</span></span>
</dt> <dd>

<span data-ttu-id="85faf-160">Unknown</span><span class="sxs-lookup"><span data-stu-id="85faf-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="85faf-161">1</span><span class="sxs-lookup"><span data-stu-id="85faf-161">1</span></span>
</dt> <dd>

<span data-ttu-id="85faf-162">Autres</span><span class="sxs-lookup"><span data-stu-id="85faf-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="85faf-163">2</span><span class="sxs-lookup"><span data-stu-id="85faf-163">2</span></span>
</dt> <dd>

<span data-ttu-id="85faf-164">PANNEAU</span><span class="sxs-lookup"><span data-stu-id="85faf-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-165">3</span><span class="sxs-lookup"><span data-stu-id="85faf-165">3</span></span>
</dt> <dd>

<span data-ttu-id="85faf-166">DIP</span><span class="sxs-lookup"><span data-stu-id="85faf-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-167">4</span><span class="sxs-lookup"><span data-stu-id="85faf-167">4</span></span>
</dt> <dd>

<span data-ttu-id="85faf-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="85faf-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-169">5</span><span class="sxs-lookup"><span data-stu-id="85faf-169">5</span></span>
</dt> <dd>

<span data-ttu-id="85faf-170">SOJ</span><span class="sxs-lookup"><span data-stu-id="85faf-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="85faf-171">6</span><span class="sxs-lookup"><span data-stu-id="85faf-171">6</span></span>
</dt> <dd>

<span data-ttu-id="85faf-172">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="85faf-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="85faf-173">7</span><span class="sxs-lookup"><span data-stu-id="85faf-173">7</span></span>
</dt> <dd>

<span data-ttu-id="85faf-174">Barrett</span><span class="sxs-lookup"><span data-stu-id="85faf-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="85faf-175">8</span><span class="sxs-lookup"><span data-stu-id="85faf-175">8</span></span>
</dt> <dd>

<span data-ttu-id="85faf-176">ESTOMPAGE</span><span class="sxs-lookup"><span data-stu-id="85faf-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="85faf-177">9</span><span class="sxs-lookup"><span data-stu-id="85faf-177">9</span></span>
</dt> <dd>

<span data-ttu-id="85faf-178">TSOP</span><span class="sxs-lookup"><span data-stu-id="85faf-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-179">10</span><span class="sxs-lookup"><span data-stu-id="85faf-179">10</span></span>
</dt> <dd>

<span data-ttu-id="85faf-180">PGA</span><span class="sxs-lookup"><span data-stu-id="85faf-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="85faf-181">11</span><span class="sxs-lookup"><span data-stu-id="85faf-181">11</span></span>
</dt> <dd>

<span data-ttu-id="85faf-182">RIMM</span><span class="sxs-lookup"><span data-stu-id="85faf-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="85faf-183">12</span><span class="sxs-lookup"><span data-stu-id="85faf-183">12</span></span>
</dt> <dd>

<span data-ttu-id="85faf-184">SODIMM</span><span class="sxs-lookup"><span data-stu-id="85faf-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="85faf-185">13</span><span class="sxs-lookup"><span data-stu-id="85faf-185">13</span></span>
</dt> <dd>

<span data-ttu-id="85faf-186">SRIMM</span><span class="sxs-lookup"><span data-stu-id="85faf-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="85faf-187">14</span><span class="sxs-lookup"><span data-stu-id="85faf-187">14</span></span>
</dt> <dd>

<span data-ttu-id="85faf-188">SMD</span><span class="sxs-lookup"><span data-stu-id="85faf-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="85faf-189">15</span><span class="sxs-lookup"><span data-stu-id="85faf-189">15</span></span>
</dt> <dd>

<span data-ttu-id="85faf-190">SSMP</span><span class="sxs-lookup"><span data-stu-id="85faf-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-191">16</span><span class="sxs-lookup"><span data-stu-id="85faf-191">16</span></span>
</dt> <dd>

<span data-ttu-id="85faf-192">QFP</span><span class="sxs-lookup"><span data-stu-id="85faf-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-193">17</span><span class="sxs-lookup"><span data-stu-id="85faf-193">17</span></span>
</dt> <dd>

<span data-ttu-id="85faf-194">TQFP</span><span class="sxs-lookup"><span data-stu-id="85faf-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="85faf-195">18</span><span class="sxs-lookup"><span data-stu-id="85faf-195">18</span></span>
</dt> <dd>

<span data-ttu-id="85faf-196">SOIC</span><span class="sxs-lookup"><span data-stu-id="85faf-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="85faf-197">19</span><span class="sxs-lookup"><span data-stu-id="85faf-197">19</span></span>
</dt> <dd>

<span data-ttu-id="85faf-198">LLC</span><span class="sxs-lookup"><span data-stu-id="85faf-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="85faf-199">20</span><span class="sxs-lookup"><span data-stu-id="85faf-199">20</span></span>
</dt> <dd>

<span data-ttu-id="85faf-200">PLCC</span><span class="sxs-lookup"><span data-stu-id="85faf-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="85faf-201">21</span><span class="sxs-lookup"><span data-stu-id="85faf-201">21</span></span>
</dt> <dd>

<span data-ttu-id="85faf-202">GRILLE</span><span class="sxs-lookup"><span data-stu-id="85faf-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="85faf-203">22</span><span class="sxs-lookup"><span data-stu-id="85faf-203">22</span></span>
</dt> <dd>

<span data-ttu-id="85faf-204">FPBGA</span><span class="sxs-lookup"><span data-stu-id="85faf-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="85faf-205">23</span><span class="sxs-lookup"><span data-stu-id="85faf-205">23</span></span>
</dt> <dd>

<span data-ttu-id="85faf-206">LGA</span><span class="sxs-lookup"><span data-stu-id="85faf-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85faf-207">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="85faf-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-208">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="85faf-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85faf-210">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="85faf-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="85faf-211">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="85faf-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="85faf-212">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="85faf-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="85faf-213">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="85faf-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="85faf-214">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="85faf-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-216">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85faf-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-218">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="85faf-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-219">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="85faf-219">Date and time the object was installed.</span></span> <span data-ttu-id="85faf-220">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="85faf-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="85faf-221">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-222">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="85faf-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-223">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85faf-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-225">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,7»)</span><span class="sxs-lookup"><span data-stu-id="85faf-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-226">Position de la mémoire physique dans une entrelacement.</span><span class="sxs-lookup"><span data-stu-id="85faf-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="85faf-227">La valeur 0 indique qu’il n’est pas entrelacé, 1 indique la première position, 2 indique la deuxième position, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="85faf-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="85faf-228">Par exemple, dans une entrelacement 2:1, la valeur 1 indique que la mémoire est dans la position paire.</span><span class="sxs-lookup"><span data-stu-id="85faf-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="85faf-229">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="85faf-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-232">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85faf-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-233">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="85faf-234">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="85faf-235">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-236">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="85faf-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85faf-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-239">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="85faf-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-240">Type de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="85faf-241">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="85faf-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="85faf-242">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="85faf-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="85faf-243">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="85faf-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="85faf-244">**DRAM synchrone** (3)</span><span class="sxs-lookup"><span data-stu-id="85faf-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="85faf-245">**Cache DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="85faf-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="85faf-246">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="85faf-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="85faf-247">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="85faf-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="85faf-248">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="85faf-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="85faf-249">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="85faf-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="85faf-250">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="85faf-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="85faf-251">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="85faf-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="85faf-252">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="85faf-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="85faf-253">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="85faf-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="85faf-254">**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="85faf-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="85faf-255">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="85faf-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="85faf-256">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="85faf-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="85faf-257">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="85faf-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="85faf-258">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="85faf-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="85faf-259">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="85faf-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="85faf-260">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="85faf-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="85faf-261">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="85faf-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="85faf-262">**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="85faf-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="85faf-263">**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="85faf-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85faf-264">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="85faf-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-265">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-267">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="85faf-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-268">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="85faf-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="85faf-269">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-270">**Nom**</span><span class="sxs-lookup"><span data-stu-id="85faf-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-273">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="85faf-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-274">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="85faf-274">Label by which the object is known.</span></span> <span data-ttu-id="85faf-275">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="85faf-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="85faf-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="85faf-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85faf-280">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="85faf-281">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="85faf-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="85faf-282">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="85faf-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="85faf-283">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-284">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="85faf-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-287">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85faf-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-288">Numéro de référence attribué par l’organisation qui a produit ou fabriqué l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="85faf-289">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-290">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="85faf-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-291">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85faf-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-293">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,6»)</span><span class="sxs-lookup"><span data-stu-id="85faf-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-294">Position de la mémoire physique dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="85faf-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="85faf-295">Par exemple, s’il utilise des périphériques de mémoire 2 8 bits pour former une ligne de 16 bits, la valeur 2 indique que la mémoire est le deuxième appareil.</span><span class="sxs-lookup"><span data-stu-id="85faf-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="85faf-296">La valeur 0 est une valeur non valide pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="85faf-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="85faf-297">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="85faf-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-298">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="85faf-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85faf-300">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="85faf-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="85faf-301">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-302">**Bande**</span><span class="sxs-lookup"><span data-stu-id="85faf-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-303">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="85faf-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85faf-305">Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="85faf-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="85faf-306">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="85faf-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="85faf-307">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="85faf-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="85faf-308">Par exemple, une puce de processeur pouvant être dégradée est amovible.</span><span class="sxs-lookup"><span data-stu-id="85faf-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="85faf-309">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-310">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="85faf-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-311">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="85faf-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85faf-313">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="85faf-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="85faf-314">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="85faf-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="85faf-315">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="85faf-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="85faf-316">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="85faf-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="85faf-317">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-318">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="85faf-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-321">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="85faf-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-322">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="85faf-323">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-324">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="85faf-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-327">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="85faf-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-328">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="85faf-329">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-330">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="85faf-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-331">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85faf-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-333">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« nanosecondes »)</span><span class="sxs-lookup"><span data-stu-id="85faf-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-334">Vitesse de la mémoire physique, en nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="85faf-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="85faf-335">**État**</span><span class="sxs-lookup"><span data-stu-id="85faf-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-338">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="85faf-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-339">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="85faf-339">Current status of the object.</span></span> <span data-ttu-id="85faf-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="85faf-341">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85faf-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="85faf-342">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="85faf-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="85faf-343">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="85faf-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="85faf-344">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="85faf-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="85faf-345">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="85faf-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="85faf-346">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="85faf-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="85faf-347">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="85faf-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="85faf-348">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="85faf-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="85faf-349">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="85faf-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="85faf-350">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="85faf-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="85faf-351">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="85faf-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="85faf-352">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="85faf-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="85faf-353">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="85faf-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85faf-354">**Tag**</span><span class="sxs-lookup"><span data-stu-id="85faf-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-357">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="85faf-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-358">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="85faf-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="85faf-359">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="85faf-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="85faf-360">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="85faf-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="85faf-361">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="85faf-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="85faf-362">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="85faf-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="85faf-363">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="85faf-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="85faf-364">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85faf-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="85faf-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-366">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85faf-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-368">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 002,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="85faf-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="85faf-369">Largeur totale, en bits, de la mémoire physique, y compris les bits de vérification ou de correction des erreurs.</span><span class="sxs-lookup"><span data-stu-id="85faf-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="85faf-370">S’il n’existe aucun bit de correction des erreurs, la valeur de cette propriété doit correspondre à celle spécifiée pour la propriété **DataWidth** .</span><span class="sxs-lookup"><span data-stu-id="85faf-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="85faf-371">**Version**</span><span class="sxs-lookup"><span data-stu-id="85faf-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85faf-372">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85faf-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85faf-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="85faf-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85faf-374">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="85faf-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="85faf-375">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="85faf-375">Version of the physical element.</span></span>

<span data-ttu-id="85faf-376">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85faf-377">Notes</span><span class="sxs-lookup"><span data-stu-id="85faf-377">Remarks</span></span>

<span data-ttu-id="85faf-378">La classe **CIM \_ PhysicalMemory** est dérivée de la [**\_ puce CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="85faf-379">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="85faf-379">WMI does not implement this class.</span></span> <span data-ttu-id="85faf-380">Pour les classes WMI dérivées de **CIM \_ PhysicalMemory**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="85faf-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="85faf-381">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="85faf-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="85faf-382">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="85faf-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="85faf-383">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85faf-383">Requirements</span></span>



| <span data-ttu-id="85faf-384">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85faf-384">Requirement</span></span> | <span data-ttu-id="85faf-385">Valeur</span><span class="sxs-lookup"><span data-stu-id="85faf-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85faf-386">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85faf-386">Minimum supported client</span></span><br/> | <span data-ttu-id="85faf-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85faf-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85faf-388">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85faf-388">Minimum supported server</span></span><br/> | <span data-ttu-id="85faf-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85faf-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85faf-390">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="85faf-390">Namespace</span></span><br/>                | <span data-ttu-id="85faf-391">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="85faf-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="85faf-392">MOF</span><span class="sxs-lookup"><span data-stu-id="85faf-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85faf-393"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85faf-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="85faf-394">DLL</span><span class="sxs-lookup"><span data-stu-id="85faf-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85faf-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85faf-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85faf-396">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85faf-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85faf-397">**\_Puce CIM**</span><span class="sxs-lookup"><span data-stu-id="85faf-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 

