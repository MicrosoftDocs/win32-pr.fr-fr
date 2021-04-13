---
description: L' \_ Association CIM PackageInChassis représente la relation dans laquelle un châssis peut contenir d’autres packages, tels que d’autres châssis et cartes.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: Classe CIM_PackageInChassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483360"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="8f86b-103">\_Classe CIM PackageInChassis</span><span class="sxs-lookup"><span data-stu-id="8f86b-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="8f86b-104">L’Association **CIM \_ PackageInChassis** représente la relation dans laquelle un châssis peut contenir d’autres packages, tels que d’autres châssis et cartes.</span><span class="sxs-lookup"><span data-stu-id="8f86b-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f86b-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8f86b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f86b-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f86b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f86b-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8f86b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8f86b-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8f86b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f86b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f86b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="8f86b-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8f86b-110">Members</span></span>

<span data-ttu-id="8f86b-111">La classe **CIM \_ PackageInChassis** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f86b-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="8f86b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f86b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f86b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f86b-113">Properties</span></span>

<span data-ttu-id="8f86b-114">La classe **CIM \_ PackageInChassis** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8f86b-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f86b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8f86b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f86b-116">Type de données **: \_ châssis CIM**</span><span class="sxs-lookup"><span data-stu-id="8f86b-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="8f86b-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f86b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f86b-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8f86b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8f86b-119">[**\_ Châssis CIM**](cim-chassis.md) décrivant le châssis qui contient d’autres packages physiques.</span><span class="sxs-lookup"><span data-stu-id="8f86b-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="8f86b-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="8f86b-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f86b-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f86b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f86b-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f86b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f86b-123">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="8f86b-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="8f86b-124">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8f86b-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="8f86b-125">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="8f86b-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="8f86b-126">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="8f86b-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f86b-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8f86b-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f86b-128">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="8f86b-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="8f86b-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f86b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f86b-130">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8f86b-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8f86b-131">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) décrivant le package physique qui est contenu dans le châssis.</span><span class="sxs-lookup"><span data-stu-id="8f86b-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f86b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="8f86b-132">Remarks</span></span>

<span data-ttu-id="8f86b-133">La classe **CIM \_ PackageInChassis** est dérivée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="8f86b-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="8f86b-134">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8f86b-134">WMI does not implement this class.</span></span>

<span data-ttu-id="8f86b-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f86b-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f86b-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8f86b-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f86b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f86b-137">Requirements</span></span>



| <span data-ttu-id="8f86b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f86b-138">Requirement</span></span> | <span data-ttu-id="8f86b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f86b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f86b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f86b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8f86b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f86b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f86b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f86b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8f86b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f86b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f86b-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f86b-144">Namespace</span></span><br/>                | <span data-ttu-id="8f86b-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8f86b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f86b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="8f86b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f86b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f86b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f86b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8f86b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f86b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f86b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f86b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f86b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f86b-151">**\_Conteneur CIM**</span><span class="sxs-lookup"><span data-stu-id="8f86b-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

