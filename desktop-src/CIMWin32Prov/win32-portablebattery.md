---
description: La \_ classe WMI PortableBattery WMI contient les propriétés associées à une batterie portable, telle qu’une batterie d’ordinateurs notebook.
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Classe Win32_PortableBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747909"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="e262c-103">\_Classe PortableBattery Win32</span><span class="sxs-lookup"><span data-stu-id="e262c-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="e262c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortableBattery** WMI contient les propriétés associées à une batterie portable, telle qu’une batterie d’ordinateurs notebook.</span><span class="sxs-lookup"><span data-stu-id="e262c-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="e262c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e262c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e262c-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e262c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e262c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e262c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
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
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
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

## <a name="members"></a><span data-ttu-id="e262c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e262c-108">Members</span></span>

<span data-ttu-id="e262c-109">La classe **Win32 \_ PortableBattery** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e262c-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="e262c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e262c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e262c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e262c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e262c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e262c-112">Methods</span></span>

<span data-ttu-id="e262c-113">La classe **Win32 \_ PortableBattery** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e262c-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="e262c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="e262c-114">Method</span></span>            | <span data-ttu-id="e262c-115">Description</span><span class="sxs-lookup"><span data-stu-id="e262c-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e262c-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="e262c-116">**Reset**</span></span>         | <span data-ttu-id="e262c-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e262c-117">Not implemented.</span></span> <span data-ttu-id="e262c-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="e262c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e262c-119">**SetPowerState**</span></span> | <span data-ttu-id="e262c-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e262c-120">Not implemented.</span></span> <span data-ttu-id="e262c-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e262c-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e262c-122">Properties</span></span>

<span data-ttu-id="e262c-123">La classe **Win32 \_ PortableBattery** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e262c-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e262c-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="e262c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e262c-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-128">Availability and status of the device.</span></span>

<span data-ttu-id="e262c-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e262c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e262c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e262c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e262c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e262c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="e262c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="e262c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e262c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="e262c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e262c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="e262c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e262c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="e262c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e262c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="e262c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e262c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="e262c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e262c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="e262c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e262c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="e262c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e262c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="e262c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e262c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="e262c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e262c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="e262c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e262c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e262c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="e262c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="e262c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e262c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="e262c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="e262c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e262c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="e262c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e262c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="e262c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="e262c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e262c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="e262c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="e262c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e262c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="e262c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="e262c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e262c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="e262c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="e262c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e262c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="e262c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="e262c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="e262c-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-163">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="e262c-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-164">Description de l’état de facturation de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-164">Description of the battery's charge status.</span></span> <span data-ttu-id="e262c-165">La valeur 10 (non définie) n’est pas valide dans le schéma Common Information Model (CIM), car dans DMI (Desktop Management Interface), cela indique qu’aucune batterie n’est installée.</span><span class="sxs-lookup"><span data-stu-id="e262c-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="e262c-166">Dans ce cas, cet objet ne doit pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="e262c-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="e262c-167">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e262c-168">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e262c-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e262c-169">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e262c-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="e262c-170">**Entièrement facturée** (3)</span><span class="sxs-lookup"><span data-stu-id="e262c-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="e262c-171">**Faible** (4)</span><span class="sxs-lookup"><span data-stu-id="e262c-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e262c-172">**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="e262c-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="e262c-173">En **charge** (6)</span><span class="sxs-lookup"><span data-stu-id="e262c-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="e262c-174">En **charge et élevé** (7)</span><span class="sxs-lookup"><span data-stu-id="e262c-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="e262c-175">En **charge et bas** (8)</span><span class="sxs-lookup"><span data-stu-id="e262c-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="e262c-176">En **charge et critique** (9)</span><span class="sxs-lookup"><span data-stu-id="e262c-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e262c-177">**Non défini** (10)</span><span class="sxs-lookup"><span data-stu-id="e262c-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="e262c-178">**Partiellement facturé** (11)</span><span class="sxs-lookup"><span data-stu-id="e262c-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-179">**CapacityMultiplier**</span><span class="sxs-lookup"><span data-stu-id="e262c-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-180">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-182">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 22 \| multiplicateur de capacité de conception")</span><span class="sxs-lookup"><span data-stu-id="e262c-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-183">Facteur de multiplication de la valeur **DesignCapacity** pour garantir que la valeur de l’heure du milliwatts heure ne dépasse pas les implémentations de la spécification de données de la batterie intelligente (sbds).</span><span class="sxs-lookup"><span data-stu-id="e262c-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="e262c-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e262c-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-187">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="e262c-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-188">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="e262c-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="e262c-189">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-190">**Chimique**</span><span class="sxs-lookup"><span data-stu-id="e262c-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-193">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="e262c-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-194">Chimie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-194">Chemistry of the battery.</span></span>

