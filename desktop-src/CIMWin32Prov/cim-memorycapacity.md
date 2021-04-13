---
description: La \_ classe CIM MemoryCapacity représente la mémoire qui peut être installée sur un élément physique et ses configurations minimale et maximale.
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: Classe CIM_MemoryCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200903"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="89f24-103">\_Classe CIM MemoryCapacity</span><span class="sxs-lookup"><span data-stu-id="89f24-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="89f24-104">La classe **CIM \_ MemoryCapacity** représente la mémoire qui peut être installée sur un élément physique et ses configurations minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="89f24-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="89f24-105">Les informations sur la mémoire qui est actuellement installée et les exigences minimales et maximales d’un élément se trouvent dans les instances de la classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="89f24-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89f24-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="89f24-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89f24-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89f24-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89f24-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="89f24-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="89f24-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="89f24-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f24-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89f24-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="89f24-111">Membres</span><span class="sxs-lookup"><span data-stu-id="89f24-111">Members</span></span>

<span data-ttu-id="89f24-112">La classe **CIM \_ MemoryCapacity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="89f24-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="89f24-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89f24-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89f24-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89f24-114">Properties</span></span>

<span data-ttu-id="89f24-115">La classe **CIM \_ MemoryCapacity** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="89f24-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89f24-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="89f24-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f24-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89f24-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f24-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f24-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f24-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="89f24-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="89f24-120">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89f24-120">Short textual description of the object.</span></span>

<span data-ttu-id="89f24-121">Cette propriété est héritée de la [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="89f24-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f24-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="89f24-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f24-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89f24-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f24-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f24-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f24-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89f24-125">Textual description of the object.</span></span>

<span data-ttu-id="89f24-126">Cette propriété est héritée de la [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="89f24-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f24-127">**MaximumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="89f24-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f24-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89f24-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89f24-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f24-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f24-130">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="89f24-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="89f24-131">Quantité maximale de mémoire, en kilo-octets, qui peut être prise en charge par l’élément physique associé.</span><span class="sxs-lookup"><span data-stu-id="89f24-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="89f24-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="89f24-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="89f24-133">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="89f24-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f24-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89f24-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89f24-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f24-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f24-136">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span><span class="sxs-lookup"><span data-stu-id="89f24-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="89f24-137">Type de mémoire, qui fait partie de la clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89f24-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="89f24-138">Les valeurs correspondent à la liste des types de mémoire possibles dans la classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="89f24-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89f24-139">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="89f24-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89f24-140">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="89f24-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="89f24-141">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="89f24-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="89f24-142">**DRAM synchrone** (3)</span><span class="sxs-lookup"><span data-stu-id="89f24-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="89f24-143">**Cache DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="89f24-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="89f24-144">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="89f24-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="89f24-145">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="89f24-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="89f24-146">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="89f24-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="89f24-147">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="89f24-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="89f24-148">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="89f24-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="89f24-149">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="89f24-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="89f24-150">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="89f24-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="89f24-151">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="89f24-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="89f24-152">**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="89f24-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="89f24-153">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="89f24-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="89f24-154">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="89f24-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="89f24-155">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="89f24-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="89f24-156">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="89f24-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="89f24-157">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="89f24-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="89f24-158">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="89f24-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="89f24-159">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="89f24-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="89f24-160">**DDR-2** (21)</span><span class="sxs-lookup"><span data-stu-id="89f24-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89f24-161">**MinimumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="89f24-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f24-162">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89f24-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89f24-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f24-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f24-164">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="89f24-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="89f24-165">Quantité minimale de mémoire, en kilo-octets, nécessaire pour que l’élément physique associé fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="89f24-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="89f24-166">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="89f24-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="89f24-167">**Nom**</span><span class="sxs-lookup"><span data-stu-id="89f24-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f24-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89f24-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f24-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f24-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f24-170">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89f24-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89f24-171">Nom de l’objet ; fait partie de la clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89f24-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89f24-172">Notes</span><span class="sxs-lookup"><span data-stu-id="89f24-172">Remarks</span></span>

<span data-ttu-id="89f24-173">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="89f24-173">WMI does not implement this class.</span></span>

<span data-ttu-id="89f24-174">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="89f24-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89f24-175">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="89f24-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f24-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89f24-176">Requirements</span></span>



| <span data-ttu-id="89f24-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89f24-177">Requirement</span></span> | <span data-ttu-id="89f24-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f24-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89f24-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89f24-179">Minimum supported client</span></span><br/> | <span data-ttu-id="89f24-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89f24-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89f24-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89f24-181">Minimum supported server</span></span><br/> | <span data-ttu-id="89f24-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89f24-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89f24-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89f24-183">Namespace</span></span><br/>                | <span data-ttu-id="89f24-184">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="89f24-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89f24-185">MOF</span><span class="sxs-lookup"><span data-stu-id="89f24-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89f24-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89f24-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89f24-187">DLL</span><span class="sxs-lookup"><span data-stu-id="89f24-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f24-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f24-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f24-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89f24-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f24-190">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="89f24-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 

