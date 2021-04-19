---
description: La \_ classe WMI du clavier Win32 représente un clavier installé sur un système informatique exécutant Windows.
ms.assetid: f42a8e4f-3db9-4f9a-88ca-336ec883e85b
ms.tgt_platform: multiple
title: Classe Win32_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Keyboard
- Win32_Keyboard.Reset
- Win32_Keyboard.SetPowerState
- Win32_Keyboard.Availability
- Win32_Keyboard.Caption
- Win32_Keyboard.ConfigManagerErrorCode
- Win32_Keyboard.ConfigManagerUserConfig
- Win32_Keyboard.CreationClassName
- Win32_Keyboard.Description
- Win32_Keyboard.DeviceID
- Win32_Keyboard.ErrorCleared
- Win32_Keyboard.ErrorDescription
- Win32_Keyboard.InstallDate
- Win32_Keyboard.IsLocked
- Win32_Keyboard.LastErrorCode
- Win32_Keyboard.Layout
- Win32_Keyboard.Name
- Win32_Keyboard.NumberOfFunctionKeys
- Win32_Keyboard.Password
- Win32_Keyboard.PNPDeviceID
- Win32_Keyboard.PowerManagementCapabilities
- Win32_Keyboard.PowerManagementSupported
- Win32_Keyboard.Status
- Win32_Keyboard.StatusInfo
- Win32_Keyboard.SystemCreationClassName
- Win32_Keyboard.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d011b6757ffa3b9378421f29cde3cb77cc04789
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516583"
---
# <a name="win32_keyboard-class"></a><span data-ttu-id="9861e-103">\_Classe de clavier Win32</span><span class="sxs-lookup"><span data-stu-id="9861e-103">Win32\_Keyboard class</span></span>

<span data-ttu-id="9861e-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) du **\_ clavier Win32** représente un clavier installé sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="9861e-104">The **Win32\_Keyboard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a keyboard installed on a computer system running Windows.</span></span>

<span data-ttu-id="9861e-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9861e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9861e-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9861e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9861e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9861e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Keyboard : CIM_Keyboard
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Layout;
  string   Name;
  uint16   NumberOfFunctionKeys;
  uint16   Password;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9861e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9861e-108">Members</span></span>

<span data-ttu-id="9861e-109">La classe de **\_ clavier Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9861e-109">The **Win32\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="9861e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9861e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9861e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9861e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9861e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9861e-112">Methods</span></span>

