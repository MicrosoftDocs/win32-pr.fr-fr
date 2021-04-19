---
description: Fournit un lien entre l’instance des fonctionnalités du commutateur Ethernet et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Classe Msvm_FeatureSettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544697"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="4d976-103">MSVM \_ FeatureSettingsDefineCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="4d976-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="4d976-104">Fournit un lien entre l’instance des fonctionnalités du commutateur Ethernet et les paramètres minimal, maximal, incrémentiel et par défaut d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="4d976-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="4d976-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4d976-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d976-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d976-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="4d976-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4d976-107">Members</span></span>

<span data-ttu-id="4d976-108">La classe **MSVM \_ FeatureSettingsDefineCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4d976-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="4d976-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d976-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d976-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d976-110">Properties</span></span>

<span data-ttu-id="4d976-111">La classe **MSVM \_ FeatureSettingsDefineCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d976-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d976-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4d976-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d976-113">Type de données : **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="4d976-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4d976-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d976-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d976-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4d976-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4d976-116">Référence à une instance de la classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) qui représente les fonctionnalités de la fonctionnalité de commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4d976-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="4d976-117">Cette propriété est héritée [**du \_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="4d976-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="4d976-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4d976-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d976-119">Type de données : **[ **MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="4d976-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4d976-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d976-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d976-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4d976-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4d976-122">Référence à une instance de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) qui représente les paramètres de ressource.</span><span class="sxs-lookup"><span data-stu-id="4d976-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="4d976-123">Cette propriété est héritée [**du \_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="4d976-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="4d976-124">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="4d976-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d976-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d976-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d976-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d976-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d976-127">Spécifie si les propriétés non **null**, non-clé de **PartComponent** sont traitées indépendamment ou comme un ensemble corrélé.</span><span class="sxs-lookup"><span data-stu-id="4d976-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="4d976-128">Par exemple, il est possible de définir un ensemble indépendant de propriétés maximales, mais il n’existe pas de relation entre chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="4d976-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="4d976-129">D’un autre côté, il peut être nécessaire de définir plusieurs ensembles corrélés de propriétés maximum lorsque les valeurs maximales de chacune sont dépendantes de certaines d’entre elles.</span><span class="sxs-lookup"><span data-stu-id="4d976-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="4d976-130">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4d976-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="4d976-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Indépendant** (0)</span><span class="sxs-lookup"><span data-stu-id="4d976-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4d976-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Corrélé** (1)</span><span class="sxs-lookup"><span data-stu-id="4d976-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4d976-133">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="4d976-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d976-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d976-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d976-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d976-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d976-136">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4d976-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d976-137">Indique une sémantique supplémentaire sur l’interprétation de toutes les propriétés non-**null** et non-clé des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="4d976-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="4d976-138">Les valeurs ci-dessous sont évaluées uniquement par rapport aux propriétés numériques non **null**, non-clé, non énumérées, non-booléennes, des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="4d976-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="4d976-139">Chaque propriété de cet ensemble doit être comparable de façon mathématique à d’autres instances de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4d976-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="4d976-140">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4d976-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="4d976-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d976-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="4d976-142">Signification</span><span class="sxs-lookup"><span data-stu-id="4d976-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="4d976-143"><dt>**Point**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="4d976-144">Cette instance de données de paramètre fournit un ensemble unique de valeurs.</span><span class="sxs-lookup"><span data-stu-id="4d976-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="4d976-145"><dt>**Minimums**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="4d976-146">Ce paramètre fournit des valeurs minimales pour les propriétés évaluées.</span><span class="sxs-lookup"><span data-stu-id="4d976-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="4d976-147">Lorsqu’il est utilisé avec **PropertyPolicy** = « Independent », un seul paramètre de ce type doit être spécifié par instance de données de paramètre particulière pour toutes les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4d976-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="4d976-148">À moins d’être restreintes par une valeur maximale sur le même jeu de propriétés, toutes les valeurs qui sont plus élevées que les valeurs spécifiées sont également considérées comme étant prises en charge par l’instance des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="4d976-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="4d976-149"><dt>**Maximums**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="4d976-150">Ce paramètre donne des valeurs maximales pour les propriétés évaluées.</span><span class="sxs-lookup"><span data-stu-id="4d976-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="4d976-151">Lorsqu’il est utilisé avec **PropertyPolicy** = « Independent », un seul paramètre de ce type doit être spécifié par instance de données de paramètre particulière pour toutes les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4d976-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="4d976-152">À moins d’être restreintes par une valeur minimale sur le même jeu de propriétés, toutes les valeurs qui comparent les valeurs spécifiées sont également considérées comme étant prises en charge par l’instance des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="4d976-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="4d976-153"><dt>**Incréments**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="4d976-154">Ce paramètre donne des valeurs d’incrément pour les propriétés évaluées.</span><span class="sxs-lookup"><span data-stu-id="4d976-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="4d976-155">Pour les fonctionnalités associées, si une propriété évaluée n’a actuellement pas de valeurs minimales ou maximales correspondantes, la propriété n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="4d976-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="4d976-156">Dans le cas contraire, pour chaque propriété évaluée, sa valeur (*x*) doit être comprise entre *MinimumValue* et *MaximumValue*, et doit avoir la propriété qui, à la fois, le résultat de *MaximumValue* moins *x* et le résultat de *x* moins *MinimumValue* sont chacun un entier multiple de l' *incrément*.</span><span class="sxs-lookup"><span data-stu-id="4d976-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="4d976-157">Si les propriétés *MinimumValue* et *MaximumValue* ne sont pas spécifiées et que l’autre est, la valeur manquante doit être respectivement considérée comme la valeur la plus basse ou la plus élevée prise en charge pour le type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4d976-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="4d976-158">En outre, si un *MinimumValue* et un *MaximumValue* sont spécifiés pour une propriété évaluée, le résultat de *MaximumValue* moins *MinimumValue* doit être un entier multiple de l' *incrément*.</span><span class="sxs-lookup"><span data-stu-id="4d976-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="4d976-159">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="4d976-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d976-160">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d976-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d976-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d976-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d976-162">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4d976-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d976-163">Spécifie une sémantique supplémentaire sur l’interprétation des propriétés non-**null** et non-clés des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="4d976-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="4d976-164">Cette propriété est héritée de la [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4d976-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="4d976-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d976-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="4d976-166">Signification</span><span class="sxs-lookup"><span data-stu-id="4d976-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="4d976-167"><dt>0</dt> <dt>**par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="4d976-168">Les valeurs de propriété des données de paramètre sont utilisées comme valeurs par défaut, lors de la création d’une nouvelle instance de données de paramètre pour les éléments dont les fonctionnalités sont définies par les fonctionnalités associées.</span><span class="sxs-lookup"><span data-stu-id="4d976-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="4d976-169">Dans les instances des données de paramètre, pour des propriétés particulières ayant le même objectif sémantique, au plus une instance de données de définition de ce type doit être spécifiée par défaut.</span><span class="sxs-lookup"><span data-stu-id="4d976-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="4d976-170"><dt>**Optimal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="4d976-171">L’instance de données de paramètre représente des valeurs de paramètre optimales pour les éléments associés aux fonctionnalités associées.</span><span class="sxs-lookup"><span data-stu-id="4d976-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="4d976-172">Plusieurs instances de données de paramètre de composant peuvent être déclarées comme optimales.</span><span class="sxs-lookup"><span data-stu-id="4d976-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="4d976-173"><dt>**Moyenne**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="4d976-174">Les propriétés numériques non **null**, non-clé, non énumérées, non-booléennes de l’instance de données de paramètre associée représentent un point moyen sur une dimension.</span><span class="sxs-lookup"><span data-stu-id="4d976-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="4d976-175">Pour différentes combinaisons de propriétés de définition de données, les instances de données de paramètre de plusieurs composants peuvent être déclarées comme la **moyenne**.</span><span class="sxs-lookup"><span data-stu-id="4d976-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="4d976-176"><dt>**Pris en charge**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="4d976-177">Les propriétés non **null**, non-clés des données de paramètre représentent un ensemble de valeurs de propriétés prises en charge qui ne sont pas qualifiées autrement.</span><span class="sxs-lookup"><span data-stu-id="4d976-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d976-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d976-178">Requirements</span></span>



| <span data-ttu-id="4d976-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d976-179">Requirement</span></span> | <span data-ttu-id="4d976-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d976-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d976-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d976-181">Minimum supported client</span></span><br/> | <span data-ttu-id="4d976-182">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d976-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4d976-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d976-183">Minimum supported server</span></span><br/> | <span data-ttu-id="4d976-184">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d976-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d976-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4d976-185">Namespace</span></span><br/>                | <span data-ttu-id="4d976-186">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4d976-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4d976-187">MOF</span><span class="sxs-lookup"><span data-stu-id="4d976-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d976-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d976-189">DLL</span><span class="sxs-lookup"><span data-stu-id="4d976-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d976-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d976-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

