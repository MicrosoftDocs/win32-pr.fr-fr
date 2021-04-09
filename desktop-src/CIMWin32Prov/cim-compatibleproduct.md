---
description: La \_ classe COMPATIBLEPRODUCT CIM représente une association entre des produits qui indique si deux produits référencés sont interopérables, par exemple s’ils peuvent être installés ensemble ou si l’un peut être le conteneur physique de l’autre, et ainsi de suite.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: Classe CIM_CompatibleProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861338"
---
# <a name="cim_compatibleproduct-class"></a><span data-ttu-id="363a9-103">\_Classe CIM CompatibleProduct</span><span class="sxs-lookup"><span data-stu-id="363a9-103">CIM\_CompatibleProduct class</span></span>

<span data-ttu-id="363a9-104">La **classe \_ CompatibleProduct CIM** représente une association entre des produits qui indique si deux produits référencés sont interopérables, par exemple s’ils peuvent être installés ensemble ou si l’un peut être le conteneur physique de l’autre, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="363a9-104">The **CIM\_CompatibleProduct** class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="363a9-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="363a9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="363a9-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="363a9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="363a9-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="363a9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="363a9-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="363a9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="363a9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="363a9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="363a9-110">Membres</span><span class="sxs-lookup"><span data-stu-id="363a9-110">Members</span></span>

<span data-ttu-id="363a9-111">La classe **CIM \_ CompatibleProduct** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="363a9-111">The **CIM\_CompatibleProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="363a9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="363a9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="363a9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="363a9-113">Properties</span></span>

<span data-ttu-id="363a9-114">La classe **CIM \_ CompatibleProduct** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="363a9-114">The **CIM\_CompatibleProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="363a9-115">**CompatibilityDescription**</span><span class="sxs-lookup"><span data-stu-id="363a9-115">**CompatibilityDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="363a9-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="363a9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="363a9-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="363a9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="363a9-118">Chaîne de forme libre qui définit la façon dont les deux produits référencés sont interopérables, compatibles et indique s’il existe des limitations de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="363a9-118">Free-form string that defines how the two referenced products are interoperable, compatible, and whether there are compatibility limitations.</span></span>

</dd> <dt>

<span data-ttu-id="363a9-119">**CompatibleProduct**</span><span class="sxs-lookup"><span data-stu-id="363a9-119">**CompatibleProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="363a9-120">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="363a9-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="363a9-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="363a9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="363a9-122">Référence au produit compatible.</span><span class="sxs-lookup"><span data-stu-id="363a9-122">Reference to the compatible product.</span></span>

</dd> <dt>

<span data-ttu-id="363a9-123">**Produit**</span><span class="sxs-lookup"><span data-stu-id="363a9-123">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="363a9-124">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="363a9-124">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="363a9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="363a9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="363a9-126">Référence au produit pour lequel des offres compatibles sont définies.</span><span class="sxs-lookup"><span data-stu-id="363a9-126">Reference to the product for which compatible offerings are defined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="363a9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="363a9-127">Remarks</span></span>

<span data-ttu-id="363a9-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="363a9-128">WMI does not implement this class.</span></span>

<span data-ttu-id="363a9-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="363a9-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="363a9-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="363a9-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="363a9-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="363a9-131">Requirements</span></span>



| <span data-ttu-id="363a9-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="363a9-132">Requirement</span></span> | <span data-ttu-id="363a9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="363a9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="363a9-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="363a9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="363a9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="363a9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="363a9-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="363a9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="363a9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="363a9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="363a9-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="363a9-138">Namespace</span></span><br/>                | <span data-ttu-id="363a9-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="363a9-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="363a9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="363a9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="363a9-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="363a9-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="363a9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="363a9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="363a9-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="363a9-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




