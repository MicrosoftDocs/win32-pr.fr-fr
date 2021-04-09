---
description: L' \_ Association CIM PackagedComponent représente une relation explicite dans laquelle un composant est généralement contenu dans un package physique, tel qu’un châssis ou une carte.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: Classe CIM_PackagedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860749"
---
# <a name="cim_packagedcomponent-class"></a><span data-ttu-id="153d8-103">\_Classe CIM PackagedComponent</span><span class="sxs-lookup"><span data-stu-id="153d8-103">CIM\_PackagedComponent class</span></span>

<span data-ttu-id="153d8-104">L’Association **CIM \_ PackagedComponent** représente une relation explicite dans laquelle un composant est généralement contenu dans un package physique, tel qu’un châssis ou une carte.</span><span class="sxs-lookup"><span data-stu-id="153d8-104">The **CIM\_PackagedComponent** association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

<span data-ttu-id="153d8-105">**Remarque**  Un composant peut être supprimé ou n’être pas encore inséré dans le package qui le contient (autrement dit, la propriété booléenne **amovible** a la **valeur true**).</span><span class="sxs-lookup"><span data-stu-id="153d8-105">**Note**  A component may be removed from, or not yet inserted into, its containing package (that is, the **Removable** Boolean property is **TRUE**).</span></span> <span data-ttu-id="153d8-106">Par conséquent, un composant peut ne pas toujours être associé à un conteneur.</span><span class="sxs-lookup"><span data-stu-id="153d8-106">Therefore, a component may not always be associated with a container.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="153d8-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="153d8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="153d8-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="153d8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="153d8-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="153d8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="153d8-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="153d8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="153d8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="153d8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="153d8-112">Membres</span><span class="sxs-lookup"><span data-stu-id="153d8-112">Members</span></span>

<span data-ttu-id="153d8-113">La classe **CIM \_ PackagedComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="153d8-113">The **CIM\_PackagedComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="153d8-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="153d8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="153d8-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="153d8-115">Properties</span></span>

<span data-ttu-id="153d8-116">La classe **CIM \_ PackagedComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="153d8-116">The **CIM\_PackagedComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="153d8-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="153d8-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153d8-118">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="153d8-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="153d8-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153d8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="153d8-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="153d8-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="153d8-121">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui décrit le package physique qui contient le ou les composants.</span><span class="sxs-lookup"><span data-stu-id="153d8-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that contains component(s).</span></span>

</dd> <dt>

<span data-ttu-id="153d8-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="153d8-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153d8-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="153d8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="153d8-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153d8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153d8-125">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="153d8-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="153d8-126">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="153d8-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="153d8-127">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="153d8-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="153d8-128">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="153d8-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="153d8-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="153d8-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153d8-130">Type de données : **CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="153d8-130">Data type: **CIM\_PhysicalComponent**</span></span>
</dt> <dt>

<span data-ttu-id="153d8-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153d8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="153d8-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="153d8-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="153d8-133">[**\_ PhysicalComponent CIM**](cim-physicalcomponent.md) décrivant le composant physique contenu dans le package.</span><span class="sxs-lookup"><span data-stu-id="153d8-133">A [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) describing the physical component which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="153d8-134">Notes</span><span class="sxs-lookup"><span data-stu-id="153d8-134">Remarks</span></span>

<span data-ttu-id="153d8-135">La classe **CIM \_ PackagedComponent** est dérivée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="153d8-135">The **CIM\_PackagedComponent** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="153d8-136">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="153d8-136">WMI does not implement this class.</span></span>

<span data-ttu-id="153d8-137">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="153d8-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="153d8-138">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="153d8-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="153d8-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="153d8-139">Requirements</span></span>



| <span data-ttu-id="153d8-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="153d8-140">Requirement</span></span> | <span data-ttu-id="153d8-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="153d8-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="153d8-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153d8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="153d8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="153d8-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="153d8-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153d8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="153d8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="153d8-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="153d8-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="153d8-146">Namespace</span></span><br/>                | <span data-ttu-id="153d8-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="153d8-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="153d8-148">MOF</span><span class="sxs-lookup"><span data-stu-id="153d8-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="153d8-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="153d8-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="153d8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="153d8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153d8-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153d8-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153d8-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="153d8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153d8-153">**\_Conteneur CIM**</span><span class="sxs-lookup"><span data-stu-id="153d8-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

