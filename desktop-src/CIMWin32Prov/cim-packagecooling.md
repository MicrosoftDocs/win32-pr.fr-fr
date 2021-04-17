---
description: L' \_ Association CIM PackageCooling représente la relation dans laquelle un appareil de refroidissement est installé dans un package, tel qu’un châssis ou un rack, pour faciliter le refroidissement du package.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: Classe CIM_PackageCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523740"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="f8acd-103">\_Classe CIM PackageCooling</span><span class="sxs-lookup"><span data-stu-id="f8acd-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="f8acd-104">L’Association **CIM \_ PackageCooling** représente la relation dans laquelle un appareil de refroidissement est installé dans un package, tel qu’un châssis ou un rack, pour faciliter le refroidissement du package.</span><span class="sxs-lookup"><span data-stu-id="f8acd-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8acd-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f8acd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8acd-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8acd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f8acd-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f8acd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f8acd-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f8acd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8acd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8acd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f8acd-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f8acd-110">Members</span></span>

<span data-ttu-id="f8acd-111">La classe **CIM \_ PackageCooling** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8acd-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="f8acd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8acd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8acd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8acd-113">Properties</span></span>

<span data-ttu-id="f8acd-114">La classe **CIM \_ PackageCooling** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8acd-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8acd-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="f8acd-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8acd-116">Type de données : **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="f8acd-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f8acd-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8acd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8acd-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f8acd-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f8acd-119">[**\_ CoolingDevice CIM**](cim-coolingdevice.md) qui décrit l’appareil de refroidissement pour le package.</span><span class="sxs-lookup"><span data-stu-id="f8acd-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="f8acd-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="f8acd-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8acd-121">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="f8acd-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="f8acd-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8acd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8acd-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="f8acd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f8acd-124">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui décrit le package physique dont l’environnement est refroidi.</span><span class="sxs-lookup"><span data-stu-id="f8acd-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8acd-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f8acd-125">Remarks</span></span>

<span data-ttu-id="f8acd-126">**CIM \_ PackageCooling** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f8acd-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f8acd-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="f8acd-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f8acd-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8acd-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8acd-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f8acd-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8acd-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8acd-130">Requirements</span></span>



| <span data-ttu-id="f8acd-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8acd-131">Requirement</span></span> | <span data-ttu-id="f8acd-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8acd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8acd-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8acd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8acd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8acd-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8acd-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8acd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8acd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8acd-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8acd-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8acd-137">Namespace</span></span><br/>                | <span data-ttu-id="f8acd-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f8acd-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8acd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f8acd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8acd-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8acd-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8acd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f8acd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8acd-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8acd-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8acd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8acd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8acd-144">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="f8acd-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

