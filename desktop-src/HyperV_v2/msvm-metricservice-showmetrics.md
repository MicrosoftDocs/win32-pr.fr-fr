---
description: Affiche les métriques spécifiées.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Méthode ShowMetrics de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868506"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="b2b13-103">Méthode ShowMetrics de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="b2b13-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="b2b13-104">Affiche les métriques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b2b13-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2b13-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b2b13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2b13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b13-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2b13-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b13-108">Le paramètre subject identifie une instance de [**\_ propriété ManagedElement CIM**](cim-managedelement.md) pour laquelle la méthode retourne des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques capturées pour le **\_ propriété ManagedElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="b2b13-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b13-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="b2b13-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b13-110">Le paramètre de définition identifie une instance [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="b2b13-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="b2b13-111">La méthode retourne des références aux instances [**de \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles les métriques définies par l’instance de **CIM \_ BaseMetricDefinition** sont disponibles pour être collectées.</span><span class="sxs-lookup"><span data-stu-id="b2b13-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="b2b13-112">*ManagedElements* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2b13-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b13-113">Une fois la méthode terminée, le paramètre *ManagedElements* \[ \] peut contenir des références à [**des \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles la mesure identifiée par le paramètre de *définition* est disponible pour la collecte.</span><span class="sxs-lookup"><span data-stu-id="b2b13-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="b2b13-114">*DefinitionList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2b13-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b13-115">En cas de réussite de la méthode, le paramètre *DefinitionList* peut contenir des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte pour le [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .</span><span class="sxs-lookup"><span data-stu-id="b2b13-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2b13-116">*MetricNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2b13-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b13-117">En cas de réussite de la méthode, chaque index de tableau du paramètre *MetricNames* doit contenir la valeur de la propriété Name pour l’instance [**du \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="b2b13-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2b13-118">*MetricCollectionEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2b13-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b13-119">Le paramètre *MetricCollectionEnabled* indique si une mesure est collectée pour un élément géré.</span><span class="sxs-lookup"><span data-stu-id="b2b13-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="b2b13-120">**Activer** (2)</span><span class="sxs-lookup"><span data-stu-id="b2b13-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="b2b13-121">**Désactiver** (3)</span><span class="sxs-lookup"><span data-stu-id="b2b13-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b2b13-122">**Réservé** (4)</span><span class="sxs-lookup"><span data-stu-id="b2b13-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b2b13-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="b2b13-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b2b13-124">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b2b13-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="b2b13-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b2b13-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b2b13-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2b13-126">Return value</span></span>

<span data-ttu-id="b2b13-127">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2b13-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b2b13-128">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="b2b13-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b2b13-129">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="b2b13-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b2b13-130">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="b2b13-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b2b13-131">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="b2b13-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b2b13-132">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b2b13-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b13-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2b13-133">Requirements</span></span>



| <span data-ttu-id="b2b13-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2b13-134">Requirement</span></span> | <span data-ttu-id="b2b13-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2b13-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b13-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2b13-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b13-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2b13-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b2b13-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2b13-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b13-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2b13-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b2b13-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2b13-140">Namespace</span></span><br/>                | <span data-ttu-id="b2b13-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2b13-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2b13-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b13-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b13-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2b13-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b13-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b13-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b13-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2b13-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2b13-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2b13-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b13-147">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="b2b13-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




