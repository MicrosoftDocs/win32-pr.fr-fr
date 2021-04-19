---
description: L' \_ Association CIM RealizesAggregatePExtent représente la relation dans laquelle la \_ classe CIM AggregatePExtent est réalisée sur un support physique.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: Classe CIM_RealizesAggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512892"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="5aa7f-103">\_Classe CIM RealizesAggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="5aa7f-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="5aa7f-104">L’Association **CIM \_ RealizesAggregatePExtent** représente la relation dans laquelle la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) est réalisée sur un support physique.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5aa7f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5aa7f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5aa7f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5aa7f-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5aa7f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa7f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5aa7f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5aa7f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5aa7f-110">Members</span></span>

<span data-ttu-id="5aa7f-111">La classe **CIM \_ RealizesAggregatePExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5aa7f-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="5aa7f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5aa7f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5aa7f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5aa7f-113">Properties</span></span>

<span data-ttu-id="5aa7f-114">La classe **CIM \_ RealizesAggregatePExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5aa7f-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa7f-116">Type de données : **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="5aa7f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5aa7f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5aa7f-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="5aa7f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5aa7f-119">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) qui décrit le support physique sur lequel l’extension est réalisée.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="5aa7f-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa7f-121">Type de données : **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="5aa7f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5aa7f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5aa7f-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="5aa7f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5aa7f-124">[**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) qui se trouve sur le média.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5aa7f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5aa7f-125">Remarks</span></span>

<span data-ttu-id="5aa7f-126">La classe **CIM \_ RealizesAggregatePExtent** est dérivée de l' [**\_ esprit CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="5aa7f-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="5aa7f-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="5aa7f-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5aa7f-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa7f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5aa7f-130">Requirements</span></span>



| <span data-ttu-id="5aa7f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5aa7f-131">Requirement</span></span> | <span data-ttu-id="5aa7f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5aa7f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa7f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aa7f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa7f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5aa7f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5aa7f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aa7f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa7f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aa7f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5aa7f-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5aa7f-137">Namespace</span></span><br/>                | <span data-ttu-id="5aa7f-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5aa7f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5aa7f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5aa7f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aa7f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aa7f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5aa7f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aa7f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa7f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aa7f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa7f-144">**CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

