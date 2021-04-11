---
description: Représente les aspects de définition d’une mesure dérivée d’une autre valeur de mesure.
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Classe Msvm_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da52c154c90b58fc147a52268025887d2dfa8f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204021"
---
# <a name="msvm_aggregationmetricdefinition-class"></a><span data-ttu-id="e67d4-103">MSVM \_ AggregationMetricDefinition, classe</span><span class="sxs-lookup"><span data-stu-id="e67d4-103">Msvm\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="e67d4-104">Représente les aspects de définition d’une mesure dérivée d’une autre valeur de mesure.</span><span class="sxs-lookup"><span data-stu-id="e67d4-104">Represents the definition aspects of a metric that is derived from another metric value.</span></span> <span data-ttu-id="e67d4-105">L’objet **MSVM \_ AggregationMetricDefinition** doit être associé aux éléments managés auxquels il s’applique.</span><span class="sxs-lookup"><span data-stu-id="e67d4-105">The **Msvm\_AggregationMetricDefinition** object should be associated with the managed elements to which it applies.</span></span>

<span data-ttu-id="e67d4-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e67d4-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e67d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e67d4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
  uint16  SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="e67d4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e67d4-108">Members</span></span>

<span data-ttu-id="e67d4-109">La classe **MSVM \_ AggregationMetricDefinition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e67d4-109">The **Msvm\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="e67d4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e67d4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e67d4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e67d4-111">Properties</span></span>

