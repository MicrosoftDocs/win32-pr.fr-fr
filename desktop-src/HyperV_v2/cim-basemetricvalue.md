---
description: Représente la valeur d’instance d’une métrique.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: Classe CIM_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952605"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="ef569-103">\_Classe CIM BaseMetricValue</span><span class="sxs-lookup"><span data-stu-id="ef569-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="ef569-104">Représente la valeur d’instance d’une métrique.</span><span class="sxs-lookup"><span data-stu-id="ef569-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef569-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef569-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a><span data-ttu-id="ef569-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ef569-106">Members</span></span>

<span data-ttu-id="ef569-107">La classe **CIM \_ BaseMetricValue** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef569-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="ef569-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef569-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef569-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef569-109">Properties</span></span>

<span data-ttu-id="ef569-110">La classe **CIM \_ BaseMetricValue** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef569-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef569-111">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="ef569-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef569-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef569-114">Dimension pour laquelle cet ensemble de valeurs de métriques est divisé en fonction de la propriété **BreakdownDimensions** de l’objet [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) associé.</span><span class="sxs-lookup"><span data-stu-id="ef569-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-115">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="ef569-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef569-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef569-118">Valeur de la propriété **BreakdownDimension** définie pour cette valeur d’instance.</span><span class="sxs-lookup"><span data-stu-id="ef569-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="ef569-119">Par exemple, si **BreakdownDimension** contient « TransactionName », cette propriété peut nommer la transaction réelle à laquelle s’applique cette valeur de mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="ef569-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-120">**Durée**</span><span class="sxs-lookup"><span data-stu-id="ef569-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-121">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef569-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef569-123">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**TimeStamp**»)</span><span class="sxs-lookup"><span data-stu-id="ef569-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="ef569-124">Durée pendant laquelle cette valeur de mesure est valide.</span><span class="sxs-lookup"><span data-stu-id="ef569-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="ef569-125">Cette propriété ne doit pas exister pour les horodatages qui s’appliquent uniquement à un point dans le temps, mais doivent être définies pour les valeurs considérées comme valides pour une certaine période (par exemple,</span><span class="sxs-lookup"><span data-stu-id="ef569-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="ef569-126">échantillonnage).</span><span class="sxs-lookup"><span data-stu-id="ef569-126">sampling).</span></span> <span data-ttu-id="ef569-127">Si la propriété **Duration** existe et n’est pas null, la valeur **timestamp** doit être la fin de l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="ef569-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef569-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef569-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef569-131">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="ef569-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="ef569-132">Identifie de façon unique une instance de cette classe dans la portée de l’espace de noms conteneur.</span><span class="sxs-lookup"><span data-stu-id="ef569-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ef569-133">Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="ef569-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="ef569-134">*Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="ef569-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="ef569-135">Ce modèle est similaire à la structure des noms de classes de schéma.</span><span class="sxs-lookup"><span data-stu-id="ef569-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="ef569-136">En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="ef569-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="ef569-137">Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="ef569-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="ef569-138">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.</span><span class="sxs-lookup"><span data-stu-id="ef569-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="ef569-139">Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ef569-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="ef569-140">Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="ef569-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="ef569-141">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="ef569-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef569-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef569-144">Nom descriptif de l’élément qui est mesuré par la métrique.</span><span class="sxs-lookup"><span data-stu-id="ef569-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="ef569-145">Cette propriété est obligatoire si la définition de métrique n’est pas associée à un objet [**CIM \_ propriété ManagedElement**](cim-managedelement.md) et peut être utilisée dans d’autres cas pour fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ef569-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="ef569-146">Cela permet de capturer les métriques indépendamment de tout objet **CIM \_ propriété ManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="ef569-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="ef569-147">Si plusieurs objets [**CIM \_ propriété ManagedElement**](cim-managedelement.md) sont associés à la valeur de métrique, vous pouvez choisir l’un des éléments gérés pour créer les informations supplémentaires pour la mesure.</span><span class="sxs-lookup"><span data-stu-id="ef569-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="ef569-148">La propriété n’est pas destinée à être utilisée comme clé étrangère pour interroger l’élément mesuré.</span><span class="sxs-lookup"><span data-stu-id="ef569-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="ef569-149">Au lieu de cela, vous devez utiliser l’Association à l' **\_ propriété ManagedElement CIM** .</span><span class="sxs-lookup"><span data-stu-id="ef569-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-150">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="ef569-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef569-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef569-153">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**»)</span><span class="sxs-lookup"><span data-stu-id="ef569-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="ef569-154">Clé de l’instance [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associée à cette valeur d’instance.</span><span class="sxs-lookup"><span data-stu-id="ef569-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-155">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="ef569-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef569-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef569-158">Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ef569-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ef569-159">Représentation sous forme de chaîne de la valeur de métrique.</span><span class="sxs-lookup"><span data-stu-id="ef569-159">A string representation of the metric value.</span></span> <span data-ttu-id="ef569-160">Le type de données d’origine de la valeur de métrique est spécifié dans l’objet [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associé.</span><span class="sxs-lookup"><span data-stu-id="ef569-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-161">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="ef569-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-162">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef569-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef569-164">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**Duration**»)</span><span class="sxs-lookup"><span data-stu-id="ef569-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="ef569-165">Heure à laquelle la valeur d’une instance de mesure est calculée.</span><span class="sxs-lookup"><span data-stu-id="ef569-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="ef569-166">Cela diffère de l’heure de création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="ef569-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="ef569-167">Si la propriété **volatile** a la valeur true, cette valeur change chaque fois qu’un nouvel instantané de mesure est pris.</span><span class="sxs-lookup"><span data-stu-id="ef569-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="ef569-168">Une application de gestion peut établir une série chronologique de données de métriques en extrayant les instances de **\_ BaseMetricValue CIM** et en les triant en fonction de leur valeur **timestamp** .</span><span class="sxs-lookup"><span data-stu-id="ef569-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="ef569-169">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="ef569-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef569-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ef569-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef569-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef569-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef569-172">True si la valeur **timestamp** change chaque fois que la valeur de l’instance Metric change.</span><span class="sxs-lookup"><span data-stu-id="ef569-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="ef569-173">False si cet objet doit rester inchangé et un nouvel objet créé pour la nouvelle valeur d' **horodatage** .</span><span class="sxs-lookup"><span data-stu-id="ef569-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef569-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef569-174">Requirements</span></span>



| <span data-ttu-id="ef569-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef569-175">Requirement</span></span> | <span data-ttu-id="ef569-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef569-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef569-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef569-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ef569-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ef569-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ef569-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef569-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ef569-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef569-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ef569-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef569-181">Namespace</span></span><br/>                | <span data-ttu-id="ef569-182">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef569-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef569-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ef569-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef569-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef569-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef569-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ef569-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef569-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef569-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef569-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef569-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef569-188">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ef569-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

