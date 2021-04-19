---
description: Affiche les métriques par classe.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Méthode ShowMetricsByClass de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544841"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="c71c5-103">Méthode ShowMetricsByClass de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="c71c5-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="c71c5-104">Affiche les métriques par classe.</span><span class="sxs-lookup"><span data-stu-id="c71c5-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c71c5-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="c71c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c71c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71c5-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c71c5-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71c5-108">Identifie une classe CIM pour laquelle la méthode retourne des références à des instances de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques qui peuvent être capturées pour toutes les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="c71c5-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c71c5-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="c71c5-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71c5-110">Identifie une instance de [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c71c5-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="c71c5-111">La méthode retourne des références aux instances [**de \_ propriété ManagedElement CIM**](cim-managedelement.md) pour lesquelles les métriques définies par l’instance de **CIM \_ BaseMetricDefinition** sont disponibles pour être collectées.</span><span class="sxs-lookup"><span data-stu-id="c71c5-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="c71c5-112">*DefinitionList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c71c5-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c71c5-113">Une fois la méthode terminée, peut contenir des références à des instances [**de \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définissent les métriques disponibles pour la collecte du [**\_ propriété ManagedElement CIM**](cim-managedelement.md) identifié par le paramètre *Subject* .</span><span class="sxs-lookup"><span data-stu-id="c71c5-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c71c5-114">*MetricNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c71c5-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c71c5-115">Une fois la méthode terminée, chaque index de tableau contient la valeur de la propriété **Name** pour l’instance de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) référencée par l’index de tableau correspondant du paramètre *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="c71c5-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c71c5-116">*MetricCollectionEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c71c5-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c71c5-117">Indique si une mesure est collectée pour toutes les instances d’une classe d’éléments managés.</span><span class="sxs-lookup"><span data-stu-id="c71c5-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c71c5-118">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="c71c5-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c71c5-119">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="c71c5-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="c71c5-120">**Réservé** (4)</span><span class="sxs-lookup"><span data-stu-id="c71c5-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c71c5-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c71c5-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c71c5-122">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c71c5-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="c71c5-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c71c5-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="c71c5-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c71c5-124">Return value</span></span>

<span data-ttu-id="c71c5-125">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c71c5-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c71c5-126">**Opération réussie** ()</span><span class="sxs-lookup"><span data-stu-id="c71c5-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="c71c5-127">**Non pris en charge** ()</span><span class="sxs-lookup"><span data-stu-id="c71c5-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="c71c5-128">**Échec** ()</span><span class="sxs-lookup"><span data-stu-id="c71c5-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="c71c5-129">**Méthode réservée** ()</span><span class="sxs-lookup"><span data-stu-id="c71c5-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="c71c5-130">**Spécifique au fournisseur** ()</span><span class="sxs-lookup"><span data-stu-id="c71c5-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c71c5-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c71c5-131">Requirements</span></span>



| <span data-ttu-id="c71c5-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c71c5-132">Requirement</span></span> | <span data-ttu-id="c71c5-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c71c5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c71c5-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c71c5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c71c5-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c71c5-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c71c5-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c71c5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c71c5-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c71c5-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c71c5-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c71c5-138">Namespace</span></span><br/>                | <span data-ttu-id="c71c5-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c71c5-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c71c5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c71c5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c71c5-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c71c5-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c71c5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c71c5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71c5-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c71c5-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c71c5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c71c5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71c5-145">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="c71c5-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




