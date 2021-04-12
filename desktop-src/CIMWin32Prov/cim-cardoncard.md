---
description: L' \_ Association CIM CardOnCard décrit des relations sur les cartes qui peuvent être connectées à des cartes mères/cartes de Baseboard, daughtercards d’un adaptateur ou des cartes qui prennent en charge des modules spéciaux de type carte.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: Classe CIM_CardOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393119"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="429dd-103">\_Classe CIM CardOnCard</span><span class="sxs-lookup"><span data-stu-id="429dd-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="429dd-104">L’Association **CIM \_ CardOnCard** décrit des relations sur les cartes qui peuvent être connectées à des cartes mères/cartes de Baseboard, daughtercards d’un adaptateur ou des cartes qui prennent en charge des modules spéciaux de type carte.</span><span class="sxs-lookup"><span data-stu-id="429dd-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="429dd-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="429dd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="429dd-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="429dd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="429dd-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="429dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="429dd-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="429dd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="429dd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="429dd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="429dd-110">Membres</span><span class="sxs-lookup"><span data-stu-id="429dd-110">Members</span></span>

<span data-ttu-id="429dd-111">La classe **CIM \_ CardOnCard** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="429dd-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="429dd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="429dd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="429dd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="429dd-113">Properties</span></span>

<span data-ttu-id="429dd-114">La classe **CIM \_ CardOnCard** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="429dd-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="429dd-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="429dd-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="429dd-116">Type de données **: \_ carte CIM**</span><span class="sxs-lookup"><span data-stu-id="429dd-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="429dd-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="429dd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="429dd-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="429dd-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="429dd-119">Une [**\_ carte CIM**](cim-card.md) qui décrit la carte qui héberge une autre carte.</span><span class="sxs-lookup"><span data-stu-id="429dd-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="429dd-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="429dd-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="429dd-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="429dd-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="429dd-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="429dd-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="429dd-123">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="429dd-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="429dd-124">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="429dd-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="429dd-125">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="429dd-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="429dd-126">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="429dd-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="429dd-127">**MountOrSlotDescription**</span><span class="sxs-lookup"><span data-stu-id="429dd-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="429dd-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="429dd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="429dd-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="429dd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="429dd-130">Décrit et identifie la manière dont la carte est montée ou branchée sur la carte « Other » (autre).</span><span class="sxs-lookup"><span data-stu-id="429dd-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="429dd-131">Les informations de l’emplacement peuvent être incluses dans ce champ et peuvent être suffisantes à certains fins de gestion, ce qui évite de créer des instanciations d’objets connecteur/emplacement uniquement pour modéliser la relation entre les cartes et les tableaux d’hébergement ou d’autres adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="429dd-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="429dd-132">En revanche, si les informations relatives aux emplacements et aux connecteurs sont disponibles, ce champ peut être utilisé pour fournir des données de montage ou d’insertion de fente détaillées.</span><span class="sxs-lookup"><span data-stu-id="429dd-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="429dd-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="429dd-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="429dd-134">Type de données **: \_ carte CIM**</span><span class="sxs-lookup"><span data-stu-id="429dd-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="429dd-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="429dd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="429dd-136">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="429dd-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="429dd-137">Une [**\_ carte CIM**](cim-card.md) qui décrit la carte qui est connectée ou montée sur une autre carte.</span><span class="sxs-lookup"><span data-stu-id="429dd-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="429dd-138">Notes</span><span class="sxs-lookup"><span data-stu-id="429dd-138">Remarks</span></span>

<span data-ttu-id="429dd-139">La classe **CIM \_ CardOnCard** est dérivée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="429dd-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="429dd-140">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="429dd-140">WMI does not implement this class.</span></span>

<span data-ttu-id="429dd-141">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="429dd-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="429dd-142">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="429dd-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="429dd-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="429dd-143">Requirements</span></span>



| <span data-ttu-id="429dd-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="429dd-144">Requirement</span></span> | <span data-ttu-id="429dd-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="429dd-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="429dd-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="429dd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="429dd-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="429dd-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="429dd-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="429dd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="429dd-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="429dd-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="429dd-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="429dd-150">Namespace</span></span><br/>                | <span data-ttu-id="429dd-151">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="429dd-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="429dd-152">MOF</span><span class="sxs-lookup"><span data-stu-id="429dd-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="429dd-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="429dd-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="429dd-154">DLL</span><span class="sxs-lookup"><span data-stu-id="429dd-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="429dd-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="429dd-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="429dd-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="429dd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429dd-157">**\_Conteneur CIM**</span><span class="sxs-lookup"><span data-stu-id="429dd-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

