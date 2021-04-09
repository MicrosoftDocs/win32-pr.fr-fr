---
description: Décrit les fonctionnalités de l’instance MSVM \_ MetricService associée.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Classe Msvm_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868501"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="2f565-103">MSVM \_ MetricServiceCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="2f565-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="2f565-104">Décrit les fonctionnalités de l’instance [**MSVM \_ MetricService**](msvm-metricservice.md) associée.</span><span class="sxs-lookup"><span data-stu-id="2f565-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="2f565-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2f565-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f565-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f565-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="2f565-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2f565-107">Members</span></span>

<span data-ttu-id="2f565-108">La classe **MSVM \_ MetricServiceCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f565-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="2f565-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f565-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f565-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f565-110">Properties</span></span>

<span data-ttu-id="2f565-111">La classe **MSVM \_ MetricServiceCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f565-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f565-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2f565-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f565-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2f565-115">A short description of the object.</span></span> <span data-ttu-id="2f565-116">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités du service métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="2f565-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="2f565-117">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="2f565-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-118">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2f565-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f565-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f565-120">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="2f565-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2f565-121">Identifie les instances de [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui peuvent être contrôlées par l' **instance \_ MetricService CIM** associée.</span><span class="sxs-lookup"><span data-stu-id="2f565-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="2f565-122">Si cette propriété a la **valeur null**, tous les éléments peuvent être contrôlés.</span><span class="sxs-lookup"><span data-stu-id="2f565-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="2f565-123">Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2f565-124">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="2f565-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-125">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2f565-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f565-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f565-127">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="2f565-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2f565-128">Identifie les instances de **\_ BaseMetricDefinition CIM** qui peuvent être contrôlées par l' **instance \_ MetricService CIM** associée.</span><span class="sxs-lookup"><span data-stu-id="2f565-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="2f565-129">Si cette propriété a la **valeur null**, toutes les mesures peuvent être contrôlées.</span><span class="sxs-lookup"><span data-stu-id="2f565-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="2f565-130">Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2f565-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="2f565-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f565-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-134">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="2f565-134">A description of the object.</span></span> <span data-ttu-id="2f565-135">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « définit les fonctionnalités du service métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="2f565-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="2f565-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2f565-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f565-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-139">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2f565-139">A display name for the object.</span></span> <span data-ttu-id="2f565-140">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités du service métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="2f565-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="2f565-141">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="2f565-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2f565-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-144">Indique si la propriété **ElementName** peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="2f565-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="2f565-145">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2f565-146">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="2f565-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f565-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-149">Spécifie les restrictions sur **ElementName**, exprimées sous la forme d’une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="2f565-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="2f565-150">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2f565-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f565-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2f565-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f565-154">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="2f565-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2f565-155">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2f565-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2f565-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2f565-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f565-157">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="2f565-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-158">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f565-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f565-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f565-160">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="2f565-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2f565-161">Identifie le type de contrôle pris en charge par l’instance **\_ MetricService CIM** associée pour l’objet [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identifié par la valeur dans le même index de tableau dans la propriété **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="2f565-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="2f565-162">Si cette propriété a la **valeur null**, tous les types de contrôle sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="2f565-163">Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="2f565-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f565-164">Value</span></span>                                                                                   | <span data-ttu-id="2f565-165">Signification</span><span class="sxs-lookup"><span data-stu-id="2f565-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2f565-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="2f565-167">Unknown</span><span class="sxs-lookup"><span data-stu-id="2f565-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="2f565-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="2f565-169">Discret</span><span class="sxs-lookup"><span data-stu-id="2f565-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="2f565-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="2f565-171">Bloc</span><span class="sxs-lookup"><span data-stu-id="2f565-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="2f565-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="2f565-173">Les deux</span><span class="sxs-lookup"><span data-stu-id="2f565-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="2f565-174"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="2f565-175">DMTF, réservé</span><span class="sxs-lookup"><span data-stu-id="2f565-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="2f565-176"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="2f565-177">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="2f565-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f565-178">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="2f565-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-179">Type de données : **unit16**</span><span class="sxs-lookup"><span data-stu-id="2f565-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="2f565-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f565-181">Qualificateurs : **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="2f565-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2f565-182">Spécifie la longueur maximale prise en charge de la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2f565-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="2f565-183">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2f565-184">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="2f565-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-185">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f565-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f565-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f565-187">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="2f565-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2f565-188">Identifie le type de contrôle pris en charge par l’instance **\_ MetricService CIM** associée pour le **\_ BaseMetricDefinition CIM** identifié par la valeur dans le même index de tableau dans la propriété **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="2f565-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="2f565-189">Si cette propriété a la **valeur null**, tous les types de contrôle sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="2f565-190">Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="2f565-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f565-191">Value</span></span>                                                                                   | <span data-ttu-id="2f565-192">Signification</span><span class="sxs-lookup"><span data-stu-id="2f565-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2f565-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="2f565-194">Unknown</span><span class="sxs-lookup"><span data-stu-id="2f565-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="2f565-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="2f565-196">Discret</span><span class="sxs-lookup"><span data-stu-id="2f565-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="2f565-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="2f565-198">Bloc</span><span class="sxs-lookup"><span data-stu-id="2f565-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="2f565-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="2f565-200">Les deux</span><span class="sxs-lookup"><span data-stu-id="2f565-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="2f565-201"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="2f565-202">DMTF, réservé</span><span class="sxs-lookup"><span data-stu-id="2f565-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="2f565-203"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="2f565-204">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="2f565-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f565-205">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="2f565-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-206">Type de données : tableau **unit16**</span><span class="sxs-lookup"><span data-stu-id="2f565-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f565-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-208">Indique les États possibles qui peuvent être demandés lors de l’utilisation de la méthode **RequestStateChange** sur l’élément logique activé.</span><span class="sxs-lookup"><span data-stu-id="2f565-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="2f565-209">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="2f565-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f565-210">Value</span></span>                                                                         | <span data-ttu-id="2f565-211">Signification</span><span class="sxs-lookup"><span data-stu-id="2f565-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="2f565-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="2f565-213">activé</span><span class="sxs-lookup"><span data-stu-id="2f565-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="2f565-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="2f565-215">Désactive</span><span class="sxs-lookup"><span data-stu-id="2f565-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="2f565-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="2f565-217">Éteindre</span><span class="sxs-lookup"><span data-stu-id="2f565-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="2f565-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="2f565-219">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="2f565-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="2f565-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="2f565-221">Test</span><span class="sxs-lookup"><span data-stu-id="2f565-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="2f565-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="2f565-223">Fenêtres</span><span class="sxs-lookup"><span data-stu-id="2f565-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="2f565-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="2f565-225">Mettre en suspens</span><span class="sxs-lookup"><span data-stu-id="2f565-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="2f565-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="2f565-227">Reboot</span><span class="sxs-lookup"><span data-stu-id="2f565-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="2f565-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="2f565-229">Réinitialiser</span><span class="sxs-lookup"><span data-stu-id="2f565-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="2f565-230">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="2f565-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f565-231">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f565-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f565-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f565-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f565-233">Spécifie les méthodes prises en charge par le service métrique.</span><span class="sxs-lookup"><span data-stu-id="2f565-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="2f565-234">Cette propriété est héritée de la **\_ MetricServiceCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2f565-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="2f565-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f565-235">Value</span></span>                                                                                   | <span data-ttu-id="2f565-236">Signification</span><span class="sxs-lookup"><span data-stu-id="2f565-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f565-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="2f565-238">La méthode [**ControlMetrics**](controlmetrics-msvm-metricservice.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="2f565-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="2f565-240">La méthode **ControlMetricsByClass** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2f565-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="2f565-242">La méthode **ShowMetrics** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="2f565-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="2f565-244">La méthode **ShowMetricsByClass** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2f565-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="2f565-246">La méthode **GetMetricValues** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="2f565-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="2f565-248">La méthode **ControlSampleTimes** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2f565-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2f565-249"><dt>8.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="2f565-250">DMTF, réservé</span><span class="sxs-lookup"><span data-stu-id="2f565-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="2f565-251"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="2f565-252">Spécifique au fournisseur</span><span class="sxs-lookup"><span data-stu-id="2f565-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f565-253">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f565-253">Requirements</span></span>



| <span data-ttu-id="2f565-254">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f565-254">Requirement</span></span> | <span data-ttu-id="2f565-255">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f565-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f565-256">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f565-256">Minimum supported client</span></span><br/> | <span data-ttu-id="2f565-257">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f565-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f565-258">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f565-258">Minimum supported server</span></span><br/> | <span data-ttu-id="2f565-259">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f565-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f565-260">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2f565-260">Namespace</span></span><br/>                | <span data-ttu-id="2f565-261">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f565-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f565-262">MOF</span><span class="sxs-lookup"><span data-stu-id="2f565-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f565-263"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f565-264">DLL</span><span class="sxs-lookup"><span data-stu-id="2f565-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f565-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f565-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f565-266">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f565-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f565-267">**\_METRICSERVICECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="2f565-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="2f565-268">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="2f565-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

