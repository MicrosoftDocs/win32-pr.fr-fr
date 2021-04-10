---
description: L' \_ Association CIM CollectionOfSensors représente les capteurs binaires qui composent le capteur à États multistates.
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfSensors
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950700"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="e41d6-103">\_Classe CIM CollectionOfSensors</span><span class="sxs-lookup"><span data-stu-id="e41d6-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="e41d6-104">L’Association **CIM \_ CollectionOfSensors** représente les capteurs binaires qui composent le capteur à États multistates.</span><span class="sxs-lookup"><span data-stu-id="e41d6-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e41d6-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e41d6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e41d6-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e41d6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e41d6-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e41d6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e41d6-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e41d6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e41d6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e41d6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e41d6-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e41d6-110">Members</span></span>

<span data-ttu-id="e41d6-111">La classe **CIM \_ CollectionOfSensors** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e41d6-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="e41d6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e41d6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e41d6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e41d6-113">Properties</span></span>

<span data-ttu-id="e41d6-114">La classe **CIM \_ CollectionOfSensors** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e41d6-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e41d6-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e41d6-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e41d6-116">Type de données : **CIM \_ MultiStateSensor**</span><span class="sxs-lookup"><span data-stu-id="e41d6-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="e41d6-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e41d6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e41d6-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e41d6-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e41d6-119">[**\_ MultiStateSensor CIM**](cim-multistatesensor.md) qui décrit le capteur à États multiples.</span><span class="sxs-lookup"><span data-stu-id="e41d6-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e41d6-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e41d6-121">Type de données : **CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="e41d6-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="e41d6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e41d6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e41d6-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e41d6-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e41d6-124">[**\_ BinarySensor CIM**](cim-binarysensor.md) qui décrit un capteur binaire qui fait partie du capteur à États multiples.</span><span class="sxs-lookup"><span data-stu-id="e41d6-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e41d6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e41d6-125">Remarks</span></span>

<span data-ttu-id="e41d6-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e41d6-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e41d6-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e41d6-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e41d6-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e41d6-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41d6-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e41d6-129">Requirements</span></span>



| <span data-ttu-id="e41d6-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e41d6-130">Requirement</span></span> | <span data-ttu-id="e41d6-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e41d6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41d6-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e41d6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e41d6-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e41d6-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e41d6-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e41d6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e41d6-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e41d6-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e41d6-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e41d6-136">Namespace</span></span><br/>                | <span data-ttu-id="e41d6-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e41d6-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e41d6-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e41d6-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e41d6-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e41d6-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e41d6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e41d6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e41d6-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e41d6-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41d6-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e41d6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41d6-143">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="e41d6-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

