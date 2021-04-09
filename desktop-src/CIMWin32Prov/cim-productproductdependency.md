---
description: La \_ classe PRODUCTPRODUCTDEPENDENCY CIM représente une association entre deux produits, ce qui indique qu’un doit être installé ou absent pour que l’autre fonctionne. Il s’agit d’un concept équivalent à l' \_ Association CIM ServiceServiceDependency.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: Classe CIM_ProductProductDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033629"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="2e391-104">\_Classe CIM ProductProductDependency</span><span class="sxs-lookup"><span data-stu-id="2e391-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="2e391-105">La **classe \_ ProductProductDependency CIM** représente une association entre deux produits, ce qui indique qu’un doit être installé ou absent pour que l’autre fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2e391-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="2e391-106">Il s’agit d’un concept équivalent à l’Association [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="2e391-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e391-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2e391-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e391-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e391-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e391-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2e391-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2e391-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2e391-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e391-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e391-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="2e391-112">Membres</span><span class="sxs-lookup"><span data-stu-id="2e391-112">Members</span></span>

<span data-ttu-id="2e391-113">La classe **CIM \_ ProductProductDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e391-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="2e391-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e391-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e391-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e391-115">Properties</span></span>

<span data-ttu-id="2e391-116">La classe **CIM \_ ProductProductDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e391-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e391-117">**DependentProduct**</span><span class="sxs-lookup"><span data-stu-id="2e391-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e391-118">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="2e391-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="2e391-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e391-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e391-120">Référence au produit qui est dépendant d’un autre produit.</span><span class="sxs-lookup"><span data-stu-id="2e391-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-121">**RequiredProduct**</span><span class="sxs-lookup"><span data-stu-id="2e391-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e391-122">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="2e391-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="2e391-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e391-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e391-124">Référence au produit requis.</span><span class="sxs-lookup"><span data-stu-id="2e391-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="2e391-125">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="2e391-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e391-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e391-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e391-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e391-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e391-128">Nature de la dépendance du produit.</span><span class="sxs-lookup"><span data-stu-id="2e391-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e391-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2e391-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2e391-130">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="2e391-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e391-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2e391-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e391-132">Autre.</span><span class="sxs-lookup"><span data-stu-id="2e391-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="2e391-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>Le **produit doit être installé** (2)</span><span class="sxs-lookup"><span data-stu-id="2e391-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e391-134">Le produit doit être installé.</span><span class="sxs-lookup"><span data-stu-id="2e391-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="2e391-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>Le **produit ne doit pas être installé** (3)</span><span class="sxs-lookup"><span data-stu-id="2e391-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e391-136">Le produit ne doit pas être installé.</span><span class="sxs-lookup"><span data-stu-id="2e391-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e391-137">Notes</span><span class="sxs-lookup"><span data-stu-id="2e391-137">Remarks</span></span>

<span data-ttu-id="2e391-138">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2e391-138">WMI does not implement this class.</span></span>

<span data-ttu-id="2e391-139">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e391-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e391-140">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2e391-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e391-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e391-141">Requirements</span></span>



| <span data-ttu-id="2e391-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e391-142">Requirement</span></span> | <span data-ttu-id="2e391-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e391-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e391-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e391-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2e391-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e391-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e391-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e391-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2e391-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e391-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e391-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e391-148">Namespace</span></span><br/>                | <span data-ttu-id="2e391-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2e391-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e391-150">MOF</span><span class="sxs-lookup"><span data-stu-id="2e391-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e391-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e391-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e391-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2e391-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e391-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e391-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




