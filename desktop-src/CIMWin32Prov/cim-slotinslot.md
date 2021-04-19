---
description: La \_ relation SLOTINSLOT CIM représente la capacité d’un adaptateur spécial à étendre la structure d’emplacement existante afin d’activer les cartes non compatibles dans une trame ou un tableau d’hébergement.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Classe CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515345"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="456db-103">\_Classe CIM SlotInSlot</span><span class="sxs-lookup"><span data-stu-id="456db-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="456db-104">La **relation \_ SlotInSlot CIM** représente la capacité d’un adaptateur spécial à étendre la structure d’emplacement existante afin d’activer les cartes non compatibles dans une trame ou un tableau d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="456db-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="456db-105">Les emplacements sont des types spéciaux de connecteurs dans lesquels les cartes d’adaptateur sont généralement insérées.</span><span class="sxs-lookup"><span data-stu-id="456db-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="456db-106">L’adaptateur crée effectivement un nouvel emplacement et peut être considéré (conceptuellement) comme un emplacement dans un emplacement.</span><span class="sxs-lookup"><span data-stu-id="456db-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="456db-107">Les cartes qui, autrement, seraient physiquement ou électriquement incompatibles avec les emplacements existants sont prises en charge par l’interfaçage avec l’emplacement fourni par l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="456db-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="456db-108">Par exemple, les cartes réseau sont très coûteuses.</span><span class="sxs-lookup"><span data-stu-id="456db-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="456db-109">À mesure que le nouveau matériel devient disponible, les configurations des châssis et des cartes changent.</span><span class="sxs-lookup"><span data-stu-id="456db-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="456db-110">Pour protéger l’investissement de leurs clients, les fournisseurs de réseau fabriquent des adaptateurs spéciaux qui permettent aux anciennes cartes de s’intégrer dans de nouveaux châssis ou cartes d’hébergement ou de nouvelles cartes pour s’adapter aux anciennes cartes à l’aide d’un adaptateur spécial qui s’ajuste à un ou plusieurs emplacements existants et présente un nouvel emplacement dans lequel la carte peut s’adapter.</span><span class="sxs-lookup"><span data-stu-id="456db-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="456db-111">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="456db-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="456db-112">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="456db-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="456db-113">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="456db-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="456db-114">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="456db-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="456db-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="456db-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="456db-116">Membres</span><span class="sxs-lookup"><span data-stu-id="456db-116">Members</span></span>

<span data-ttu-id="456db-117">La classe **CIM \_ SlotInSlot** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="456db-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="456db-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="456db-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="456db-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="456db-119">Properties</span></span>

<span data-ttu-id="456db-120">La classe **CIM \_ SlotInSlot** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="456db-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="456db-121">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="456db-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456db-122">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="456db-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="456db-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="456db-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="456db-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="456db-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="456db-125">[**\_ Emplacement CIM**](cim-slot.md) qui décrit le ou les emplacements existants du tableau d’hébergement, ou cadre qui sont adaptés pour accueillir une carte qui, autrement, ne serait pas physiquement et/ou électriquement compatible avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="456db-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="456db-126">**Charge**</span><span class="sxs-lookup"><span data-stu-id="456db-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456db-127">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="456db-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="456db-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="456db-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="456db-129">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="456db-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="456db-130">[**\_ Emplacement CIM**](cim-slot.md) qui décrit le nouvel emplacement fourni par la carte de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="456db-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="456db-131">Notes</span><span class="sxs-lookup"><span data-stu-id="456db-131">Remarks</span></span>

<span data-ttu-id="456db-132">La classe **CIM \_ SlotInSlot** est dérivée de [**CIM \_ ConnectedTo**](cim-connectedto.md).</span><span class="sxs-lookup"><span data-stu-id="456db-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="456db-133">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="456db-133">WMI does not implement this class.</span></span>

<span data-ttu-id="456db-134">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="456db-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="456db-135">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="456db-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="456db-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="456db-136">Requirements</span></span>



| <span data-ttu-id="456db-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="456db-137">Requirement</span></span> | <span data-ttu-id="456db-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="456db-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="456db-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="456db-139">Minimum supported client</span></span><br/> | <span data-ttu-id="456db-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="456db-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="456db-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="456db-141">Minimum supported server</span></span><br/> | <span data-ttu-id="456db-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="456db-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="456db-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="456db-143">Namespace</span></span><br/>                | <span data-ttu-id="456db-144">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="456db-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="456db-145">MOF</span><span class="sxs-lookup"><span data-stu-id="456db-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="456db-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="456db-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="456db-147">DLL</span><span class="sxs-lookup"><span data-stu-id="456db-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="456db-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="456db-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456db-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="456db-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456db-150">**\_CONNECTEDTO CIM**</span><span class="sxs-lookup"><span data-stu-id="456db-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

