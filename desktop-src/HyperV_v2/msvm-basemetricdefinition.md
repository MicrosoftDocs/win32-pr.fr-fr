---
description: Représente les aspects de définition d’une mesure.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Classe Msvm_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524725"
---
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="c8a90-103">MSVM \_ BaseMetricDefinition, classe</span><span class="sxs-lookup"><span data-stu-id="c8a90-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="c8a90-104">Représente les aspects de définition d’une mesure.</span><span class="sxs-lookup"><span data-stu-id="c8a90-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="c8a90-105">La classe **MSVM \_ BaseMetricDefinition** doit être associée à la [**\_ ManagedElements CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) à laquelle elle s’applique.</span><span class="sxs-lookup"><span data-stu-id="c8a90-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="c8a90-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c8a90-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a90-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8a90-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
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
};
```

## <a name="members"></a><span data-ttu-id="c8a90-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c8a90-108">Members</span></span>

<span data-ttu-id="c8a90-109">La classe **MSVM \_ BaseMetricDefinition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8a90-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="c8a90-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8a90-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8a90-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8a90-111">Properties</span></span>

<span data-ttu-id="c8a90-112">La classe **MSVM \_ BaseMetricDefinition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8a90-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8a90-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="c8a90-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c8a90-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-116">Définit une ou plusieurs chaînes qui peuvent être utilisées pour affiner (décomposer) des requêtes sur les valeurs de métrique le long d’une certaine dimension.</span><span class="sxs-lookup"><span data-stu-id="c8a90-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="c8a90-117">Par exemple, un nom de transaction, qui permet de décomposer la valeur totale de toutes les transactions en un ensemble de valeurs, une pour chaque nom de transaction.</span><span class="sxs-lookup"><span data-stu-id="c8a90-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="c8a90-118">Il peut s’agir, par exemple, d’un nom de système d’application ou de groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c8a90-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="c8a90-119">Les chaînes sont au format libre et doivent être significatives pour les utilisateurs finaux des données de métriques.</span><span class="sxs-lookup"><span data-stu-id="c8a90-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="c8a90-120">Les chaînes indiquent les dimensions de rupture prises en charge pour cette définition de métrique, par l’instrumentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="c8a90-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="c8a90-121">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-122">**Calculable**</span><span class="sxs-lookup"><span data-stu-id="c8a90-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8a90-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-125">Décrit les caractéristiques de la mesure dans le cadre de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="c8a90-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="c8a90-126">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="c8a90-127">Il peut s’agir de la **valeur null** ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8a90-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="c8a90-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8a90-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="c8a90-129">Signification</span><span class="sxs-lookup"><span data-stu-id="c8a90-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="c8a90-130"><dt>**Non calculable**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c8a90-131">La valeur ne peut pas être calculée.</span><span class="sxs-lookup"><span data-stu-id="c8a90-131">The value cannot be calculated.</span></span> <span data-ttu-id="c8a90-132">Par exemple, une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c8a90-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="c8a90-133"><dt>**Summable**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="c8a90-134">La valeur peut être additionnée sur de nombreuses instances.</span><span class="sxs-lookup"><span data-stu-id="c8a90-134">The value can be summed over many instances.</span></span> <span data-ttu-id="c8a90-135">Par exemple, si chaque travail de sauvegarde est une unité de travail et que chaque travail sauvegarde 27 000 fichiers en moyenne, 100 travaux de sauvegarde ont traité 2,7 millions fichiers.</span><span class="sxs-lookup"><span data-stu-id="c8a90-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="c8a90-136"><dt> **Non-summable**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="c8a90-137">Cette valeur ne peut pas être additionnée sur de nombreuses instances.</span><span class="sxs-lookup"><span data-stu-id="c8a90-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="c8a90-138">C’est le cas, par exemple, d’une mesure qui mesure la longueur de la file d’attente lorsqu’un travail arrive sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="c8a90-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="c8a90-139">Si chaque travail est une unité de travail et que la longueur moyenne de la file d’attente lorsque chaque travail arrive est 33, il n’est pas judicieux de préciser que la longueur de la file d’attente pour les travaux 100 est 3300.</span><span class="sxs-lookup"><span data-stu-id="c8a90-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="c8a90-140">Il est logique de dire que la moyenne est de 33.</span><span class="sxs-lookup"><span data-stu-id="c8a90-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8a90-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c8a90-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-144">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c8a90-144">A short description of the object.</span></span> <span data-ttu-id="c8a90-145">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8a90-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="c8a90-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8a90-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-149">Indique comment la valeur de la métrique change, sous la forme de combinaisons typiques d’attributs de grain plus fins tels que le changement de direction, les valeurs minimales et maximales et la sémantique d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="c8a90-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="c8a90-150">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="c8a90-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8a90-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="c8a90-152">Signification</span><span class="sxs-lookup"><span data-stu-id="c8a90-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c8a90-153"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="c8a90-154">Le concepteur de mesures n’a pas qualifié le **ChangeType.**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="c8a90-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="c8a90-156">Si la propriété **IsContinuous** est définie sur « false », **ChangeType** n’a pas de sens et doit avoir la valeur « N/A ».</span><span class="sxs-lookup"><span data-stu-id="c8a90-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="c8a90-157"><dt>**Compteur**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="c8a90-158">La métrique est une mesure de compteur.</span><span class="sxs-lookup"><span data-stu-id="c8a90-158">The metric is a counter metric.</span></span> <span data-ttu-id="c8a90-159">Ils ont des valeurs entières non négatives qui augmentent jusqu’à atteindre le nombre maximal pouvant être représenté, puis encapsulent et commencent à augmenter de 0.</span><span class="sxs-lookup"><span data-stu-id="c8a90-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="c8a90-160"><dt>**Jauge**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="c8a90-161">La métrique est une mesure de jauge.</span><span class="sxs-lookup"><span data-stu-id="c8a90-161">The metric is a gauge metric.</span></span> <span data-ttu-id="c8a90-162">Celles-ci ont des valeurs entières ou float qui peuvent augmenter et diminuer de façon arbitraire.</span><span class="sxs-lookup"><span data-stu-id="c8a90-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c8a90-163"><dt>**DMTF réservé**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="c8a90-164"><dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="c8a90-165">Les fournisseurs peuvent étendre la propriété **ChangeType** dans la plage réservée du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c8a90-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="c8a90-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="c8a90-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8a90-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-169">Type de données de la mesure.</span><span class="sxs-lookup"><span data-stu-id="c8a90-169">The data type of the metric.</span></span> <span data-ttu-id="c8a90-170">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="c8a90-171"><span id="boolean"></span><span id="BOOLEAN"></span>**booléen** (1)</span><span class="sxs-lookup"><span data-stu-id="c8a90-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="c8a90-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="c8a90-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="c8a90-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="c8a90-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="c8a90-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="c8a90-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="c8a90-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="c8a90-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-180"><span id="string"></span><span id="STRING"></span>**chaîne** (10)</span><span class="sxs-lookup"><span data-stu-id="c8a90-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="c8a90-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="c8a90-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="c8a90-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-184"><span id="uint8_"></span><span id="UINT8_"></span>**UInt8** (14)</span><span class="sxs-lookup"><span data-stu-id="c8a90-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8a90-185">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8a90-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-188">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="c8a90-188">A description of the object.</span></span> <span data-ttu-id="c8a90-189">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8a90-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c8a90-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-193">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c8a90-193">A display name for the object.</span></span> <span data-ttu-id="c8a90-194">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8a90-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="c8a90-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8a90-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-198">Indique comment les valeurs de métriques sont collectées par l’instrumentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="c8a90-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="c8a90-199">Cela permet à l’application cliente de choisir la mesure appropriée à cet effet.</span><span class="sxs-lookup"><span data-stu-id="c8a90-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="c8a90-200">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="c8a90-201">Il peut s’agir de la **valeur null** ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8a90-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="c8a90-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8a90-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="c8a90-203">Signification</span><span class="sxs-lookup"><span data-stu-id="c8a90-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c8a90-204"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="c8a90-205">Le type de regroupement n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="c8a90-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="c8a90-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="c8a90-207">Les valeurs de métriques sont mises à jour immédiatement lorsque les valeurs à l’intérieur de la ressource mesurée changent.</span><span class="sxs-lookup"><span data-stu-id="c8a90-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="c8a90-208"><dt>**Périodique**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c8a90-209">Les valeurs de mesure sont mises à jour régulièrement.</span><span class="sxs-lookup"><span data-stu-id="c8a90-209">The metric values get updated periodically.</span></span> <span data-ttu-id="c8a90-210">Par exemple, pour une application cliente, une valeur métrique qui s’applique à l’heure actuelle apparaîtra constante pendant chaque intervalle de collecte, puis passera à la nouvelle valeur à la fin de chaque intervalle de collecte.</span><span class="sxs-lookup"><span data-stu-id="c8a90-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="c8a90-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="c8a90-212">La valeur de la métrique est déterminée chaque fois qu’une application cliente la lit.</span><span class="sxs-lookup"><span data-stu-id="c8a90-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c8a90-213"><dt>**DMTF réservé**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="c8a90-214"><dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="c8a90-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="c8a90-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-218">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="c8a90-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-219">Chaîne qui identifie de façon unique la définition de la métrique.</span><span class="sxs-lookup"><span data-stu-id="c8a90-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="c8a90-220">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c8a90-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-224">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="c8a90-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-225">Chaîne qui identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c8a90-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c8a90-226">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8a90-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="c8a90-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-228">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c8a90-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-230">Indique si la valeur de la métrique est continue ou scalaire.</span><span class="sxs-lookup"><span data-stu-id="c8a90-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="c8a90-231">Les mesures de performances sont un exemple de mesure continue.</span><span class="sxs-lookup"><span data-stu-id="c8a90-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="c8a90-232">Les codes d’erreur ou les États opérationnels sont des exemples de métriques scalaires.</span><span class="sxs-lookup"><span data-stu-id="c8a90-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="c8a90-233">Les métriques continues peuvent être comparées à l’aide de la relation « supérieur à ».</span><span class="sxs-lookup"><span data-stu-id="c8a90-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="c8a90-234">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-235">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c8a90-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-238">Nom de la mesure.</span><span class="sxs-lookup"><span data-stu-id="c8a90-238">The name of the metric.</span></span> <span data-ttu-id="c8a90-239">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="c8a90-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-243">Identifie les unités spécifiques d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="c8a90-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="c8a90-244">La valeur de cette propriété est une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c8a90-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="c8a90-245">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="c8a90-246">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="c8a90-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-247">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8a90-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-249">Indique l’étendue de temps à laquelle la valeur de mesure s’applique.</span><span class="sxs-lookup"><span data-stu-id="c8a90-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="c8a90-250">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="c8a90-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8a90-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="c8a90-252">Signification</span><span class="sxs-lookup"><span data-stu-id="c8a90-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c8a90-253"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="c8a90-254">La portée de l’heure n’a pas été qualifiée par le concepteur de mesures ou est inconnue du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c8a90-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="c8a90-255"><dt>**Point**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="c8a90-256">La mesure s’applique à un point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="c8a90-256">The metric applies to a point in time.</span></span> <span data-ttu-id="c8a90-257">Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie le point dans le temps, et la propriété **Duration** est toujours égale à 0.</span><span class="sxs-lookup"><span data-stu-id="c8a90-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="c8a90-258"><dt>**Intervalle**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c8a90-259">La mesure s’applique à un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="c8a90-259">The metric applies to a time interval.</span></span> <span data-ttu-id="c8a90-260">Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie la fin de l’intervalle de temps et la propriété **Duration** spécifie sa durée.</span><span class="sxs-lookup"><span data-stu-id="c8a90-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="c8a90-261"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="c8a90-262">La mesure s’applique à un intervalle de temps qui a commencé au démarrage de la ressource mesurée (autrement dit, le propriété ManagedElement associé à MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="c8a90-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="c8a90-263">Sur les instances [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondantes, la propriété **timestamp** spécifie la fin de l’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="c8a90-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="c8a90-264">Si la propriété **Duration** est égale à 0, cela indique que le temps de démarrage de la ressource mesurée est inconnu.</span><span class="sxs-lookup"><span data-stu-id="c8a90-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="c8a90-265">Dans le cas contraire, **Duration** spécifie la durée entre le démarrage de la ressource et l' **horodateur**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c8a90-266"><dt>**DMTF réservé**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="c8a90-267"><dt> **Fournisseur réservé**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="c8a90-268">**Unités**</span><span class="sxs-lookup"><span data-stu-id="c8a90-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8a90-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8a90-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8a90-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8a90-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8a90-271">Identifie les unités spécifiques d’une valeur, par exemple, « mégaoctets ».</span><span class="sxs-lookup"><span data-stu-id="c8a90-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="c8a90-272">Cette propriété est héritée de la **\_ BaseMetricDefinition CIM**.</span><span class="sxs-lookup"><span data-stu-id="c8a90-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8a90-273">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8a90-273">Requirements</span></span>



| <span data-ttu-id="c8a90-274">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8a90-274">Requirement</span></span> | <span data-ttu-id="c8a90-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8a90-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a90-276">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8a90-276">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a90-277">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8a90-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8a90-278">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8a90-278">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a90-279">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8a90-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8a90-280">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8a90-280">Namespace</span></span><br/>                | <span data-ttu-id="c8a90-281">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c8a90-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8a90-282">MOF</span><span class="sxs-lookup"><span data-stu-id="c8a90-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8a90-283"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8a90-284">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a90-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8a90-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8a90-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

