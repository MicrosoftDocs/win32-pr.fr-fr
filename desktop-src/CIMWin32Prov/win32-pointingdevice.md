---
description: La \_ classe WMI PointingDevice WMI représente un périphérique d’entrée utilisé pour pointer vers et sélectionner des régions sur l’affichage d’un système informatique exécutant Windows.
ms.assetid: ed81abe3-3d8f-48aa-ab64-9e6c87e44f64
ms.tgt_platform: multiple
title: Classe Win32_PointingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PointingDevice
- Win32_PointingDevice.Reset
- Win32_PointingDevice.SetPowerState
- Win32_PointingDevice.Availability
- Win32_PointingDevice.Caption
- Win32_PointingDevice.ConfigManagerErrorCode
- Win32_PointingDevice.ConfigManagerUserConfig
- Win32_PointingDevice.CreationClassName
- Win32_PointingDevice.Description
- Win32_PointingDevice.DeviceID
- Win32_PointingDevice.DeviceInterface
- Win32_PointingDevice.DoubleSpeedThreshold
- Win32_PointingDevice.ErrorCleared
- Win32_PointingDevice.ErrorDescription
- Win32_PointingDevice.Handedness
- Win32_PointingDevice.HardwareType
- Win32_PointingDevice.InfFileName
- Win32_PointingDevice.InfSection
- Win32_PointingDevice.InstallDate
- Win32_PointingDevice.IsLocked
- Win32_PointingDevice.LastErrorCode
- Win32_PointingDevice.Manufacturer
- Win32_PointingDevice.Name
- Win32_PointingDevice.NumberOfButtons
- Win32_PointingDevice.PNPDeviceID
- Win32_PointingDevice.PointingType
- Win32_PointingDevice.PowerManagementCapabilities
- Win32_PointingDevice.PowerManagementSupported
- Win32_PointingDevice.QuadSpeedThreshold
- Win32_PointingDevice.Resolution
- Win32_PointingDevice.SampleRate
- Win32_PointingDevice.Status
- Win32_PointingDevice.StatusInfo
- Win32_PointingDevice.Synch
- Win32_PointingDevice.SystemCreationClassName
- Win32_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e4f2359e19476dfae111fc361f48e6f73d8cfac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512878"
---
# <a name="win32_pointingdevice-class"></a><span data-ttu-id="4e863-103">\_Classe PointingDevice Win32</span><span class="sxs-lookup"><span data-stu-id="4e863-103">Win32\_PointingDevice class</span></span>

<span data-ttu-id="4e863-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PointingDevice** WMI représente un périphérique d’entrée utilisé pour pointer vers et sélectionner des régions sur l’affichage d’un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="4e863-104">The **Win32\_PointingDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents an input device used to point to and select regions on the display of a computer system running Windows.</span></span> <span data-ttu-id="4e863-105">Tout appareil utilisé pour manipuler un pointeur ou pointer sur l’affichage sur un système d’ordinateur exécutant Windows est membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4e863-105">Any device used to manipulate a pointer, or point to the display on a computer system running Windows is a member of this class.</span></span>

<span data-ttu-id="4e863-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4e863-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4e863-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4e863-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e863-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e863-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PointingDevice : CIM_PointingDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DeviceInterface;
  uint32   DoubleSpeedThreshold;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  string   HardwareType;
  string   InfFileName;
  string   InfSection;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   QuadSpeedThreshold;
  uint32   Resolution;
  uint32   SampleRate;
  string   Status;
  uint16   StatusInfo;
  uint32   Synch;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="4e863-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4e863-109">Members</span></span>

<span data-ttu-id="4e863-110">La classe **Win32 \_ PointingDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4e863-110">The **Win32\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4e863-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4e863-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e863-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4e863-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e863-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4e863-113">Methods</span></span>

<span data-ttu-id="4e863-114">La classe **Win32 \_ PointingDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4e863-114">The **Win32\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="4e863-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="4e863-115">Method</span></span>            | <span data-ttu-id="4e863-116">Description</span><span class="sxs-lookup"><span data-stu-id="4e863-116">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e863-117">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="4e863-117">**Reset**</span></span>         | <span data-ttu-id="4e863-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="4e863-118">Not implemented.</span></span> <span data-ttu-id="4e863-119">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/>                 |
| <span data-ttu-id="4e863-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4e863-120">**SetPowerState**</span></span> | <span data-ttu-id="4e863-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="4e863-121">Not implemented.</span></span> <span data-ttu-id="4e863-122">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e863-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4e863-123">Properties</span></span>

