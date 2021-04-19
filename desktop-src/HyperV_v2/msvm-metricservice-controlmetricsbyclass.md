---
description: Contrôle les métriques par classe.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Méthode ControlMetricsByClass de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524688"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="bf197-103">Méthode ControlMetricsByClass de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="bf197-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="bf197-104">Contrôle les métriques par classe.</span><span class="sxs-lookup"><span data-stu-id="bf197-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf197-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf197-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="bf197-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf197-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf197-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf197-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf197-108">Identifie la classe CIM pour laquelle les mesures seront contrôlées.</span><span class="sxs-lookup"><span data-stu-id="bf197-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="bf197-109">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="bf197-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf197-110">Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les mesures seront contrôlées.</span><span class="sxs-lookup"><span data-stu-id="bf197-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="bf197-111">*MetricCollectionEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf197-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf197-112">Indique l’opération souhaitée à effectuer sur les mesures.</span><span class="sxs-lookup"><span data-stu-id="bf197-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="bf197-113">**Activer** (2)</span><span class="sxs-lookup"><span data-stu-id="bf197-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="bf197-114">**Désactiver** (3)</span><span class="sxs-lookup"><span data-stu-id="bf197-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="bf197-115">**Réinitialiser** (4)</span><span class="sxs-lookup"><span data-stu-id="bf197-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bf197-116">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="bf197-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bf197-117">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bf197-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="bf197-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bf197-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="bf197-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf197-119">Return value</span></span>

<span data-ttu-id="bf197-120">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf197-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bf197-121">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="bf197-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf197-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="bf197-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bf197-123">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="bf197-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bf197-124">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="bf197-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bf197-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bf197-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bf197-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf197-126">Requirements</span></span>



| <span data-ttu-id="bf197-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf197-127">Requirement</span></span> | <span data-ttu-id="bf197-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf197-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf197-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf197-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bf197-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bf197-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bf197-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf197-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bf197-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bf197-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bf197-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf197-133">Namespace</span></span><br/>                | <span data-ttu-id="bf197-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bf197-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bf197-135">MOF</span><span class="sxs-lookup"><span data-stu-id="bf197-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf197-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf197-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf197-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bf197-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf197-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf197-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf197-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf197-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf197-140">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="bf197-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




