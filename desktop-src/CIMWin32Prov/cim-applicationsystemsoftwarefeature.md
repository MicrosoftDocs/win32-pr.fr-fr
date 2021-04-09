---
description: La \_ classe CIM ApplicationSystemSoftwareFeature représente une association qui identifie les fonctionnalités logicielles qui composent un système d’applications particulier. Les fonctionnalités du logiciel peuvent être incluses dans différents produits.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861425"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="3cc6e-104">\_Classe CIM ApplicationSystemSoftwareFeature</span><span class="sxs-lookup"><span data-stu-id="3cc6e-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="3cc6e-105">La classe **CIM \_ ApplicationSystemSoftwareFeature** représente une association qui identifie les fonctionnalités logicielles qui composent un système d’applications particulier.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="3cc6e-106">Les fonctionnalités du logiciel peuvent être incluses dans différents produits.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cc6e-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3cc6e-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3cc6e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3cc6e-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3cc6e-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc6e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cc6e-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="3cc6e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3cc6e-112">Members</span></span>

<span data-ttu-id="3cc6e-113">La classe **CIM \_ ApplicationSystemSoftwareFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3cc6e-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="3cc6e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3cc6e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cc6e-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3cc6e-115">Properties</span></span>

<span data-ttu-id="3cc6e-116">La classe **CIM \_ ApplicationSystemSoftwareFeature** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cc6e-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3cc6e-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cc6e-118">Type de données : **CIM \_ ApplicationSystem**</span><span class="sxs-lookup"><span data-stu-id="3cc6e-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3cc6e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3cc6e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cc6e-120">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="3cc6e-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3cc6e-121">[**\_ ApplicationSystem CIM**](cim-applicationsystem.md) qui contient le système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="3cc6e-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3cc6e-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cc6e-123">Type de données : **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="3cc6e-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="3cc6e-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3cc6e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cc6e-125">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3cc6e-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3cc6e-126">[**\_ SoftwareFeature CIM**](cim-softwarefeature.md) qui contient l’élément enfant qui est un composant d’un système.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cc6e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3cc6e-127">Remarks</span></span>

<span data-ttu-id="3cc6e-128">La classe **CIM \_ ApplicationSystemSoftwareFeature** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3cc6e-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="3cc6e-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-129">WMI does not implement this class.</span></span>

<span data-ttu-id="3cc6e-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3cc6e-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3cc6e-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc6e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cc6e-132">Requirements</span></span>



| <span data-ttu-id="3cc6e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cc6e-133">Requirement</span></span> | <span data-ttu-id="3cc6e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cc6e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc6e-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cc6e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3cc6e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cc6e-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cc6e-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cc6e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3cc6e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cc6e-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cc6e-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3cc6e-139">Namespace</span></span><br/>                | <span data-ttu-id="3cc6e-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3cc6e-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3cc6e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3cc6e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cc6e-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cc6e-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cc6e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3cc6e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cc6e-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cc6e-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc6e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cc6e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc6e-146">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3cc6e-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