<span data-ttu-id="4e863-124">La classe **Win32 \_ PointingDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4e863-124">The **Win32\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e863-125">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="4e863-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e863-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-128">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="4e863-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-129">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-129">Availability and status of the device.</span></span>

<span data-ttu-id="4e863-130">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e863-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4e863-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4e863-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4e863-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="4e863-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-134">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="4e863-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4e863-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="4e863-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4e863-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="4e863-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4e863-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="4e863-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4e863-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="4e863-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4e863-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="4e863-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4e863-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="4e863-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e863-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="4e863-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4e863-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="4e863-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4e863-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="4e863-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4e863-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="4e863-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="4e863-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4e863-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="4e863-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="4e863-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4e863-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="4e863-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-149">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="4e863-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4e863-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="4e863-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4e863-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="4e863-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4e863-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4e863-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="4e863-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="4e863-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4e863-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="4e863-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="4e863-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4e863-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="4e863-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="4e863-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4e863-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="4e863-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="4e863-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4e863-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-164">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="4e863-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-165">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e863-165">Short description of the object.</span></span>

<span data-ttu-id="4e863-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4e863-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-170">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4e863-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-171">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="4e863-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="4e863-172">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4e863-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="4e863-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4e863-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="4e863-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-175">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="4e863-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4e863-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="4e863-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4e863-177">(1)</span><span class="sxs-lookup"><span data-stu-id="4e863-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-178">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="4e863-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4e863-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4e863-180">(2)</span><span class="sxs-lookup"><span data-stu-id="4e863-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4e863-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="4e863-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4e863-182">(3)</span><span class="sxs-lookup"><span data-stu-id="4e863-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-183">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="4e863-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4e863-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="4e863-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4e863-185">(4)</span><span class="sxs-lookup"><span data-stu-id="4e863-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-186">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="4e863-186">Device is not working properly.</span></span> <span data-ttu-id="4e863-187">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="4e863-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4e863-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="4e863-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4e863-189">(5)</span><span class="sxs-lookup"><span data-stu-id="4e863-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-190">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="4e863-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4e863-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="4e863-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4e863-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="4e863-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-193">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="4e863-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4e863-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="4e863-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4e863-195">(7)</span><span class="sxs-lookup"><span data-stu-id="4e863-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4e863-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="4e863-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4e863-197">(8)</span><span class="sxs-lookup"><span data-stu-id="4e863-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-198">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="4e863-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4e863-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4e863-200">(9)</span><span class="sxs-lookup"><span data-stu-id="4e863-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-201">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="4e863-201">Device is not working properly.</span></span> <span data-ttu-id="4e863-202">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4e863-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4e863-204">(10)</span><span class="sxs-lookup"><span data-stu-id="4e863-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-205">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4e863-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4e863-207">(11)</span><span class="sxs-lookup"><span data-stu-id="4e863-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-208">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4e863-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="4e863-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4e863-210">douze</span><span class="sxs-lookup"><span data-stu-id="4e863-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-211">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4e863-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4e863-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4e863-213">(13)</span><span class="sxs-lookup"><span data-stu-id="4e863-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-214">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4e863-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="4e863-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4e863-216">(14)</span><span class="sxs-lookup"><span data-stu-id="4e863-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-217">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="4e863-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4e863-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="4e863-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4e863-219">(15)</span><span class="sxs-lookup"><span data-stu-id="4e863-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-220">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="4e863-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4e863-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4e863-222">(16)</span><span class="sxs-lookup"><span data-stu-id="4e863-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-223">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4e863-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="4e863-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4e863-225">(17)</span><span class="sxs-lookup"><span data-stu-id="4e863-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-226">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="4e863-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4e863-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4e863-228">(18)</span><span class="sxs-lookup"><span data-stu-id="4e863-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-229">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="4e863-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4e863-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="4e863-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4e863-231">(19)</span><span class="sxs-lookup"><span data-stu-id="4e863-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4e863-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="4e863-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4e863-233">(20)</span><span class="sxs-lookup"><span data-stu-id="4e863-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-234">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="4e863-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4e863-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4e863-236">(21)</span><span class="sxs-lookup"><span data-stu-id="4e863-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-237">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="4e863-237">System failure.</span></span> <span data-ttu-id="4e863-238">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="4e863-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4e863-239">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4e863-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="4e863-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4e863-241">(22)</span><span class="sxs-lookup"><span data-stu-id="4e863-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-242">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4e863-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4e863-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="4e863-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4e863-244">(23)</span><span class="sxs-lookup"><span data-stu-id="4e863-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-245">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="4e863-245">System failure.</span></span> <span data-ttu-id="4e863-246">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="4e863-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4e863-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="4e863-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4e863-248">(24)</span><span class="sxs-lookup"><span data-stu-id="4e863-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-249">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="4e863-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4e863-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4e863-251">(25)</span><span class="sxs-lookup"><span data-stu-id="4e863-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-252">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4e863-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4e863-254">(26)</span><span class="sxs-lookup"><span data-stu-id="4e863-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-255">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e863-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4e863-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="4e863-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4e863-257">(27)</span><span class="sxs-lookup"><span data-stu-id="4e863-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-258">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="4e863-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4e863-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="4e863-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4e863-260">(28)</span><span class="sxs-lookup"><span data-stu-id="4e863-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-261">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="4e863-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4e863-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="4e863-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4e863-263">(29)</span><span class="sxs-lookup"><span data-stu-id="4e863-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-264">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4e863-264">Device is disabled.</span></span> <span data-ttu-id="4e863-265">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="4e863-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4e863-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="4e863-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4e863-267">(30)</span><span class="sxs-lookup"><span data-stu-id="4e863-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-268">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="4e863-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4e863-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4e863-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4e863-270">31</span><span class="sxs-lookup"><span data-stu-id="4e863-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-271">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="4e863-271">Device is not working properly.</span></span> <span data-ttu-id="4e863-272">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="4e863-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4e863-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-274">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4e863-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-276">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4e863-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-277">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e863-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4e863-278">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e863-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-282">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4e863-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4e863-283">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="4e863-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4e863-284">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="4e863-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4e863-285">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-286">**Description**</span><span class="sxs-lookup"><span data-stu-id="4e863-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-289">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4e863-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-290">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e863-290">Description of the object.</span></span>

