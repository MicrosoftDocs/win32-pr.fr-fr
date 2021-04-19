---
description: La \_ classe CIM MemoryOnCard associe la mémoire physique située sur les cartes d’hébergement, les cartes d’adaptateur, etc. Cette association définit explicitement la relation entre la mémoire et les cartes.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: Classe CIM_MemoryOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516382"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="329dc-104">\_Classe CIM MemoryOnCard</span><span class="sxs-lookup"><span data-stu-id="329dc-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="329dc-105">La classe **CIM \_ MemoryOnCard** associe la mémoire physique située sur les cartes d’hébergement, les cartes d’adaptateur, etc.</span><span class="sxs-lookup"><span data-stu-id="329dc-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="329dc-106">Cette association définit explicitement la relation entre la mémoire et les cartes.</span><span class="sxs-lookup"><span data-stu-id="329dc-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="329dc-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="329dc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="329dc-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="329dc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="329dc-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="329dc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="329dc-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="329dc-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="329dc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="329dc-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="329dc-112">Membres</span><span class="sxs-lookup"><span data-stu-id="329dc-112">Members</span></span>

<span data-ttu-id="329dc-113">La classe **CIM \_ MemoryOnCard** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="329dc-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="329dc-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="329dc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="329dc-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="329dc-115">Properties</span></span>

<span data-ttu-id="329dc-116">La classe **CIM \_ MemoryOnCard** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="329dc-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="329dc-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="329dc-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329dc-118">Type de données **: \_ carte CIM**</span><span class="sxs-lookup"><span data-stu-id="329dc-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="329dc-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="329dc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329dc-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="329dc-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="329dc-121">Une [**\_ carte CIM**](cim-card.md) décrivant la carte qui inclut ou « contient » de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="329dc-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="329dc-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="329dc-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329dc-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="329dc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329dc-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="329dc-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="329dc-125">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="329dc-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="329dc-126">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="329dc-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="329dc-127">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="329dc-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="329dc-128">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="329dc-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="329dc-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="329dc-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329dc-130">Type de données : **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="329dc-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="329dc-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="329dc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329dc-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="329dc-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="329dc-133">[**\_ PhysicalMemory CIM**](cim-physicalmemory.md) décrivant la mémoire physique qui se trouve sur la carte.</span><span class="sxs-lookup"><span data-stu-id="329dc-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="329dc-134">Notes</span><span class="sxs-lookup"><span data-stu-id="329dc-134">Remarks</span></span>

<span data-ttu-id="329dc-135">La classe **CIM \_ MemoryOnCard** est dérivée de [**CIM \_ PackagedComponent**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="329dc-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="329dc-136">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="329dc-136">WMI does not implement this class.</span></span>

<span data-ttu-id="329dc-137">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="329dc-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="329dc-138">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="329dc-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="329dc-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="329dc-139">Requirements</span></span>



| <span data-ttu-id="329dc-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="329dc-140">Requirement</span></span> | <span data-ttu-id="329dc-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="329dc-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="329dc-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="329dc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="329dc-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="329dc-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="329dc-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="329dc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="329dc-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="329dc-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="329dc-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="329dc-146">Namespace</span></span><br/>                | <span data-ttu-id="329dc-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="329dc-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="329dc-148">MOF</span><span class="sxs-lookup"><span data-stu-id="329dc-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="329dc-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="329dc-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="329dc-150">DLL</span><span class="sxs-lookup"><span data-stu-id="329dc-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="329dc-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="329dc-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="329dc-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="329dc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="329dc-153">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="329dc-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

