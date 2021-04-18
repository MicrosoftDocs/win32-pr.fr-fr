---
description: La \_ classe CIM ComputerSystemIRQ représente une association entre un système informatique et ses lignes de requête d’interruption (IRQ) disponibles.
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemIRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516181"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="146ff-103">\_Classe CIM ComputerSystemIRQ</span><span class="sxs-lookup"><span data-stu-id="146ff-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="146ff-104">La classe **CIM \_ ComputerSystemIRQ** représente une association entre un système informatique et ses lignes de requête d’interruption (IRQ) disponibles.</span><span class="sxs-lookup"><span data-stu-id="146ff-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="146ff-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="146ff-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="146ff-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="146ff-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="146ff-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="146ff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="146ff-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="146ff-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="146ff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="146ff-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="146ff-110">Membres</span><span class="sxs-lookup"><span data-stu-id="146ff-110">Members</span></span>

<span data-ttu-id="146ff-111">La classe **CIM \_ ComputerSystemIRQ** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="146ff-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="146ff-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="146ff-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="146ff-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="146ff-113">Properties</span></span>

<span data-ttu-id="146ff-114">La classe **CIM \_ ComputerSystemIRQ** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="146ff-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="146ff-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="146ff-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="146ff-116">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="146ff-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="146ff-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="146ff-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="146ff-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="146ff-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="146ff-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) décrivant l’ordinateur associé à l’IRQ.</span><span class="sxs-lookup"><span data-stu-id="146ff-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="146ff-120">Cette propriété est héritée de [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="146ff-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="146ff-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="146ff-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="146ff-122">Type de données : l' **\_ IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="146ff-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="146ff-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="146ff-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="146ff-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="146ff-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="146ff-125">Une [**\_ IRQ CIM**](cim-irq.md) décrivant une IRQ du système informatique.</span><span class="sxs-lookup"><span data-stu-id="146ff-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="146ff-126">Notes</span><span class="sxs-lookup"><span data-stu-id="146ff-126">Remarks</span></span>

<span data-ttu-id="146ff-127">La classe **CIM \_ ComputerSystemIRQ** est dérivée de [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="146ff-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="146ff-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="146ff-128">WMI does not implement this class.</span></span>

<span data-ttu-id="146ff-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="146ff-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="146ff-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="146ff-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="146ff-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="146ff-131">Requirements</span></span>



| <span data-ttu-id="146ff-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="146ff-132">Requirement</span></span> | <span data-ttu-id="146ff-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="146ff-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="146ff-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="146ff-134">Minimum supported client</span></span><br/> | <span data-ttu-id="146ff-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="146ff-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="146ff-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="146ff-136">Minimum supported server</span></span><br/> | <span data-ttu-id="146ff-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="146ff-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="146ff-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="146ff-138">Namespace</span></span><br/>                | <span data-ttu-id="146ff-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="146ff-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="146ff-140">MOF</span><span class="sxs-lookup"><span data-stu-id="146ff-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="146ff-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="146ff-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="146ff-142">DLL</span><span class="sxs-lookup"><span data-stu-id="146ff-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="146ff-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="146ff-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="146ff-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="146ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="146ff-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="146ff-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