<span data-ttu-id="e262c-195">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e262c-196">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e262c-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e262c-197">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e262c-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="e262c-198">**Acidité** (3)</span><span class="sxs-lookup"><span data-stu-id="e262c-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="e262c-199">**Nickel cadmium** (4)</span><span class="sxs-lookup"><span data-stu-id="e262c-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="e262c-200">**Nickel-métal-hydrure** (5)</span><span class="sxs-lookup"><span data-stu-id="e262c-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="e262c-201">**Lithium-ion** (6)</span><span class="sxs-lookup"><span data-stu-id="e262c-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="e262c-202">**Air zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="e262c-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="e262c-203">**Lithium-polymère** (8)</span><span class="sxs-lookup"><span data-stu-id="e262c-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-204">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e262c-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-205">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-207">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e262c-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-208">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="e262c-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e262c-209">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e262c-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="e262c-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e262c-211"> (0)</span><span class="sxs-lookup"><span data-stu-id="e262c-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-212">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="e262c-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e262c-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="e262c-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e262c-214">(1)</span><span class="sxs-lookup"><span data-stu-id="e262c-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-215">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="e262c-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e262c-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e262c-217">(2)</span><span class="sxs-lookup"><span data-stu-id="e262c-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e262c-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="e262c-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e262c-219">(3)</span><span class="sxs-lookup"><span data-stu-id="e262c-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-220">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="e262c-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e262c-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="e262c-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e262c-222">(4)</span><span class="sxs-lookup"><span data-stu-id="e262c-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-223">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e262c-223">Device is not working properly.</span></span> <span data-ttu-id="e262c-224">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="e262c-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e262c-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="e262c-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e262c-226">(5)</span><span class="sxs-lookup"><span data-stu-id="e262c-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-227">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="e262c-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e262c-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="e262c-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e262c-229"> (6)</span><span class="sxs-lookup"><span data-stu-id="e262c-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-230">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="e262c-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e262c-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="e262c-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e262c-232">(7)</span><span class="sxs-lookup"><span data-stu-id="e262c-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e262c-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="e262c-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e262c-234">(8)</span><span class="sxs-lookup"><span data-stu-id="e262c-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-235">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="e262c-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e262c-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e262c-237">(9)</span><span class="sxs-lookup"><span data-stu-id="e262c-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-238">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e262c-238">Device is not working properly.</span></span> <span data-ttu-id="e262c-239">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e262c-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e262c-241">(10)</span><span class="sxs-lookup"><span data-stu-id="e262c-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-242">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e262c-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e262c-244">(11)</span><span class="sxs-lookup"><span data-stu-id="e262c-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-245">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e262c-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="e262c-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e262c-247">douze</span><span class="sxs-lookup"><span data-stu-id="e262c-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-248">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e262c-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e262c-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e262c-250">(13)</span><span class="sxs-lookup"><span data-stu-id="e262c-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-251">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e262c-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="e262c-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e262c-253">(14)</span><span class="sxs-lookup"><span data-stu-id="e262c-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-254">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="e262c-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e262c-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="e262c-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e262c-256">(15)</span><span class="sxs-lookup"><span data-stu-id="e262c-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-257">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="e262c-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e262c-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e262c-259">(16)</span><span class="sxs-lookup"><span data-stu-id="e262c-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-260">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e262c-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="e262c-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e262c-262">(17)</span><span class="sxs-lookup"><span data-stu-id="e262c-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-263">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="e262c-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e262c-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e262c-265">(18)</span><span class="sxs-lookup"><span data-stu-id="e262c-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-266">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="e262c-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e262c-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="e262c-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e262c-268">(19)</span><span class="sxs-lookup"><span data-stu-id="e262c-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e262c-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="e262c-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e262c-270">(20)</span><span class="sxs-lookup"><span data-stu-id="e262c-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-271">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="e262c-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e262c-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e262c-273">(21)</span><span class="sxs-lookup"><span data-stu-id="e262c-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-274">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="e262c-274">System failure.</span></span> <span data-ttu-id="e262c-275">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="e262c-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e262c-276">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e262c-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="e262c-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e262c-278">(22)</span><span class="sxs-lookup"><span data-stu-id="e262c-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-279">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e262c-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e262c-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="e262c-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e262c-281">(23)</span><span class="sxs-lookup"><span data-stu-id="e262c-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-282">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="e262c-282">System failure.</span></span> <span data-ttu-id="e262c-283">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="e262c-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e262c-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="e262c-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e262c-285">(24)</span><span class="sxs-lookup"><span data-stu-id="e262c-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-286">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="e262c-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e262c-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e262c-288">(25)</span><span class="sxs-lookup"><span data-stu-id="e262c-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-289">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e262c-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e262c-291">(26)</span><span class="sxs-lookup"><span data-stu-id="e262c-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-292">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e262c-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e262c-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="e262c-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e262c-294">(27)</span><span class="sxs-lookup"><span data-stu-id="e262c-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-295">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="e262c-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e262c-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="e262c-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e262c-297">(28)</span><span class="sxs-lookup"><span data-stu-id="e262c-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-298">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="e262c-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e262c-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="e262c-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e262c-300">(29)</span><span class="sxs-lookup"><span data-stu-id="e262c-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-301">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e262c-301">Device is disabled.</span></span> <span data-ttu-id="e262c-302">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="e262c-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e262c-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="e262c-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e262c-304">(30)</span><span class="sxs-lookup"><span data-stu-id="e262c-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-305">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="e262c-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e262c-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e262c-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e262c-307">31</span><span class="sxs-lookup"><span data-stu-id="e262c-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-308">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e262c-308">Device is not working properly.</span></span> <span data-ttu-id="e262c-309">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="e262c-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-310">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e262c-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-311">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e262c-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-313">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e262c-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-314">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e262c-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e262c-315">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e262c-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-319">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e262c-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e262c-320">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="e262c-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e262c-321">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e262c-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e262c-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-323">**Description**</span><span class="sxs-lookup"><span data-stu-id="e262c-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-326">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e262c-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-327">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e262c-327">Description of the object.</span></span>

