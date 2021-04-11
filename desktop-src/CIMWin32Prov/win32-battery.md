---
description: Représente une batterie connectée au système de l’ordinateur.
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Classe Win32_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033766"
---
# <a name="win32_battery-class"></a><span data-ttu-id="bd239-103">\_Classe de batterie Win32</span><span class="sxs-lookup"><span data-stu-id="bd239-103">Win32\_Battery class</span></span>

<span data-ttu-id="bd239-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ batterie Win32** représente une batterie connectée au système informatique.</span><span class="sxs-lookup"><span data-stu-id="bd239-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="bd239-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bd239-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bd239-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bd239-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd239-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd239-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="bd239-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bd239-108">Members</span></span>

<span data-ttu-id="bd239-109">La classe de **\_ batterie Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bd239-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="bd239-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd239-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bd239-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bd239-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bd239-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd239-112">Methods</span></span>

<span data-ttu-id="bd239-113">La classe de **\_ batterie Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bd239-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="bd239-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="bd239-114">Method</span></span>            | <span data-ttu-id="bd239-115">Description</span><span class="sxs-lookup"><span data-stu-id="bd239-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd239-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="bd239-116">**Reset**</span></span>         | <span data-ttu-id="bd239-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="bd239-117">Not implemented.</span></span> <span data-ttu-id="bd239-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans la [**\_ batterie CIM**](cim-battery.md) pour la documentation.</span><span class="sxs-lookup"><span data-stu-id="bd239-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="bd239-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bd239-119">**SetPowerState**</span></span> | <span data-ttu-id="bd239-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="bd239-120">Not implemented.</span></span> <span data-ttu-id="bd239-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans la [**\_ batterie CIM**](cim-battery.md) pour la documentation.</span><span class="sxs-lookup"><span data-stu-id="bd239-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bd239-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bd239-122">Properties</span></span>

<span data-ttu-id="bd239-123">La classe de **\_ batterie Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bd239-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd239-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="bd239-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bd239-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-127">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="bd239-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-128">Availability and status of the device.</span></span>

