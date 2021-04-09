---
description: Représente une valeur de métrique définie par une instance de la \_ classe MSVM BaseMetricDefinition.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Classe Msvm_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867974"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="cbb50-103">MSVM \_ BaseMetricValue, classe</span><span class="sxs-lookup"><span data-stu-id="cbb50-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="cbb50-104">Représente une valeur de métrique définie par une instance de la classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb50-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="cbb50-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cbb50-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb50-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbb50-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a><span data-ttu-id="cbb50-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cbb50-107">Members</span></span>

<span data-ttu-id="cbb50-108">La classe **MSVM \_ BaseMetricValue** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cbb50-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="cbb50-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cbb50-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbb50-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cbb50-110">Properties</span></span>

<span data-ttu-id="cbb50-111">La classe **MSVM \_ BaseMetricValue** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cbb50-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbb50-112">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="cbb50-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-115">Spécifie une dimension de répartition à partir du tableau **BreakdownDimensions** défini dans le [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)associé.</span><span class="sxs-lookup"><span data-stu-id="cbb50-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="cbb50-116">Il s’agit de la dimension selon laquelle cet ensemble de valeurs de métriques est divisé.</span><span class="sxs-lookup"><span data-stu-id="cbb50-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="cbb50-117">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-118">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="cbb50-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-121">Définit une valeur de la propriété **BreakdownDimension** définie pour cette instance de la valeur métrique.</span><span class="sxs-lookup"><span data-stu-id="cbb50-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="cbb50-122">Par exemple, si **BreakdownDimension** est « TransactionName », cette propriété peut nommer la transaction réelle à laquelle s’applique cette valeur de mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="cbb50-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="cbb50-123">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cbb50-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-127">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cbb50-127">A short description of the object.</span></span> <span data-ttu-id="cbb50-128">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="cbb50-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-132">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="cbb50-132">A description of the object.</span></span> <span data-ttu-id="cbb50-133">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-134">**Durée**</span><span class="sxs-lookup"><span data-stu-id="cbb50-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-135">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cbb50-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-137">Spécifie la durée pendant laquelle cette valeur métrique est valide.</span><span class="sxs-lookup"><span data-stu-id="cbb50-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="cbb50-138">Cette propriété ne doit pas exister pour les horodatages qui s’appliquent uniquement à un point dans le temps, mais doivent être spécifiées pour les valeurs considérées comme valides pour une certaine période (par exemple, échantillonnage).</span><span class="sxs-lookup"><span data-stu-id="cbb50-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="cbb50-139">Si la propriété **Duration** existe et que n’a pas la **valeur null**, la propriété **timestamp** spécifie la fin de l’intervalle.</span><span class="sxs-lookup"><span data-stu-id="cbb50-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="cbb50-140">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cbb50-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-144">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cbb50-144">A display name for the object.</span></span> <span data-ttu-id="cbb50-145">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cbb50-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-149">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="cbb50-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-150">Chaîne qui identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="cbb50-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cbb50-151">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-152">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="cbb50-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-155">Nom descriptif de l’élément auquel la valeur de la métrique appartient (l’élément mesuré).</span><span class="sxs-lookup"><span data-stu-id="cbb50-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="cbb50-156">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-157">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="cbb50-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-160">Clé de l’instance [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="cbb50-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="cbb50-161">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-162">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="cbb50-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cbb50-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-165">Valeur de la métrique représentée sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cbb50-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="cbb50-166">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-167">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="cbb50-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-168">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cbb50-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-170">Spécifie l’heure à laquelle la valeur de mesure a été capturée ou calculée.</span><span class="sxs-lookup"><span data-stu-id="cbb50-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="cbb50-171">Sachez que cela diffère de l’heure de création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="cbb50-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="cbb50-172">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cbb50-173">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="cbb50-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbb50-174">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cbb50-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbb50-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbb50-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cbb50-176">**True** si la valeur du point suivant dans le temps utilise la même instance de classe et modifie simplement les valeurs de propriété (telles que la **valeur** ou l' **horodateur**).</span><span class="sxs-lookup"><span data-stu-id="cbb50-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="cbb50-177">Si la **valeur est true**, l’instance est réutilisée.</span><span class="sxs-lookup"><span data-stu-id="cbb50-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="cbb50-178">Si la **valeur est false**, les instances existantes restent inchangées et une nouvelle instance est créée pour le nouveau point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="cbb50-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="cbb50-179">Cette propriété est héritée de la [**\_ BaseMetricDefinition CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cbb50-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbb50-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbb50-180">Requirements</span></span>



| <span data-ttu-id="cbb50-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbb50-181">Requirement</span></span> | <span data-ttu-id="cbb50-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbb50-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb50-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbb50-183">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb50-184">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbb50-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cbb50-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbb50-185">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb50-186">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbb50-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbb50-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cbb50-187">Namespace</span></span><br/>                | <span data-ttu-id="cbb50-188">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cbb50-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cbb50-189">MOF</span><span class="sxs-lookup"><span data-stu-id="cbb50-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbb50-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbb50-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbb50-191">DLL</span><span class="sxs-lookup"><span data-stu-id="cbb50-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbb50-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbb50-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

