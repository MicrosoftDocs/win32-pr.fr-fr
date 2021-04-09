---
description: La \_ classe PSEXTENTBASEDONPEXTENT CIM associe des extensions d’espace protégé basées sur une extension physique.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: Classe CIM_PSExtentBasedOnPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110615"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="8ce64-103">\_Classe CIM PSExtentBasedOnPExtent</span><span class="sxs-lookup"><span data-stu-id="8ce64-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="8ce64-104">La **classe \_ PSExtentBasedOnPExtent CIM** associe des extensions d’espace protégé basées sur une extension physique.</span><span class="sxs-lookup"><span data-stu-id="8ce64-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ce64-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8ce64-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8ce64-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8ce64-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8ce64-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8ce64-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8ce64-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8ce64-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce64-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ce64-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8ce64-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8ce64-110">Members</span></span>

<span data-ttu-id="8ce64-111">La classe **CIM \_ PSExtentBasedOnPExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8ce64-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="8ce64-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ce64-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ce64-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ce64-113">Properties</span></span>

<span data-ttu-id="8ce64-114">La classe **CIM \_ PSExtentBasedOnPExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ce64-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ce64-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="8ce64-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ce64-116">Type de données : **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="8ce64-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="8ce64-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ce64-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ce64-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="8ce64-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8ce64-119">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) qui décrit l’extension physique.</span><span class="sxs-lookup"><span data-stu-id="8ce64-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="8ce64-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="8ce64-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ce64-121">Type de données : **CIM \_ ProtectedSpaceExtent**</span><span class="sxs-lookup"><span data-stu-id="8ce64-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="8ce64-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ce64-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ce64-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="8ce64-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8ce64-124">[**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md) qui décrit l’extension d’espace protégé qui repose sur l’extension physique.</span><span class="sxs-lookup"><span data-stu-id="8ce64-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="8ce64-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="8ce64-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ce64-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8ce64-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ce64-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ce64-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ce64-128">Indique la fin de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="8ce64-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="8ce64-129">Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8ce64-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="8ce64-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8ce64-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="8ce64-131">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="8ce64-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ce64-132">**De la**</span><span class="sxs-lookup"><span data-stu-id="8ce64-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ce64-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8ce64-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ce64-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ce64-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ce64-135">Indique le début de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="8ce64-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="8ce64-136">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8ce64-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="8ce64-137">Cette propriété est héritée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="8ce64-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ce64-138">Notes</span><span class="sxs-lookup"><span data-stu-id="8ce64-138">Remarks</span></span>

<span data-ttu-id="8ce64-139">La classe **CIM \_ PSExtentBasedOnPExtent** est dérivée de [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="8ce64-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="8ce64-140">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8ce64-140">WMI does not implement this class.</span></span>

<span data-ttu-id="8ce64-141">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8ce64-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8ce64-142">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8ce64-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce64-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ce64-143">Requirements</span></span>



| <span data-ttu-id="8ce64-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ce64-144">Requirement</span></span> | <span data-ttu-id="8ce64-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ce64-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce64-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ce64-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8ce64-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ce64-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ce64-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ce64-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8ce64-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ce64-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ce64-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ce64-150">Namespace</span></span><br/>                | <span data-ttu-id="8ce64-151">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8ce64-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8ce64-152">MOF</span><span class="sxs-lookup"><span data-stu-id="8ce64-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ce64-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ce64-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ce64-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8ce64-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ce64-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ce64-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce64-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ce64-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce64-157">**Basé sur CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8ce64-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

