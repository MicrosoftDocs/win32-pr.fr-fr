---
description: L' \_ Association CIM LogicalDiskBasedOnVolumeSet associe les disques logiques au volume sur lequel ils sont trouvés. Les disques logiques peuvent être basés sur un volume unique (par exemple, exposé par un gestionnaire de volume logiciel) ou sur une partition de disque.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnVolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110270"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="35e04-104">\_Classe CIM LogicalDiskBasedOnVolumeSet</span><span class="sxs-lookup"><span data-stu-id="35e04-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="35e04-105">L’Association **CIM \_ LogicalDiskBasedOnVolumeSet** associe les disques logiques au volume sur lequel ils sont trouvés.</span><span class="sxs-lookup"><span data-stu-id="35e04-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="35e04-106">Les disques logiques peuvent être basés sur un volume unique (par exemple, exposé par un gestionnaire de volume logiciel) ou sur une partition de disque.</span><span class="sxs-lookup"><span data-stu-id="35e04-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35e04-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="35e04-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="35e04-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="35e04-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="35e04-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="35e04-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="35e04-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="35e04-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e04-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35e04-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="35e04-112">Membres</span><span class="sxs-lookup"><span data-stu-id="35e04-112">Members</span></span>

<span data-ttu-id="35e04-113">La classe **CIM \_ LogicalDiskBasedOnVolumeSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="35e04-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="35e04-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35e04-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35e04-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35e04-115">Properties</span></span>

<span data-ttu-id="35e04-116">La classe **CIM \_ LogicalDiskBasedOnVolumeSet** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="35e04-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35e04-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="35e04-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e04-118">Type de données : **CIM \_ VolumeSet**</span><span class="sxs-lookup"><span data-stu-id="35e04-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="35e04-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35e04-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e04-120">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="35e04-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="35e04-121">[**\_ VolumeSet CIM**](cim-volumeset.md) qui décrit l’ensemble de volumes.</span><span class="sxs-lookup"><span data-stu-id="35e04-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="35e04-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="35e04-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e04-123">Type de données **: \_ disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="35e04-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="35e04-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35e04-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e04-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="35e04-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="35e04-126">Un disque logique [**CIM \_**](cim-logicaldisk.md) qui décrit le disque logique qui est créé sur le jeu de volumes.</span><span class="sxs-lookup"><span data-stu-id="35e04-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="35e04-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="35e04-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e04-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35e04-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35e04-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35e04-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35e04-130">Indique la fin de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="35e04-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="35e04-131">Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="35e04-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="35e04-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="35e04-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="35e04-133">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="35e04-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="35e04-134">**De la**</span><span class="sxs-lookup"><span data-stu-id="35e04-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e04-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35e04-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35e04-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35e04-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35e04-137">Indique le début de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="35e04-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="35e04-138">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="35e04-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="35e04-139">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="35e04-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35e04-140">Notes</span><span class="sxs-lookup"><span data-stu-id="35e04-140">Remarks</span></span>

<span data-ttu-id="35e04-141">La classe **CIM \_ LogicalDiskBasedOnVolumeSet** est dérivée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="35e04-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="35e04-142">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="35e04-142">WMI does not implement this class.</span></span>

<span data-ttu-id="35e04-143">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="35e04-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="35e04-144">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="35e04-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e04-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35e04-145">Requirements</span></span>



| <span data-ttu-id="35e04-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35e04-146">Requirement</span></span> | <span data-ttu-id="35e04-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="35e04-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35e04-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e04-148">Minimum supported client</span></span><br/> | <span data-ttu-id="35e04-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35e04-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35e04-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e04-150">Minimum supported server</span></span><br/> | <span data-ttu-id="35e04-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35e04-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35e04-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35e04-152">Namespace</span></span><br/>                | <span data-ttu-id="35e04-153">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="35e04-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35e04-154">MOF</span><span class="sxs-lookup"><span data-stu-id="35e04-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35e04-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35e04-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35e04-156">DLL</span><span class="sxs-lookup"><span data-stu-id="35e04-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e04-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35e04-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e04-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35e04-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e04-159">**Basé sur CIM \_**</span><span class="sxs-lookup"><span data-stu-id="35e04-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

