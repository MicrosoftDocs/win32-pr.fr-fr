---
description: La \_ classe de conteneur CIM représente une association entre un élément physique contenu et un élément physique contenant. Un objet conteneur doit être un package physique.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: Classe CIM_Container
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950695"
---
# <a name="cim_container-class"></a><span data-ttu-id="f1a52-104">\_Classe de conteneur CIM</span><span class="sxs-lookup"><span data-stu-id="f1a52-104">CIM\_Container class</span></span>

<span data-ttu-id="f1a52-105">La classe de **\_ conteneur CIM** représente une association entre un élément physique contenu et un élément physique contenant.</span><span class="sxs-lookup"><span data-stu-id="f1a52-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="f1a52-106">Un objet conteneur doit être un package physique.</span><span class="sxs-lookup"><span data-stu-id="f1a52-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1a52-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f1a52-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1a52-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f1a52-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f1a52-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f1a52-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f1a52-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f1a52-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a52-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1a52-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="f1a52-112">Membres</span><span class="sxs-lookup"><span data-stu-id="f1a52-112">Members</span></span>

<span data-ttu-id="f1a52-113">La classe de **\_ conteneur CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1a52-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="f1a52-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1a52-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1a52-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1a52-115">Properties</span></span>

<span data-ttu-id="f1a52-116">La classe de **\_ conteneur CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f1a52-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1a52-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f1a52-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a52-118">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="f1a52-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="f1a52-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1a52-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1a52-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f1a52-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f1a52-121">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) qui représente le package physique qui contient d’autres éléments physiques, y compris d’autres packages.</span><span class="sxs-lookup"><span data-stu-id="f1a52-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="f1a52-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="f1a52-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a52-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1a52-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1a52-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1a52-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1a52-125">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="f1a52-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="f1a52-126">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="f1a52-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="f1a52-127">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="f1a52-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f1a52-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f1a52-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a52-129">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="f1a52-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="f1a52-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1a52-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1a52-131">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f1a52-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1a52-132">[**\_ PhysicalElement CIM**](cim-physicalelement.md) qui décrit l’élément physique contenu dans le package.</span><span class="sxs-lookup"><span data-stu-id="f1a52-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1a52-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f1a52-133">Remarks</span></span>

<span data-ttu-id="f1a52-134">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="f1a52-134">WMI does not implement this class.</span></span> <span data-ttu-id="f1a52-135">Pour plus d’informations sur les classes dérivées du **\_ conteneur CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f1a52-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f1a52-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f1a52-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1a52-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f1a52-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a52-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1a52-138">Requirements</span></span>



| <span data-ttu-id="f1a52-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1a52-139">Requirement</span></span> | <span data-ttu-id="f1a52-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a52-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a52-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1a52-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a52-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1a52-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1a52-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1a52-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a52-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1a52-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1a52-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1a52-145">Namespace</span></span><br/>                | <span data-ttu-id="f1a52-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f1a52-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1a52-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f1a52-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1a52-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1a52-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1a52-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f1a52-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1a52-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1a52-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a52-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1a52-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a52-152">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="f1a52-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

