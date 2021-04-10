---
description: La \_ classe CIM ComputerSystemPackage représente une association qui définit explicitement la relation entre les systèmes informatiques unitaires et un ou plusieurs packages physiques.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950697"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="e1d4e-103">\_Classe CIM ComputerSystemPackage</span><span class="sxs-lookup"><span data-stu-id="e1d4e-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="e1d4e-104">La classe **CIM \_ ComputerSystemPackage** représente une association qui définit explicitement la relation entre les systèmes informatiques unitaires et un ou plusieurs packages physiques.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="e1d4e-105">L’Association est semblable à la façon dont les unités logiques sont réalisées par les éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1d4e-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e1d4e-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e1d4e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e1d4e-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e1d4e-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d4e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1d4e-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e1d4e-111">Membres</span><span class="sxs-lookup"><span data-stu-id="e1d4e-111">Members</span></span>

<span data-ttu-id="e1d4e-112">La classe **CIM \_ ComputerSystemPackage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e1d4e-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="e1d4e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1d4e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1d4e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1d4e-114">Properties</span></span>

<span data-ttu-id="e1d4e-115">La classe **CIM \_ ComputerSystemPackage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1d4e-116">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e1d4e-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1d4e-117">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="e1d4e-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="e1d4e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1d4e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1d4e-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e1d4e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e1d4e-120">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui décrit le ou les packages physiques qui réalisent un système informatique unitaire.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e1d4e-121">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e1d4e-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1d4e-122">Type de données : **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e1d4e-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e1d4e-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1d4e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1d4e-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="e1d4e-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e1d4e-125">[**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) qui décrit le système informatique unitaire.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1d4e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="e1d4e-126">Remarks</span></span>

<span data-ttu-id="e1d4e-127">La classe **CIM \_ ComputerSystemPackage** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e1d4e-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e1d4e-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-128">WMI does not implement this class.</span></span>

<span data-ttu-id="e1d4e-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e1d4e-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e1d4e-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d4e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1d4e-131">Requirements</span></span>



| <span data-ttu-id="e1d4e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1d4e-132">Requirement</span></span> | <span data-ttu-id="e1d4e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1d4e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d4e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1d4e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d4e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1d4e-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1d4e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1d4e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d4e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1d4e-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1d4e-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1d4e-138">Namespace</span></span><br/>                | <span data-ttu-id="e1d4e-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e1d4e-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e1d4e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e1d4e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1d4e-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1d4e-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1d4e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e1d4e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1d4e-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d4e-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d4e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1d4e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d4e-145">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="e1d4e-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

