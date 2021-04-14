---
description: L' \_ Association CIM ProductParentChild définit une hiérarchie parent-enfant parmi les produits. Par exemple, un produit peut être fourni avec d’autres produits.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: Classe CIM_ProductParentChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523212"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="3b91e-104">\_Classe CIM ProductParentChild</span><span class="sxs-lookup"><span data-stu-id="3b91e-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="3b91e-105">L’Association **CIM \_ ProductParentChild** définit une hiérarchie parent-enfant parmi les produits.</span><span class="sxs-lookup"><span data-stu-id="3b91e-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="3b91e-106">Par exemple, un produit peut être fourni avec d’autres produits.</span><span class="sxs-lookup"><span data-stu-id="3b91e-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b91e-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3b91e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b91e-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3b91e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b91e-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3b91e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3b91e-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3b91e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b91e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b91e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="3b91e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3b91e-112">Members</span></span>

<span data-ttu-id="3b91e-113">La classe **CIM \_ ProductParentChild** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b91e-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="3b91e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b91e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b91e-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b91e-115">Properties</span></span>

<span data-ttu-id="3b91e-116">La classe **CIM \_ ProductParentChild** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b91e-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b91e-117">**Enfant**</span><span class="sxs-lookup"><span data-stu-id="3b91e-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b91e-118">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="3b91e-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="3b91e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b91e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b91e-120">Référence au produit enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="3b91e-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="3b91e-121">**Parent**</span><span class="sxs-lookup"><span data-stu-id="3b91e-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b91e-122">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="3b91e-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="3b91e-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b91e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b91e-124">Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b91e-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b91e-125">Référence au produit parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="3b91e-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b91e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="3b91e-126">Remarks</span></span>

<span data-ttu-id="3b91e-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="3b91e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3b91e-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3b91e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b91e-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3b91e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b91e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b91e-130">Requirements</span></span>



| <span data-ttu-id="3b91e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b91e-131">Requirement</span></span> | <span data-ttu-id="3b91e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b91e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b91e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b91e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3b91e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b91e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b91e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b91e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3b91e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b91e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b91e-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b91e-137">Namespace</span></span><br/>                | <span data-ttu-id="3b91e-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3b91e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b91e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3b91e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b91e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b91e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b91e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3b91e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b91e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b91e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

