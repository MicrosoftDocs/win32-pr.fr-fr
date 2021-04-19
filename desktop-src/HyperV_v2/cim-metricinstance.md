---
description: Représente une association entre une instance d’une valeur de métrique et une définition de métrique.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: Classe CIM_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: defba85f46e037c226a96cfaa8ffac44b99244f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536704"
---
# <a name="cim_metricinstance-class"></a><span data-ttu-id="b2a97-103">\_Classe CIM MetricInstance</span><span class="sxs-lookup"><span data-stu-id="b2a97-103">CIM\_MetricInstance class</span></span>

<span data-ttu-id="b2a97-104">Représente une association entre une instance d’une valeur de métrique et une définition de métrique.</span><span class="sxs-lookup"><span data-stu-id="b2a97-104">Represents an association between an instance of a metric value and a metric definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2a97-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b2a97-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b2a97-106">Members</span></span>

<span data-ttu-id="b2a97-107">La classe **CIM \_ MetricInstance** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2a97-107">The **CIM\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="b2a97-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2a97-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2a97-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2a97-109">Properties</span></span>

<span data-ttu-id="b2a97-110">La classe **CIM \_ MetricInstance** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2a97-110">The **CIM\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2a97-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b2a97-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2a97-112">Type de données : **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="b2a97-112">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="b2a97-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2a97-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2a97-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b2a97-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b2a97-115">Définition de la valeur de la métrique.</span><span class="sxs-lookup"><span data-stu-id="b2a97-115">The definition of the metric value.</span></span>

</dd> <dt>

<span data-ttu-id="b2a97-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b2a97-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2a97-117">Type de données : **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="b2a97-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="b2a97-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2a97-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2a97-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="b2a97-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b2a97-120">Valeur de métrique associée à la définition de métrique.</span><span class="sxs-lookup"><span data-stu-id="b2a97-120">The metric value that is associated with the metric definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2a97-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2a97-121">Requirements</span></span>



| <span data-ttu-id="b2a97-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2a97-122">Requirement</span></span> | <span data-ttu-id="b2a97-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2a97-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a97-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2a97-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a97-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b2a97-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b2a97-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2a97-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a97-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2a97-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b2a97-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2a97-128">Namespace</span></span><br/>                | <span data-ttu-id="b2a97-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2a97-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2a97-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b2a97-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2a97-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2a97-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2a97-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b2a97-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2a97-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2a97-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2a97-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2a97-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a97-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="b2a97-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