<span data-ttu-id="9861e-113">La classe de **\_ clavier Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9861e-113">The **Win32\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="9861e-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="9861e-114">Method</span></span>            | <span data-ttu-id="9861e-115">Description</span><span class="sxs-lookup"><span data-stu-id="9861e-115">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9861e-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="9861e-116">**Reset**</span></span>         | <span data-ttu-id="9861e-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="9861e-117">Not implemented.</span></span> <span data-ttu-id="9861e-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans le [**\_ clavier CIM**](cim-keyboard.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="9861e-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Keyboard**](cim-keyboard.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="9861e-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9861e-119">**SetPowerState**</span></span> | <span data-ttu-id="9861e-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="9861e-120">Not implemented.</span></span> <span data-ttu-id="9861e-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans le [**\_ clavier CIM**](cim-keyboard.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="9861e-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Keyboard**](cim-keyboard.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9861e-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9861e-122">Properties</span></span>

<span data-ttu-id="9861e-123">La classe de **\_ clavier Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9861e-123">The **Win32\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9861e-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="9861e-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9861e-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-127">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9861e-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-128">Availability and status of the device.</span></span>

<span data-ttu-id="9861e-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9861e-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9861e-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9861e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9861e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9861e-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="9861e-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="9861e-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9861e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="9861e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9861e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="9861e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9861e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9861e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9861e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="9861e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9861e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="9861e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9861e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="9861e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9861e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="9861e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9861e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="9861e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9861e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="9861e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9861e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="9861e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="9861e-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9861e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="9861e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="9861e-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9861e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="9861e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="9861e-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9861e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="9861e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9861e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="9861e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="9861e-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9861e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="9861e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="9861e-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9861e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="9861e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="9861e-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9861e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="9861e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="9861e-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9861e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="9861e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="9861e-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9861e-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9861e-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-163">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="9861e-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-164">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="9861e-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="9861e-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9861e-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9861e-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-169">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9861e-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-170">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="9861e-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9861e-171">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9861e-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="9861e-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9861e-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="9861e-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-174">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="9861e-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9861e-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="9861e-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9861e-176">(1)</span><span class="sxs-lookup"><span data-stu-id="9861e-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-177">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="9861e-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9861e-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9861e-179">(2)</span><span class="sxs-lookup"><span data-stu-id="9861e-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9861e-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="9861e-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9861e-181">(3)</span><span class="sxs-lookup"><span data-stu-id="9861e-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-182">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="9861e-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9861e-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9861e-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9861e-184">(4)</span><span class="sxs-lookup"><span data-stu-id="9861e-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-185">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9861e-185">Device is not working properly.</span></span> <span data-ttu-id="9861e-186">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="9861e-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9861e-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="9861e-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9861e-188">(5)</span><span class="sxs-lookup"><span data-stu-id="9861e-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-189">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="9861e-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9861e-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="9861e-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9861e-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="9861e-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-192">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="9861e-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9861e-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="9861e-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9861e-194">(7)</span><span class="sxs-lookup"><span data-stu-id="9861e-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9861e-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="9861e-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9861e-196">(8)</span><span class="sxs-lookup"><span data-stu-id="9861e-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-197">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="9861e-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9861e-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9861e-199">(9)</span><span class="sxs-lookup"><span data-stu-id="9861e-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-200">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9861e-200">Device is not working properly.</span></span> <span data-ttu-id="9861e-201">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9861e-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9861e-203">(10)</span><span class="sxs-lookup"><span data-stu-id="9861e-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-204">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9861e-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9861e-206">(11)</span><span class="sxs-lookup"><span data-stu-id="9861e-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-207">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9861e-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="9861e-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9861e-209">douze</span><span class="sxs-lookup"><span data-stu-id="9861e-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-210">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9861e-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9861e-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9861e-212">(13)</span><span class="sxs-lookup"><span data-stu-id="9861e-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-213">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9861e-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="9861e-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9861e-215">(14)</span><span class="sxs-lookup"><span data-stu-id="9861e-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-216">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="9861e-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9861e-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="9861e-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9861e-218">(15)</span><span class="sxs-lookup"><span data-stu-id="9861e-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-219">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="9861e-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9861e-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9861e-221">(16)</span><span class="sxs-lookup"><span data-stu-id="9861e-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-222">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9861e-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="9861e-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9861e-224">(17)</span><span class="sxs-lookup"><span data-stu-id="9861e-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-225">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="9861e-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9861e-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9861e-227">(18)</span><span class="sxs-lookup"><span data-stu-id="9861e-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-228">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="9861e-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9861e-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="9861e-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9861e-230">(19)</span><span class="sxs-lookup"><span data-stu-id="9861e-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9861e-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="9861e-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9861e-232">(20)</span><span class="sxs-lookup"><span data-stu-id="9861e-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-233">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="9861e-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9861e-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9861e-235">(21)</span><span class="sxs-lookup"><span data-stu-id="9861e-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-236">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="9861e-236">System failure.</span></span> <span data-ttu-id="9861e-237">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="9861e-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9861e-238">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9861e-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="9861e-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9861e-240">(22)</span><span class="sxs-lookup"><span data-stu-id="9861e-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-241">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9861e-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9861e-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="9861e-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9861e-243">(23)</span><span class="sxs-lookup"><span data-stu-id="9861e-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="9861e-244">System failure.</span></span> <span data-ttu-id="9861e-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="9861e-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9861e-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9861e-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9861e-247">(24)</span><span class="sxs-lookup"><span data-stu-id="9861e-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-248">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="9861e-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9861e-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9861e-250">(25)</span><span class="sxs-lookup"><span data-stu-id="9861e-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-251">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9861e-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9861e-253">(26)</span><span class="sxs-lookup"><span data-stu-id="9861e-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-254">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9861e-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9861e-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="9861e-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9861e-256">(27)</span><span class="sxs-lookup"><span data-stu-id="9861e-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-257">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="9861e-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9861e-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="9861e-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9861e-259">(28)</span><span class="sxs-lookup"><span data-stu-id="9861e-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-260">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="9861e-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9861e-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="9861e-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9861e-262">(29)</span><span class="sxs-lookup"><span data-stu-id="9861e-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-263">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9861e-263">Device is disabled.</span></span> <span data-ttu-id="9861e-264">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="9861e-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9861e-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="9861e-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9861e-266">(30)</span><span class="sxs-lookup"><span data-stu-id="9861e-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-267">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="9861e-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9861e-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9861e-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9861e-269">31</span><span class="sxs-lookup"><span data-stu-id="9861e-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-270">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9861e-270">Device is not working properly.</span></span> <span data-ttu-id="9861e-271">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="9861e-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9861e-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9861e-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-273">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9861e-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-275">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9861e-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-276">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9861e-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9861e-277">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9861e-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-281">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9861e-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9861e-282">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9861e-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9861e-283">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="9861e-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="9861e-284">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-285">**Description**</span><span class="sxs-lookup"><span data-stu-id="9861e-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-288">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9861e-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-289">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9861e-289">Description of the object.</span></span>

<span data-ttu-id="9861e-290">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9861e-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-294">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9861e-294">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9861e-295">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9861e-295">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9861e-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9861e-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-298">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9861e-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-300">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="9861e-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="9861e-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9861e-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-305">Informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode**, et actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="9861e-305">More information about the error recorded in **LastErrorCode**, and corrective actions that may be taken.</span></span>

<span data-ttu-id="9861e-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9861e-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-308">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9861e-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-310">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="9861e-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-311">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9861e-311">Date and time the object was installed.</span></span> <span data-ttu-id="9861e-312">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="9861e-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9861e-313">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-314">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="9861e-314">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-315">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9861e-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-317">Si la **valeur est true**, l’appareil est verrouillé, ce qui empêche l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9861e-317">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="9861e-318">Cette propriété est héritée de la [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-318">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-319">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9861e-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-320">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9861e-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-322">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9861e-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9861e-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-324">**Disposition**</span><span class="sxs-lookup"><span data-stu-id="9861e-324">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-327">Chaîne de forme libre indiquant la disposition du clavier.</span><span class="sxs-lookup"><span data-stu-id="9861e-327">Free-form string indicating the layout of the keyboard.</span></span>

<span data-ttu-id="9861e-328">Cette propriété est héritée [**du \_ clavier CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-328">This property is inherited from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-329">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9861e-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-332">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9861e-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-333">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9861e-333">Label by which the object is known.</span></span> <span data-ttu-id="9861e-334">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="9861e-334">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9861e-335">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-336">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="9861e-336">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-337">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9861e-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-339">Nombre de touches de fonction sur le clavier.</span><span class="sxs-lookup"><span data-stu-id="9861e-339">Number of function keys on the keyboard.</span></span>

<span data-ttu-id="9861e-340">Cette propriété est héritée [**du \_ clavier CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-340">This property is inherited from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-341">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="9861e-341">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-342">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9861e-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-344">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="9861e-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-345">État du mot de passe au niveau du matériel activé sur le clavier (valeur = 4), empêchant l’entrée locale.</span><span class="sxs-lookup"><span data-stu-id="9861e-345">Status of hardware-level password enabled at the keyboard (value=4), preventing local input.</span></span>

<span data-ttu-id="9861e-346">Cette propriété est héritée [**du \_ clavier CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-346">This property is inherited from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9861e-347">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9861e-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9861e-348">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9861e-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9861e-349">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="9861e-349">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9861e-350">**Activé** (4)</span><span class="sxs-lookup"><span data-stu-id="9861e-350">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="9861e-351">**Non implémenté** (5)</span><span class="sxs-lookup"><span data-stu-id="9861e-351">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9861e-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9861e-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-355">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9861e-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-356">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9861e-356">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9861e-357">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9861e-358">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="9861e-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9861e-359">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9861e-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-360">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9861e-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9861e-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-362">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="9861e-362">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9861e-363">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="9861e-363">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9861e-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9861e-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9861e-365"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="9861e-365"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9861e-366"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="9861e-366"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9861e-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9861e-367"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-368">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="9861e-368">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9861e-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="9861e-369"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-370">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="9861e-370">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9861e-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="9861e-371"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-372">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9861e-372">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9861e-373">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="9861e-373">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9861e-374">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9861e-374">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9861e-375"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="9861e-375"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-376">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="9861e-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9861e-377"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="9861e-377"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9861e-378">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="9861e-378">Timed Power-On Supported</span></span>

<span data-ttu-id="9861e-379">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="9861e-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9861e-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9861e-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-381">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9861e-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9861e-383">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="9861e-383">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="9861e-384">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="9861e-384">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="9861e-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-386">**État**</span><span class="sxs-lookup"><span data-stu-id="9861e-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-389">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9861e-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-390">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9861e-390">Current status of the object.</span></span> <span data-ttu-id="9861e-391">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="9861e-391">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9861e-392">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="9861e-392">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9861e-393">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="9861e-393">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9861e-394">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="9861e-394">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9861e-395">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="9861e-395">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9861e-396">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-396">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9861e-397">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9861e-397">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9861e-398">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="9861e-398">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9861e-399">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="9861e-399">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9861e-400">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9861e-400">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9861e-401">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="9861e-401">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9861e-402">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9861e-402">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9861e-403">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9861e-403">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9861e-404">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9861e-404">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9861e-405">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="9861e-405">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9861e-406">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="9861e-406">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9861e-407">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="9861e-407">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9861e-408">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="9861e-408">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9861e-409">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="9861e-409">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9861e-410">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9861e-410">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-411">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9861e-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-413">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9861e-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9861e-414">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9861e-414">State of the logical device.</span></span> <span data-ttu-id="9861e-415">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9861e-415">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9861e-416">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-416">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9861e-417">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9861e-417">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9861e-418">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="9861e-418">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9861e-419">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="9861e-419">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9861e-420">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="9861e-420">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9861e-421">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9861e-421">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9861e-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9861e-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-423">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-425">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9861e-425">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9861e-426">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9861e-426">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="9861e-427">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9861e-428">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9861e-428">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9861e-429">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9861e-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9861e-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9861e-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9861e-431">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9861e-431">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9861e-432">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9861e-432">Name of the scoping system.</span></span>

<span data-ttu-id="9861e-433">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9861e-434">Notes</span><span class="sxs-lookup"><span data-stu-id="9861e-434">Remarks</span></span>

<span data-ttu-id="9861e-435">La classe de **\_ clavier Win32** est dérivée du [**\_ clavier CIM**](cim-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="9861e-435">The **Win32\_Keyboard** class is derived from [**CIM\_Keyboard**](cim-keyboard.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9861e-436">Exemples</span><span class="sxs-lookup"><span data-stu-id="9861e-436">Examples</span></span>

<span data-ttu-id="9861e-437">Le code PowerShell suivant détecte un clavier et une souris sans fil.</span><span class="sxs-lookup"><span data-stu-id="9861e-437">The following PowerShell code finds a wireless keyboard and mouse.</span></span>


```PowerShell
class = "win32_pointingdevice","win32_keyboard"

$class | % {gwmi $_ | ? description -match 'hid'} | ft description, PNPDeviceID -A -Wr
```



<span data-ttu-id="9861e-438">L’exemple VBScript suivant répertorie les propriétés du clavier.</span><span class="sxs-lookup"><span data-stu-id="9861e-438">The following VBScript sample lists the keyboard properties.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Keyboard") 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Is Locked: " & objItem.IsLocked 
    Wscript.Echo "Layout: " & objItem.Layout 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number of Function Keys: " & objItem.NumberOfFunctionKeys 
    Wscript.Echo "Password: " & objItem.Password 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
Next
```



## <a name="requirements"></a><span data-ttu-id="9861e-439">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9861e-439">Requirements</span></span>



| <span data-ttu-id="9861e-440">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9861e-440">Requirement</span></span> | <span data-ttu-id="9861e-441">Valeur</span><span class="sxs-lookup"><span data-stu-id="9861e-441">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9861e-442">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9861e-442">Minimum supported client</span></span><br/> | <span data-ttu-id="9861e-443">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9861e-443">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9861e-444">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9861e-444">Minimum supported server</span></span><br/> | <span data-ttu-id="9861e-445">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9861e-445">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9861e-446">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9861e-446">Namespace</span></span><br/>                | <span data-ttu-id="9861e-447">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9861e-447">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9861e-448">MOF</span><span class="sxs-lookup"><span data-stu-id="9861e-448">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9861e-449"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9861e-449"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9861e-450">DLL</span><span class="sxs-lookup"><span data-stu-id="9861e-450">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9861e-451"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9861e-451"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9861e-452">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9861e-452">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9861e-453">**\_Clavier CIM**</span><span class="sxs-lookup"><span data-stu-id="9861e-453">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dt>

[<span data-ttu-id="9861e-454">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="9861e-454">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

