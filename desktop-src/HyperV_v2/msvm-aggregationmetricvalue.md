---
description: Représente la valeur d’instance d’une mesure définie par une instance de la \_ classe MSVM AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Classe Msvm_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034961"
---
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="65fcd-103">MSVM \_ AggregationMetricValue, classe</span><span class="sxs-lookup"><span data-stu-id="65fcd-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="65fcd-104">Représente la valeur d’instance d’une mesure définie par une instance de la classe [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="65fcd-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="65fcd-105">Les propriétés héritées de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) fournissent la valeur de métrique réelle.</span><span class="sxs-lookup"><span data-stu-id="65fcd-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="65fcd-106">Les propriétés définies par cette classe fournissent des informations sur l’intervalle auquel la fonction d’agrégation a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="65fcd-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="65fcd-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="65fcd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fcd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65fcd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="65fcd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="65fcd-109">Members</span></span>

<span data-ttu-id="65fcd-110">La classe **MSVM \_ AggregationMetricValue** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="65fcd-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="65fcd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65fcd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65fcd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65fcd-112">Properties</span></span>

<span data-ttu-id="65fcd-113">La classe **MSVM \_ AggregationMetricValue** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="65fcd-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65fcd-114">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="65fcd-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-115">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65fcd-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-117">Représente la durée pendant laquelle l’agrégation a été calculée.</span><span class="sxs-lookup"><span data-stu-id="65fcd-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="65fcd-118">Le début d’un intervalle d’analyse sur lequel la fonction d’agrégation est appliquée est déterminé par la soustraction des **AggregationDuration** du **AggregationTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="65fcd-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="65fcd-119">Cette propriété est héritée de la **\_ AggregationMetricValue CIM**.</span><span class="sxs-lookup"><span data-stu-id="65fcd-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-120">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="65fcd-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-121">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65fcd-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-123">Identifie l’heure à laquelle la fonction d’agrégation a été appliquée pour déterminer la valeur de l’instance de métrique.</span><span class="sxs-lookup"><span data-stu-id="65fcd-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="65fcd-124">Ce n’est pas le même que l’heure de création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="65fcd-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="65fcd-125">Pour une instance **\_ AggregationMetricValue CIM** donnée, **AggregationTimeStamp** change chaque fois que la fonction d’agrégation est appliquée pour calculer la valeur.</span><span class="sxs-lookup"><span data-stu-id="65fcd-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="65fcd-126">Cette propriété est héritée de la **\_ AggregationMetricValue CIM**.</span><span class="sxs-lookup"><span data-stu-id="65fcd-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-127">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="65fcd-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-130">Spécifie une dimension de répartition à partir du tableau **BreakdownDimensions** défini dans le [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)associé.</span><span class="sxs-lookup"><span data-stu-id="65fcd-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="65fcd-131">Il s’agit de la dimension selon laquelle cet ensemble de valeurs de métriques est divisé.</span><span class="sxs-lookup"><span data-stu-id="65fcd-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="65fcd-132">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-133">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="65fcd-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-136">Définit une valeur de la propriété **BreakdownDimension** définie pour cette instance de la valeur métrique.</span><span class="sxs-lookup"><span data-stu-id="65fcd-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="65fcd-137">Par exemple, si **BreakdownDimension** est « TransactionName », cette propriété peut nommer la transaction réelle à laquelle s’applique cette valeur de mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="65fcd-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="65fcd-138">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="65fcd-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-142">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65fcd-142">A short description of the object.</span></span> <span data-ttu-id="65fcd-143">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="65fcd-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-147">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="65fcd-147">A description of the object.</span></span> <span data-ttu-id="65fcd-148">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-149">**Durée**</span><span class="sxs-lookup"><span data-stu-id="65fcd-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-150">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65fcd-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-152">Spécifie la durée pendant laquelle cette valeur métrique est valide.</span><span class="sxs-lookup"><span data-stu-id="65fcd-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="65fcd-153">Cette propriété ne doit pas exister pour les horodatages qui s’appliquent uniquement à un point dans le temps, mais doivent être spécifiées pour les valeurs considérées comme valides pour une certaine période (par exemple, échantillonnage).</span><span class="sxs-lookup"><span data-stu-id="65fcd-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="65fcd-154">Si la propriété **Duration** existe et que n’a pas la **valeur null**, la propriété **timestamp** spécifie la fin de l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="65fcd-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="65fcd-155">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="65fcd-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-159">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65fcd-159">A display name for the object.</span></span> <span data-ttu-id="65fcd-160">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="65fcd-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-164">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="65fcd-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-165">Chaîne qui identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="65fcd-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="65fcd-166">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-167">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="65fcd-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-170">Nom descriptif de l’élément auquel la valeur de la métrique appartient (l’élément mesuré).</span><span class="sxs-lookup"><span data-stu-id="65fcd-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="65fcd-171">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-172">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="65fcd-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-175">Clé de l’instance [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="65fcd-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="65fcd-176">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-177">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="65fcd-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="65fcd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-180">Valeur de la métrique représentée sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="65fcd-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="65fcd-181">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-182">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="65fcd-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-183">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65fcd-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-185">Spécifie l’heure à laquelle la valeur de mesure a été capturée ou calculée.</span><span class="sxs-lookup"><span data-stu-id="65fcd-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="65fcd-186">Sachez que cela diffère de l’heure de création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="65fcd-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="65fcd-187">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fcd-188">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="65fcd-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fcd-189">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="65fcd-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65fcd-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65fcd-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fcd-191">**True** si la valeur du point suivant dans le temps utilise la même instance de classe et modifie simplement les valeurs de propriété (telles que la **valeur** ou l' **horodateur**).</span><span class="sxs-lookup"><span data-stu-id="65fcd-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="65fcd-192">Si la **valeur est true**, l’instance est réutilisée.</span><span class="sxs-lookup"><span data-stu-id="65fcd-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="65fcd-193">Si la **valeur est false**, les instances existantes restent inchangées et une nouvelle instance est créée pour le nouveau point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="65fcd-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="65fcd-194">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fcd-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65fcd-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65fcd-195">Requirements</span></span>



| <span data-ttu-id="65fcd-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65fcd-196">Requirement</span></span> | <span data-ttu-id="65fcd-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="65fcd-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65fcd-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65fcd-198">Minimum supported client</span></span><br/> | <span data-ttu-id="65fcd-199">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65fcd-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="65fcd-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65fcd-200">Minimum supported server</span></span><br/> | <span data-ttu-id="65fcd-201">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65fcd-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65fcd-202">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65fcd-202">Namespace</span></span><br/>                | <span data-ttu-id="65fcd-203">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="65fcd-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="65fcd-204">MOF</span><span class="sxs-lookup"><span data-stu-id="65fcd-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65fcd-205"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65fcd-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65fcd-206">DLL</span><span class="sxs-lookup"><span data-stu-id="65fcd-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65fcd-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65fcd-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

