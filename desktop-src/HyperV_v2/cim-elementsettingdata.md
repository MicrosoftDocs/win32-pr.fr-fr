---
description: Représente une association entre un élément managé et ses données de paramètre associées. Cette Association indique également s’il s’agit d’un paramètre par défaut ou actuel.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Classe CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536374"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="e7c86-104">\_Classe CIM ElementSettingData</span><span class="sxs-lookup"><span data-stu-id="e7c86-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="e7c86-105">Représente une association entre un élément managé et ses données de paramètre associées.</span><span class="sxs-lookup"><span data-stu-id="e7c86-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="e7c86-106">Cette Association indique également s’il s’agit d’un paramètre par défaut ou actuel.</span><span class="sxs-lookup"><span data-stu-id="e7c86-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c86-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7c86-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="e7c86-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e7c86-108">Members</span></span>

<span data-ttu-id="e7c86-109">La classe **CIM \_ ElementSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e7c86-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e7c86-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e7c86-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7c86-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e7c86-111">Properties</span></span>

<span data-ttu-id="e7c86-112">La classe **CIM \_ ElementSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7c86-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7c86-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="e7c86-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c86-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7c86-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e7c86-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c86-116">Indique si le paramètre référencé est actuellement utilisé par l’élément.</span><span class="sxs-lookup"><span data-stu-id="e7c86-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7c86-117">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e7c86-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="e7c86-118">**Est actuel** (1)</span><span class="sxs-lookup"><span data-stu-id="e7c86-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="e7c86-119">**N’est pas à jour** (2)</span><span class="sxs-lookup"><span data-stu-id="e7c86-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7c86-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="e7c86-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c86-121">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7c86-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e7c86-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c86-123">Indique si le paramètre est un paramètre par défaut pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="e7c86-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7c86-124">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e7c86-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="e7c86-125">**Est la valeur par défaut** (1)</span><span class="sxs-lookup"><span data-stu-id="e7c86-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="e7c86-126">**N’est pas une valeur par défaut** (2)</span><span class="sxs-lookup"><span data-stu-id="e7c86-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7c86-127">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="e7c86-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c86-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7c86-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e7c86-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c86-130">Indicateur qui signale quand et à quelle fréquence appliquer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="e7c86-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="e7c86-131">Par exemple, le paramètre peut être appliqué à une demande de réinitialisation, de réinitialisation et de reconfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7c86-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="e7c86-132">Il peut s’agir d’un paramètre permanent, ou d’un paramètre utilisé une seule fois, comme indiqué par l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="e7c86-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="e7c86-133">S’il s’agit d’un paramètre permanent, le paramètre est appliqué à chaque réinitialisation de l’élément managé, jusqu’à ce que cet indicateur soit réinitialisé manuellement.</span><span class="sxs-lookup"><span data-stu-id="e7c86-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="e7c86-134">Toutefois, s’il s’agit d’une utilisation unique, l’indicateur est automatiquement effacé après l’application des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e7c86-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="e7c86-135">En outre, si cet indicateur est défini sur une valeur autre que 0 (inconnu), il est prioritaire sur une propriété **SettingData** définie sur « default ».</span><span class="sxs-lookup"><span data-stu-id="e7c86-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="e7c86-136">Si l’élément géré est un système informatique et que la valeur de cet indicateur est « est suivant », le paramètre sera effectif à la prochaine réinitialisation du système.</span><span class="sxs-lookup"><span data-stu-id="e7c86-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="e7c86-137">Et, sauf si cet indicateur est modifié, il est conservé pour les réinitialisations ultérieures du système.</span><span class="sxs-lookup"><span data-stu-id="e7c86-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="e7c86-138">Toutefois, si cet indicateur est défini sur « est suivant pour une utilisation unique », ce paramètre n’est utilisé qu’une seule fois et l’indicateur est réinitialisé après cette valeur sur 2 (n’est pas suivant).</span><span class="sxs-lookup"><span data-stu-id="e7c86-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="e7c86-139">Ainsi, dans l’exemple ci-dessus, si le système redémarre rapidement en succession, le paramètre ne sera pas utilisé au deuxième redémarrage.</span><span class="sxs-lookup"><span data-stu-id="e7c86-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7c86-140">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e7c86-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="e7c86-141">**Est suivant** (1)</span><span class="sxs-lookup"><span data-stu-id="e7c86-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="e7c86-142">**N’est pas suivant** (2)</span><span class="sxs-lookup"><span data-stu-id="e7c86-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="e7c86-143">**Est ensuite utilisé pour une utilisation unique** (3)</span><span class="sxs-lookup"><span data-stu-id="e7c86-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7c86-144">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e7c86-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c86-145">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e7c86-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e7c86-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-147">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7c86-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e7c86-148">Élément managé.</span><span class="sxs-lookup"><span data-stu-id="e7c86-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="e7c86-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="e7c86-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c86-150">Type de données **: \_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="e7c86-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e7c86-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7c86-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7c86-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e7c86-153">Données de paramètre associées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="e7c86-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7c86-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7c86-154">Requirements</span></span>



| <span data-ttu-id="e7c86-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7c86-155">Requirement</span></span> | <span data-ttu-id="e7c86-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7c86-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c86-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7c86-157">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c86-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7c86-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e7c86-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7c86-159">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c86-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7c86-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e7c86-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7c86-161">Namespace</span></span><br/>                | <span data-ttu-id="e7c86-162">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e7c86-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7c86-163">MOF</span><span class="sxs-lookup"><span data-stu-id="e7c86-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7c86-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7c86-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7c86-165">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c86-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7c86-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7c86-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

