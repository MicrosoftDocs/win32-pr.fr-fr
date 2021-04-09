---
description: La \_ classe CIM BIOSFeatureBIOSElements associe une fonctionnalité BIOS et ses éléments BIOS agrégés.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeatureBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111082"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="eebf0-103">\_Classe CIM BIOSFeatureBIOSElements</span><span class="sxs-lookup"><span data-stu-id="eebf0-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="eebf0-104">La classe **CIM \_ BIOSFeatureBIOSElements** associe une fonctionnalité BIOS et ses éléments BIOS agrégés.</span><span class="sxs-lookup"><span data-stu-id="eebf0-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eebf0-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="eebf0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eebf0-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eebf0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eebf0-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eebf0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eebf0-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="eebf0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebf0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eebf0-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="eebf0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="eebf0-110">Members</span></span>

<span data-ttu-id="eebf0-111">La classe **CIM \_ BIOSFeatureBIOSElements** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eebf0-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="eebf0-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eebf0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eebf0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eebf0-113">Properties</span></span>

<span data-ttu-id="eebf0-114">La classe **CIM \_ BIOSFeatureBIOSElements** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eebf0-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eebf0-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="eebf0-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eebf0-116">Type de données : **CIM \_ BIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="eebf0-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="eebf0-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eebf0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eebf0-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="eebf0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="eebf0-119">[**\_ BIOSFeature CIM**](cim-biosfeature.md) qui décrit la fonctionnalité BIOS.</span><span class="sxs-lookup"><span data-stu-id="eebf0-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="eebf0-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eebf0-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eebf0-121">Type de données : **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="eebf0-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="eebf0-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eebf0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eebf0-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="eebf0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="eebf0-124">[**\_ BIOSElement CIM**](cim-bioselement.md) qui décrit l’élément BIOS qui implémente les fonctionnalités décrites par la fonctionnalité BIOS.</span><span class="sxs-lookup"><span data-stu-id="eebf0-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eebf0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="eebf0-125">Remarks</span></span>

<span data-ttu-id="eebf0-126">La classe **CIM \_ BIOSFeatureBIOSElements** est dérivée de [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="eebf0-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="eebf0-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="eebf0-127">WMI does not implement this class.</span></span>

<span data-ttu-id="eebf0-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="eebf0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eebf0-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="eebf0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eebf0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eebf0-130">Requirements</span></span>



| <span data-ttu-id="eebf0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eebf0-131">Requirement</span></span> | <span data-ttu-id="eebf0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="eebf0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eebf0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eebf0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eebf0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eebf0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eebf0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eebf0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eebf0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eebf0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eebf0-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eebf0-137">Namespace</span></span><br/>                | <span data-ttu-id="eebf0-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="eebf0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eebf0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="eebf0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eebf0-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eebf0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eebf0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="eebf0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eebf0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eebf0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eebf0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eebf0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebf0-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="eebf0-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

