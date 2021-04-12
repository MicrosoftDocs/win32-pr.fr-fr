---
description: Active et désactive la collecte des métriques.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Méthode ControlMetrics de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203087"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="97958-103">Méthode ControlMetrics de la \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="97958-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="97958-104">Active et désactive la collecte des métriques. **ControlMetrics** est utilisé pour contrôler la collection de chaque type de métrique pour un [**\_ propriété ManagedElement CIM**](cim-managedelement.md), la collection d’un type donné de métrique pour tous les éléments managés ou la collection d’une métrique spécifique pour un élément managé spécifique.</span><span class="sxs-lookup"><span data-stu-id="97958-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="97958-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97958-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="97958-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97958-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97958-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97958-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97958-108">[**\_ Propriété ManagedElement CIM**](cim-managedelement.md) qui identifie les éléments managés pour lesquels les mesures seront contrôlées.</span><span class="sxs-lookup"><span data-stu-id="97958-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="97958-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="97958-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97958-110">Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les mesures seront contrôlées.</span><span class="sxs-lookup"><span data-stu-id="97958-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="97958-111">*MetricCollectionEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97958-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97958-112">Indique l’opération souhaitée à effectuer sur les mesures.</span><span class="sxs-lookup"><span data-stu-id="97958-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="97958-113">**Activer** (2)</span><span class="sxs-lookup"><span data-stu-id="97958-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="97958-114">**Désactiver** (3)</span><span class="sxs-lookup"><span data-stu-id="97958-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="97958-115">**Réinitialiser** (4)</span><span class="sxs-lookup"><span data-stu-id="97958-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="97958-116">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="97958-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="97958-117">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="97958-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="97958-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="97958-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="97958-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97958-119">Return value</span></span>

<span data-ttu-id="97958-120">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="97958-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="97958-121">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="97958-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="97958-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="97958-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="97958-123">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="97958-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="97958-124">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="97958-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="97958-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="97958-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="97958-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97958-126">Requirements</span></span>



| <span data-ttu-id="97958-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97958-127">Requirement</span></span> | <span data-ttu-id="97958-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="97958-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97958-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97958-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97958-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="97958-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="97958-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97958-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97958-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97958-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="97958-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97958-133">Namespace</span></span><br/>                | <span data-ttu-id="97958-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="97958-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="97958-135">MOF</span><span class="sxs-lookup"><span data-stu-id="97958-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97958-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97958-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97958-137">DLL</span><span class="sxs-lookup"><span data-stu-id="97958-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97958-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97958-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97958-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97958-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97958-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="97958-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




