---
description: La \_ classe basée sur CIM représente une association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: CIM_BasedOn, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201068"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="89fe9-103">CIM_BasedOn, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="89fe9-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="89fe9-104">La classe basée sur **CIM \_** représente une association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="89fe9-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="89fe9-105">Par exemple, les extensions physiques incluent des extensions d’espace protégé.</span><span class="sxs-lookup"><span data-stu-id="89fe9-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="89fe9-106">Par conséquent, les jeux de volumes sont assemblés à partir d’une ou de plusieurs extensions d’espace physique ou protégé.</span><span class="sxs-lookup"><span data-stu-id="89fe9-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="89fe9-107">La mémoire cache peut être définie indépendamment et réalisée dans un élément physique, ou elle peut être basée sur des extensions de stockage volatiles ou non volatiles.</span><span class="sxs-lookup"><span data-stu-id="89fe9-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89fe9-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="89fe9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89fe9-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89fe9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89fe9-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="89fe9-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fe9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89fe9-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="89fe9-112">Membres</span><span class="sxs-lookup"><span data-stu-id="89fe9-112">Members</span></span>

<span data-ttu-id="89fe9-113">La classe **CIM \_ basé** sur les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="89fe9-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="89fe9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89fe9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89fe9-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89fe9-115">Properties</span></span>

<span data-ttu-id="89fe9-116">La classe de type **CIM \_** avec ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="89fe9-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89fe9-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="89fe9-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89fe9-118">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="89fe9-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="89fe9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89fe9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89fe9-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="89fe9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="89fe9-121">[**\_ StorageExtent CIM**](cim-storageextent.md) qui décrit l’extension de stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="89fe9-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="89fe9-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="89fe9-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89fe9-123">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="89fe9-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="89fe9-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89fe9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89fe9-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="89fe9-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="89fe9-126">[**\_ StorageExtent CIM**](cim-storageextent.md) qui décrit l’extension de stockage de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="89fe9-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="89fe9-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="89fe9-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89fe9-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89fe9-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89fe9-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89fe9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89fe9-130">Indique la fin de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="89fe9-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="89fe9-131">Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="89fe9-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="89fe9-132">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="89fe9-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="89fe9-133">**De la**</span><span class="sxs-lookup"><span data-stu-id="89fe9-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89fe9-134">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89fe9-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89fe9-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89fe9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89fe9-136">Indique le début de l’étendue de haut niveau dans le stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="89fe9-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="89fe9-137">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="89fe9-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89fe9-138">Notes</span><span class="sxs-lookup"><span data-stu-id="89fe9-138">Remarks</span></span>

<span data-ttu-id="89fe9-139">La **classe \_ CIM** , dérivée de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="89fe9-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="89fe9-140">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="89fe9-140">WMI does not implement this class.</span></span>

<span data-ttu-id="89fe9-141">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="89fe9-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89fe9-142">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="89fe9-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89fe9-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89fe9-143">Requirements</span></span>



| <span data-ttu-id="89fe9-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89fe9-144">Requirement</span></span> | <span data-ttu-id="89fe9-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="89fe9-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89fe9-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89fe9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="89fe9-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89fe9-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89fe9-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89fe9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="89fe9-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89fe9-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89fe9-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89fe9-150">Namespace</span></span><br/>                | <span data-ttu-id="89fe9-151">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="89fe9-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89fe9-152">MOF</span><span class="sxs-lookup"><span data-stu-id="89fe9-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89fe9-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89fe9-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89fe9-154">DLL</span><span class="sxs-lookup"><span data-stu-id="89fe9-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89fe9-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89fe9-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fe9-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89fe9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fe9-157">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="89fe9-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

