---
description: La \_ classe CIM ProductFRU représente une association entre le produit et une unité remplaçable sur site (FRU), qui fournit des informations sur les composants du produit qui ont été ou sont remplacés.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: Classe CIM_ProductFRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110371"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="be712-103">\_Classe CIM ProductFRU</span><span class="sxs-lookup"><span data-stu-id="be712-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="be712-104">La classe **CIM \_ ProductFRU** représente une association entre le produit et une unité remplaçable sur site (FRU), qui fournit des informations sur les composants du produit qui ont été ou sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="be712-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be712-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="be712-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be712-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be712-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be712-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be712-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="be712-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="be712-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be712-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be712-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="be712-110">Membres</span><span class="sxs-lookup"><span data-stu-id="be712-110">Members</span></span>

<span data-ttu-id="be712-111">La classe **CIM \_ ProductFRU** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be712-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="be712-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be712-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be712-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be712-113">Properties</span></span>

<span data-ttu-id="be712-114">La classe **CIM \_ ProductFRU** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="be712-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be712-115">**FRU**</span><span class="sxs-lookup"><span data-stu-id="be712-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be712-116">Type de données **: \_ FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="be712-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="be712-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be712-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be712-118">Référence à la FRU.</span><span class="sxs-lookup"><span data-stu-id="be712-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="be712-119">**Produit**</span><span class="sxs-lookup"><span data-stu-id="be712-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be712-120">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="be712-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="be712-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be712-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be712-122">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="be712-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="be712-123">Référence au produit auquel la FRU est appliquée.</span><span class="sxs-lookup"><span data-stu-id="be712-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be712-124">Notes</span><span class="sxs-lookup"><span data-stu-id="be712-124">Remarks</span></span>

<span data-ttu-id="be712-125">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="be712-125">WMI does not implement this class.</span></span>

<span data-ttu-id="be712-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="be712-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be712-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="be712-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be712-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be712-128">Requirements</span></span>



| <span data-ttu-id="be712-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be712-129">Requirement</span></span> | <span data-ttu-id="be712-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="be712-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be712-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be712-131">Minimum supported client</span></span><br/> | <span data-ttu-id="be712-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be712-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be712-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be712-133">Minimum supported server</span></span><br/> | <span data-ttu-id="be712-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be712-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be712-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be712-135">Namespace</span></span><br/>                | <span data-ttu-id="be712-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="be712-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be712-137">MOF</span><span class="sxs-lookup"><span data-stu-id="be712-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be712-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be712-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be712-139">DLL</span><span class="sxs-lookup"><span data-stu-id="be712-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be712-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be712-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

