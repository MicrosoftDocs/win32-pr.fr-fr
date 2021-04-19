---
description: L' \_ Association CIM RealizesPExtent représente la relation dans laquelle les extensions physiques sont réalisées sur un support physique. En outre, l’adresse de début de l’étendue physique sur le support physique est spécifiée.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: Classe CIM_RealizesPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514528"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="e4d36-104">\_Classe CIM RealizesPExtent</span><span class="sxs-lookup"><span data-stu-id="e4d36-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="e4d36-105">L’Association **CIM \_ RealizesPExtent** représente la relation dans laquelle les extensions physiques sont réalisées sur un support physique.</span><span class="sxs-lookup"><span data-stu-id="e4d36-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="e4d36-106">En outre, l’adresse de début de l’étendue physique sur le support physique est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e4d36-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4d36-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e4d36-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e4d36-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e4d36-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e4d36-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e4d36-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e4d36-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e4d36-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d36-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4d36-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="e4d36-112">Membres</span><span class="sxs-lookup"><span data-stu-id="e4d36-112">Members</span></span>

<span data-ttu-id="e4d36-113">La classe **CIM \_ RealizesPExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4d36-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="e4d36-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4d36-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4d36-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4d36-115">Properties</span></span>

<span data-ttu-id="e4d36-116">La classe **CIM \_ RealizesPExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e4d36-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4d36-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e4d36-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d36-118">Type de données : **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="e4d36-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="e4d36-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4d36-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d36-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e4d36-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e4d36-121">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) qui décrit le support physique sur lequel l’extension est réalisée.</span><span class="sxs-lookup"><span data-stu-id="e4d36-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="e4d36-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e4d36-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d36-123">Type de données : **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="e4d36-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="e4d36-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4d36-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d36-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="e4d36-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e4d36-126">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) qui décrit l’étendue physique qui se trouve sur le média.</span><span class="sxs-lookup"><span data-stu-id="e4d36-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="e4d36-127">**De la**</span><span class="sxs-lookup"><span data-stu-id="e4d36-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d36-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d36-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d36-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4d36-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d36-130">Adresse de départ sur le support physique où commence l’extension physique.</span><span class="sxs-lookup"><span data-stu-id="e4d36-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="e4d36-131">L’adresse de fin de l’extension physique est déterminée à l’aide des propriétés **NumberOfBlocks** et **BlockSize** de l’objet [**CIM \_ PhysicalExtent**](cim-physicalextent.md) .</span><span class="sxs-lookup"><span data-stu-id="e4d36-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="e4d36-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e4d36-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4d36-133">Notes</span><span class="sxs-lookup"><span data-stu-id="e4d36-133">Remarks</span></span>

<span data-ttu-id="e4d36-134">La classe **CIM \_ RealizesPExtent** est dérivée de l' [**\_ esprit CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="e4d36-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="e4d36-135">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e4d36-135">WMI does not implement this class.</span></span>

<span data-ttu-id="e4d36-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e4d36-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e4d36-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e4d36-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d36-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4d36-138">Requirements</span></span>



| <span data-ttu-id="e4d36-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4d36-139">Requirement</span></span> | <span data-ttu-id="e4d36-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4d36-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d36-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4d36-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d36-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d36-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4d36-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4d36-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d36-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4d36-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4d36-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4d36-145">Namespace</span></span><br/>                | <span data-ttu-id="e4d36-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e4d36-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4d36-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e4d36-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4d36-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4d36-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4d36-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e4d36-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4d36-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4d36-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d36-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4d36-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d36-152">**CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e4d36-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

