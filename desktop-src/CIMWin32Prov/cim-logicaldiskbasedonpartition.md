---
description: La \_ classe CIM LogicalDiskBasedOnPartition associe un disque logique à la partition de disque sur laquelle il réside.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523135"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="2427b-103">\_Classe CIM LogicalDiskBasedOnPartition</span><span class="sxs-lookup"><span data-stu-id="2427b-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="2427b-104">La classe **CIM \_ LogicalDiskBasedOnPartition** associe un disque logique à la partition de disque sur laquelle il réside.</span><span class="sxs-lookup"><span data-stu-id="2427b-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="2427b-105">Par exemple, le lecteur C d’un ordinateur peut se trouver sur une partition sur un support physique local, ce qui indique qu’un disque logique ne peut pas s’étendre sur plus d’une partition.</span><span class="sxs-lookup"><span data-stu-id="2427b-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="2427b-106">Toutefois, lorsqu’un disque logique peut s’étendre sur plusieurs partitions, le disque logique est basé sur une configuration RAID (par exemple, un miroir ou un ensemble entrelacé).</span><span class="sxs-lookup"><span data-stu-id="2427b-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="2427b-107">Dans ce cas, le disque logique est basé sur le volume de stockage.</span><span class="sxs-lookup"><span data-stu-id="2427b-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="2427b-108">Pour empêcher l’utilisation incorrecte de l’Association **CIM \_ LogicalDiskBasedOnPartition** , le qualificateur **Max (1)** a été placé sur la référence **Antecedent** à la partition de disque.</span><span class="sxs-lookup"><span data-stu-id="2427b-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2427b-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2427b-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2427b-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2427b-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2427b-111">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2427b-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2427b-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2427b-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2427b-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2427b-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2427b-114">Membres</span><span class="sxs-lookup"><span data-stu-id="2427b-114">Members</span></span>

<span data-ttu-id="2427b-115">La classe **CIM \_ LogicalDiskBasedOnPartition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2427b-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="2427b-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2427b-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2427b-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2427b-117">Properties</span></span>

<span data-ttu-id="2427b-118">La classe **CIM \_ LogicalDiskBasedOnPartition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2427b-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2427b-119">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="2427b-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2427b-120">Type de données : **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="2427b-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="2427b-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2427b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2427b-122">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2427b-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2427b-123">[**\_ DiskPartition CIM**](cim-diskpartition.md) qui décrit la partition de disque.</span><span class="sxs-lookup"><span data-stu-id="2427b-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="2427b-124">**Charge**</span><span class="sxs-lookup"><span data-stu-id="2427b-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2427b-125">Type de données **: \_ disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="2427b-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="2427b-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2427b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2427b-127">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="2427b-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2427b-128">Un disque logique [**CIM \_**](cim-logicaldisk.md) qui décrit le disque logique qui est créé sur la partition.</span><span class="sxs-lookup"><span data-stu-id="2427b-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="2427b-129">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="2427b-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2427b-130">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2427b-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2427b-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2427b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2427b-132">Indique la fin de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="2427b-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="2427b-133">Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2427b-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="2427b-134">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2427b-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2427b-135">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="2427b-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="2427b-136">**De la**</span><span class="sxs-lookup"><span data-stu-id="2427b-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2427b-137">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2427b-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2427b-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2427b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2427b-139">Indique le début de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="2427b-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="2427b-140">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2427b-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2427b-141">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="2427b-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2427b-142">Notes</span><span class="sxs-lookup"><span data-stu-id="2427b-142">Remarks</span></span>

<span data-ttu-id="2427b-143">La classe **CIM \_ LogicalDiskBasedOnPartition** est dérivée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="2427b-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="2427b-144">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2427b-144">WMI does not implement this class.</span></span> <span data-ttu-id="2427b-145">Pour les classes dérivées de **CIM \_ LogicalDiskBasedOnPartition**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2427b-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2427b-146">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2427b-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2427b-147">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2427b-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2427b-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2427b-148">Requirements</span></span>



| <span data-ttu-id="2427b-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2427b-149">Requirement</span></span> | <span data-ttu-id="2427b-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="2427b-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2427b-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2427b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2427b-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2427b-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2427b-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2427b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2427b-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2427b-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2427b-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2427b-155">Namespace</span></span><br/>                | <span data-ttu-id="2427b-156">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2427b-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2427b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="2427b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2427b-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2427b-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2427b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="2427b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2427b-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2427b-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2427b-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2427b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2427b-162">**Basé sur CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2427b-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