<span data-ttu-id="e262c-328">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-329">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="e262c-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-330">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-332">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,8 "), [**unités**](../wmisdk/standard-qualifiers.md) (" milliwatts heure-heures ")</span><span class="sxs-lookup"><span data-stu-id="e262c-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-333">Capacité de conception de la batterie en milliwatts heure-heures.</span><span class="sxs-lookup"><span data-stu-id="e262c-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="e262c-334">Si cette propriété n’est pas prise en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e262c-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="e262c-335">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-336">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="e262c-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-337">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e262c-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-339">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,9 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="e262c-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-340">Tension de conception de la batterie en millivolts.</span><span class="sxs-lookup"><span data-stu-id="e262c-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="e262c-341">Si cet attribut n’est pas pris en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e262c-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="e262c-342">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="e262c-343">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-344">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e262c-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-347">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="e262c-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-348">Identificateur de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-348">Battery identifier.</span></span>

<span data-ttu-id="e262c-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e262c-350">Exemple : « batterie interne »</span><span class="sxs-lookup"><span data-stu-id="e262c-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="e262c-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e262c-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-352">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e262c-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e262c-354">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="e262c-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e262c-355">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e262c-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-357">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e262c-359">Informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et toutes les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="e262c-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="e262c-360">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-361">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="e262c-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-362">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-364">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) ("pourcentage")</span><span class="sxs-lookup"><span data-stu-id="e262c-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-365">Estimation du pourcentage de facturation totale restante.</span><span class="sxs-lookup"><span data-stu-id="e262c-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="e262c-366">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="e262c-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-368">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-370">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,15 "), [**unités**](../wmisdk/standard-qualifiers.md) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="e262c-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-371">Estimation en minutes du temps de l’épuisement de la charge de la batterie dans les conditions de charge actuelles si l’alimentation de l’utilitaire est désactivée, perdue et conservée, ou un ordinateur portable est déconnecté d’une source d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e262c-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="e262c-372">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-373">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="e262c-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-374">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e262c-376">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e262c-376">Not supported.</span></span>