<span data-ttu-id="4e863-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4e863-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-295">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4e863-295">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-296">Identificateur unique du périphérique de pointage avec d’autres périphériques sur le système.</span><span class="sxs-lookup"><span data-stu-id="4e863-296">Unique identifier of the pointing device with other devices on the system.</span></span>

<span data-ttu-id="4e863-297">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-298">**DeviceInterface**</span><span class="sxs-lookup"><span data-stu-id="4e863-298">**DeviceInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-299">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e863-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-301">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 21 \| interface")</span><span class="sxs-lookup"><span data-stu-id="4e863-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 21\|Interface")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-302">Type d’interface utilisé pour le dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="4e863-302">Type of interface used for the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e863-303">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4e863-303">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-304">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4e863-304">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial"></span><span id="serial"></span><span id="SERIAL"></span>

<span data-ttu-id="4e863-305">**Série** (3)</span><span class="sxs-lookup"><span data-stu-id="4e863-305">**Serial** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="4e863-306">**PS/2** (4)</span><span class="sxs-lookup"><span data-stu-id="4e863-306">**PS/2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="4e863-307">**Infrarouge** (5)</span><span class="sxs-lookup"><span data-stu-id="4e863-307">**Infrared** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="4e863-308">**HP-HIL** (6)</span><span class="sxs-lookup"><span data-stu-id="4e863-308">**HP-HIL** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="4e863-309">**Souris bus** (7)</span><span class="sxs-lookup"><span data-stu-id="4e863-309">**Bus mouse** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB__Apple_Desktop_Bus_"></span><span id="adb__apple_desktop_bus_"></span><span id="ADB__APPLE_DESKTOP_BUS_"></span>

<span data-ttu-id="4e863-310">**ADB (Apple Desktop bus)** (8)</span><span class="sxs-lookup"><span data-stu-id="4e863-310">**ADB (Apple Desktop Bus)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_DB-9"></span><span id="bus_mouse_db-9"></span><span id="BUS_MOUSE_DB-9"></span>

<span data-ttu-id="4e863-311">**DB Mouse DB-9** (160)</span><span class="sxs-lookup"><span data-stu-id="4e863-311">**Bus mouse DB-9** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_micro-DIN"></span><span id="bus_mouse_micro-din"></span><span id="BUS_MOUSE_MICRO-DIN"></span>