<span data-ttu-id="bd239-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd239-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bd239-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd239-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="bd239-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bd239-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="bd239-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="bd239-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bd239-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="bd239-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bd239-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="bd239-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bd239-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="bd239-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bd239-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="bd239-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bd239-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="bd239-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bd239-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="bd239-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bd239-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="bd239-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bd239-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="bd239-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bd239-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="bd239-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bd239-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="bd239-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="bd239-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bd239-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="bd239-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="bd239-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bd239-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="bd239-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="bd239-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bd239-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="bd239-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bd239-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="bd239-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="bd239-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bd239-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="bd239-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="bd239-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bd239-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="bd239-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="bd239-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bd239-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="bd239-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="bd239-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bd239-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="bd239-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="bd239-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-160">**BatteryRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="bd239-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-163">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ local \_ machine \\ \\ System \\ \\ CurrentControlSet \\ \\ services \| recompresseur"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="bd239-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-164">Temps nécessaire pour charger entièrement la batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="bd239-165">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bd239-165">This property is not supported.</span></span> <span data-ttu-id="bd239-166">**BatteryRechargeTime** ne possède pas de propriété de remplacement et est désormais considéré comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="bd239-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="bd239-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="bd239-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bd239-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-170">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="bd239-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-171">État de la batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-171">Status of the battery.</span></span> <span data-ttu-id="bd239-172">La valeur 10 (non définie) n’est pas valide dans le schéma CIM, car dans DMI, elle indique qu’aucune batterie n’est installée.</span><span class="sxs-lookup"><span data-stu-id="bd239-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="bd239-173">Dans ce cas, l’objet ne doit pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="bd239-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="bd239-174">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd239-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bd239-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-176">La batterie est en décharge.</span><span class="sxs-lookup"><span data-stu-id="bd239-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd239-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="bd239-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-178">Le système a accès à AC et aucune batterie n’est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="bd239-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="bd239-179">Toutefois, la batterie n’est pas nécessairement en charge.</span><span class="sxs-lookup"><span data-stu-id="bd239-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="bd239-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Entièrement facturée** (3)</span><span class="sxs-lookup"><span data-stu-id="bd239-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="bd239-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (4)</span><span class="sxs-lookup"><span data-stu-id="bd239-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="bd239-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="bd239-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="bd239-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>En **charge** (6)</span><span class="sxs-lookup"><span data-stu-id="bd239-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="bd239-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>En **charge et élevé** (7)</span><span class="sxs-lookup"><span data-stu-id="bd239-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="bd239-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>En **charge et bas** (8)</span><span class="sxs-lookup"><span data-stu-id="bd239-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="bd239-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>En **charge et critique** (9)</span><span class="sxs-lookup"><span data-stu-id="bd239-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="bd239-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (10)</span><span class="sxs-lookup"><span data-stu-id="bd239-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="bd239-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partiellement facturé** (11)</span><span class="sxs-lookup"><span data-stu-id="bd239-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bd239-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="bd239-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-193">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="bd239-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="bd239-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-195">**Chimique**</span><span class="sxs-lookup"><span data-stu-id="bd239-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bd239-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-198">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="bd239-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-199">Énumération qui décrit la chimie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="bd239-200">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd239-201">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bd239-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd239-202">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="bd239-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="bd239-203">**Acidité** (3)</span><span class="sxs-lookup"><span data-stu-id="bd239-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="bd239-204">**Nickel cadmium** (4)</span><span class="sxs-lookup"><span data-stu-id="bd239-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="bd239-205">**Nickel-métal-hydrure** (5)</span><span class="sxs-lookup"><span data-stu-id="bd239-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="bd239-206">**Lithium-ion** (6)</span><span class="sxs-lookup"><span data-stu-id="bd239-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="bd239-207">**Air zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="bd239-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="bd239-208">**Lithium-polymère** (8)</span><span class="sxs-lookup"><span data-stu-id="bd239-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-209">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bd239-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-210">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-212">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bd239-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-213">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bd239-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="bd239-214">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bd239-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="bd239-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="bd239-216"> (0)</span><span class="sxs-lookup"><span data-stu-id="bd239-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-217">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="bd239-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bd239-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="bd239-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="bd239-219">(1)</span><span class="sxs-lookup"><span data-stu-id="bd239-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-220">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="bd239-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bd239-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bd239-222">(2)</span><span class="sxs-lookup"><span data-stu-id="bd239-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bd239-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="bd239-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bd239-224">(3)</span><span class="sxs-lookup"><span data-stu-id="bd239-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-225">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="bd239-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bd239-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="bd239-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bd239-227">(4)</span><span class="sxs-lookup"><span data-stu-id="bd239-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-228">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="bd239-228">Device is not working properly.</span></span> <span data-ttu-id="bd239-229">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="bd239-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bd239-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="bd239-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bd239-231">(5)</span><span class="sxs-lookup"><span data-stu-id="bd239-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-232">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="bd239-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bd239-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="bd239-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bd239-234"> (6)</span><span class="sxs-lookup"><span data-stu-id="bd239-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-235">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="bd239-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bd239-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="bd239-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="bd239-237">(7)</span><span class="sxs-lookup"><span data-stu-id="bd239-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bd239-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="bd239-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bd239-239">(8)</span><span class="sxs-lookup"><span data-stu-id="bd239-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-240">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="bd239-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bd239-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bd239-242">(9)</span><span class="sxs-lookup"><span data-stu-id="bd239-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-243">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="bd239-243">Device is not working properly.</span></span> <span data-ttu-id="bd239-244">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bd239-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="bd239-246">(10)</span><span class="sxs-lookup"><span data-stu-id="bd239-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-247">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bd239-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="bd239-249">(11)</span><span class="sxs-lookup"><span data-stu-id="bd239-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-250">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bd239-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="bd239-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bd239-252">douze</span><span class="sxs-lookup"><span data-stu-id="bd239-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-253">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bd239-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bd239-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bd239-255">(13)</span><span class="sxs-lookup"><span data-stu-id="bd239-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-256">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bd239-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="bd239-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bd239-258">(14)</span><span class="sxs-lookup"><span data-stu-id="bd239-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-259">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="bd239-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bd239-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="bd239-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bd239-261">(15)</span><span class="sxs-lookup"><span data-stu-id="bd239-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-262">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="bd239-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bd239-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bd239-264">(16)</span><span class="sxs-lookup"><span data-stu-id="bd239-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-265">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bd239-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="bd239-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bd239-267">(17)</span><span class="sxs-lookup"><span data-stu-id="bd239-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-268">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="bd239-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bd239-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bd239-270">(18)</span><span class="sxs-lookup"><span data-stu-id="bd239-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-271">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="bd239-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bd239-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="bd239-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="bd239-273">(19)</span><span class="sxs-lookup"><span data-stu-id="bd239-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bd239-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="bd239-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="bd239-275">(20)</span><span class="sxs-lookup"><span data-stu-id="bd239-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-276">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="bd239-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bd239-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bd239-278">(21)</span><span class="sxs-lookup"><span data-stu-id="bd239-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-279">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="bd239-279">System failure.</span></span> <span data-ttu-id="bd239-280">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="bd239-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="bd239-281">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bd239-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="bd239-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="bd239-283">(22)</span><span class="sxs-lookup"><span data-stu-id="bd239-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-284">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="bd239-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bd239-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="bd239-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bd239-286">(23)</span><span class="sxs-lookup"><span data-stu-id="bd239-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-287">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="bd239-287">System failure.</span></span> <span data-ttu-id="bd239-288">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="bd239-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bd239-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="bd239-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bd239-290">(24)</span><span class="sxs-lookup"><span data-stu-id="bd239-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-291">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="bd239-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bd239-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bd239-293">(25)</span><span class="sxs-lookup"><span data-stu-id="bd239-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-294">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bd239-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bd239-296">(26)</span><span class="sxs-lookup"><span data-stu-id="bd239-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-297">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd239-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bd239-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="bd239-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bd239-299">(27)</span><span class="sxs-lookup"><span data-stu-id="bd239-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-300">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="bd239-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bd239-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="bd239-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bd239-302">(28)</span><span class="sxs-lookup"><span data-stu-id="bd239-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-303">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="bd239-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bd239-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="bd239-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bd239-305">(29)</span><span class="sxs-lookup"><span data-stu-id="bd239-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-306">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="bd239-306">Device is disabled.</span></span> <span data-ttu-id="bd239-307">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="bd239-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bd239-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="bd239-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bd239-309">(30)</span><span class="sxs-lookup"><span data-stu-id="bd239-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-310">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="bd239-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bd239-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bd239-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bd239-312">31</span><span class="sxs-lookup"><span data-stu-id="bd239-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-313">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="bd239-313">Device is not working properly.</span></span> <span data-ttu-id="bd239-314">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="bd239-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-315">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="bd239-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-316">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd239-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-318">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bd239-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-319">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd239-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bd239-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-321">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd239-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-324">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd239-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd239-325">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="bd239-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="bd239-326">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="bd239-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="bd239-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-328">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd239-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-331">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="bd239-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-332">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd239-332">Description of the object.</span></span>

