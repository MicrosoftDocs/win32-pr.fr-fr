---
description: Associe un élément managé à ses données de configuration.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Classe Msvm_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515885"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="ead11-103">MSVM \_ ElementSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ead11-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="ead11-104">Associe un élément managé à ses données de configuration.</span><span class="sxs-lookup"><span data-stu-id="ead11-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="ead11-105">Certaines des applications les plus notables de cette association sont utilisées pour lier un ordinateur virtuel et les périphériques logiques qui ont été attribués à ce système avec leurs informations de configuration de capture instantanée.</span><span class="sxs-lookup"><span data-stu-id="ead11-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="ead11-106">Les informations de configuration actuelles sont associées à la machine virtuelle et à ses appareils par le biais de l’Association [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .</span><span class="sxs-lookup"><span data-stu-id="ead11-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="ead11-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ead11-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ead11-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="ead11-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ead11-109">Members</span></span>

<span data-ttu-id="ead11-110">La classe **MSVM \_ ElementSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ead11-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ead11-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ead11-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ead11-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ead11-112">Properties</span></span>

<span data-ttu-id="ead11-113">La classe **MSVM \_ ElementSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ead11-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ead11-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="ead11-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ead11-115">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ead11-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ead11-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ead11-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ead11-117">Indique que le paramètre référencé est actuellement utilisé dans l’opération de l’élément ou que ces informations sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="ead11-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="ead11-118">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ead11-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="ead11-119">La valeur par défaut est 0 (inconnu).</span><span class="sxs-lookup"><span data-stu-id="ead11-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="ead11-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ead11-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Est actuel** (1)</span><span class="sxs-lookup"><span data-stu-id="ead11-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**N’est pas à jour** (2)</span><span class="sxs-lookup"><span data-stu-id="ead11-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ead11-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="ead11-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ead11-124">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ead11-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ead11-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ead11-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ead11-126">Indique que le paramètre référencé est un paramètre par défaut pour l’élément ou que ces informations sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="ead11-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="ead11-127">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ead11-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="ead11-128">La valeur par défaut est 0 (inconnu).</span><span class="sxs-lookup"><span data-stu-id="ead11-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="ead11-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ead11-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Est la valeur par défaut** (1)</span><span class="sxs-lookup"><span data-stu-id="ead11-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**N’est pas une valeur par défaut** (2)</span><span class="sxs-lookup"><span data-stu-id="ead11-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ead11-132">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="ead11-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ead11-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ead11-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ead11-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ead11-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ead11-135">Indique si le paramètre référencé est le paramètre suivant à appliquer.</span><span class="sxs-lookup"><span data-stu-id="ead11-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="ead11-136">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ead11-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="ead11-137">La valeur par défaut est 0 (inconnu).</span><span class="sxs-lookup"><span data-stu-id="ead11-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="ead11-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ead11-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Est suivant** (1)</span><span class="sxs-lookup"><span data-stu-id="ead11-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**N’est pas suivant** (2)</span><span class="sxs-lookup"><span data-stu-id="ead11-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ead11-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Est ensuite utilisé pour une utilisation unique** (3)</span><span class="sxs-lookup"><span data-stu-id="ead11-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ead11-142">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="ead11-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ead11-143">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="ead11-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="ead11-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ead11-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ead11-145">Référence à la machine virtuelle ou à l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="ead11-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="ead11-146">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ead11-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ead11-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="ead11-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ead11-148">Type de données : **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ead11-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="ead11-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ead11-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ead11-150">Référence aux paramètres de l’instantané de l’ordinateur virtuel ou de l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="ead11-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="ead11-151">Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ead11-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ead11-152">Notes</span><span class="sxs-lookup"><span data-stu-id="ead11-152">Remarks</span></span>

<span data-ttu-id="ead11-153">L’accès à la classe **MSVM \_ ElementSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="ead11-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ead11-154">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ead11-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ead11-155">Exemples</span><span class="sxs-lookup"><span data-stu-id="ead11-155">Examples</span></span>

<span data-ttu-id="ead11-156">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ead11-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ead11-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ead11-157">Requirements</span></span>



| <span data-ttu-id="ead11-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ead11-158">Requirement</span></span> | <span data-ttu-id="ead11-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead11-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead11-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ead11-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ead11-161">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ead11-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ead11-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ead11-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ead11-163">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ead11-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ead11-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ead11-164">Namespace</span></span><br/>                | <span data-ttu-id="ead11-165">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ead11-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ead11-166">MOF</span><span class="sxs-lookup"><span data-stu-id="ead11-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ead11-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ead11-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ead11-168">DLL</span><span class="sxs-lookup"><span data-stu-id="ead11-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ead11-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ead11-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ead11-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ead11-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead11-171">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ead11-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ead11-172">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ead11-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="ead11-173">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="ead11-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

