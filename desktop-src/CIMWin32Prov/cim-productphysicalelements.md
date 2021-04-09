---
description: La \_ classe CIM ProductPhysicalElements représente les éléments physiques qui composent un produit.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: Classe CIM_ProductPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110370"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="9b481-103">\_Classe CIM ProductPhysicalElements</span><span class="sxs-lookup"><span data-stu-id="9b481-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="9b481-104">La classe **CIM \_ ProductPhysicalElements** représente les éléments physiques qui composent un produit.</span><span class="sxs-lookup"><span data-stu-id="9b481-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b481-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9b481-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b481-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b481-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b481-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9b481-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9b481-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9b481-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b481-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b481-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="9b481-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9b481-110">Members</span></span>

<span data-ttu-id="9b481-111">La classe **CIM \_ ProductPhysicalElements** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9b481-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="9b481-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b481-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b481-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b481-113">Properties</span></span>

<span data-ttu-id="9b481-114">La classe **CIM \_ ProductPhysicalElements** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b481-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b481-115">**Composant**</span><span class="sxs-lookup"><span data-stu-id="9b481-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b481-116">Type de données : **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="9b481-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="9b481-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b481-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b481-118">Référence à l’élément physique qui fait partie du produit.</span><span class="sxs-lookup"><span data-stu-id="9b481-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="9b481-119">**Produit**</span><span class="sxs-lookup"><span data-stu-id="9b481-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b481-120">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="9b481-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="9b481-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9b481-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b481-122">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9b481-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9b481-123">Référence au produit.</span><span class="sxs-lookup"><span data-stu-id="9b481-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b481-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9b481-124">Remarks</span></span>

<span data-ttu-id="9b481-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="9b481-125">WMI does not implement this class.</span></span>

<span data-ttu-id="9b481-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b481-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b481-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9b481-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b481-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b481-128">Requirements</span></span>



| <span data-ttu-id="9b481-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b481-129">Requirement</span></span> | <span data-ttu-id="9b481-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b481-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b481-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b481-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9b481-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b481-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b481-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b481-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9b481-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b481-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b481-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b481-135">Namespace</span></span><br/>                | <span data-ttu-id="9b481-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9b481-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b481-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9b481-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b481-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b481-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b481-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9b481-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b481-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b481-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

