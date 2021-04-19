---
description: Utilisé pour contrôler la collection de mesures pour un ou des éléments managés.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Méthode ControlMetrics de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530602"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="1da8e-103">Méthode ControlMetrics de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="1da8e-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="1da8e-104">Utilisé pour contrôler la collection de mesures pour un ou des éléments managés.</span><span class="sxs-lookup"><span data-stu-id="1da8e-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1da8e-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="1da8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1da8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da8e-107">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1da8e-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da8e-108">Instance [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui identifie les éléments managés pour lesquels des mesures seront collectées.</span><span class="sxs-lookup"><span data-stu-id="1da8e-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="1da8e-109">Si ce paramètre a la **valeur null**, les métriques de tous les éléments managés associés au paramètre de *définition* seront collectées.</span><span class="sxs-lookup"><span data-stu-id="1da8e-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="1da8e-110">*Définition* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="1da8e-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da8e-111">Instance [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) qui spécifie les métriques qui seront collectées.</span><span class="sxs-lookup"><span data-stu-id="1da8e-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="1da8e-112">Si ce paramètre a la **valeur null**, les métriques de toutes les définitions associées à l’élément géré identifié par le paramètre *Subject* sont collectées.</span><span class="sxs-lookup"><span data-stu-id="1da8e-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="1da8e-113">*MetricCollectionEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1da8e-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da8e-114">Spécifie l’opération à effectuer sur la collection de mesures.</span><span class="sxs-lookup"><span data-stu-id="1da8e-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="1da8e-115">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1da8e-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="1da8e-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Activer** (2)</span><span class="sxs-lookup"><span data-stu-id="1da8e-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1da8e-117">Activez la collecte des métriques.</span><span class="sxs-lookup"><span data-stu-id="1da8e-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="1da8e-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (3)</span><span class="sxs-lookup"><span data-stu-id="1da8e-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1da8e-119">Désactivez la collecte des métriques.</span><span class="sxs-lookup"><span data-stu-id="1da8e-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="1da8e-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (4)</span><span class="sxs-lookup"><span data-stu-id="1da8e-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1da8e-121">Réinitialiser les valeurs des métriques.</span><span class="sxs-lookup"><span data-stu-id="1da8e-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1da8e-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="1da8e-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1da8e-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1da8e-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="1da8e-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1da8e-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1da8e-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1da8e-125">Return value</span></span>

<span data-ttu-id="1da8e-126">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1da8e-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1da8e-127">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="1da8e-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1da8e-128">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="1da8e-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1da8e-129">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="1da8e-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1da8e-130">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="1da8e-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1da8e-131">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1da8e-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1da8e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="1da8e-132">Remarks</span></span>

<span data-ttu-id="1da8e-133">Cette méthode échouera dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="1da8e-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="1da8e-134">Les paramètres *Subject* et *definition* ont tous deux la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1da8e-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="1da8e-135">Les paramètres *Subject* et *definition* sont tous deux non **null** et il n’y a pas d’instance de [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md) qui associe les deux instances.</span><span class="sxs-lookup"><span data-stu-id="1da8e-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="1da8e-136">Le paramètre de *définition* est une référence à une instance de [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) qui n’est pas associée [**au \_ MetricService MSVM**](msvm-metricservice.md) via [**MSVM \_ ServiceAffectsElement**](msvm-serviceaffectselement.md).</span><span class="sxs-lookup"><span data-stu-id="1da8e-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1da8e-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1da8e-137">Requirements</span></span>



| <span data-ttu-id="1da8e-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1da8e-138">Requirement</span></span> | <span data-ttu-id="1da8e-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="1da8e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1da8e-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da8e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1da8e-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1da8e-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1da8e-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da8e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1da8e-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1da8e-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1da8e-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1da8e-144">Namespace</span></span><br/>                | <span data-ttu-id="1da8e-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1da8e-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1da8e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1da8e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1da8e-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1da8e-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1da8e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1da8e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1da8e-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1da8e-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1da8e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1da8e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da8e-151">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="1da8e-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

