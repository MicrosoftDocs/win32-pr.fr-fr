---
description: La \_ classe CIM RealizesDiskPartition représente une partition de disque sur un support physique qui modélise la création de partitions sur un disque SCSI ou IDE brut.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: Classe CIM_RealizesDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110614"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="ea287-103">\_Classe CIM RealizesDiskPartition</span><span class="sxs-lookup"><span data-stu-id="ea287-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="ea287-104">La classe **CIM \_ RealizesDiskPartition** représente une partition de disque sur un support physique qui modélise la création de partitions sur un disque SCSI ou IDE brut.</span><span class="sxs-lookup"><span data-stu-id="ea287-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea287-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ea287-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ea287-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ea287-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ea287-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ea287-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ea287-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ea287-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea287-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea287-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="ea287-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ea287-110">Members</span></span>

<span data-ttu-id="ea287-111">La classe **CIM \_ RealizesDiskPartition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea287-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="ea287-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea287-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea287-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea287-113">Properties</span></span>

<span data-ttu-id="ea287-114">La classe **CIM \_ RealizesDiskPartition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea287-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea287-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="ea287-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea287-116">Type de données : **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="ea287-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="ea287-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea287-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea287-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ea287-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ea287-119">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) qui décrit le support physique sur lequel l’extension est réalisée.</span><span class="sxs-lookup"><span data-stu-id="ea287-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="ea287-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="ea287-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea287-121">Type de données : **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="ea287-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="ea287-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea287-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea287-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="ea287-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ea287-124">[**\_ DiskPartition CIM**](cim-diskpartition.md) qui décrit la partition de disque qui se trouve sur le média.</span><span class="sxs-lookup"><span data-stu-id="ea287-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="ea287-125">**De la**</span><span class="sxs-lookup"><span data-stu-id="ea287-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea287-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea287-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea287-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea287-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea287-128">Adresse de départ sur le support physique où la partition de disque commence.</span><span class="sxs-lookup"><span data-stu-id="ea287-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="ea287-129">L’adresse de fin de la partition est déterminée à l’aide des propriétés **NumberOfBlocks** et **BlockSize** de l’objet [**CIM \_ DiskPartition**](cim-diskpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="ea287-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="ea287-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ea287-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea287-131">Notes</span><span class="sxs-lookup"><span data-stu-id="ea287-131">Remarks</span></span>

<span data-ttu-id="ea287-132">La classe **CIM \_ RealizesDiskPartition** est dérivée de l' [**\_ esprit CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="ea287-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="ea287-133">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ea287-133">WMI does not implement this class.</span></span>

<span data-ttu-id="ea287-134">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ea287-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ea287-135">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ea287-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea287-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea287-136">Requirements</span></span>



| <span data-ttu-id="ea287-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea287-137">Requirement</span></span> | <span data-ttu-id="ea287-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea287-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea287-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea287-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ea287-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea287-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea287-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea287-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ea287-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea287-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea287-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ea287-143">Namespace</span></span><br/>                | <span data-ttu-id="ea287-144">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ea287-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea287-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ea287-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea287-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea287-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea287-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ea287-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea287-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea287-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea287-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea287-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea287-150">**CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ea287-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

