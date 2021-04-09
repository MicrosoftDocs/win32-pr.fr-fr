---
description: L' \_ Association CIM PackageInSlot représente la relation entre les cartes d’appareil et le châssis dans lequel elles sont montées.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: Classe CIM_PackageInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110262"
---
# <a name="cim_packageinslot-class"></a><span data-ttu-id="f446f-103">\_Classe CIM PackageInSlot</span><span class="sxs-lookup"><span data-stu-id="f446f-103">CIM\_PackageInSlot class</span></span>

<span data-ttu-id="f446f-104">L’Association **CIM \_ PackageInSlot** représente la relation entre les cartes d’appareil et le châssis dans lequel elles sont montées.</span><span class="sxs-lookup"><span data-stu-id="f446f-104">The **CIM\_PackageInSlot** association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f446f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f446f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f446f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f446f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f446f-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f446f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f446f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f446f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f446f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f446f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f446f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f446f-110">Members</span></span>

<span data-ttu-id="f446f-111">La classe **CIM \_ PackageInSlot** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f446f-111">The **CIM\_PackageInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="f446f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f446f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f446f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f446f-113">Properties</span></span>

<span data-ttu-id="f446f-114">La classe **CIM \_ PackageInSlot** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f446f-114">The **CIM\_PackageInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f446f-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="f446f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f446f-116">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="f446f-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="f446f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f446f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f446f-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f446f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f446f-119">[**\_ Emplacement CIM**](cim-slot.md) décrivant l’emplacement dans lequel le package physique est inséré.</span><span class="sxs-lookup"><span data-stu-id="f446f-119">A [**CIM\_Slot**](cim-slot.md) describing the slot into which the physical package is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="f446f-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="f446f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f446f-121">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="f446f-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="f446f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f446f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f446f-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f446f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f446f-124">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) décrivant le package dans l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="f446f-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the package in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f446f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f446f-125">Remarks</span></span>

<span data-ttu-id="f446f-126">**CIM \_ PackageInSlot** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f446f-126">**CIM\_PackageInSlot** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f446f-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="f446f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f446f-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f446f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f446f-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f446f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f446f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f446f-130">Requirements</span></span>



| <span data-ttu-id="f446f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f446f-131">Requirement</span></span> | <span data-ttu-id="f446f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f446f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f446f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f446f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f446f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f446f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f446f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f446f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f446f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f446f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f446f-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f446f-137">Namespace</span></span><br/>                | <span data-ttu-id="f446f-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f446f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f446f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f446f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f446f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f446f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f446f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f446f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f446f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f446f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f446f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f446f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f446f-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="f446f-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

