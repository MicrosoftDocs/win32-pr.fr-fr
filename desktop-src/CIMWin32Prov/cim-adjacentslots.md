---
description: L' \_ Association CIM AdjacentSlots décrit la disposition des emplacements sur un tableau d’hébergement ou une carte d’adaptateur.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: Classe CIM_AdjacentSlots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111106"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="2fd0e-103">\_Classe CIM AdjacentSlots</span><span class="sxs-lookup"><span data-stu-id="2fd0e-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="2fd0e-104">L’Association **CIM \_ AdjacentSlots** décrit la disposition des emplacements sur un tableau d’hébergement ou une carte d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="2fd0e-105">Les informations, telles que la distance entre les emplacements et si elles sont « partagées » (si l’une d’elles est remplie, l’autre emplacement ne peut pas être utilisé), sont transmises en tant que propriétés d’association.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fd0e-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2fd0e-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2fd0e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2fd0e-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2fd0e-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd0e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fd0e-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="2fd0e-111">Membres</span><span class="sxs-lookup"><span data-stu-id="2fd0e-111">Members</span></span>

<span data-ttu-id="2fd0e-112">La classe **CIM \_ AdjacentSlots** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2fd0e-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="2fd0e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2fd0e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fd0e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2fd0e-114">Properties</span></span>

<span data-ttu-id="2fd0e-115">La classe **CIM \_ AdjacentSlots** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fd0e-116">**DistanceBetweenSlots**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd0e-117">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2fd0e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fd0e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fd0e-119">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="2fd0e-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="2fd0e-120">Distance, en pouces, entre les emplacements adjacents.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="2fd0e-121">**SharedSlots**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd0e-122">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fd0e-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fd0e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fd0e-124">Si la **valeur est true**, l’un des emplacements est rempli par une carte d’adaptateur ; l’autre emplacement doit être laissé vide.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="2fd0e-125">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd0e-126">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="2fd0e-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fd0e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fd0e-128">Référence à l’un des emplacements adjacents.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="2fd0e-129">**SlotB**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd0e-130">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="2fd0e-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="2fd0e-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2fd0e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fd0e-132">Référence à l’emplacement adjacent « other ».</span><span class="sxs-lookup"><span data-stu-id="2fd0e-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fd0e-133">Notes</span><span class="sxs-lookup"><span data-stu-id="2fd0e-133">Remarks</span></span>

<span data-ttu-id="2fd0e-134">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-134">WMI does not implement this class.</span></span>

<span data-ttu-id="2fd0e-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2fd0e-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2fd0e-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd0e-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fd0e-137">Requirements</span></span>



| <span data-ttu-id="2fd0e-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fd0e-138">Requirement</span></span> | <span data-ttu-id="2fd0e-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fd0e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd0e-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fd0e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd0e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fd0e-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fd0e-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fd0e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd0e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fd0e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fd0e-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2fd0e-144">Namespace</span></span><br/>                | <span data-ttu-id="2fd0e-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2fd0e-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fd0e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="2fd0e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fd0e-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fd0e-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fd0e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd0e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd0e-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fd0e-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd0e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fd0e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd0e-151">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="2fd0e-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