<span data-ttu-id="bd239-333">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-334">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="bd239-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-335">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts heure-heures ")</span><span class="sxs-lookup"><span data-stu-id="bd239-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-338">Capacité de conception de la batterie en milliwatts heure-heures.</span><span class="sxs-lookup"><span data-stu-id="bd239-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="bd239-339">Si la propriété n’est pas prise en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="bd239-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="bd239-340">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-341">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="bd239-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bd239-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-344">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,9 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="bd239-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-345">Tension de conception de la batterie en millivolts.</span><span class="sxs-lookup"><span data-stu-id="bd239-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="bd239-346">Si l’attribut n’est pas pris en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="bd239-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="bd239-347">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="bd239-348">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bd239-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bd239-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-352">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« DeviceID »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="bd239-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-353">Identifie la batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-353">Identifies the battery.</span></span>

<span data-ttu-id="bd239-354">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bd239-355">Exemple : « batterie interne »</span><span class="sxs-lookup"><span data-stu-id="bd239-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="bd239-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bd239-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-357">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd239-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd239-359">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="bd239-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="bd239-360">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bd239-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd239-364">Chaîne de forme libre qui fournit plus d’informations sur l’erreur enregistrée dans la propriété **LastErrorCode** , ainsi que des informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="bd239-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="bd239-365">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-366">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="bd239-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-367">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bd239-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-369">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pourcentage")</span><span class="sxs-lookup"><span data-stu-id="bd239-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-370">Estimation du pourcentage de facturation totale restante.</span><span class="sxs-lookup"><span data-stu-id="bd239-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="bd239-371">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="bd239-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-373">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-375">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="bd239-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-376">Estimation en minutes du temps de l’épuisement de la charge de la batterie dans les conditions de charge actuelles si l’alimentation de l’utilitaire est désactivée, perdue et conservée, ou un ordinateur portable est déconnecté d’une source d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="bd239-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="bd239-377">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-378">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="bd239-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-379">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-381">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ local \_ machine \\ \\ System \\ \\ CurrentControlSet \\ \\ services \| batterylife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="bd239-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-382">Durée nécessaire pour vider complètement la batterie une fois qu’elle est entièrement chargée.</span><span class="sxs-lookup"><span data-stu-id="bd239-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="bd239-383">Cette propriété n’est plus utilisée et est considérée comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="bd239-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="bd239-384">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="bd239-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-385">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-387">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="bd239-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-388">Durée de vie prévue de la batterie en minutes, en supposant que la batterie est entièrement chargée.</span><span class="sxs-lookup"><span data-stu-id="bd239-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="bd239-389">La propriété représente la durée de vie totale attendue de la batterie, pas sa durée de vie restante, qui est indiquée par la propriété **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="bd239-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="bd239-390">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-391">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="bd239-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-392">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatts heure-heures ")</span><span class="sxs-lookup"><span data-stu-id="bd239-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-395">Capacité de charge totale de la batterie en milliwatts heure-heures.</span><span class="sxs-lookup"><span data-stu-id="bd239-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="bd239-396">La comparaison de la valeur à la propriété **DesignCapacity** détermine le moment où la batterie doit être remplacée.</span><span class="sxs-lookup"><span data-stu-id="bd239-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="bd239-397">La fin de vie d’une batterie se produit généralement lorsque la propriété **FullChargeCapacity** passe sous 80% de la propriété **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="bd239-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="bd239-398">Si la propriété n’est pas prise en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="bd239-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="bd239-399">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bd239-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-401">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bd239-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-403">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="bd239-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-404">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd239-404">Date and time the object was installed.</span></span> <span data-ttu-id="bd239-405">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="bd239-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bd239-406">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-407">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bd239-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-408">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd239-410">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bd239-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bd239-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-412">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="bd239-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-413">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-415">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="bd239-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-416">Durée maximale, en minutes, pour le chargement complet de la batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="bd239-417">La propriété représente le temps de rechargement d’une batterie entièrement épuisée, et non le temps de facturation restant actuel, qui est indiqué dans la propriété **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="bd239-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="bd239-418">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-419">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bd239-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-422">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bd239-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-423">Définit l’étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="bd239-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="bd239-424">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="bd239-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="bd239-425">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bd239-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-429">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bd239-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-430">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bd239-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="bd239-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bd239-432">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="bd239-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="bd239-433">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bd239-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-434">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bd239-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd239-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd239-436">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="bd239-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="bd239-437">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="bd239-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd239-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="bd239-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bd239-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="bd239-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bd239-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="bd239-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bd239-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="bd239-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-442">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="bd239-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bd239-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="bd239-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-444">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="bd239-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bd239-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="bd239-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-446">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bd239-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="bd239-447">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="bd239-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="bd239-448">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="bd239-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bd239-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="bd239-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-450">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="bd239-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bd239-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="bd239-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bd239-452">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd239-452">Timed Power-On Supported</span></span>

