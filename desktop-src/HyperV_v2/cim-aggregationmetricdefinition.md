---
description: Représente la définition d’une mesure dérivée d’une autre valeur de mesure. Un \_ objet CIM AggregationMetricDefinition doit être associé aux \_ objets propriété ManagedElement CIM auxquels il s’applique.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: Classe CIM_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755445"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="0ff61-104">\_Classe CIM AggregationMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="0ff61-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="0ff61-105">Représente la définition d’une mesure dérivée d’une autre valeur de mesure.</span><span class="sxs-lookup"><span data-stu-id="0ff61-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="0ff61-106">Un objet **CIM \_ AggregationMetricDefinition** doit être associé aux objets **\_ propriété ManagedElement CIM** auxquels il s’applique.</span><span class="sxs-lookup"><span data-stu-id="0ff61-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff61-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ff61-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="0ff61-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0ff61-108">Members</span></span>

<span data-ttu-id="0ff61-109">La classe **CIM \_ AggregationMetricDefinition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0ff61-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="0ff61-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ff61-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ff61-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ff61-111">Properties</span></span>

<span data-ttu-id="0ff61-112">La classe **CIM \_ AggregationMetricDefinition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ff61-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ff61-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="0ff61-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff61-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ff61-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ff61-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ff61-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ff61-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricDefinition**.**IsContinuous**")</span><span class="sxs-lookup"><span data-stu-id="0ff61-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="0ff61-117">Indique comment la valeur de métrique change à l’aide d’attributs courants tels que le changement de direction, les valeurs minimales et maximales et la sémantique d’encapsulage.</span><span class="sxs-lookup"><span data-stu-id="0ff61-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="0ff61-118">**Fonction simple** (5)</span><span class="sxs-lookup"><span data-stu-id="0ff61-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ff61-119">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0ff61-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0ff61-120">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0ff61-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ff61-121">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="0ff61-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ff61-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ff61-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ff61-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ff61-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ff61-124">Calcul de base effectué sur une mesure sous-jacente pour arriver à la valeur de cette mesure dérivée.</span><span class="sxs-lookup"><span data-stu-id="0ff61-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="0ff61-125">Cette propriété est **null** lorsque la propriété **ChangeType** a une valeur autre que « 5 » (fonction simple).</span><span class="sxs-lookup"><span data-stu-id="0ff61-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ff61-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0ff61-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="0ff61-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span><span class="sxs-lookup"><span data-stu-id="0ff61-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0ff61-128">La métrique signale la valeur la plus faible détectée pour l’entité surveillée associée.</span><span class="sxs-lookup"><span data-stu-id="0ff61-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="0ff61-129">On parle également de limite inférieure.</span><span class="sxs-lookup"><span data-stu-id="0ff61-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="0ff61-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="0ff61-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0ff61-131">La métrique signale la valeur maximale détectée pour l’entité surveillée associée.</span><span class="sxs-lookup"><span data-stu-id="0ff61-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="0ff61-132">Il s’agit également d’une limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="0ff61-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="0ff61-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Moyenne** (4)</span><span class="sxs-lookup"><span data-stu-id="0ff61-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0ff61-134">La métrique signale la valeur moyenne des valeurs métriques sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="0ff61-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="0ff61-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Médiane** (5)</span><span class="sxs-lookup"><span data-stu-id="0ff61-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0ff61-136">La métrique signale la valeur médiane des valeurs de métriques sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="0ff61-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="0ff61-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span><span class="sxs-lookup"><span data-stu-id="0ff61-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0ff61-138">la métrique signale la valeur modale des valeurs de métriques sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="0ff61-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0ff61-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0ff61-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="0ff61-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0ff61-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0ff61-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ff61-141">Requirements</span></span>



| <span data-ttu-id="0ff61-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ff61-142">Requirement</span></span> | <span data-ttu-id="0ff61-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ff61-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff61-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ff61-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff61-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0ff61-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0ff61-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ff61-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff61-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ff61-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0ff61-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ff61-148">Namespace</span></span><br/>                | <span data-ttu-id="0ff61-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0ff61-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0ff61-150">MOF</span><span class="sxs-lookup"><span data-stu-id="0ff61-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ff61-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ff61-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ff61-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0ff61-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ff61-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ff61-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ff61-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ff61-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff61-155">**\_BASEMETRICDEFINITION CIM**</span><span class="sxs-lookup"><span data-stu-id="0ff61-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 

