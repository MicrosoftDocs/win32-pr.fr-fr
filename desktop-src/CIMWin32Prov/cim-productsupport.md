---
description: La \_ classe CIM ProductSupport représente une association entre le produit et l’accès au support qui indique comment le support est obtenu pour le produit.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Classe CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513920"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="433db-103">\_Classe CIM ProductSupport</span><span class="sxs-lookup"><span data-stu-id="433db-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="433db-104">La classe **CIM \_ ProductSupport** représente une association entre le produit et l’accès au support qui indique comment le support est obtenu pour le produit.</span><span class="sxs-lookup"><span data-stu-id="433db-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="433db-105">Différents types de support sont disponibles pour un produit. le même objet de support peut fournir une assistance pour plusieurs produits.</span><span class="sxs-lookup"><span data-stu-id="433db-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="433db-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="433db-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="433db-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="433db-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="433db-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="433db-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="433db-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="433db-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="433db-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="433db-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="433db-111">Membres</span><span class="sxs-lookup"><span data-stu-id="433db-111">Members</span></span>

<span data-ttu-id="433db-112">La classe **CIM \_ ProductSupport** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="433db-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="433db-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="433db-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="433db-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="433db-114">Properties</span></span>

<span data-ttu-id="433db-115">La classe **CIM \_ ProductSupport** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="433db-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="433db-116">**Produit**</span><span class="sxs-lookup"><span data-stu-id="433db-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433db-117">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="433db-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="433db-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="433db-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="433db-119">Référence au produit.</span><span class="sxs-lookup"><span data-stu-id="433db-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="433db-120">**Support**</span><span class="sxs-lookup"><span data-stu-id="433db-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="433db-121">Type de données : **CIM \_ SupportAccess**</span><span class="sxs-lookup"><span data-stu-id="433db-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="433db-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="433db-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="433db-123">Référence au support technique.</span><span class="sxs-lookup"><span data-stu-id="433db-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="433db-124">Notes</span><span class="sxs-lookup"><span data-stu-id="433db-124">Remarks</span></span>

<span data-ttu-id="433db-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="433db-125">WMI does not implement this class.</span></span>

<span data-ttu-id="433db-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="433db-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="433db-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="433db-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="433db-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="433db-128">Requirements</span></span>



| <span data-ttu-id="433db-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="433db-129">Requirement</span></span> | <span data-ttu-id="433db-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="433db-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="433db-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="433db-131">Minimum supported client</span></span><br/> | <span data-ttu-id="433db-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="433db-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="433db-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="433db-133">Minimum supported server</span></span><br/> | <span data-ttu-id="433db-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="433db-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="433db-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="433db-135">Namespace</span></span><br/>                | <span data-ttu-id="433db-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="433db-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="433db-137">MOF</span><span class="sxs-lookup"><span data-stu-id="433db-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="433db-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="433db-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="433db-139">DLL</span><span class="sxs-lookup"><span data-stu-id="433db-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="433db-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="433db-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




