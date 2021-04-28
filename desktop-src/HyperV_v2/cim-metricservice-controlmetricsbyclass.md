---
description: La méthode ControlMetricsByClass de la classe CIM_MetricService-active et désactive la collection de mesures.
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Méthode ControlMetricsByClass de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109707"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="fff4d-103">Méthode ControlMetricsByClass de la \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="fff4d-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="fff4d-104">Active et désactive la collecte des métriques. **ControlMetricsByClass** est utilisé pour contrôler la collection de chaque type de mesure pour toutes les instances d’une classe ou la collection d’une métrique spécifique pour toutes les instances d’une classe.</span><span class="sxs-lookup"><span data-stu-id="fff4d-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fff4d-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="fff4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fff4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff4d-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fff4d-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff4d-108">Identifie la [**classe \_ propriété ManagedElement CIM**](cim-managedelement.md) pour laquelle les mesures seront contrôlées.</span><span class="sxs-lookup"><span data-stu-id="fff4d-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="fff4d-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="fff4d-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff4d-110">Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les mesures seront contrôlées.</span><span class="sxs-lookup"><span data-stu-id="fff4d-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="fff4d-111">*MetricCollectionEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fff4d-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff4d-112">Indique l’opération souhaitée à effectuer sur les mesures.</span><span class="sxs-lookup"><span data-stu-id="fff4d-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="fff4d-113">**Activer** (2)</span><span class="sxs-lookup"><span data-stu-id="fff4d-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="fff4d-114">**Désactiver** (3)</span><span class="sxs-lookup"><span data-stu-id="fff4d-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="fff4d-115">**Réinitialiser** (4)</span><span class="sxs-lookup"><span data-stu-id="fff4d-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fff4d-116">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fff4d-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="fff4d-117">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fff4d-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="fff4d-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fff4d-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="fff4d-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fff4d-119">Return value</span></span>

<span data-ttu-id="fff4d-120">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="fff4d-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fff4d-121">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="fff4d-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fff4d-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="fff4d-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fff4d-123">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="fff4d-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fff4d-124">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="fff4d-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fff4d-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fff4d-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fff4d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fff4d-126">Requirements</span></span>



| <span data-ttu-id="fff4d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fff4d-127">Requirement</span></span> | <span data-ttu-id="fff4d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fff4d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fff4d-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff4d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fff4d-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fff4d-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fff4d-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff4d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fff4d-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fff4d-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fff4d-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fff4d-133">Namespace</span></span><br/>                | <span data-ttu-id="fff4d-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fff4d-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fff4d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fff4d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fff4d-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fff4d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fff4d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fff4d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff4d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fff4d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fff4d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fff4d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff4d-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fff4d-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