<span data-ttu-id="bd239-453">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="bd239-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-454">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bd239-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-455">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd239-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd239-457">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="bd239-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="bd239-458">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="bd239-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="bd239-459">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-460">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="bd239-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-461">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-462">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-463">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="bd239-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-464">Numéro de version de la spécification de données pris en charge par la batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="bd239-465">Si la batterie ne prend pas en charge cette fonction, la valeur doit être laissée vide.</span><span class="sxs-lookup"><span data-stu-id="bd239-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="bd239-466">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-467">**État**</span><span class="sxs-lookup"><span data-stu-id="bd239-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-468">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-470">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="bd239-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-471">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd239-471">Current status of the object.</span></span> <span data-ttu-id="bd239-472">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="bd239-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bd239-473">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="bd239-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bd239-474">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="bd239-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bd239-475">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="bd239-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bd239-476">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="bd239-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bd239-477">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bd239-478">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd239-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bd239-479">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="bd239-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bd239-480">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="bd239-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bd239-481">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="bd239-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd239-482">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="bd239-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bd239-483">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="bd239-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bd239-484">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bd239-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bd239-485">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="bd239-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bd239-486">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="bd239-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bd239-487">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="bd239-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bd239-488">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="bd239-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bd239-489">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="bd239-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bd239-490">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="bd239-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bd239-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-492">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bd239-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-494">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bd239-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-495">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bd239-495">State of the logical device.</span></span> <span data-ttu-id="bd239-496">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bd239-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="bd239-497">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bd239-498">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bd239-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd239-499">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="bd239-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bd239-500">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="bd239-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bd239-501">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="bd239-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bd239-502">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="bd239-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd239-503">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd239-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-504">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-505">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-506">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd239-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd239-507">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="bd239-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="bd239-508">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-509">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bd239-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-510">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd239-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-511">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-512">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bd239-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bd239-513">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="bd239-513">Name of the scoping system.</span></span>