<span data-ttu-id="e262c-377">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-378">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="e262c-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-379">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-381">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="e262c-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-382">Durée de vie prévue de la batterie en minutes, en supposant que la batterie est entièrement chargée.</span><span class="sxs-lookup"><span data-stu-id="e262c-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="e262c-383">Cette propriété représente la durée de vie totale attendue de la batterie, pas sa durée de vie restante, qui est indiquée par la propriété **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="e262c-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="e262c-384">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-385">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="e262c-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-386">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-388">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,11 "), [**unités**](../wmisdk/standard-qualifiers.md) (" milliwatts heure-heures ")</span><span class="sxs-lookup"><span data-stu-id="e262c-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-389">Capacité de charge totale de la batterie en milliwatts heure-heures.</span><span class="sxs-lookup"><span data-stu-id="e262c-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="e262c-390">La comparaison de cette valeur à la propriété **DesignCapacity** détermine le moment où la batterie doit être remplacée.</span><span class="sxs-lookup"><span data-stu-id="e262c-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="e262c-391">La fin de vie d’une batterie se produit généralement lorsque la propriété **FullChargeCapacity** passe sous 80% de la propriété **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="e262c-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="e262c-392">Si cette propriété n’est pas prise en charge, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e262c-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="e262c-393">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e262c-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-395">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e262c-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-397">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e262c-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-398">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e262c-398">Date and time the object was installed.</span></span> <span data-ttu-id="e262c-399">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="e262c-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e262c-400">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-401">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e262c-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-402">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e262c-404">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e262c-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e262c-405">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-406">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="e262c-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-407">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-409">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 22 \| location")</span><span class="sxs-lookup"><span data-stu-id="e262c-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-410">Emplacement physique de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-410">Physical location of the battery.</span></span> <span data-ttu-id="e262c-411">Cette propriété est renseignée par le fabricant de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e262c-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="e262c-412">Exemple : « à l’arrière, à gauche »</span><span class="sxs-lookup"><span data-stu-id="e262c-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="e262c-413">**Fabrication**</span><span class="sxs-lookup"><span data-stu-id="e262c-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-414">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-416">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 22 \| manufacture date")</span><span class="sxs-lookup"><span data-stu-id="e262c-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-417">Date de fabrication de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="e262c-418">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="e262c-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-419">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-421">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 22 \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="e262c-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-422">Fabricant de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="e262c-423">**MaxBatteryError**</span><span class="sxs-lookup"><span data-stu-id="e262c-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-424">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-426">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 22 \| Error maximal in Data Battery"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span><span class="sxs-lookup"><span data-stu-id="e262c-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-427">Différence entre la quantité d’énergie restante la plus élevée dans la batterie et la quantité actuelle indiquée par la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="e262c-428">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="e262c-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-429">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-431">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="e262c-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-432">Durée maximale, en minutes, pour le chargement complet de la batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="e262c-433">Cette propriété représente le temps de rechargement d’une batterie entièrement épuisée, et non le temps de facturation restant actuel, qui est indiqué dans la propriété **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="e262c-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="e262c-434">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-435">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e262c-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-438">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e262c-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-439">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="e262c-439">Label by which the object is known.</span></span> <span data-ttu-id="e262c-440">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="e262c-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e262c-441">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e262c-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-445">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e262c-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-446">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e262c-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e262c-447">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e262c-448">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="e262c-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e262c-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e262c-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-450">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e262c-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e262c-452">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="e262c-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e262c-453">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="e262c-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e262c-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e262c-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e262c-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e262c-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e262c-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="e262c-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e262c-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="e262c-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-458">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e262c-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e262c-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="e262c-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-460">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="e262c-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e262c-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="e262c-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-462">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e262c-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e262c-463">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="e262c-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e262c-464">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e262c-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="e262c-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-466">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="e262c-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e262c-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="e262c-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e262c-468">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="e262c-468">Timed Power-On Supported</span></span>

