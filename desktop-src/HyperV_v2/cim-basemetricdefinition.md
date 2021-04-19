---
description: Représente une définition de métrique qui contient les métadonnées d’un \_ objet CIM MetricInstance.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Classe CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529484"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="e106c-103">\_Classe CIM BaseMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="e106c-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="e106c-104">Représente une définition de métrique qui contient les métadonnées d’un objet **CIM \_ MetricInstance** .</span><span class="sxs-lookup"><span data-stu-id="e106c-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e106c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e106c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

## <a name="members"></a><span data-ttu-id="e106c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e106c-106">Members</span></span>

<span data-ttu-id="e106c-107">La classe **CIM \_ BaseMetricDefinition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e106c-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="e106c-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e106c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e106c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e106c-109">Properties</span></span>

<span data-ttu-id="e106c-110">La classe **CIM \_ BaseMetricDefinition** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e106c-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e106c-111">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="e106c-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-112">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e106c-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e106c-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-114">Tableau qui contient des chaînes de format libre qui peuvent être utilisées pour décomposer des requêtes d’objets [**\_ BaseMetricValue CIM**](cim-basemetricvalue.md) le long d’une certaine dimension.</span><span class="sxs-lookup"><span data-stu-id="e106c-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="e106c-115">Les chaînes doivent être significatives pour les utilisateurs finaux des données de métriques.</span><span class="sxs-lookup"><span data-stu-id="e106c-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="e106c-116">En outre, les chaînes doivent indiquer les dimensions de rupture prises en charge pour la définition de métrique, par l’instrumentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e106c-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="e106c-117">Par exemple, un nom de transaction permet de décomposer la valeur totale de toutes les transactions en un ensemble de valeurs, une pour chaque nom de transaction.</span><span class="sxs-lookup"><span data-stu-id="e106c-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="e106c-118">D’autres exemples sont un système d’applications ou un nom de groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e106c-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="e106c-119">**Calculable**</span><span class="sxs-lookup"><span data-stu-id="e106c-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-120">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e106c-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-122">Caractéristiques de la mesure utilisée pour effectuer des calculs.</span><span class="sxs-lookup"><span data-stu-id="e106c-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="e106c-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span><span class="sxs-lookup"><span data-stu-id="e106c-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-124">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="e106c-124">A string.</span></span> <span data-ttu-id="e106c-125">L’arithmétique n’est pas appropriée.</span><span class="sxs-lookup"><span data-stu-id="e106c-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="e106c-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span><span class="sxs-lookup"><span data-stu-id="e106c-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-127">Il est raisonnable de calculer cette valeur sur de nombreuses instances de, par exemple, UnitOfWork, telles que le nombre de fichiers traités dans un travail de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="e106c-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="e106c-128">Par exemple, si chaque travail de sauvegarde est un UnitOfWork et que chaque travail sauvegarde 27 000 fichiers en moyenne, il est logique de préciser que 100 travaux de sauvegarde ont traité 2,7 millions fichiers.</span><span class="sxs-lookup"><span data-stu-id="e106c-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="e106c-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non summable** (3)</span><span class="sxs-lookup"><span data-stu-id="e106c-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-130">Il n’est pas judicieux de faire la somme de cette valeur sur de nombreuses instances de UnitOfWork.</span><span class="sxs-lookup"><span data-stu-id="e106c-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="e106c-131">C’est le cas, par exemple, d’une mesure qui mesure la longueur de la file d’attente lorsqu’un travail arrive sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="e106c-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="e106c-132">Si chaque travail est un UnitOfWork et que la longueur moyenne de la file d’attente lorsque chaque travail arrive est 33, il n’est pas judicieux de préciser que la longueur de la file d’attente pour les travaux 100 est 3300.</span><span class="sxs-lookup"><span data-stu-id="e106c-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="e106c-133">Il est logique de dire que la moyenne est de 33.</span><span class="sxs-lookup"><span data-stu-id="e106c-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e106c-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="e106c-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e106c-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e106c-137">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**IsContinuous**")</span><span class="sxs-lookup"><span data-stu-id="e106c-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="e106c-138">Indique comment la valeur de métrique change à l’aide d’attributs courants tels que le changement de direction, les valeurs minimales et maximales et la sémantique d’encapsulage.</span><span class="sxs-lookup"><span data-stu-id="e106c-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e106c-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e106c-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-140">Le concepteur de mesures n’a pas qualifié le ChangeType.</span><span class="sxs-lookup"><span data-stu-id="e106c-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="e106c-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span><span class="sxs-lookup"><span data-stu-id="e106c-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-142">Si la propriété « IsContinuous » a la valeur « false », ChangeType n’a pas de sens et doit être défini sur « N/A ».</span><span class="sxs-lookup"><span data-stu-id="e106c-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="e106c-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Compteur** (3)</span><span class="sxs-lookup"><span data-stu-id="e106c-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-144">La métrique est une mesure de compteur.</span><span class="sxs-lookup"><span data-stu-id="e106c-144">The metric is a counter metric.</span></span> <span data-ttu-id="e106c-145">Il s’agit d’une valeur entière non négative qui augmente de façon monotone jusqu’à atteindre le nombre maximal pouvant être représenté, puis encapsuler et commencer à augmenter de 0.</span><span class="sxs-lookup"><span data-stu-id="e106c-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="e106c-146">De tels compteurs, également appelés compteurs de substitution, peuvent être utilisés par exemple pour compter le nombre d’erreurs réseau ou le nombre de transactions traitées.</span><span class="sxs-lookup"><span data-stu-id="e106c-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="e106c-147">La seule façon pour une application cliente d’effectuer le suivi de la boucle est de récupérer la valeur du compteur dans des intervalles de temps appropriés.</span><span class="sxs-lookup"><span data-stu-id="e106c-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="e106c-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Jauge** (4)</span><span class="sxs-lookup"><span data-stu-id="e106c-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-149">La métrique est une mesure de jauge.</span><span class="sxs-lookup"><span data-stu-id="e106c-149">The metric is a gauge metric.</span></span> <span data-ttu-id="e106c-150">Celles-ci ont des valeurs entières ou float qui peuvent augmenter et diminuer de façon arbitraire.</span><span class="sxs-lookup"><span data-stu-id="e106c-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="e106c-151">Une jauge ne doit pas être renvoyée à la ligne lors de l’atteinte du nombre minimal ou maximal pouvant être représenté, à la place de la valeur « sticks » à ce nombre.</span><span class="sxs-lookup"><span data-stu-id="e106c-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="e106c-152">Valeurs minimales ou maximales à l’intérieur de la plage de valeurs représentables auxquelles la valeur de métrique « bâtons » peut ou non être définie.</span><span class="sxs-lookup"><span data-stu-id="e106c-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e106c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e106c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e106c-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e106c-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e106c-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="e106c-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-156">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e106c-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-158">Type de données de la mesure.</span><span class="sxs-lookup"><span data-stu-id="e106c-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="e106c-159">**booléen** (1)</span><span class="sxs-lookup"><span data-stu-id="e106c-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="e106c-160">**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="e106c-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="e106c-161">**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="e106c-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="e106c-162">**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="e106c-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="e106c-163">**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="e106c-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="e106c-164">**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="e106c-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="e106c-165">**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="e106c-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="e106c-166">**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="e106c-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="e106c-167">**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="e106c-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="e106c-168">**chaîne** (10)</span><span class="sxs-lookup"><span data-stu-id="e106c-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="e106c-169">**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="e106c-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="e106c-170">**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="e106c-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="e106c-171">**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="e106c-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="e106c-172">**UInt8** (14)</span><span class="sxs-lookup"><span data-stu-id="e106c-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e106c-173">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="e106c-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-174">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e106c-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-176">Indique comment les valeurs de métriques sont collectées par l’instrumentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e106c-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e106c-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e106c-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-178">Indique que le GatheringType est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e106c-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="e106c-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span><span class="sxs-lookup"><span data-stu-id="e106c-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-180">Indique que les valeurs métriques CIM sont mises à jour immédiatement lorsque les valeurs de la ressource mesurée sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="e106c-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="e106c-181">Les valeurs des mesures OnChange reflètent véritablement la situation actuelle dans la ressource à tout moment.</span><span class="sxs-lookup"><span data-stu-id="e106c-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="e106c-182">Par exemple, il s’agit du nombre d’utilisateurs connectés qui sont mis à jour immédiatement à mesure que les utilisateurs se connectent et se déconnectent.</span><span class="sxs-lookup"><span data-stu-id="e106c-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="e106c-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Périodique** (3)</span><span class="sxs-lookup"><span data-stu-id="e106c-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-184">" : Indique que les valeurs métriques CIM sont mises à jour régulièrement.</span><span class="sxs-lookup"><span data-stu-id="e106c-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="e106c-185">Par exemple, pour une application cliente, une valeur métrique s’appliquant à l’heure actuelle est constante pendant chaque intervalle de collecte, puis passe à la nouvelle valeur à la fin de chaque intervalle de collecte.</span><span class="sxs-lookup"><span data-stu-id="e106c-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="e106c-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span><span class="sxs-lookup"><span data-stu-id="e106c-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-187">Indique que la valeur métrique CIM est déterminée à chaque fois qu’une application cliente la lit.</span><span class="sxs-lookup"><span data-stu-id="e106c-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="e106c-188">Les valeurs des métriques OnRequest retournent véritablement la situation actuelle au sein de la ressource si une personne en fait la demande.</span><span class="sxs-lookup"><span data-stu-id="e106c-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="e106c-189">Toutefois, ils ne changent pas « non respecté » et, par conséquent, l’abonnement aux modifications de valeur des métriques OnRequest n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="e106c-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e106c-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e106c-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e106c-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e106c-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e106c-192">**Id**</span><span class="sxs-lookup"><span data-stu-id="e106c-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e106c-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e106c-195">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e106c-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e106c-196">ID unique de la définition de la métrique.</span><span class="sxs-lookup"><span data-stu-id="e106c-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="e106c-197">Les GUID/UUID OSF (Open Software Foundation) sont recommandés.</span><span class="sxs-lookup"><span data-stu-id="e106c-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="e106c-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="e106c-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-199">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e106c-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-201">True si la valeur métrique est continue ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="e106c-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="e106c-202">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e106c-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e106c-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-205">Nom de la mesure.</span><span class="sxs-lookup"><span data-stu-id="e106c-205">The name of the metric.</span></span> <span data-ttu-id="e106c-206">Ce nom ne doit pas nécessairement être unique, mais il doit être descriptif et peut contenir des espaces vides.</span><span class="sxs-lookup"><span data-stu-id="e106c-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="e106c-207">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="e106c-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e106c-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-210">Unités spécifiques d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="e106c-210">The specific units of a value.</span></span> <span data-ttu-id="e106c-211">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e106c-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e106c-212">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="e106c-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e106c-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e106c-215">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ BaseMetricValue**.**Duration**»)</span><span class="sxs-lookup"><span data-stu-id="e106c-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="e106c-216">Étendue de temps qui s’applique au concepteur de mesures.</span><span class="sxs-lookup"><span data-stu-id="e106c-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e106c-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e106c-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-218">Indique que l’étendue de l’heure n’a pas été qualifiée par le concepteur de mesures ou qu’elle est inconnue du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e106c-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="e106c-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span><span class="sxs-lookup"><span data-stu-id="e106c-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-220">Indique que la mesure s’applique à un point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="e106c-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="e106c-221">Sur les instances BaseMetricValue correspondantes, TimeStamp spécifie le point dans le temps et la durée est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="e106c-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="e106c-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervalle** (3)</span><span class="sxs-lookup"><span data-stu-id="e106c-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-223">Indique que la mesure s’applique à un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="e106c-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="e106c-224">Sur les instances BaseMetricValue correspondantes, TimeStamp spécifie la fin de l’intervalle de temps et la durée spécifie sa durée</span><span class="sxs-lookup"><span data-stu-id="e106c-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="e106c-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span><span class="sxs-lookup"><span data-stu-id="e106c-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e106c-226">Indique que la mesure s’applique à un intervalle de temps qui a commencé au démarrage de la ressource mesurée (c’est-à-dire, le propriété ManagedElement associé à MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="e106c-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="e106c-227">Sur les instances BaseMetricValue correspondantes, TimeStamp spécifie la fin de l’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="e106c-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="e106c-228">Si la durée est égale à 0, cela indique que le temps de démarrage de la ressource mesurée est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e106c-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="e106c-229">Sinon, Duration spécifie la durée entre le démarrage de la ressource et l’horodateur.</span><span class="sxs-lookup"><span data-stu-id="e106c-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e106c-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e106c-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e106c-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e106c-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e106c-232">**Unités**</span><span class="sxs-lookup"><span data-stu-id="e106c-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e106c-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e106c-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e106c-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e106c-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e106c-235">Unités de la métrique.</span><span class="sxs-lookup"><span data-stu-id="e106c-235">The units of the metric.</span></span> <span data-ttu-id="e106c-236">Par exemple, les octets, les paquets, les travaux, les fichiers, les millisecondes et les ampères.</span><span class="sxs-lookup"><span data-stu-id="e106c-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e106c-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e106c-237">Requirements</span></span>



| <span data-ttu-id="e106c-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e106c-238">Requirement</span></span> | <span data-ttu-id="e106c-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="e106c-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e106c-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e106c-240">Minimum supported client</span></span><br/> | <span data-ttu-id="e106c-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e106c-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e106c-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e106c-242">Minimum supported server</span></span><br/> | <span data-ttu-id="e106c-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e106c-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e106c-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e106c-244">Namespace</span></span><br/>                | <span data-ttu-id="e106c-245">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e106c-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e106c-246">MOF</span><span class="sxs-lookup"><span data-stu-id="e106c-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e106c-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e106c-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e106c-248">DLL</span><span class="sxs-lookup"><span data-stu-id="e106c-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e106c-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e106c-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e106c-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e106c-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e106c-251">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e106c-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

