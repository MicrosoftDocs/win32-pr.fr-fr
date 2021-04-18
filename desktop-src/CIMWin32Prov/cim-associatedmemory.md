---
description: La \_ classe ASSOCIATEMEMORY CIM associe la mémoire installée ou associée, telle que la mémoire cache avec un périphérique logique.
ms.assetid: b108d0cc-9353-4940-a5f6-34bb93330a62
ms.tgt_platform: multiple
title: Classe CIM_AssociatedMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedMemory
- CIM_AssociatedMemory.Dependent
- CIM_AssociatedMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cb1443f54ab273ef6c114b8645e5322c24785f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483640"
---
# <a name="cim_associatedmemory-class"></a><span data-ttu-id="6ba24-103">\_Classe CIM AssociatedMemory</span><span class="sxs-lookup"><span data-stu-id="6ba24-103">CIM\_AssociatedMemory class</span></span>

<span data-ttu-id="6ba24-104">La **classe \_ AssociateMemory CIM** associe la mémoire installée ou associée, telle que la mémoire cache avec un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="6ba24-104">The **CIM\_AssociateMemory** class associates installed or associated memory, such as cache memory with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ba24-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6ba24-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6ba24-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6ba24-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6ba24-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6ba24-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6ba24-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6ba24-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba24-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ba24-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB0-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedMemory : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Memory        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6ba24-110">Membres</span><span class="sxs-lookup"><span data-stu-id="6ba24-110">Members</span></span>

<span data-ttu-id="6ba24-111">La classe **CIM \_ AssociatedMemory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6ba24-111">The **CIM\_AssociatedMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="6ba24-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ba24-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ba24-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ba24-113">Properties</span></span>

<span data-ttu-id="6ba24-114">La classe **CIM \_ AssociatedMemory** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ba24-114">The **CIM\_AssociatedMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ba24-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="6ba24-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba24-116">Type de données **: \_ mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="6ba24-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="6ba24-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ba24-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba24-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6ba24-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6ba24-119">[**\_ Mémoire CIM**](cim-memory.md) qui décrit la mémoire installée sur un appareil ou associée à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6ba24-119">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

</dd> <dt>

<span data-ttu-id="6ba24-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="6ba24-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba24-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6ba24-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6ba24-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ba24-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba24-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="6ba24-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6ba24-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6ba24-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ba24-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6ba24-125">Remarks</span></span>

<span data-ttu-id="6ba24-126">La classe **CIM \_ AssociatedMemory** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6ba24-126">The **CIM\_AssociatedMemory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="6ba24-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6ba24-127">WMI does not implement this class.</span></span>

<span data-ttu-id="6ba24-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6ba24-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6ba24-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6ba24-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba24-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ba24-130">Requirements</span></span>



| <span data-ttu-id="6ba24-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ba24-131">Requirement</span></span> | <span data-ttu-id="6ba24-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ba24-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba24-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ba24-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba24-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ba24-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ba24-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ba24-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba24-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ba24-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ba24-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6ba24-137">Namespace</span></span><br/>                | <span data-ttu-id="6ba24-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6ba24-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ba24-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6ba24-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ba24-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ba24-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ba24-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6ba24-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba24-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba24-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba24-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ba24-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba24-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="6ba24-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

