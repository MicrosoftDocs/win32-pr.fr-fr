---
description: La \_ classe CIM SoftwareFeatureServiceImplementation représente une association entre un service et la manière dont il est implémenté dans le logiciel.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110178"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="fce48-103">\_Classe CIM SoftwareFeatureServiceImplementation</span><span class="sxs-lookup"><span data-stu-id="fce48-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="fce48-104">La classe **CIM \_ SoftwareFeatureServiceImplementation** représente une association entre un service et la manière dont il est implémenté dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="fce48-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="fce48-105">Un service peut être fourni par plusieurs fonctionnalités logicielles, qui fonctionnent conjointement les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="fce48-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="fce48-106">En outre, une fonctionnalité logicielle peut fournir plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="fce48-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="fce48-107">Lorsque plusieurs fonctionnalités logicielles sont associées à un seul service, il est supposé que les éléments fonctionnent conjointement pour fournir le service.</span><span class="sxs-lookup"><span data-stu-id="fce48-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="fce48-108">Si différentes implémentations d’un service existent, chaque implémentation entraînerait des instanciations individuelles de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="fce48-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="fce48-109">Les instanciations individuelles ont alors des associations avec les implémentations uniques.</span><span class="sxs-lookup"><span data-stu-id="fce48-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fce48-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="fce48-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fce48-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fce48-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fce48-112">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fce48-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fce48-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fce48-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce48-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fce48-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fce48-115">Membres</span><span class="sxs-lookup"><span data-stu-id="fce48-115">Members</span></span>

<span data-ttu-id="fce48-116">La classe **CIM \_ SoftwareFeatureServiceImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fce48-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="fce48-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fce48-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fce48-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fce48-118">Properties</span></span>

<span data-ttu-id="fce48-119">La classe **CIM \_ SoftwareFeatureServiceImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fce48-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fce48-120">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="fce48-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fce48-121">Type de données : **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="fce48-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="fce48-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fce48-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fce48-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="fce48-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fce48-124">[**\_ SoftwareFeature CIM**](cim-softwarefeature.md) qui décrit la fonctionnalité de logiciel antécédent.</span><span class="sxs-lookup"><span data-stu-id="fce48-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="fce48-125">**Charge**</span><span class="sxs-lookup"><span data-stu-id="fce48-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fce48-126">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="fce48-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="fce48-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fce48-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fce48-128">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="fce48-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fce48-129">[**\_ Service CIM**](cim-service.md) qui décrit le service dépendant.</span><span class="sxs-lookup"><span data-stu-id="fce48-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fce48-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fce48-130">Remarks</span></span>

<span data-ttu-id="fce48-131">La classe **CIM \_ SoftwareFeatureServiceImplementation** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="fce48-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fce48-132">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="fce48-132">WMI does not implement this class.</span></span>

<span data-ttu-id="fce48-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="fce48-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fce48-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fce48-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce48-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fce48-135">Requirements</span></span>



| <span data-ttu-id="fce48-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fce48-136">Requirement</span></span> | <span data-ttu-id="fce48-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="fce48-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce48-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce48-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fce48-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fce48-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fce48-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce48-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fce48-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fce48-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fce48-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fce48-142">Namespace</span></span><br/>                | <span data-ttu-id="fce48-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fce48-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fce48-144">MOF</span><span class="sxs-lookup"><span data-stu-id="fce48-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fce48-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fce48-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fce48-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fce48-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fce48-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce48-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce48-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce48-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce48-149">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="fce48-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

