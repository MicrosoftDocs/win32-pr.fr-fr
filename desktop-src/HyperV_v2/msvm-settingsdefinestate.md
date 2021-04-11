---
description: Associe un ordinateur virtuel et ses appareils à des instances de CIM \_ SettingData qui représentent les paramètres actuels qui s’appliquent à ces objets.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Classe Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203602"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="c5ac2-103">MSVM \_ SettingsDefineState, classe</span><span class="sxs-lookup"><span data-stu-id="c5ac2-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="c5ac2-104">Associe un ordinateur virtuel et ses appareils à des instances de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) qui représentent les paramètres actuels qui s’appliquent à ces objets.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="c5ac2-105">Plus spécifiquement, il associe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) à des instances de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)et associe \*\* \_ \* MSVM\* _ DERIVES de [_ *CIM \_ LogicalDevice* \*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) avec les dérivés \**MSVM \_ \** _ de [_ *CIM \_ ResourceAllocationSettingData* \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c5ac2-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="c5ac2-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ac2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5ac2-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="c5ac2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c5ac2-108">Members</span></span>

<span data-ttu-id="c5ac2-109">La classe **MSVM \_ SettingsDefineState** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c5ac2-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="c5ac2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c5ac2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5ac2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c5ac2-111">Properties</span></span>

<span data-ttu-id="c5ac2-112">La classe **MSVM \_ SettingsDefineState** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5ac2-113">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5ac2-114">Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c5ac2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5ac2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5ac2-116">Référence à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c5ac2-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5ac2-118">Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c5ac2-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5ac2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5ac2-120">Référence aux paramètres actuellement actifs pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5ac2-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c5ac2-121">Remarks</span></span>

<span data-ttu-id="c5ac2-122">L’accès à la classe **MSVM \_ SettingsDefineState** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="c5ac2-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c5ac2-123">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c5ac2-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ac2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5ac2-124">Requirements</span></span>



| <span data-ttu-id="c5ac2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5ac2-125">Requirement</span></span> | <span data-ttu-id="c5ac2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5ac2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ac2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5ac2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ac2-128">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5ac2-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c5ac2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5ac2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ac2-130">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5ac2-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c5ac2-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c5ac2-131">Namespace</span></span><br/>                | <span data-ttu-id="c5ac2-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5ac2-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c5ac2-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c5ac2-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5ac2-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac2-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5ac2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ac2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ac2-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac2-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5ac2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5ac2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ac2-138">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="c5ac2-139">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="c5ac2-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="c5ac2-140">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="c5ac2-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

