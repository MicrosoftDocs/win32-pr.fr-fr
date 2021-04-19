---
description: Offre la possibilité de retourner une liste filtrée d' \_ instances BASEMETRICVALUE CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Méthode GetMetricValues de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527507"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a><span data-ttu-id="b73fc-103">Méthode GetMetricValues de la \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="b73fc-103">GetMetricValues method of the CIM\_MetricService class</span></span>

<span data-ttu-id="b73fc-104">Offre la possibilité de retourner une liste filtrée d' [**instances \_ BaseMetricValue CIM**](cim-basemetricvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="b73fc-104">Provides the ability to return a filtered list of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b73fc-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="b73fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b73fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73fc-107">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="b73fc-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73fc-108">Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les métriques seront retournées.</span><span class="sxs-lookup"><span data-stu-id="b73fc-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b73fc-109">*Plage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b73fc-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73fc-110">Identifie la manière dont les instances sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="b73fc-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="b73fc-111">L’algorithme de classement des instances de valeur est spécifique à la définition de métrique.</span><span class="sxs-lookup"><span data-stu-id="b73fc-111">The algorithm for ordering value instances is metric-definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="b73fc-112">**Minimum** (2)</span><span class="sxs-lookup"><span data-stu-id="b73fc-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="b73fc-113">**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="b73fc-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b73fc-114">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="b73fc-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="b73fc-115">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b73fc-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b73fc-116">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b73fc-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73fc-117">Identifie le nombre maximal d’instances qui doivent être retournées par la méthode.</span><span class="sxs-lookup"><span data-stu-id="b73fc-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="b73fc-118">*Valeurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b73fc-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b73fc-119">Une fois la méthode terminée, contient des références à des instances [**de \_ BaseMetricValue CIM**](cim-basemetricvalue.md), filtrées en fonction des valeurs des paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b73fc-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73fc-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b73fc-120">Return value</span></span>

<span data-ttu-id="b73fc-121">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="b73fc-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b73fc-122">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="b73fc-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b73fc-123">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="b73fc-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b73fc-124">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="b73fc-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b73fc-125">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="b73fc-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b73fc-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b73fc-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b73fc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b73fc-127">Requirements</span></span>



| <span data-ttu-id="b73fc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b73fc-128">Requirement</span></span> | <span data-ttu-id="b73fc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b73fc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73fc-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73fc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b73fc-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b73fc-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b73fc-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73fc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b73fc-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b73fc-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b73fc-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b73fc-134">Namespace</span></span><br/>                | <span data-ttu-id="b73fc-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b73fc-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b73fc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b73fc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b73fc-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b73fc-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b73fc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b73fc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b73fc-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b73fc-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b73fc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b73fc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73fc-141">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b73fc-141">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




