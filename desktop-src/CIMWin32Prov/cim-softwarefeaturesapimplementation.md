---
description: La \_ classe CIM SoftwareFeatureSAPImplementation représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté dans le logiciel.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860641"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a><span data-ttu-id="65ed2-103">\_Classe CIM SoftwareFeatureSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="65ed2-103">CIM\_SoftwareFeatureSAPImplementation class</span></span>

<span data-ttu-id="65ed2-104">La classe **CIM \_ SoftwareFeatureSAPImplementation** représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="65ed2-104">The **CIM\_SoftwareFeatureSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented in software.</span></span> <span data-ttu-id="65ed2-105">Un SAP peut être fourni par plusieurs fonctionnalités logicielles pour fonctionner conjointement.</span><span class="sxs-lookup"><span data-stu-id="65ed2-105">A SAP can be provided by more than one software feature to operate in conjunction with one another.</span></span> <span data-ttu-id="65ed2-106">En outre, une fonctionnalité logicielle peut fournir plusieurs SAP.</span><span class="sxs-lookup"><span data-stu-id="65ed2-106">Additionally, a software feature can provide more than one SAP.</span></span> <span data-ttu-id="65ed2-107">Lorsque de nombreuses fonctionnalités logicielles sont associées à un seul SAP, il est supposé que les éléments fonctionnent conjointement pour fournir le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="65ed2-107">When many software features are associated with a single SAP, it is assumed that the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="65ed2-108">Si différentes implémentations d’un SAP existent, chaque implémentation entraînerait des instanciations individuelles de l’objet SAP.</span><span class="sxs-lookup"><span data-stu-id="65ed2-108">If different implementations of a SAP exist, each implementation would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="65ed2-109">Les instanciations individuelles ont alors des associations avec les implémentations uniques.</span><span class="sxs-lookup"><span data-stu-id="65ed2-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65ed2-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="65ed2-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65ed2-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65ed2-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65ed2-112">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="65ed2-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="65ed2-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="65ed2-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ed2-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65ed2-114">Syntax</span></span>

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="65ed2-115">Membres</span><span class="sxs-lookup"><span data-stu-id="65ed2-115">Members</span></span>

<span data-ttu-id="65ed2-116">La classe **CIM \_ SoftwareFeatureSAPImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="65ed2-116">The **CIM\_SoftwareFeatureSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="65ed2-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65ed2-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65ed2-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65ed2-118">Properties</span></span>

<span data-ttu-id="65ed2-119">La classe **CIM \_ SoftwareFeatureSAPImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="65ed2-119">The **CIM\_SoftwareFeatureSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65ed2-120">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="65ed2-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ed2-121">Type de données : **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="65ed2-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="65ed2-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65ed2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ed2-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="65ed2-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="65ed2-124">[**\_ SoftwareFeature CIM**](cim-softwarefeature.md) qui décrit la fonctionnalité de logiciel antécédent.</span><span class="sxs-lookup"><span data-stu-id="65ed2-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="65ed2-125">**Charge**</span><span class="sxs-lookup"><span data-stu-id="65ed2-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ed2-126">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="65ed2-126">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="65ed2-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65ed2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ed2-128">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="65ed2-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="65ed2-129">Un [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) qui décrit le point d’accès au service dépendant.</span><span class="sxs-lookup"><span data-stu-id="65ed2-129">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the dependent service access point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65ed2-130">Notes</span><span class="sxs-lookup"><span data-stu-id="65ed2-130">Remarks</span></span>

<span data-ttu-id="65ed2-131">La classe **CIM \_ SoftwareFeatureSAPImplementation** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="65ed2-131">The **CIM\_SoftwareFeatureSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="65ed2-132">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="65ed2-132">WMI does not implement this class.</span></span>

<span data-ttu-id="65ed2-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="65ed2-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65ed2-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="65ed2-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ed2-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65ed2-135">Requirements</span></span>



| <span data-ttu-id="65ed2-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65ed2-136">Requirement</span></span> | <span data-ttu-id="65ed2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="65ed2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65ed2-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ed2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="65ed2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65ed2-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65ed2-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ed2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="65ed2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65ed2-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65ed2-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65ed2-142">Namespace</span></span><br/>                | <span data-ttu-id="65ed2-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="65ed2-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65ed2-144">MOF</span><span class="sxs-lookup"><span data-stu-id="65ed2-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65ed2-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65ed2-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65ed2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="65ed2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65ed2-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ed2-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ed2-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ed2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ed2-149">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="65ed2-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

