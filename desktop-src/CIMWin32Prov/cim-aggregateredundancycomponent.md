---
description: La \_ classe CIM AggregateRedundancyComponent décrit l’étendue physique agrégée dans un groupe de redondance de stockage.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: Classe CIM_AggregateRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748716"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="ef72e-103">\_Classe CIM AggregateRedundancyComponent</span><span class="sxs-lookup"><span data-stu-id="ef72e-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="ef72e-104">La classe **CIM \_ AggregateRedundancyComponent** décrit l’étendue physique agrégée dans un groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="ef72e-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef72e-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ef72e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ef72e-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ef72e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ef72e-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ef72e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ef72e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ef72e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef72e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef72e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="ef72e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ef72e-110">Members</span></span>

<span data-ttu-id="ef72e-111">La classe **CIM \_ AggregateRedundancyComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef72e-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="ef72e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef72e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef72e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef72e-113">Properties</span></span>

<span data-ttu-id="ef72e-114">La classe **CIM \_ AggregateRedundancyComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef72e-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef72e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ef72e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef72e-116">Type de données : **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="ef72e-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="ef72e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef72e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef72e-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="ef72e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ef72e-119">[**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) qui contient le groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="ef72e-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="ef72e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ef72e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef72e-121">Type de données : **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="ef72e-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="ef72e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef72e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef72e-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="ef72e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ef72e-124">[**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) qui contient l’extension physique globale qui participe au groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="ef72e-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef72e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ef72e-125">Remarks</span></span>

<span data-ttu-id="ef72e-126">La classe **CIM \_ AggregateRedundancyComponent** est dérivée de [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="ef72e-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="ef72e-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ef72e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ef72e-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ef72e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ef72e-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ef72e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef72e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef72e-130">Requirements</span></span>



| <span data-ttu-id="ef72e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef72e-131">Requirement</span></span> | <span data-ttu-id="ef72e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef72e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef72e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef72e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef72e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef72e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef72e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef72e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef72e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef72e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef72e-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef72e-137">Namespace</span></span><br/>                | <span data-ttu-id="ef72e-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ef72e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef72e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ef72e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef72e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef72e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef72e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ef72e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef72e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef72e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef72e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef72e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef72e-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ef72e-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

