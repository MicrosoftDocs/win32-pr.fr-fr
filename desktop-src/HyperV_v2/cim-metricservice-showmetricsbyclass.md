---
description: 'Signale les éléments suivants : les métriques pouvant être collectées pour toutes les instances d’une classe CIM, les classes CIM pour lesquelles une mesure définie par une instance de CIM \_ BaseMetricDefinition est disponible pour être collectée, et si une mesure particulière est actuellement collectée pour un élément géré.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Méthode ShowMetricsByClass de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865541"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="88001-103">Méthode ShowMetricsByClass de la \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="88001-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="88001-104">Signale les éléments suivants : les métriques pouvant être collectées pour toutes les instances d’une classe CIM, les classes CIM pour lesquelles une mesure définie par une instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) est disponible pour être collectée, et si une mesure particulière est actuellement collectée pour un élément géré.</span><span class="sxs-lookup"><span data-stu-id="88001-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="88001-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88001-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="88001-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88001-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88001-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88001-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88001-108">Identifie une classe CIM pour laquelle la méthode retourne des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques qui peuvent être capturées pour toutes les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="88001-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="88001-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="88001-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88001-110">Identifie une instance de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="88001-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="88001-111">La méthode retourne des références aux instances [**de \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles les métriques définies par l’instance de **CIM \_ BaseMetricDefinition** sont disponibles pour être collectées.</span><span class="sxs-lookup"><span data-stu-id="88001-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="88001-112">*DefinitionList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88001-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88001-113">En cas de réussite, peut contenir des références à des instances d’objets [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte pour le [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .</span><span class="sxs-lookup"><span data-stu-id="88001-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="88001-114">*MetricNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88001-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88001-115">En cas de réussite, chaque index de tableau doit contenir la valeur de la propriété **Name** pour l’instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="88001-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="88001-116">*MetricCollectionEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88001-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88001-117">Indique si une mesure est collectée pour toutes les instances d’une classe d’éléments managés.</span><span class="sxs-lookup"><span data-stu-id="88001-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="88001-118">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="88001-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="88001-119">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="88001-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="88001-120">**Réservé** (4)</span><span class="sxs-lookup"><span data-stu-id="88001-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88001-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="88001-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="88001-122">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="88001-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="88001-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="88001-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="88001-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88001-124">Return value</span></span>

<span data-ttu-id="88001-125">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="88001-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="88001-126">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="88001-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88001-127">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="88001-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88001-128">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="88001-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88001-129">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="88001-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="88001-130">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="88001-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="88001-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88001-131">Requirements</span></span>



| <span data-ttu-id="88001-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88001-132">Requirement</span></span> | <span data-ttu-id="88001-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="88001-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88001-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88001-134">Minimum supported client</span></span><br/> | <span data-ttu-id="88001-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="88001-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="88001-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88001-136">Minimum supported server</span></span><br/> | <span data-ttu-id="88001-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="88001-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="88001-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="88001-138">Namespace</span></span><br/>                | <span data-ttu-id="88001-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="88001-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="88001-140">MOF</span><span class="sxs-lookup"><span data-stu-id="88001-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88001-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88001-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88001-142">DLL</span><span class="sxs-lookup"><span data-stu-id="88001-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88001-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88001-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88001-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88001-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88001-145">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="88001-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