<span data-ttu-id="e262c-469">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="e262c-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e262c-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-471">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e262c-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e262c-473">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="e262c-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="e262c-474">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e262c-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="e262c-475">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-476">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="e262c-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-477">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-478">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-479">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="e262c-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-480">Numéro de version de la spécification de données de batterie intelligente prise en charge par cette batterie.</span><span class="sxs-lookup"><span data-stu-id="e262c-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="e262c-481">Si la batterie ne prend pas en charge cette fonction, la valeur doit être laissée vide.</span><span class="sxs-lookup"><span data-stu-id="e262c-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="e262c-482">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-483">**État**</span><span class="sxs-lookup"><span data-stu-id="e262c-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-484">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-485">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-486">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e262c-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-487">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e262c-487">Current status of the object.</span></span> <span data-ttu-id="e262c-488">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="e262c-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e262c-489">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="e262c-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e262c-490">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e262c-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e262c-491">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e262c-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e262c-492">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e262c-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e262c-493">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e262c-494">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e262c-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e262c-495">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e262c-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e262c-496">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e262c-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e262c-497">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e262c-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e262c-498">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e262c-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e262c-499">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e262c-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e262c-500">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e262c-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e262c-501">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e262c-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e262c-502">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e262c-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e262c-503">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e262c-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e262c-504">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e262c-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e262c-505">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e262c-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e262c-506">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e262c-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e262c-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-508">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e262c-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-510">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e262c-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-511">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e262c-511">State of the logical device.</span></span> <span data-ttu-id="e262c-512">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e262c-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e262c-513">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e262c-514">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e262c-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e262c-515">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e262c-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e262c-516">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="e262c-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e262c-517">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="e262c-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e262c-518">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="e262c-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e262c-519">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e262c-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-521">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-522">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e262c-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e262c-523">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e262c-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e262c-524">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-525">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e262c-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-526">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e262c-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-527">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-528">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e262c-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e262c-529">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e262c-529">Name of the scoping system.</span></span>

<span data-ttu-id="e262c-530">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-531">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="e262c-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-532">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-533">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-534">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="e262c-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-535">Durée écoulée en secondes depuis le dernier redémarrage de l’onduleur du système de l’ordinateur, selon la valeur la plus petite du système ou de l’onduleur.</span><span class="sxs-lookup"><span data-stu-id="e262c-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="e262c-536">Si la batterie est en ligne, la valeur 0 (zéro) est retournée.</span><span class="sxs-lookup"><span data-stu-id="e262c-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="e262c-537">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="e262c-538">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="e262c-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262c-539">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e262c-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e262c-540">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e262c-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262c-541">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batterie portable DMTF \| 002,16 "), [**unités**](../wmisdk/standard-qualifiers.md) (" minutes ")</span><span class="sxs-lookup"><span data-stu-id="e262c-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="e262c-542">Durée restante en minutes pour charger entièrement la batterie au tarif et à l’utilisation actuels.</span><span class="sxs-lookup"><span data-stu-id="e262c-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="e262c-543">Cette propriété est héritée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e262c-544">Notes</span><span class="sxs-lookup"><span data-stu-id="e262c-544">Remarks</span></span>

<span data-ttu-id="e262c-545">La classe **Win32 \_ PortableBattery** est dérivée de la [**\_ batterie CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="e262c-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e262c-546">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e262c-546">Requirements</span></span>



| <span data-ttu-id="e262c-547">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e262c-547">Requirement</span></span> | <span data-ttu-id="e262c-548">Valeur</span><span class="sxs-lookup"><span data-stu-id="e262c-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e262c-549">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e262c-549">Minimum supported client</span></span><br/> | <span data-ttu-id="e262c-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e262c-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e262c-551">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e262c-551">Minimum supported server</span></span><br/> | <span data-ttu-id="e262c-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e262c-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e262c-553">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e262c-553">Namespace</span></span><br/>                | <span data-ttu-id="e262c-554">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e262c-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e262c-555">MOF</span><span class="sxs-lookup"><span data-stu-id="e262c-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e262c-556"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e262c-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e262c-557">DLL</span><span class="sxs-lookup"><span data-stu-id="e262c-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e262c-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e262c-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e262c-559">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e262c-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e262c-560">**\_Batterie CIM**</span><span class="sxs-lookup"><span data-stu-id="e262c-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="e262c-561">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="e262c-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
