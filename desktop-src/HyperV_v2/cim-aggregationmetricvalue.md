---
description: Représente la valeur d’instance d’une mesure définie par une instance de \_ AGGREGATIONMETRICDEFINITION CIM.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Classe CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519639"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="ef65b-103">\_Classe CIM AggregationMetricValue</span><span class="sxs-lookup"><span data-stu-id="ef65b-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="ef65b-104">Représente la valeur d’instance d’une mesure définie par une instance **de \_ AggregationMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="ef65b-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef65b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef65b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="ef65b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ef65b-106">Members</span></span>

<span data-ttu-id="ef65b-107">La classe **CIM \_ AggregationMetricValue** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef65b-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="ef65b-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef65b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef65b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef65b-109">Properties</span></span>

<span data-ttu-id="ef65b-110">La classe **CIM \_ AggregationMetricValue** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef65b-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef65b-111">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="ef65b-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef65b-112">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef65b-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef65b-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef65b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef65b-114">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="ef65b-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="ef65b-115">Représente la durée pendant laquelle l’agrégation a été calculée.</span><span class="sxs-lookup"><span data-stu-id="ef65b-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="ef65b-116">Le début d’un intervalle de surveillance sur lequel la fonction d’agrégation est appliquée est déterminé par la soustraction de la valeur **AggregationDuration** de la valeur **AggregationTimestamp** .</span><span class="sxs-lookup"><span data-stu-id="ef65b-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="ef65b-117">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="ef65b-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef65b-118">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef65b-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef65b-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef65b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef65b-120">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Duration**»)</span><span class="sxs-lookup"><span data-stu-id="ef65b-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="ef65b-121">Heure à laquelle la fonction d’agrégation a été appliquée pour déterminer la valeur de l’instance de métrique.</span><span class="sxs-lookup"><span data-stu-id="ef65b-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="ef65b-122">Cela diffère de l’heure de création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="ef65b-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="ef65b-123">La valeur **AggregationTimeStamp** change chaque fois que la fonction d’agrégation est appliquée pour calculer la valeur.</span><span class="sxs-lookup"><span data-stu-id="ef65b-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef65b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef65b-124">Requirements</span></span>



| <span data-ttu-id="ef65b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef65b-125">Requirement</span></span> | <span data-ttu-id="ef65b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef65b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef65b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef65b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef65b-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ef65b-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ef65b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef65b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef65b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef65b-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ef65b-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef65b-131">Namespace</span></span><br/>                | <span data-ttu-id="ef65b-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef65b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef65b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ef65b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef65b-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef65b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef65b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ef65b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef65b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef65b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef65b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef65b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef65b-138">**\_BASEMETRICVALUE CIM**</span><span class="sxs-lookup"><span data-stu-id="ef65b-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 

