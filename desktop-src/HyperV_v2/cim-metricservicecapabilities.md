---
description: Décrit les fonctionnalités d’un \_ objet CIM MetricService.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: Classe CIM_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518315"
---
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="29360-103">\_Classe CIM MetricServiceCapabilities</span><span class="sxs-lookup"><span data-stu-id="29360-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="29360-104">Décrit les fonctionnalités d’un objet [**CIM \_ MetricService**](cim-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29360-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="29360-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29360-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="29360-106">Membres</span><span class="sxs-lookup"><span data-stu-id="29360-106">Members</span></span>

<span data-ttu-id="29360-107">La classe **CIM \_ MetricServiceCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29360-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="29360-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29360-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29360-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29360-109">Properties</span></span>

<span data-ttu-id="29360-110">La classe **CIM \_ MetricServiceCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="29360-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29360-111">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="29360-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-112">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="29360-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29360-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29360-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29360-114">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ManagedElementControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="29360-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="29360-115">Tableau qui contient les identificateurs des instances [**CIM \_ propriété ManagedElement**](cim-managedelement.md) contrôlées par le service de métrique.</span><span class="sxs-lookup"><span data-stu-id="29360-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="29360-116">Les identificateurs doivent être mis en forme comme des URI WBEM (Web-Based Enterprise Management).</span><span class="sxs-lookup"><span data-stu-id="29360-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="29360-117">Pour pouvoir utiliser cette propriété, le service de métriques doit prendre en charge l’activation ou la désactivation d’au moins une métrique définie pour l’instance **CIM \_ propriété ManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="29360-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="29360-118">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="29360-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-119">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="29360-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29360-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29360-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29360-121">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**MetricControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="29360-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="29360-122">Tableau qui contient les identificateurs de l' [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) qui définit les métriques gérées par le service de métrique.</span><span class="sxs-lookup"><span data-stu-id="29360-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="29360-123">Les identificateurs doivent être mis en forme comme des URI WBEM (Web-Based Enterprise Management).</span><span class="sxs-lookup"><span data-stu-id="29360-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="29360-124">Pour pouvoir utiliser cette propriété, une instance [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) doit être associée à une instance [**\_ MetricService**](cim-metricservice.md) CIM par le biais de la classe [**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md) .</span><span class="sxs-lookup"><span data-stu-id="29360-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="29360-125">En outre, le service de métriques doit prendre en charge l’activation ou la désactivation d’au moins une métrique définie par l’instance **CIM \_ BaseMetricDefinition** .</span><span class="sxs-lookup"><span data-stu-id="29360-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="29360-126">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="29360-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-127">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29360-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="29360-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29360-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29360-129">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableManagedElements**")</span><span class="sxs-lookup"><span data-stu-id="29360-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="29360-130">Tableau qui indique les types de contrôle pris en charge par le service de métrique pour les éléments managés dans le tableau **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="29360-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="29360-131">Ce tableau correspond au tableau **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="29360-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="29360-132">Les types de contrôle de ce tableau sont associés à des métriques par le biais du tableau **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="29360-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="29360-133">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="29360-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="29360-134">**Discret** (2)</span><span class="sxs-lookup"><span data-stu-id="29360-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="29360-135">**Bulk** (3)</span><span class="sxs-lookup"><span data-stu-id="29360-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="29360-136">**Les deux** (4)</span><span class="sxs-lookup"><span data-stu-id="29360-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="29360-137">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="29360-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="29360-138">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="29360-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29360-139">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="29360-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-140">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29360-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="29360-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29360-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29360-142">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableMetrics**")</span><span class="sxs-lookup"><span data-stu-id="29360-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="29360-143">Tableau qui indique les types de contrôle pris en charge par le service de métrique.</span><span class="sxs-lookup"><span data-stu-id="29360-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="29360-144">Ce tableau correspond au tableau **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="29360-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="29360-145">Les types de contrôle de ce tableau sont associés à des métriques par le biais du tableau **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="29360-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="29360-146">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="29360-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="29360-147">**Discret** (2)</span><span class="sxs-lookup"><span data-stu-id="29360-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="29360-148">**Bulk** (3)</span><span class="sxs-lookup"><span data-stu-id="29360-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="29360-149">**Les deux** (4)</span><span class="sxs-lookup"><span data-stu-id="29360-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="29360-150">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="29360-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="29360-151">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="29360-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29360-152">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="29360-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-153">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29360-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="29360-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29360-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29360-155">Tableau qui contient les noms des méthodes prises en charge par le service de métrique.</span><span class="sxs-lookup"><span data-stu-id="29360-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="29360-156">**ControlMetrics** (2)</span><span class="sxs-lookup"><span data-stu-id="29360-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="29360-157">**ControlMetricsByClass** (3)</span><span class="sxs-lookup"><span data-stu-id="29360-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="29360-158">**ShowMetrics** (4)</span><span class="sxs-lookup"><span data-stu-id="29360-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="29360-159">**ShowMetricsByClass** (5)</span><span class="sxs-lookup"><span data-stu-id="29360-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="29360-160">**GetMetricValues** (6)</span><span class="sxs-lookup"><span data-stu-id="29360-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="29360-161">**ControlSampleTimes** (7)</span><span class="sxs-lookup"><span data-stu-id="29360-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="29360-162">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="29360-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="29360-163">**Spécifique au fournisseur** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="29360-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="29360-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="29360-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="29360-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29360-165">Requirements</span></span>



| <span data-ttu-id="29360-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29360-166">Requirement</span></span> | <span data-ttu-id="29360-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="29360-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29360-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29360-168">Minimum supported client</span></span><br/> | <span data-ttu-id="29360-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29360-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="29360-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29360-170">Minimum supported server</span></span><br/> | <span data-ttu-id="29360-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29360-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="29360-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29360-172">Namespace</span></span><br/>                | <span data-ttu-id="29360-173">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="29360-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="29360-174">MOF</span><span class="sxs-lookup"><span data-stu-id="29360-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29360-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29360-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29360-176">DLL</span><span class="sxs-lookup"><span data-stu-id="29360-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29360-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29360-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29360-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29360-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29360-179">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="29360-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