<span data-ttu-id="4e863-312">**Souris bus micro-DIN** (161)</span><span class="sxs-lookup"><span data-stu-id="4e863-312">**Bus mouse micro-DIN** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="4e863-313">**USB** (162)</span><span class="sxs-lookup"><span data-stu-id="4e863-313">**USB** (162)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-314">**DoubleSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="4e863-314">**DoubleSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-315">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-317">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information Functions \| SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="4e863-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-318">Une des deux valeurs d’accélération.</span><span class="sxs-lookup"><span data-stu-id="4e863-318">One of two acceleration values.</span></span> <span data-ttu-id="4e863-319">La sensibilité du dispositif de pointage double (bascule de la première à la deuxième valeur) lorsque le dispositif de pointage déplace une distance supérieure à cette valeur de seuil.</span><span class="sxs-lookup"><span data-stu-id="4e863-319">The sensitivity of the pointing device doubles (toggles from the first to the second value) when the pointing device moves a distance greater than this threshold value.</span></span>

</dd> <dt>

<span data-ttu-id="4e863-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4e863-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-321">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4e863-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-323">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="4e863-323">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="4e863-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4e863-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-328">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="4e863-328">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="4e863-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-330">**Ergonomie**</span><span class="sxs-lookup"><span data-stu-id="4e863-330">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-331">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e863-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-333">Configuration du dispositif de pointage pour une opération à gauche ou à droite.</span><span class="sxs-lookup"><span data-stu-id="4e863-333">Configuration of the pointing device for left-hand or right-hand operation.</span></span>

<span data-ttu-id="4e863-334">Cette propriété est héritée de la [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-334">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4e863-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4e863-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (1)</span><span class="sxs-lookup"><span data-stu-id="4e863-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="4e863-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Bon fonctionnement** de la main (2)</span><span class="sxs-lookup"><span data-stu-id="4e863-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-338">Opération de Right-Handed</span><span class="sxs-lookup"><span data-stu-id="4e863-338">Right-Handed Operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="4e863-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Opération gauche** de la main (3)</span><span class="sxs-lookup"><span data-stu-id="4e863-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-340">Opération de Left-Handed</span><span class="sxs-lookup"><span data-stu-id="4e863-340">Left-Handed Operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-341">**HardwareType**</span><span class="sxs-lookup"><span data-stu-id="4e863-341">**HardwareType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-344">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ machine \\ \\ System \\ \\ ControlSet001 \\ \\ \\ \\ , classe de contrôle \| DriverDesc")</span><span class="sxs-lookup"><span data-stu-id="4e863-344">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\ControlSet001\\\\Control\\\\Class\|DriverDesc")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-345">Type de matériel utilisé pour le dispositif de pointage Windows.</span><span class="sxs-lookup"><span data-stu-id="4e863-345">Type of hardware used for the Windows pointing device.</span></span>

<span data-ttu-id="4e863-346">Exemple : « souris PS2 MICROSOFT »</span><span class="sxs-lookup"><span data-stu-id="4e863-346">Example: "MICROSOFT PS2 MOUSE"</span></span>

</dd> <dt>

<span data-ttu-id="4e863-347">**InfFileName**</span><span class="sxs-lookup"><span data-stu-id="4e863-347">**InfFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-350">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="4e863-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-351">Nom du fichier. inf du dispositif de pointage Windows.</span><span class="sxs-lookup"><span data-stu-id="4e863-351">Name of the .inf file for the Windows pointing device.</span></span>

<span data-ttu-id="4e863-352">Exemple : "AB. inf"</span><span class="sxs-lookup"><span data-stu-id="4e863-352">Example: "ab.inf"</span></span>

</dd> <dt>

<span data-ttu-id="4e863-353">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="4e863-353">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-356">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="4e863-356">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-357">Section du fichier. inf qui contient les informations de configuration du dispositif de pointage Windows.</span><span class="sxs-lookup"><span data-stu-id="4e863-357">Section of the .inf file that holds configuration information for the Windows pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="4e863-358">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e863-358">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-359">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e863-359">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-361">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="4e863-361">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-362">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e863-362">Date and time the object was installed.</span></span> <span data-ttu-id="4e863-363">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="4e863-363">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4e863-364">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-365">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="4e863-365">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-366">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4e863-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-368">Si la **valeur est true**, l’appareil est verrouillé, ce qui empêche l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e863-368">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="4e863-369">Cette propriété est héritée de la [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-369">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4e863-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-371">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-373">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4e863-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4e863-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-375">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="4e863-375">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-378">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="4e863-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-379">Nom du fabricant du processeur.</span><span class="sxs-lookup"><span data-stu-id="4e863-379">Name of the processor's manufacturer.</span></span>

