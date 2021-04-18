---
description: Obtient des valeurs de métriques.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Méthode GetMetricValues de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534126"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="37643-103">Méthode GetMetricValues de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="37643-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="37643-104">Obtient des valeurs de métriques.</span><span class="sxs-lookup"><span data-stu-id="37643-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="37643-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37643-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="37643-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37643-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37643-107">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="37643-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37643-108">Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les métriques seront retournées.</span><span class="sxs-lookup"><span data-stu-id="37643-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="37643-109">*Plage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37643-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37643-110">Identifie la manière dont les instances sont sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="37643-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="37643-111">L’algorithme de classement des instances de valeur est spécifique à la définition de métrique.</span><span class="sxs-lookup"><span data-stu-id="37643-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="37643-112">**Minimum** (2)</span><span class="sxs-lookup"><span data-stu-id="37643-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="37643-113">**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="37643-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="37643-114">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="37643-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="37643-115">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="37643-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="37643-116">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37643-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37643-117">Identifie le nombre maximal d’instances qui doivent être retournées par la méthode.</span><span class="sxs-lookup"><span data-stu-id="37643-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="37643-118">*Valeurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="37643-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37643-119">Une fois la méthode terminée, contient des références à des instances [**de \_ BaseMetricValue CIM**](cim-basemetricvalue.md), filtrées en fonction des valeurs des paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="37643-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37643-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37643-120">Return value</span></span>

<span data-ttu-id="37643-121">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="37643-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="37643-122">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="37643-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37643-123">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="37643-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="37643-124">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="37643-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="37643-125">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="37643-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="37643-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="37643-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="37643-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37643-127">Requirements</span></span>



| <span data-ttu-id="37643-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37643-128">Requirement</span></span> | <span data-ttu-id="37643-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="37643-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37643-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37643-130">Minimum supported client</span></span><br/> | <span data-ttu-id="37643-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="37643-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="37643-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37643-132">Minimum supported server</span></span><br/> | <span data-ttu-id="37643-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37643-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="37643-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37643-134">Namespace</span></span><br/>                | <span data-ttu-id="37643-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="37643-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37643-136">MOF</span><span class="sxs-lookup"><span data-stu-id="37643-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37643-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37643-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37643-138">DLL</span><span class="sxs-lookup"><span data-stu-id="37643-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37643-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37643-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37643-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37643-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37643-141">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="37643-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




