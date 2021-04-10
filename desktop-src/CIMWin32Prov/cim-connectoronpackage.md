---
description: La \_ classe CIM ConnectorOnPackage représente une association qui rend explicite la relation d’imbrication entre les connecteurs et les packages. Les packages physiques contiennent des connecteurs et d’autres éléments physiques.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: Classe CIM_ConnectorOnPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861333"
---
# <a name="cim_connectoronpackage-class"></a><span data-ttu-id="324cd-104">\_Classe CIM ConnectorOnPackage</span><span class="sxs-lookup"><span data-stu-id="324cd-104">CIM\_ConnectorOnPackage class</span></span>

<span data-ttu-id="324cd-105">La classe **CIM \_ ConnectorOnPackage** représente une association qui rend explicite la relation d’imbrication entre les connecteurs et les packages.</span><span class="sxs-lookup"><span data-stu-id="324cd-105">The **CIM\_ConnectorOnPackage** class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="324cd-106">Les packages physiques contiennent des connecteurs et d’autres éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="324cd-106">Physical packages contain connectors as well as other physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="324cd-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="324cd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="324cd-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="324cd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="324cd-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="324cd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="324cd-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="324cd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="324cd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="324cd-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="324cd-112">Membres</span><span class="sxs-lookup"><span data-stu-id="324cd-112">Members</span></span>

<span data-ttu-id="324cd-113">La classe **CIM \_ ConnectorOnPackage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="324cd-113">The **CIM\_ConnectorOnPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="324cd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="324cd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="324cd-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="324cd-115">Properties</span></span>

<span data-ttu-id="324cd-116">La classe **CIM \_ ConnectorOnPackage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="324cd-116">The **CIM\_ConnectorOnPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="324cd-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="324cd-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="324cd-118">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="324cd-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="324cd-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="324cd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="324cd-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="324cd-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="324cd-121">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui décrit le package physique qui possède un connecteur.</span><span class="sxs-lookup"><span data-stu-id="324cd-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="324cd-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="324cd-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="324cd-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="324cd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="324cd-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="324cd-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="324cd-125">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="324cd-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="324cd-126">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="324cd-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="324cd-127">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="324cd-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="324cd-128">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="324cd-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="324cd-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="324cd-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="324cd-130">Type de données : **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="324cd-130">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="324cd-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="324cd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="324cd-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="324cd-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="324cd-133">[**\_ PhysicalConnector CIM**](cim-physicalconnector.md) qui décrit le connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="324cd-133">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="324cd-134">Notes</span><span class="sxs-lookup"><span data-stu-id="324cd-134">Remarks</span></span>

<span data-ttu-id="324cd-135">La classe **CIM \_ ConnectorOnPackage** est dérivée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="324cd-135">The **CIM\_ConnectorOnPackage** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="324cd-136">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="324cd-136">WMI does not implement this class.</span></span>

<span data-ttu-id="324cd-137">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="324cd-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="324cd-138">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="324cd-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="324cd-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="324cd-139">Requirements</span></span>



| <span data-ttu-id="324cd-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="324cd-140">Requirement</span></span> | <span data-ttu-id="324cd-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="324cd-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="324cd-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="324cd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="324cd-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="324cd-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="324cd-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="324cd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="324cd-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="324cd-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="324cd-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="324cd-146">Namespace</span></span><br/>                | <span data-ttu-id="324cd-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="324cd-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="324cd-148">MOF</span><span class="sxs-lookup"><span data-stu-id="324cd-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="324cd-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="324cd-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="324cd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="324cd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="324cd-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="324cd-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="324cd-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="324cd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324cd-153">**\_Conteneur CIM**</span><span class="sxs-lookup"><span data-stu-id="324cd-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

