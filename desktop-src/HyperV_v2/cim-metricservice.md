---
description: Gère les métriques pour les éléments managés.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538682"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="c7646-103">\_Classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="c7646-103">CIM\_MetricService class</span></span>

<span data-ttu-id="c7646-104">Gère les métriques pour les éléments managés.</span><span class="sxs-lookup"><span data-stu-id="c7646-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7646-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7646-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="c7646-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c7646-106">Members</span></span>

<span data-ttu-id="c7646-107">La classe **CIM \_ MetricService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c7646-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="c7646-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c7646-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c7646-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c7646-109">Methods</span></span>

<span data-ttu-id="c7646-110">La classe **CIM \_ MetricService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c7646-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="c7646-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="c7646-111">Method</span></span>                                                                   | <span data-ttu-id="c7646-112">Description</span><span class="sxs-lookup"><span data-stu-id="c7646-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7646-113">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="c7646-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="c7646-114">Active et désactive la collecte des métriques.</span><span class="sxs-lookup"><span data-stu-id="c7646-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="c7646-115">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="c7646-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="c7646-116">Active et désactive la collection de mesures pour une classe.</span><span class="sxs-lookup"><span data-stu-id="c7646-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="c7646-117">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="c7646-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="c7646-118">Spécifie quand les métriques sont collectées.</span><span class="sxs-lookup"><span data-stu-id="c7646-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="c7646-119">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="c7646-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="c7646-120">Récupère une liste filtrée de valeurs de métriques.</span><span class="sxs-lookup"><span data-stu-id="c7646-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="c7646-121">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="c7646-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="c7646-122">Indique si la collection de mesures est activée pour les éléments managés spécifiés, et indique les métriques qui sont disponibles pour la collection pour chaque élément managé.</span><span class="sxs-lookup"><span data-stu-id="c7646-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="c7646-123">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="c7646-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="c7646-124">Indique les métriques disponibles pour la collecte de toutes les instances d’une classe CIM.</span><span class="sxs-lookup"><span data-stu-id="c7646-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="c7646-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7646-125">Requirements</span></span>



| <span data-ttu-id="c7646-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7646-126">Requirement</span></span> | <span data-ttu-id="c7646-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7646-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7646-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7646-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c7646-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7646-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7646-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7646-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c7646-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7646-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7646-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7646-132">Namespace</span></span><br/>                | <span data-ttu-id="c7646-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7646-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c7646-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c7646-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7646-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7646-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7646-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c7646-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7646-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7646-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7646-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7646-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7646-139">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="c7646-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




