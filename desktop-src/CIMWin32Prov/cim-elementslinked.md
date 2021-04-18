---
description: L' \_ Association CIM ElementsLinked représente des éléments physiques reliés par un lien physique.
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: Classe CIM_ElementsLinked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515935"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="7f1b8-103">\_Classe CIM ElementsLinked</span><span class="sxs-lookup"><span data-stu-id="7f1b8-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="7f1b8-104">L’Association **CIM \_ ElementsLinked** représente des éléments physiques reliés par un lien physique.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f1b8-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7f1b8-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7f1b8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7f1b8-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7f1b8-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f1b8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7f1b8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7f1b8-110">Members</span></span>

<span data-ttu-id="7f1b8-111">La classe **CIM \_ ElementsLinked** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7f1b8-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="7f1b8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f1b8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f1b8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f1b8-113">Properties</span></span>

<span data-ttu-id="7f1b8-114">La classe **CIM \_ ElementsLinked** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f1b8-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7f1b8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f1b8-116">Type de données : **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="7f1b8-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="7f1b8-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f1b8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f1b8-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7f1b8-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7f1b8-119">[**\_ PhysicalLink CIM**](cim-physicallink.md) qui décrit le lien physique.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="7f1b8-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7f1b8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f1b8-121">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="7f1b8-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="7f1b8-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f1b8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f1b8-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="7f1b8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7f1b8-124">[**\_ PhysicalElement CIM**](cim-physicalelement.md) qui décrit l’élément physique lié.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f1b8-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7f1b8-125">Remarks</span></span>

<span data-ttu-id="7f1b8-126">La classe **CIM \_ ElementsLinked** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7f1b8-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7f1b8-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7f1b8-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7f1b8-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7f1b8-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f1b8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f1b8-130">Requirements</span></span>



| <span data-ttu-id="7f1b8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f1b8-131">Requirement</span></span> | <span data-ttu-id="7f1b8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f1b8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1b8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f1b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7f1b8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f1b8-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f1b8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f1b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7f1b8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f1b8-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f1b8-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f1b8-137">Namespace</span></span><br/>                | <span data-ttu-id="7f1b8-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7f1b8-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f1b8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7f1b8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f1b8-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b8-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f1b8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7f1b8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f1b8-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b8-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f1b8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f1b8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1b8-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="7f1b8-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

