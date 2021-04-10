---
description: La \_ classe CIM CardInSlot associe une carte d’adaptateur au conteneur dans lequel elle est insérée.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: Classe CIM_CardInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861358"
---
# <a name="cim_cardinslot-class"></a><span data-ttu-id="dc91e-103">\_Classe CIM CardInSlot</span><span class="sxs-lookup"><span data-stu-id="dc91e-103">CIM\_CardInSlot class</span></span>

<span data-ttu-id="dc91e-104">La classe **CIM \_ CardInSlot** associe une carte d’adaptateur au conteneur dans lequel elle est insérée.</span><span class="sxs-lookup"><span data-stu-id="dc91e-104">The **CIM\_CardInSlot** class associates an adapter card with the container into which it is inserted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc91e-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="dc91e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dc91e-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dc91e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dc91e-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dc91e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dc91e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="dc91e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc91e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc91e-109">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="dc91e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="dc91e-110">Members</span></span>

<span data-ttu-id="dc91e-111">La classe **CIM \_ CardInSlot** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dc91e-111">The **CIM\_CardInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="dc91e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dc91e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc91e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dc91e-113">Properties</span></span>

<span data-ttu-id="dc91e-114">La classe **CIM \_ CardInSlot** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="dc91e-114">The **CIM\_CardInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc91e-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="dc91e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc91e-116">Type de données **: \_ emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="dc91e-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="dc91e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc91e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc91e-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="dc91e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dc91e-119">[**\_ Emplacement CIM**](cim-slot.md) qui décrit l’emplacement dans lequel la carte est insérée.</span><span class="sxs-lookup"><span data-stu-id="dc91e-119">A [**CIM\_Slot**](cim-slot.md) that describes the slot into which the card is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="dc91e-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="dc91e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc91e-121">Type de données **: \_ carte CIM**</span><span class="sxs-lookup"><span data-stu-id="dc91e-121">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="dc91e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dc91e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc91e-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dc91e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dc91e-124">Une [**\_ carte CIM**](cim-card.md) qui décrit la carte dans l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="dc91e-124">A [**CIM\_Card**](cim-card.md) that describes the card in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc91e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="dc91e-125">Remarks</span></span>

<span data-ttu-id="dc91e-126">La classe **CIM \_ CardInSlot** est dérivée de [**CIM \_ PackageInSlot**](cim-packageinslot.md).</span><span class="sxs-lookup"><span data-stu-id="dc91e-126">The **CIM\_CardInSlot** class is derived from [**CIM\_PackageInSlot**](cim-packageinslot.md).</span></span>

<span data-ttu-id="dc91e-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="dc91e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="dc91e-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="dc91e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dc91e-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="dc91e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc91e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc91e-130">Requirements</span></span>



| <span data-ttu-id="dc91e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc91e-131">Requirement</span></span> | <span data-ttu-id="dc91e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc91e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc91e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc91e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dc91e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc91e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc91e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc91e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dc91e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc91e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc91e-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dc91e-137">Namespace</span></span><br/>                | <span data-ttu-id="dc91e-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dc91e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc91e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="dc91e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc91e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc91e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc91e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dc91e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc91e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc91e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc91e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc91e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc91e-144">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="dc91e-144">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> </dl>

 

