---
description: 'Signale les éléments suivants : les métriques qui peuvent être collectées pour un élément managé, les éléments managés pour lesquels une mesure définie par une instance de CIM \_ BaseMetricDefinition est disponible pour être collectée, et si une mesure particulière est actuellement collectée pour un élément géré.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Méthode ShowMetrics de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115631"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="905e1-103">Méthode ShowMetrics de la \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="905e1-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="905e1-104">Signale les éléments suivants : les métriques qui peuvent être collectées pour un élément managé, les éléments managés pour lesquels une mesure définie par une instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) est disponible pour être collectée, et si une mesure particulière est actuellement collectée pour un élément géré.</span><span class="sxs-lookup"><span data-stu-id="905e1-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="905e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="905e1-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="905e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="905e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905e1-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="905e1-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="905e1-108">Identifie une instance de [**\_ propriété ManagedElement CIM**](cim-managedelement.md) pour laquelle la méthode retourne des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques capturées pour le **\_ propriété ManagedElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="905e1-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="905e1-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="905e1-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="905e1-110">Identifie une instance de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="905e1-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="905e1-111">La méthode retourne des références aux instances [**de \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles les métriques définies par l’instance de **CIM \_ BaseMetricDefinition** sont disponibles pour être collectées.</span><span class="sxs-lookup"><span data-stu-id="905e1-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="905e1-112">*ManagedElements* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="905e1-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e1-113">En cas de réussite, peut contenir des références aux objets [**CIM \_ propriété ManagedElement**](cim-managedelement.md) pour lesquels la mesure identifiée par le paramètre de *définition* est disponible pour la collecte.</span><span class="sxs-lookup"><span data-stu-id="905e1-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="905e1-114">*DefinitionList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="905e1-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e1-115">En cas de réussite, peut contenir des références à des instances d’objets [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte pour le [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .</span><span class="sxs-lookup"><span data-stu-id="905e1-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="905e1-116">*MetricNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="905e1-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e1-117">En cas de réussite, chaque index de tableau doit contenir la valeur de la propriété **Name** pour l’instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="905e1-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="905e1-118">*MetricCollectionEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="905e1-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e1-119">Indique si une mesure est collectée pour un élément managé.</span><span class="sxs-lookup"><span data-stu-id="905e1-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="905e1-120">**Activer** (2)</span><span class="sxs-lookup"><span data-stu-id="905e1-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="905e1-121">**Désactiver** (3)</span><span class="sxs-lookup"><span data-stu-id="905e1-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="905e1-122">**Réservé** (4)</span><span class="sxs-lookup"><span data-stu-id="905e1-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="905e1-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="905e1-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="905e1-124">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="905e1-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="905e1-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="905e1-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="905e1-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="905e1-126">Return value</span></span>

<span data-ttu-id="905e1-127">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="905e1-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="905e1-128">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="905e1-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="905e1-129">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="905e1-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="905e1-130">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="905e1-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="905e1-131">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="905e1-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="905e1-132">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="905e1-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="905e1-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="905e1-133">Requirements</span></span>



| <span data-ttu-id="905e1-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="905e1-134">Requirement</span></span> | <span data-ttu-id="905e1-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="905e1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905e1-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="905e1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="905e1-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="905e1-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="905e1-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="905e1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="905e1-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="905e1-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="905e1-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="905e1-140">Namespace</span></span><br/>                | <span data-ttu-id="905e1-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="905e1-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="905e1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="905e1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="905e1-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="905e1-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="905e1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="905e1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="905e1-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="905e1-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="905e1-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="905e1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905e1-147">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="905e1-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




