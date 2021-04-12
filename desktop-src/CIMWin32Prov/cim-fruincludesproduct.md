---
description: La \_ classe CIM FRUIncludesProduct indique qu’une unité remplaçable sur site (FRU) peut être composée d’autres produits.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: Classe CIM_FRUIncludesProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211247"
---
# <a name="cim_fruincludesproduct-class"></a><span data-ttu-id="66416-103">\_Classe CIM FRUIncludesProduct</span><span class="sxs-lookup"><span data-stu-id="66416-103">CIM\_FRUIncludesProduct class</span></span>

<span data-ttu-id="66416-104">La classe **CIM \_ FRUIncludesProduct** indique qu’une unité remplaçable sur site (FRU) peut être composée d’autres produits.</span><span class="sxs-lookup"><span data-stu-id="66416-104">The **CIM\_FRUIncludesProduct** class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66416-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="66416-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="66416-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="66416-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="66416-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="66416-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="66416-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="66416-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66416-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66416-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="66416-110">Membres</span><span class="sxs-lookup"><span data-stu-id="66416-110">Members</span></span>

<span data-ttu-id="66416-111">La classe **CIM \_ FRUIncludesProduct** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="66416-111">The **CIM\_FRUIncludesProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="66416-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66416-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66416-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66416-113">Properties</span></span>

<span data-ttu-id="66416-114">La classe **CIM \_ FRUIncludesProduct** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="66416-114">The **CIM\_FRUIncludesProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66416-115">**Composant**</span><span class="sxs-lookup"><span data-stu-id="66416-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66416-116">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="66416-116">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="66416-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66416-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66416-118">Référence au produit qui fait partie de la FRU.</span><span class="sxs-lookup"><span data-stu-id="66416-118">Reference to the product that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="66416-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="66416-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66416-120">Type de données **: \_ FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="66416-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="66416-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66416-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66416-122">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="66416-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="66416-123">Référence à la FRU.</span><span class="sxs-lookup"><span data-stu-id="66416-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66416-124">Notes</span><span class="sxs-lookup"><span data-stu-id="66416-124">Remarks</span></span>

<span data-ttu-id="66416-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="66416-125">WMI does not implement this class.</span></span>

<span data-ttu-id="66416-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="66416-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="66416-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="66416-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="66416-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66416-128">Requirements</span></span>



| <span data-ttu-id="66416-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66416-129">Requirement</span></span> | <span data-ttu-id="66416-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="66416-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66416-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66416-131">Minimum supported client</span></span><br/> | <span data-ttu-id="66416-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66416-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66416-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66416-133">Minimum supported server</span></span><br/> | <span data-ttu-id="66416-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66416-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66416-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66416-135">Namespace</span></span><br/>                | <span data-ttu-id="66416-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="66416-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66416-137">MOF</span><span class="sxs-lookup"><span data-stu-id="66416-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66416-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66416-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66416-139">DLL</span><span class="sxs-lookup"><span data-stu-id="66416-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66416-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66416-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