<span data-ttu-id="bd239-514">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-515">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="bd239-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-516">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-517">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-518">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="bd239-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-519">Durée écoulée en secondes depuis le dernier redémarrage de l’onduleur du système de l’ordinateur, selon la valeur la plus petite du système ou de l’onduleur.</span><span class="sxs-lookup"><span data-stu-id="bd239-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="bd239-520">Si la batterie est « en ligne », la valeur 0 (zéro) est retournée.</span><span class="sxs-lookup"><span data-stu-id="bd239-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="bd239-521">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd239-522">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="bd239-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd239-523">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd239-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd239-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd239-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd239-525">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batterie portable DMTF \| 002,16 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="bd239-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd239-526">Temps restant pour charger entièrement la batterie en quelques minutes à la vitesse de chargement et à l’utilisation actuelles.</span><span class="sxs-lookup"><span data-stu-id="bd239-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="bd239-527">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd239-528">Notes</span><span class="sxs-lookup"><span data-stu-id="bd239-528">Remarks</span></span>

<span data-ttu-id="bd239-529">La classe de **\_ batterie Win32** est dérivée de la [**\_ batterie CIM**](cim-battery.md) qui dérive de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bd239-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bd239-530">Windows Server 2008 contient les pilotes de l’onduleur (APC) dans le système d’exploitation, ce qui vous permet de traiter l’onduleur comme une alimentation de batterie.</span><span class="sxs-lookup"><span data-stu-id="bd239-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="bd239-531">Cela vous permet de surveiller l’état de l’onduleur à l’aide d’un script et de prendre les mesures nécessaires.</span><span class="sxs-lookup"><span data-stu-id="bd239-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="bd239-532">Exemples</span><span class="sxs-lookup"><span data-stu-id="bd239-532">Examples</span></span>

<span data-ttu-id="bd239-533">L’exemple de code [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell interroge la **\_ batterie Win32** pour déterminer s’il faut ou non basculer la connexion sans fil pour économiser de l’énergie.</span><span class="sxs-lookup"><span data-stu-id="bd239-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="bd239-534">L’exemple [List ups information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) perl répertorie des informations sur les sources d’alimentation sans coupure associées à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd239-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd239-535">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd239-535">Requirements</span></span>



| <span data-ttu-id="bd239-536">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd239-536">Requirement</span></span> | <span data-ttu-id="bd239-537">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd239-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd239-538">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd239-538">Minimum supported client</span></span><br/> | <span data-ttu-id="bd239-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd239-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd239-540">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd239-540">Minimum supported server</span></span><br/> | <span data-ttu-id="bd239-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd239-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd239-542">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bd239-542">Namespace</span></span><br/>                | <span data-ttu-id="bd239-543">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bd239-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd239-544">MOF</span><span class="sxs-lookup"><span data-stu-id="bd239-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd239-545"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd239-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd239-546">DLL</span><span class="sxs-lookup"><span data-stu-id="bd239-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd239-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd239-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd239-548">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd239-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd239-549">**\_Batterie CIM**</span><span class="sxs-lookup"><span data-stu-id="bd239-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="bd239-550">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="bd239-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