<span data-ttu-id="e67d4-112">La classe **MSVM \_ AggregationMetricDefinition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e67d4-112">The **Msvm\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e67d4-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="e67d4-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e67d4-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-116">Définit une ou plusieurs chaînes qui peuvent être utilisées pour affiner (décomposer) des requêtes sur les valeurs de métrique le long d’une certaine dimension.</span><span class="sxs-lookup"><span data-stu-id="e67d4-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="e67d4-117">Par exemple, un nom de transaction, qui permet de décomposer la valeur totale de toutes les transactions en un ensemble de valeurs, une pour chaque nom de transaction.</span><span class="sxs-lookup"><span data-stu-id="e67d4-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="e67d4-118">Il peut s’agir, par exemple, d’un nom de système d’application ou de groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e67d4-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="e67d4-119">Les chaînes sont au format libre et doivent être significatives pour les utilisateurs finaux des données de métriques.</span><span class="sxs-lookup"><span data-stu-id="e67d4-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="e67d4-120">Les chaînes indiquent les dimensions de rupture prises en charge pour cette définition de métrique par l’instrumentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e67d4-120">The strings indicate which break down dimensions are supported for this metric definition by the underlying instrumentation.</span></span> <span data-ttu-id="e67d4-121">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-122">**Calculable**</span><span class="sxs-lookup"><span data-stu-id="e67d4-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67d4-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-125">Décrit les caractéristiques de la mesure dans le cadre de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="e67d4-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="e67d4-126">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="e67d4-127">Il peut s’agir de la **valeur null** ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e67d4-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="e67d4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67d4-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="e67d4-129">Signification</span><span class="sxs-lookup"><span data-stu-id="e67d4-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="e67d4-130"><dt>**Non calculable**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e67d4-131">La valeur ne peut pas être calculée.</span><span class="sxs-lookup"><span data-stu-id="e67d4-131">The value cannot be calculated.</span></span> <span data-ttu-id="e67d4-132">Par exemple, une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e67d4-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="e67d4-133"><dt>**Summable**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="e67d4-134">La valeur peut être additionnée sur de nombreuses instances.</span><span class="sxs-lookup"><span data-stu-id="e67d4-134">The value can be summed over many instances.</span></span> <span data-ttu-id="e67d4-135">Par exemple, si chaque travail de sauvegarde est une unité de travail et que chaque travail sauvegarde 27 000 fichiers en moyenne, 100 travaux de sauvegarde ont traité 2,7 millions fichiers.</span><span class="sxs-lookup"><span data-stu-id="e67d4-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="e67d4-136"><dt> **Non-summable**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="e67d4-137">Cette valeur ne peut pas être additionnée sur de nombreuses instances.</span><span class="sxs-lookup"><span data-stu-id="e67d4-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="e67d4-138">C’est le cas, par exemple, d’une mesure qui mesure la longueur de la file d’attente lorsqu’un travail arrive sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="e67d4-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="e67d4-139">Si chaque travail est une unité de travail et que la longueur moyenne de la file d’attente lorsque chaque travail arrive est 33, il n’est pas judicieux de préciser que la longueur de la file d’attente pour les travaux 100 est 3300.</span><span class="sxs-lookup"><span data-stu-id="e67d4-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="e67d4-140">Il est logique de dire que la moyenne est de 33.</span><span class="sxs-lookup"><span data-stu-id="e67d4-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e67d4-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e67d4-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-144">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e67d4-144">A short description of the object.</span></span> <span data-ttu-id="e67d4-145">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e67d4-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="e67d4-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67d4-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-149">Indique comment la valeur de la métrique change, sous la forme de combinaisons typiques d’attributs de grain plus fins tels que le changement de direction, les valeurs minimales et maximales et la sémantique d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="e67d4-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="e67d4-150">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="e67d4-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67d4-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e67d4-152">Signification</span><span class="sxs-lookup"><span data-stu-id="e67d4-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e67d4-153"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e67d4-154">Le concepteur de mesures n’a pas qualifié le **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-154">The metric designer did not qualify the **ChangeType**.</span></span><br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="e67d4-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="e67d4-156">Si la propriété **IsContinuous** est définie sur « false », **ChangeType** n’a pas de sens et doit avoir la valeur « N/A ».</span><span class="sxs-lookup"><span data-stu-id="e67d4-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="e67d4-157"><dt>**Compteur**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="e67d4-158">La métrique est une mesure de compteur.</span><span class="sxs-lookup"><span data-stu-id="e67d4-158">The metric is a counter metric.</span></span> <span data-ttu-id="e67d4-159">Ils ont des valeurs entières non négatives qui augmentent jusqu’à atteindre le nombre maximal pouvant être représenté, puis encapsulent et commencent à augmenter de 0.</span><span class="sxs-lookup"><span data-stu-id="e67d4-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="e67d4-160"><dt>**Jauge**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="e67d4-161">La métrique est une mesure de jauge.</span><span class="sxs-lookup"><span data-stu-id="e67d4-161">The metric is a gauge metric.</span></span> <span data-ttu-id="e67d4-162">Celles-ci ont des valeurs entières ou float qui peuvent augmenter et diminuer de façon arbitraire.</span><span class="sxs-lookup"><span data-stu-id="e67d4-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e67d4-163"><dt>**DMTF réservé**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e67d4-164"><dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="e67d4-165">Les fournisseurs peuvent étendre la propriété **ChangeType** dans la plage réservée du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e67d4-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e67d4-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="e67d4-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67d4-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-169">Type de données de la mesure.</span><span class="sxs-lookup"><span data-stu-id="e67d4-169">The data type of the metric.</span></span> <span data-ttu-id="e67d4-170">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="e67d4-171"><span id="boolean"></span><span id="BOOLEAN"></span>**booléen** (1)</span><span class="sxs-lookup"><span data-stu-id="e67d4-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="e67d4-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="e67d4-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="e67d4-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="e67d4-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="e67d4-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="e67d4-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="e67d4-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="e67d4-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-180"><span id="string"></span><span id="STRING"></span>**chaîne** (10)</span><span class="sxs-lookup"><span data-stu-id="e67d4-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="e67d4-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="e67d4-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="e67d4-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-184"><span id="uint8_"></span><span id="UINT8_"></span>**UInt8** (14)</span><span class="sxs-lookup"><span data-stu-id="e67d4-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e67d4-185">**Description**</span><span class="sxs-lookup"><span data-stu-id="e67d4-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-188">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="e67d4-188">A description of the object.</span></span> <span data-ttu-id="e67d4-189">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e67d4-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e67d4-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-193">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e67d4-193">A display name for the object.</span></span> <span data-ttu-id="e67d4-194">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e67d4-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="e67d4-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67d4-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-198">Indique comment les valeurs de métriques sont collectées par l’instrumentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e67d4-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="e67d4-199">Cela permet à l’application cliente de choisir la mesure appropriée à cet effet.</span><span class="sxs-lookup"><span data-stu-id="e67d4-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="e67d4-200">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="e67d4-201">Il peut s’agir de la **valeur null** ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e67d4-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="e67d4-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67d4-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e67d4-203">Signification</span><span class="sxs-lookup"><span data-stu-id="e67d4-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e67d4-204"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e67d4-205">Le type de regroupement n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="e67d4-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="e67d4-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="e67d4-207">Les valeurs de métriques sont mises à jour immédiatement lorsque les valeurs à l’intérieur de la ressource mesurée changent.</span><span class="sxs-lookup"><span data-stu-id="e67d4-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="e67d4-208"><dt>**Périodique**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e67d4-209">Les valeurs de mesure sont mises à jour régulièrement.</span><span class="sxs-lookup"><span data-stu-id="e67d4-209">The metric values get updated periodically.</span></span> <span data-ttu-id="e67d4-210">Par exemple, pour une application cliente, une valeur métrique qui s’applique à l’heure actuelle apparaîtra constante pendant chaque intervalle de collecte, puis passera à la nouvelle valeur à la fin de chaque intervalle de collecte.</span><span class="sxs-lookup"><span data-stu-id="e67d4-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="e67d4-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="e67d4-212">La valeur de la métrique est déterminée chaque fois qu’une application cliente la lit.</span><span class="sxs-lookup"><span data-stu-id="e67d4-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e67d4-213"><dt>**DMTF réservé**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e67d4-214"><dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="e67d4-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="e67d4-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-218">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="e67d4-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-219">Chaîne qui identifie de façon unique la définition de la métrique.</span><span class="sxs-lookup"><span data-stu-id="e67d4-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="e67d4-220">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e67d4-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-224">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="e67d4-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-225">Chaîne qui identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e67d4-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e67d4-226">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e67d4-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="e67d4-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-228">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67d4-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-230">Indique si la valeur de la métrique est continue ou scalaire.</span><span class="sxs-lookup"><span data-stu-id="e67d4-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="e67d4-231">Les mesures de performances sont un exemple de mesure continue.</span><span class="sxs-lookup"><span data-stu-id="e67d4-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="e67d4-232">Les codes d’erreur ou les États opérationnels sont des exemples de métriques scalaires.</span><span class="sxs-lookup"><span data-stu-id="e67d4-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="e67d4-233">Les métriques continues peuvent être comparées à l’aide de la relation « supérieur à ».</span><span class="sxs-lookup"><span data-stu-id="e67d4-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="e67d4-234">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-235">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e67d4-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-238">Nom de la mesure.</span><span class="sxs-lookup"><span data-stu-id="e67d4-238">The name of the metric.</span></span> <span data-ttu-id="e67d4-239">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="e67d4-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-243">Identifie les unités spécifiques d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="e67d4-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="e67d4-244">La valeur de cette propriété est une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e67d4-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="e67d4-245">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e67d4-246">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="e67d4-246">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-247">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67d4-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-248">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e67d4-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-249">Identifie le calcul de base effectué sur une mesure sous-jacente pour arriver à la valeur de cette mesure dérivée.</span><span class="sxs-lookup"><span data-stu-id="e67d4-249">Identifies the basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="e67d4-250">Cette propriété est héritée de **CIM \_ AggregationMetricDefinition** et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e67d4-250">This property is inherited from **CIM\_AggregationMetricDefinition** and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e67d4-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span><span class="sxs-lookup"><span data-stu-id="e67d4-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="e67d4-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Moyenne** (4)</span><span class="sxs-lookup"><span data-stu-id="e67d4-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Médiane** (5)</span><span class="sxs-lookup"><span data-stu-id="e67d4-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span><span class="sxs-lookup"><span data-stu-id="e67d4-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e67d4-256">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="e67d4-256">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67d4-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-259">Indique l’étendue de temps à laquelle la valeur de mesure s’applique.</span><span class="sxs-lookup"><span data-stu-id="e67d4-259">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="e67d4-260">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-260">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="e67d4-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67d4-261">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e67d4-262">Signification</span><span class="sxs-lookup"><span data-stu-id="e67d4-262">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e67d4-263"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-263"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e67d4-264">La portée de l’heure n’a pas été qualifiée par le concepteur de mesures ou est inconnue du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e67d4-264">The time scope was not qualified by the metric designer, or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="e67d4-265"><dt>**Point**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-265"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="e67d4-266">La mesure s’applique à un point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="e67d4-266">The metric applies to a point in time.</span></span> <span data-ttu-id="e67d4-267">Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie le point dans le temps, et la propriété **Duration** est toujours égale à 0.</span><span class="sxs-lookup"><span data-stu-id="e67d4-267">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="e67d4-268"><dt>**Intervalle**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-268"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e67d4-269">La mesure s’applique à un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="e67d4-269">The metric applies to a time interval.</span></span> <span data-ttu-id="e67d4-270">Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie la fin de l’intervalle de temps et la propriété **Duration** spécifie sa durée.</span><span class="sxs-lookup"><span data-stu-id="e67d4-270">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="e67d4-271"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-271"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="e67d4-272">La mesure s’applique à un intervalle de temps qui a commencé au démarrage de la ressource mesurée (autrement dit, le propriété ManagedElement associé à MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="e67d4-272">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="e67d4-273">Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie la fin de l’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="e67d4-273">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="e67d4-274">Si la propriété **Duration** est égale à 0, cela indique que le temps de démarrage de la ressource mesurée est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e67d4-274">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="e67d4-275">Dans le cas contraire, **Duration** spécifie la durée entre le démarrage de la ressource et l' **horodateur**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-275">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e67d4-276"><dt>**DMTF réservé**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-276"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e67d4-277"><dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-277"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="e67d4-278">**Unités**</span><span class="sxs-lookup"><span data-stu-id="e67d4-278">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67d4-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67d4-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67d4-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67d4-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67d4-281">Identifie les unités d’une valeur, par exemple, « mégaoctets ».</span><span class="sxs-lookup"><span data-stu-id="e67d4-281">Identifies the units of a value, for example, "megabytes".</span></span> <span data-ttu-id="e67d4-282">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="e67d4-282">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e67d4-283">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e67d4-283">Requirements</span></span>



| <span data-ttu-id="e67d4-284">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e67d4-284">Requirement</span></span> | <span data-ttu-id="e67d4-285">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67d4-285">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e67d4-286">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67d4-286">Minimum supported client</span></span><br/> | <span data-ttu-id="e67d4-287">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e67d4-287">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e67d4-288">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67d4-288">Minimum supported server</span></span><br/> | <span data-ttu-id="e67d4-289">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e67d4-289">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e67d4-290">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e67d4-290">Namespace</span></span><br/>                | <span data-ttu-id="e67d4-291">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e67d4-291">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e67d4-292">MOF</span><span class="sxs-lookup"><span data-stu-id="e67d4-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e67d4-293"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-293"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e67d4-294">DLL</span><span class="sxs-lookup"><span data-stu-id="e67d4-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e67d4-295"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e67d4-295"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

