---
description: La \_ classe CIM VideoBIOSFeatureVideoBIOSElements associe une fonctionnalité BIOS vidéo et ses éléments BIOS vidéo agrégés.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSFeatureVideoBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110603"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="6ad34-103">\_Classe CIM VideoBIOSFeatureVideoBIOSElements</span><span class="sxs-lookup"><span data-stu-id="6ad34-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="6ad34-104">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** associe une fonctionnalité BIOS vidéo et ses éléments BIOS vidéo agrégés.</span><span class="sxs-lookup"><span data-stu-id="6ad34-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ad34-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6ad34-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6ad34-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6ad34-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6ad34-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6ad34-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6ad34-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6ad34-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad34-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ad34-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="6ad34-110">Membres</span><span class="sxs-lookup"><span data-stu-id="6ad34-110">Members</span></span>

<span data-ttu-id="6ad34-111">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6ad34-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="6ad34-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ad34-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ad34-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ad34-113">Properties</span></span>

<span data-ttu-id="6ad34-114">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ad34-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ad34-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6ad34-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad34-116">Type de données : **CIM \_ VideoBIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="6ad34-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="6ad34-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad34-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ad34-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="6ad34-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6ad34-119">[**\_ VideoBIOSFeature CIM**](cim-videobiosfeature.md) qui décrit la fonctionnalité vidéo du BIOS.</span><span class="sxs-lookup"><span data-stu-id="6ad34-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="6ad34-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6ad34-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ad34-121">Type de données : **CIM \_ VideoBIOSElement**</span><span class="sxs-lookup"><span data-stu-id="6ad34-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="6ad34-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ad34-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ad34-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="6ad34-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6ad34-124">[**\_ VideoBIOSElement CIM**](cim-videobioselement.md) qui décrit l’élément Video BIOS qui implémente les fonctionnalités décrites par la fonctionnalité Video BIOS.</span><span class="sxs-lookup"><span data-stu-id="6ad34-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ad34-125">Notes</span><span class="sxs-lookup"><span data-stu-id="6ad34-125">Remarks</span></span>

<span data-ttu-id="6ad34-126">La classe **CIM \_ VideoBIOSFeatureVideoBIOSElements** est dérivée de [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="6ad34-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="6ad34-127">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6ad34-127">WMI does not implement this class.</span></span>

<span data-ttu-id="6ad34-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6ad34-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6ad34-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6ad34-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad34-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ad34-130">Requirements</span></span>



| <span data-ttu-id="6ad34-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ad34-131">Requirement</span></span> | <span data-ttu-id="6ad34-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ad34-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad34-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad34-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad34-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ad34-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ad34-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad34-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad34-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ad34-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ad34-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6ad34-137">Namespace</span></span><br/>                | <span data-ttu-id="6ad34-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6ad34-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ad34-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6ad34-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ad34-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ad34-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad34-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ad34-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad34-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad34-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad34-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad34-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="6ad34-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