<span data-ttu-id="4e863-380">Exemple : « GenuineSilicon »</span><span class="sxs-lookup"><span data-stu-id="4e863-380">Example: "GenuineSilicon"</span></span>

</dd> <dt>

<span data-ttu-id="4e863-381">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4e863-381">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-384">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4e863-384">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-385">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4e863-385">Label by which the object is known.</span></span> <span data-ttu-id="4e863-386">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="4e863-386">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="4e863-387">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-388">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="4e863-388">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-389">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="4e863-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-391">Nombre de boutons sur le dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="4e863-391">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="4e863-392">Cette propriété est héritée de la [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-392">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="4e863-393">Exemple : 2</span><span class="sxs-lookup"><span data-stu-id="4e863-393">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="4e863-394">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4e863-394">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-395">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-397">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4e863-397">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-398">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4e863-398">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4e863-399">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4e863-400">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="4e863-400">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4e863-401">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="4e863-401">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-402">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e863-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-404">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Périphérique de pointage DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="4e863-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-405">Type de dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="4e863-405">Type of pointing device.</span></span>

<span data-ttu-id="4e863-406">Cette propriété est héritée de la [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-406">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e863-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4e863-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4e863-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="4e863-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Souris** (3)</span><span class="sxs-lookup"><span data-stu-id="4e863-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="4e863-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Suivre la balle** (4)</span><span class="sxs-lookup"><span data-stu-id="4e863-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-411">Boule</span><span class="sxs-lookup"><span data-stu-id="4e863-411">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="4e863-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Point de suivi** (5)</span><span class="sxs-lookup"><span data-stu-id="4e863-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="4e863-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Point coulissant** (6)</span><span class="sxs-lookup"><span data-stu-id="4e863-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="4e863-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Pavé tactile** (7)</span><span class="sxs-lookup"><span data-stu-id="4e863-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="4e863-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Écran tactile** (8)</span><span class="sxs-lookup"><span data-stu-id="4e863-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="4e863-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Capteur de souris optique** (9)</span><span class="sxs-lookup"><span data-stu-id="4e863-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-417">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4e863-417">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-418">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e863-418">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e863-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-420">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="4e863-420">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4e863-421">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="4e863-421">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4e863-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4e863-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4e863-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e863-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="4e863-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4e863-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="4e863-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-426">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="4e863-426">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4e863-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="4e863-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-428">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="4e863-428">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4e863-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="4e863-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-430">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e863-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4e863-431">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="4e863-431">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4e863-432">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-432">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4e863-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="4e863-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-434">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="4e863-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4e863-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="4e863-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4e863-436">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e863-436">Timed Power-On Supported</span></span>

<span data-ttu-id="4e863-437">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="4e863-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-438">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4e863-438">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-439">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4e863-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e863-441">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="4e863-441">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="4e863-442">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4e863-442">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="4e863-443">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-444">**QuadSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="4e863-444">**QuadSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-445">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-447">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information Functions \| SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="4e863-447">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-448">Une des deux valeurs de seuil d’accélération.</span><span class="sxs-lookup"><span data-stu-id="4e863-448">One of two acceleration threshold values.</span></span> <span data-ttu-id="4e863-449">Le système double la vitesse du mouvement du pointeur lorsque l’appareil de pointeur déplace une distance supérieure à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="4e863-449">The system doubles the speed of the pointer movement when the pointer device moves a distance greater than this value.</span></span> <span data-ttu-id="4e863-450">Étant donné que cette augmentation de la vitesse se produit après que la valeur **DoubleSpeedThreshold** a été remplie, le pointeur se déplace effectivement à quatre fois sa vitesse d’origine.</span><span class="sxs-lookup"><span data-stu-id="4e863-450">Because this speed increase occurs after the **DoubleSpeedThreshold** value has been met, the pointer effectively moves at four times its original speed.</span></span>

</dd> <dt>

<span data-ttu-id="4e863-451">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="4e863-451">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-452">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-454">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« nombres par pouce »)</span><span class="sxs-lookup"><span data-stu-id="4e863-454">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-455">Résolution du suivi.</span><span class="sxs-lookup"><span data-stu-id="4e863-455">Tracking resolution.</span></span>

