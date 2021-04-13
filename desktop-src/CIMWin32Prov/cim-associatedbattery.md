---
description: La \_ dépendance ASSOCIATEDBATTERY CIM associe une batterie à une unité logique. Utilisez cette association pour modéliser les batteries individuelles qui composent un onduleur.
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201071"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="d289a-104">\_Classe CIM AssociatedBattery</span><span class="sxs-lookup"><span data-stu-id="d289a-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="d289a-105">La **dépendance \_ AssociatedBattery CIM** associe une batterie à une unité logique.</span><span class="sxs-lookup"><span data-stu-id="d289a-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="d289a-106">Utilisez cette association pour modéliser les batteries individuelles qui composent un onduleur.</span><span class="sxs-lookup"><span data-stu-id="d289a-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d289a-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d289a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d289a-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d289a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d289a-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d289a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d289a-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d289a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d289a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d289a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d289a-112">Membres</span><span class="sxs-lookup"><span data-stu-id="d289a-112">Members</span></span>

<span data-ttu-id="d289a-113">La classe **CIM \_ AssociatedBattery** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d289a-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="d289a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d289a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d289a-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d289a-115">Properties</span></span>

<span data-ttu-id="d289a-116">La classe **CIM \_ AssociatedBattery** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d289a-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d289a-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="d289a-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d289a-118">Type de données **: \_ batterie CIM**</span><span class="sxs-lookup"><span data-stu-id="d289a-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="d289a-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d289a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d289a-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d289a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d289a-121">[**\_ Batterie CIM**](cim-battery.md) qui décrit la batterie.</span><span class="sxs-lookup"><span data-stu-id="d289a-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="d289a-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="d289a-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d289a-123">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="d289a-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d289a-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d289a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d289a-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="d289a-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d289a-126">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui contient l’appareil logique nécessitant ou associé à la batterie.</span><span class="sxs-lookup"><span data-stu-id="d289a-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d289a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d289a-127">Remarks</span></span>

<span data-ttu-id="d289a-128">La classe **CIM \_ AssociatedBattery** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d289a-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d289a-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d289a-129">WMI does not implement this class.</span></span> <span data-ttu-id="d289a-130">Pour plus d’informations sur les classes dérivées de **CIM \_ AssociatedBattery**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d289a-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d289a-131">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d289a-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d289a-132">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d289a-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d289a-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d289a-133">Requirements</span></span>



| <span data-ttu-id="d289a-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d289a-134">Requirement</span></span> | <span data-ttu-id="d289a-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d289a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d289a-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d289a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d289a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d289a-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d289a-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d289a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d289a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d289a-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d289a-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d289a-140">Namespace</span></span><br/>                | <span data-ttu-id="d289a-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d289a-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d289a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d289a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d289a-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d289a-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d289a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d289a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d289a-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d289a-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d289a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d289a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d289a-147">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="d289a-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

