---
description: Représente une association entre les propriétés d’une \_ instance de la SETTINGDATA CIM et une \_ instance des fonctionnalités CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: Classe CIM_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521055"
---
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="0e128-103">\_Classe CIM SettingsDefineCapabilities</span><span class="sxs-lookup"><span data-stu-id="0e128-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="0e128-104">Représente une association entre les propriétés d’une instance de la [**\_ SettingData CIM**](cim-settingdata.md) et une instance des [**\_ fonctionnalités CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="0e128-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e128-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e128-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="0e128-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0e128-106">Members</span></span>

<span data-ttu-id="0e128-107">La classe **CIM \_ SettingsDefineCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e128-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0e128-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e128-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e128-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e128-109">Properties</span></span>

<span data-ttu-id="0e128-110">La classe **CIM \_ SettingsDefineCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e128-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e128-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0e128-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e128-112">Type de données **: \_ fonctionnalités CIM**</span><span class="sxs-lookup"><span data-stu-id="0e128-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="0e128-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e128-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e128-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0e128-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0e128-115">Référence à l’instance [**des \_ fonctionnalités CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="0e128-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="0e128-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0e128-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e128-117">Type de données **: \_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="0e128-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="0e128-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e128-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e128-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="0e128-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0e128-120">Référence à l’instance [**du \_ SettingData CIM**](cim-settingdata.md) utilisée pour définir l’instance des [**\_ fonctionnalités CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="0e128-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="0e128-121">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="0e128-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e128-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e128-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e128-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e128-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e128-124">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="0e128-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="0e128-125">Indique si les propriétés non null, non-clé de l’instance du [**\_ SettingData CIM**](cim-settingdata.md) associée sont traitées indépendamment ou comme un ensemble corrélé.</span><span class="sxs-lookup"><span data-stu-id="0e128-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="0e128-126">Par exemple, un ensemble indépendant de propriétés maximales peut être défini lorsqu’il n’existe aucune relation entre chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="0e128-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="0e128-127">En revanche, il peut être nécessaire de définir plusieurs ensembles corrélés de propriétés maximum lorsque les valeurs maximales de chacune sont dépendantes de certaines d’entre elles.</span><span class="sxs-lookup"><span data-stu-id="0e128-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="0e128-128">**Indépendant** (0)</span><span class="sxs-lookup"><span data-stu-id="0e128-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="0e128-129">**Corrélé** (1)</span><span class="sxs-lookup"><span data-stu-id="0e128-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e128-130">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0e128-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e128-131">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="0e128-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e128-132">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e128-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e128-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e128-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e128-134">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRole**")</span><span class="sxs-lookup"><span data-stu-id="0e128-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="0e128-135">Indique le type de plage de valeurs utilisé par les propriétés des propriétés non-null et non-clé de l’instance du [**\_ SettingData CIM**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="0e128-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="0e128-136">**Point** (0)</span><span class="sxs-lookup"><span data-stu-id="0e128-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="0e128-137">**Valeurs minimales** (1)</span><span class="sxs-lookup"><span data-stu-id="0e128-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="0e128-138">**Valeurs maximales** (2)</span><span class="sxs-lookup"><span data-stu-id="0e128-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="0e128-139">**Incréments** (3)</span><span class="sxs-lookup"><span data-stu-id="0e128-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e128-140">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0e128-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e128-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="0e128-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e128-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e128-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e128-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e128-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e128-144">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="0e128-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="0e128-145">Sémantique supplémentaire pour l’interprétation des propriétés non-null et non-clé de l’instance de la [**\_ SettingData CIM**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="0e128-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="0e128-146">« Default » indique que les valeurs de propriété de l’instance de l’SettingData du composant seront utilisées comme valeurs par défaut, lorsqu’une nouvelle instance SettingData est créée pour les éléments dont les fonctionnalités sont définies par l’instance des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="0e128-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="0e128-147">Dans les instances de SettingData, pour des propriétés particulières ayant le même objectif sémantique, au plus une de ces instances SettingData sera spécifiée comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e128-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="0e128-148">« Optimal » indique que l’instance de SettingData représente des valeurs de paramètre optimales pour les éléments associés à l’instance des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="0e128-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="0e128-149">Plusieurs instances de SettingData de composant peuvent être déclarées comme optimales.» Mean» indique que les propriétés numériques non-null, non-clé, non énumérées, non-booléennes de l’instance SettingData associée représentent un point moyen sur une dimension.</span><span class="sxs-lookup"><span data-stu-id="0e128-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="0e128-150">Pour différentes combinaisons de propriétés SettingData, plusieurs instances de SettingData de composant peuvent être déclarées comme « moyennes ».</span><span class="sxs-lookup"><span data-stu-id="0e128-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="0e128-151">« Pris en charge » indique que les propriétés non null, non-clé de l’instance de l’élément SettingData du composant représentent un ensemble de valeurs de propriétés prises en charge qui ne sont pas qualifiées autrement.</span><span class="sxs-lookup"><span data-stu-id="0e128-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="0e128-152">**Valeur par défaut** (0)</span><span class="sxs-lookup"><span data-stu-id="0e128-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="0e128-153">**Optimal** (1)</span><span class="sxs-lookup"><span data-stu-id="0e128-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="0e128-154">**Moyenne** (2)</span><span class="sxs-lookup"><span data-stu-id="0e128-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="0e128-155">**Pris en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="0e128-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e128-156">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0e128-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="0e128-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0e128-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0e128-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e128-158">Requirements</span></span>



| <span data-ttu-id="0e128-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e128-159">Requirement</span></span> | <span data-ttu-id="0e128-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e128-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e128-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e128-161">Minimum supported client</span></span><br/> | <span data-ttu-id="0e128-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0e128-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0e128-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e128-163">Minimum supported server</span></span><br/> | <span data-ttu-id="0e128-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e128-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0e128-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e128-165">Namespace</span></span><br/>                | <span data-ttu-id="0e128-166">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e128-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e128-167">MOF</span><span class="sxs-lookup"><span data-stu-id="0e128-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e128-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e128-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e128-169">DLL</span><span class="sxs-lookup"><span data-stu-id="0e128-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e128-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e128-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e128-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e128-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e128-172">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="0e128-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

