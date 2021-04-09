---
description: La \_ classe CIM RedundancyComponent associe un groupe de redondance composé d’éléments système gérés et indique que, ensemble, les éléments assurent la redondance.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: Classe CIM_RedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860646"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="cb1f2-103">\_Classe CIM RedundancyComponent</span><span class="sxs-lookup"><span data-stu-id="cb1f2-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="cb1f2-104">La classe **CIM \_ RedundancyComponent** associe un groupe de redondance composé d’éléments système gérés et indique que, ensemble, les éléments assurent la redondance.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="cb1f2-105">Tous les éléments agrégés dans un groupe de redondance doivent être des instanciations de la même classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb1f2-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb1f2-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cb1f2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cb1f2-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cb1f2-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1f2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb1f2-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="cb1f2-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cb1f2-111">Members</span></span>

<span data-ttu-id="cb1f2-112">La classe **CIM \_ RedundancyComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb1f2-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="cb1f2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb1f2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb1f2-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb1f2-114">Properties</span></span>

<span data-ttu-id="cb1f2-115">La classe **CIM \_ RedundancyComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb1f2-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cb1f2-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb1f2-117">Type de données : **CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="cb1f2-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="cb1f2-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb1f2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb1f2-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="cb1f2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cb1f2-120">L’Association **CIM \_ RedundancyComponent** indique que « cet ensemble de fans » ou « ces extensions physiques » participent à un seul groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="cb1f2-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cb1f2-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb1f2-122">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="cb1f2-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="cb1f2-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb1f2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb1f2-124">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) qui décrit l’élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="cb1f2-125">Cette propriété est héritée [**du \_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="cb1f2-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb1f2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="cb1f2-126">Remarks</span></span>

<span data-ttu-id="cb1f2-127">**CIM \_ RedundancyComponent** est dérivé du [**\_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="cb1f2-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="cb1f2-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-128">WMI does not implement this class.</span></span>

<span data-ttu-id="cb1f2-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb1f2-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cb1f2-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb1f2-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb1f2-131">Requirements</span></span>



| <span data-ttu-id="cb1f2-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb1f2-132">Requirement</span></span> | <span data-ttu-id="cb1f2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb1f2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1f2-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb1f2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cb1f2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb1f2-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb1f2-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb1f2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cb1f2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb1f2-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb1f2-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb1f2-138">Namespace</span></span><br/>                | <span data-ttu-id="cb1f2-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cb1f2-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb1f2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="cb1f2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb1f2-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb1f2-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb1f2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cb1f2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb1f2-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb1f2-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb1f2-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb1f2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb1f2-145">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="cb1f2-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

