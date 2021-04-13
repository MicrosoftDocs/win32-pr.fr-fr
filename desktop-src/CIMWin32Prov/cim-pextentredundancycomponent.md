---
description: La \_ classe CIM PExtentRedundancyComponent représente les extensions physiques qui participent à un groupe de redondance de stockage.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: Classe CIM_PExtentRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482936"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="2c1c3-103">\_Classe CIM PExtentRedundancyComponent</span><span class="sxs-lookup"><span data-stu-id="2c1c3-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="2c1c3-104">La classe **CIM \_ PExtentRedundancyComponent** représente les extensions physiques qui participent à un groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c1c3-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2c1c3-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2c1c3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2c1c3-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2c1c3-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1c3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c1c3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="2c1c3-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2c1c3-110">Members</span></span>

<span data-ttu-id="2c1c3-111">La classe **CIM \_ PExtentRedundancyComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c1c3-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2c1c3-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c1c3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c1c3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c1c3-113">Properties</span></span>

<span data-ttu-id="2c1c3-114">La classe **CIM \_ PExtentRedundancyComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c1c3-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2c1c3-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1c3-116">Type de données : **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="2c1c3-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="2c1c3-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c1c3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c1c3-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2c1c3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2c1c3-119">[**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) qui décrit le groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="2c1c3-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2c1c3-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1c3-121">Type de données : **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="2c1c3-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="2c1c3-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c1c3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c1c3-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2c1c3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2c1c3-124">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) qui décrit l’extension physique qui participe au groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c1c3-125">Notes</span><span class="sxs-lookup"><span data-stu-id="2c1c3-125">Remarks</span></span>

<span data-ttu-id="2c1c3-126">La classe **CIM \_ PExtentRedundancyComponent** est dérivée de [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="2c1c3-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="2c1c3-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2c1c3-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2c1c3-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2c1c3-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c1c3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c1c3-130">Requirements</span></span>



| <span data-ttu-id="2c1c3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c1c3-131">Requirement</span></span> | <span data-ttu-id="2c1c3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c1c3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1c3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c1c3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2c1c3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c1c3-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c1c3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c1c3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2c1c3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c1c3-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c1c3-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c1c3-137">Namespace</span></span><br/>                | <span data-ttu-id="2c1c3-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2c1c3-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c1c3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2c1c3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c1c3-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c1c3-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c1c3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2c1c3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c1c3-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c1c3-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c1c3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c1c3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1c3-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2c1c3-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

