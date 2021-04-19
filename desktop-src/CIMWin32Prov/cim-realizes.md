---
description: La \_ classe CIM réalise la représentation de l’Association qui définit le mappage entre un périphérique logique et le composant physique qui implémente l’appareil.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: Classe CIM_Realizes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515563"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="e8292-103">CIM \_ réalise la classe</span><span class="sxs-lookup"><span data-stu-id="e8292-103">CIM\_Realizes class</span></span>

<span data-ttu-id="e8292-104">La classe **CIM \_ réalise** la représentation de l’Association qui définit le mappage entre un périphérique logique et le composant physique qui implémente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e8292-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8292-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e8292-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e8292-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e8292-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e8292-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e8292-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e8292-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e8292-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8292-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8292-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e8292-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e8292-110">Members</span></span>

<span data-ttu-id="e8292-111">La classe **CIM \_ réalise** les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e8292-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="e8292-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e8292-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8292-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e8292-113">Properties</span></span>

<span data-ttu-id="e8292-114">La classe **CIM \_ réalise** les propriétés.</span><span class="sxs-lookup"><span data-stu-id="e8292-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8292-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e8292-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8292-116">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="e8292-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="e8292-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8292-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8292-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e8292-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e8292-119">[**\_ PhysicalElement CIM**](cim-physicalelement.md) qui décrit le composant physique qui implémente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e8292-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="e8292-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e8292-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8292-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="e8292-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e8292-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8292-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8292-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="e8292-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e8292-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e8292-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8292-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e8292-125">Remarks</span></span>

<span data-ttu-id="e8292-126">La classe **CIM \_ réalise** la dérivation de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e8292-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e8292-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e8292-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e8292-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e8292-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e8292-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e8292-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8292-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8292-130">Requirements</span></span>



| <span data-ttu-id="e8292-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8292-131">Requirement</span></span> | <span data-ttu-id="e8292-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8292-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8292-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8292-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e8292-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8292-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8292-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8292-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e8292-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8292-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8292-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e8292-137">Namespace</span></span><br/>                | <span data-ttu-id="e8292-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e8292-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8292-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e8292-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8292-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8292-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8292-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e8292-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8292-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8292-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8292-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8292-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8292-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="e8292-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