<span data-ttu-id="4e863-456">Cette propriété est héritée de la [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-456">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="4e863-457">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="4e863-457">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="4e863-458">**SampleRate**</span><span class="sxs-lookup"><span data-stu-id="4e863-458">**SampleRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-459">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-459">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-461">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| samplerate"), [**Units**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="4e863-461">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-462">Vitesse à laquelle le dispositif de pointage est interrogé pour obtenir des informations d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4e863-462">Rate at which the pointing device is polled for input information.</span></span>

</dd> <dt>

<span data-ttu-id="4e863-463">**État**</span><span class="sxs-lookup"><span data-stu-id="4e863-463">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-464">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-466">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4e863-466">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-467">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e863-467">Current status of the object.</span></span> <span data-ttu-id="4e863-468">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="4e863-468">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4e863-469">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="4e863-469">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4e863-470">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="4e863-470">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4e863-471">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="4e863-471">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4e863-472">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="4e863-472">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4e863-473">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-473">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4e863-474">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e863-474">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4e863-475">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="4e863-475">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4e863-476">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="4e863-476">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e863-477">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="4e863-477">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-478">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="4e863-478">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4e863-479">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="4e863-479">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4e863-480">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="4e863-480">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4e863-481">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="4e863-481">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4e863-482">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="4e863-482">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4e863-483">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="4e863-483">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4e863-484">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="4e863-484">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4e863-485">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="4e863-485">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4e863-486">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="4e863-486">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-487">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4e863-487">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-488">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e863-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-489">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-490">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4e863-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-491">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4e863-491">State of the logical device.</span></span> <span data-ttu-id="4e863-492">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e863-492">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4e863-493">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-493">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e863-494">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4e863-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e863-495">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4e863-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4e863-496">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="4e863-496">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e863-497">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="4e863-497">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4e863-498">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="4e863-498">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e863-499">**Synchronisation**</span><span class="sxs-lookup"><span data-stu-id="4e863-499">**Synch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-500">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e863-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-501">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-502">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| MouseSynchIn100ns"), [**unités**](../wmisdk/standard-qualifiers.md) ("100 nanosecondes")</span><span class="sxs-lookup"><span data-stu-id="4e863-502">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|MouseSynchIn100ns"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4e863-503">Durée après laquelle l’interruption suivante est supposée indiquer le début d’un nouveau paquet d’appareil (les paquets partiels sont ignorés).</span><span class="sxs-lookup"><span data-stu-id="4e863-503">Length of time after which the next interrupt is assumed to indicate the start of a new device packet (partial packets are discarded).</span></span> <span data-ttu-id="4e863-504">En cas de perte d’une interruption, cela permet au pilote de périphérique de pointage de synchroniser sa représentation interne de l’état du paquet avec l’état du matériel.</span><span class="sxs-lookup"><span data-stu-id="4e863-504">In the event that an interrupt is lost, this allows the pointing device driver to synchronize its internal representation of the packet state with the hardware state.</span></span>

</dd> <dt>

<span data-ttu-id="4e863-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e863-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-506">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-508">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4e863-508">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4e863-509">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4e863-509">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="4e863-510">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e863-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4e863-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e863-512">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e863-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e863-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e863-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e863-514">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4e863-514">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4e863-515">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4e863-515">Name of the scoping system.</span></span>

<span data-ttu-id="4e863-516">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e863-517">Notes</span><span class="sxs-lookup"><span data-stu-id="4e863-517">Remarks</span></span>

<span data-ttu-id="4e863-518">La classe **Win32 \_ PointingDevice** est dérivée de [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4e863-518">The **Win32\_PointingDevice** class is derived from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e863-519">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e863-519">Requirements</span></span>



| <span data-ttu-id="4e863-520">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e863-520">Requirement</span></span> | <span data-ttu-id="4e863-521">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e863-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e863-522">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e863-522">Minimum supported client</span></span><br/> | <span data-ttu-id="4e863-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e863-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e863-524">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e863-524">Minimum supported server</span></span><br/> | <span data-ttu-id="4e863-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e863-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e863-526">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4e863-526">Namespace</span></span><br/>                | <span data-ttu-id="4e863-527">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4e863-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e863-528">MOF</span><span class="sxs-lookup"><span data-stu-id="4e863-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e863-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e863-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e863-530">DLL</span><span class="sxs-lookup"><span data-stu-id="4e863-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e863-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e863-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e863-532">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e863-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e863-533">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4e863-533">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="4e863-534">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="4e863-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
