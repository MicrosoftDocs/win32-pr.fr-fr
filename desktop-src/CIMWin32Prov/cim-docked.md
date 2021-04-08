---
description: L’Association de la \_ station d’accueil CIM représente la relation entre deux châssis. Par exemple, un ordinateur portable (un type de châssis) peut être ancré dans une station d’accueil (un autre type de châssis). Cette relation classique est décrite de manière explicite.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Classe CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748492"
---
# <a name="cim_docked-class"></a><span data-ttu-id="f531c-105">\_Classe ancrée CIM</span><span class="sxs-lookup"><span data-stu-id="f531c-105">CIM\_Docked class</span></span>

<span data-ttu-id="f531c-106">L’Association de la **\_ station d’accueil CIM** représente la relation entre deux châssis.</span><span class="sxs-lookup"><span data-stu-id="f531c-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="f531c-107">Par exemple, un ordinateur portable (un type de châssis) peut être ancré dans une station d’accueil (un autre type de châssis).</span><span class="sxs-lookup"><span data-stu-id="f531c-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="f531c-108">Cette relation classique est décrite de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="f531c-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f531c-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f531c-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f531c-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f531c-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f531c-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f531c-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f531c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f531c-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f531c-113">Membres</span><span class="sxs-lookup"><span data-stu-id="f531c-113">Members</span></span>

<span data-ttu-id="f531c-114">La **classe \_ ancrée CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f531c-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="f531c-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f531c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f531c-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f531c-116">Properties</span></span>

<span data-ttu-id="f531c-117">La **classe \_ ancrée CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f531c-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f531c-118">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="f531c-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f531c-119">Type de données **: \_ châssis CIM**</span><span class="sxs-lookup"><span data-stu-id="f531c-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="f531c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f531c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f531c-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f531c-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f531c-122">[**\_ Châssis CIM**](cim-chassis.md) décrivant la station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="f531c-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="f531c-123">**Charge**</span><span class="sxs-lookup"><span data-stu-id="f531c-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f531c-124">Type de données **: \_ châssis CIM**</span><span class="sxs-lookup"><span data-stu-id="f531c-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="f531c-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f531c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f531c-126">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f531c-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f531c-127">[**\_ Châssis CIM**](cim-chassis.md) décrivant l’ordinateur portable ancré.</span><span class="sxs-lookup"><span data-stu-id="f531c-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f531c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="f531c-128">Remarks</span></span>

<span data-ttu-id="f531c-129">La **classe \_ ancrée CIM** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f531c-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f531c-130">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="f531c-130">WMI does not implement this class.</span></span>

<span data-ttu-id="f531c-131">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f531c-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f531c-132">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f531c-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f531c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f531c-133">Requirements</span></span>



| <span data-ttu-id="f531c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f531c-134">Requirement</span></span> | <span data-ttu-id="f531c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f531c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f531c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f531c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f531c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f531c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f531c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f531c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f531c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f531c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f531c-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f531c-140">Namespace</span></span><br/>                | <span data-ttu-id="f531c-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f531c-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f531c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f531c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f531c-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f531c-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f531c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f531c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f531c-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f531c-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f531c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f531c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f531c-147">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="f531c-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

