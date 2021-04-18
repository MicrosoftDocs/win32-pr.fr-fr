---
description: L' \_ Association CIM ProductSoftwareFeatures identifie les fonctionnalités logicielles pour un produit particulier.
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: Classe CIM_ProductSoftwareFeatures
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513307"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="48568-103">\_Classe CIM ProductSoftwareFeatures</span><span class="sxs-lookup"><span data-stu-id="48568-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="48568-104">L’Association **CIM \_ ProductSoftwareFeatures** identifie les fonctionnalités logicielles pour un produit particulier.</span><span class="sxs-lookup"><span data-stu-id="48568-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48568-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="48568-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48568-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="48568-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48568-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="48568-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="48568-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="48568-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48568-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48568-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="48568-110">Membres</span><span class="sxs-lookup"><span data-stu-id="48568-110">Members</span></span>

<span data-ttu-id="48568-111">La classe **CIM \_ ProductSoftwareFeatures** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="48568-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="48568-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="48568-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48568-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="48568-113">Properties</span></span>

<span data-ttu-id="48568-114">La classe **CIM \_ ProductSoftwareFeatures** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="48568-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48568-115">**Composant**</span><span class="sxs-lookup"><span data-stu-id="48568-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48568-116">Type de données : **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="48568-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="48568-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="48568-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48568-118">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48568-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48568-119">Référence au composant.</span><span class="sxs-lookup"><span data-stu-id="48568-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="48568-120">**Produit**</span><span class="sxs-lookup"><span data-stu-id="48568-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48568-121">Type de données **: \_ produit CIM**</span><span class="sxs-lookup"><span data-stu-id="48568-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="48568-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="48568-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48568-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48568-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48568-124">Référence au produit.</span><span class="sxs-lookup"><span data-stu-id="48568-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48568-125">Notes</span><span class="sxs-lookup"><span data-stu-id="48568-125">Remarks</span></span>

<span data-ttu-id="48568-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="48568-126">WMI does not implement this class.</span></span> <span data-ttu-id="48568-127">Pour les classes WMI dérivées de **CIM \_ ProductSoftwareFeatures**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="48568-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="48568-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="48568-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48568-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="48568-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48568-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48568-130">Requirements</span></span>



| <span data-ttu-id="48568-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48568-131">Requirement</span></span> | <span data-ttu-id="48568-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="48568-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48568-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48568-133">Minimum supported client</span></span><br/> | <span data-ttu-id="48568-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48568-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48568-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48568-135">Minimum supported server</span></span><br/> | <span data-ttu-id="48568-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48568-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48568-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="48568-137">Namespace</span></span><br/>                | <span data-ttu-id="48568-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="48568-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48568-139">MOF</span><span class="sxs-lookup"><span data-stu-id="48568-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48568-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48568-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48568-141">DLL</span><span class="sxs-lookup"><span data-stu-id="48568-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48568-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48568-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

