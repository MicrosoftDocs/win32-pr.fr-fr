---
description: La \_ classe WMI SerialPort Win32 représente un port série sur un système informatique exécutant Windows.
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Classe Win32_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110159"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="e67e1-103">\_Classe SerialPort Win32</span><span class="sxs-lookup"><span data-stu-id="e67e1-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="e67e1-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPort Win32** représente un port série sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="e67e1-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="e67e1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e67e1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e67e1-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e67e1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e67e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e67e1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="e67e1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e67e1-108">Members</span></span>

<span data-ttu-id="e67e1-109">La **classe \_ SerialPort Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e67e1-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="e67e1-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e67e1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e67e1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e67e1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e67e1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e67e1-112">Methods</span></span>

<span data-ttu-id="e67e1-113">La **classe \_ SerialPort Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e67e1-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="e67e1-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="e67e1-114">Method</span></span>            | <span data-ttu-id="e67e1-115">Description</span><span class="sxs-lookup"><span data-stu-id="e67e1-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e67e1-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="e67e1-116">**Reset**</span></span>         | <span data-ttu-id="e67e1-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e67e1-117">Not implemented.</span></span> <span data-ttu-id="e67e1-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="e67e1-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e67e1-119">**SetPowerState**</span></span> | <span data-ttu-id="e67e1-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e67e1-120">Not implemented.</span></span> <span data-ttu-id="e67e1-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e67e1-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e67e1-122">Properties</span></span>

<span data-ttu-id="e67e1-123">La **classe \_ SerialPort Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e67e1-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e67e1-124">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="e67e1-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67e1-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-128">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-128">Availability and status of the device.</span></span>

<span data-ttu-id="e67e1-129">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e67e1-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e67e1-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e67e1-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e67e1-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e67e1-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="e67e1-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-133">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="e67e1-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e67e1-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="e67e1-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e67e1-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="e67e1-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e67e1-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="e67e1-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e67e1-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="e67e1-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e67e1-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="e67e1-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e67e1-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="e67e1-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e67e1-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="e67e1-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e67e1-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="e67e1-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e67e1-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="e67e1-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e67e1-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="e67e1-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-144">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e67e1-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e67e1-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="e67e1-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-146">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="e67e1-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e67e1-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="e67e1-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-148">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="e67e1-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e67e1-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="e67e1-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e67e1-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="e67e1-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-151">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="e67e1-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e67e1-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="e67e1-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-153">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="e67e1-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e67e1-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="e67e1-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-155">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="e67e1-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e67e1-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="e67e1-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-157">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="e67e1-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e67e1-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="e67e1-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-159">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="e67e1-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-160">**Binaire**</span><span class="sxs-lookup"><span data-stu-id="e67e1-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-161">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-163">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="e67e1-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-164">Si la **valeur est true**, le port série est configuré pour le transfert de données binaires.</span><span class="sxs-lookup"><span data-stu-id="e67e1-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="e67e1-165">Étant donné que l’API Windows ne prend pas en charge les transferts en mode non binaire, cette propriété doit avoir la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="e67e1-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-166">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e67e1-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-167">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67e1-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-169">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ports série DMTF \| 004,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="e67e1-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-170">Tableau de compatibilité au niveau du processeur pour le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="e67e1-171">Cette propriété décrit la mise en mémoire tampon et d’autres fonctionnalités du contrôleur série qui peuvent être inhérentes au matériel de puce.</span><span class="sxs-lookup"><span data-stu-id="e67e1-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="e67e1-172">La propriété est un entier énuméré.</span><span class="sxs-lookup"><span data-stu-id="e67e1-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="e67e1-173">Cette propriété est héritée de la [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e67e1-174">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e67e1-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e67e1-175">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e67e1-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="e67e1-176">**Compatible XT/AT** (3)</span><span class="sxs-lookup"><span data-stu-id="e67e1-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="e67e1-177">**Compatible 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="e67e1-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="e67e1-178">**Compatible 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="e67e1-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="e67e1-179">**compatible 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="e67e1-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="e67e1-180">**Compatible 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="e67e1-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="e67e1-181">**compatible 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="e67e1-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-182">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e67e1-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-183">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e67e1-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-185">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="e67e1-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-186">Tableau de chaînes de forme libre fournissant des explications plus détaillées sur les fonctionnalités du contrôleur série indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="e67e1-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="e67e1-187">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="e67e1-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="e67e1-188">Cette propriété est héritée de la [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e67e1-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-192">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-193">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e67e1-193">Short description of the object.</span></span>

<span data-ttu-id="e67e1-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e67e1-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-196">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67e1-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-198">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e67e1-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-199">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="e67e1-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e67e1-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e67e1-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e67e1-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="e67e1-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-203">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="e67e1-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e67e1-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e67e1-205">(1)</span><span class="sxs-lookup"><span data-stu-id="e67e1-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-206">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="e67e1-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e67e1-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e67e1-208">(2)</span><span class="sxs-lookup"><span data-stu-id="e67e1-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e67e1-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e67e1-210">(3)</span><span class="sxs-lookup"><span data-stu-id="e67e1-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-211">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="e67e1-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e67e1-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e67e1-213">(4)</span><span class="sxs-lookup"><span data-stu-id="e67e1-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-214">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e67e1-214">Device is not working properly.</span></span> <span data-ttu-id="e67e1-215">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e67e1-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e67e1-217">(5)</span><span class="sxs-lookup"><span data-stu-id="e67e1-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-218">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="e67e1-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e67e1-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e67e1-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="e67e1-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-221">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="e67e1-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e67e1-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e67e1-223">(7)</span><span class="sxs-lookup"><span data-stu-id="e67e1-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e67e1-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e67e1-225">(8)</span><span class="sxs-lookup"><span data-stu-id="e67e1-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-226">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="e67e1-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e67e1-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e67e1-228">(9)</span><span class="sxs-lookup"><span data-stu-id="e67e1-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-229">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e67e1-229">Device is not working properly.</span></span> <span data-ttu-id="e67e1-230">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e67e1-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e67e1-232">(10)</span><span class="sxs-lookup"><span data-stu-id="e67e1-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-233">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e67e1-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e67e1-235">(11)</span><span class="sxs-lookup"><span data-stu-id="e67e1-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-236">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e67e1-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e67e1-238">douze</span><span class="sxs-lookup"><span data-stu-id="e67e1-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-239">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e67e1-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e67e1-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e67e1-241">(13)</span><span class="sxs-lookup"><span data-stu-id="e67e1-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-242">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e67e1-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e67e1-244">(14)</span><span class="sxs-lookup"><span data-stu-id="e67e1-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-245">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="e67e1-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e67e1-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e67e1-247">(15)</span><span class="sxs-lookup"><span data-stu-id="e67e1-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-248">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="e67e1-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e67e1-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e67e1-250">(16)</span><span class="sxs-lookup"><span data-stu-id="e67e1-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-251">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e67e1-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e67e1-253">(17)</span><span class="sxs-lookup"><span data-stu-id="e67e1-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-254">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="e67e1-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e67e1-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e67e1-256">(18)</span><span class="sxs-lookup"><span data-stu-id="e67e1-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-257">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="e67e1-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e67e1-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e67e1-259">(19)</span><span class="sxs-lookup"><span data-stu-id="e67e1-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e67e1-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e67e1-261">(20)</span><span class="sxs-lookup"><span data-stu-id="e67e1-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-262">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e67e1-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e67e1-264">(21)</span><span class="sxs-lookup"><span data-stu-id="e67e1-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-265">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="e67e1-265">System failure.</span></span> <span data-ttu-id="e67e1-266">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="e67e1-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e67e1-267">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e67e1-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e67e1-269">(22)</span><span class="sxs-lookup"><span data-stu-id="e67e1-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-270">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e67e1-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e67e1-272">(23)</span><span class="sxs-lookup"><span data-stu-id="e67e1-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-273">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="e67e1-273">System failure.</span></span> <span data-ttu-id="e67e1-274">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="e67e1-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e67e1-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e67e1-276">(24)</span><span class="sxs-lookup"><span data-stu-id="e67e1-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-277">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="e67e1-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e67e1-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e67e1-279">(25)</span><span class="sxs-lookup"><span data-stu-id="e67e1-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-280">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e67e1-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e67e1-282">(26)</span><span class="sxs-lookup"><span data-stu-id="e67e1-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-283">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e67e1-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e67e1-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e67e1-285">(27)</span><span class="sxs-lookup"><span data-stu-id="e67e1-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-286">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="e67e1-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e67e1-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e67e1-288">(28)</span><span class="sxs-lookup"><span data-stu-id="e67e1-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-289">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="e67e1-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e67e1-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e67e1-291">(29)</span><span class="sxs-lookup"><span data-stu-id="e67e1-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-292">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-292">Device is disabled.</span></span> <span data-ttu-id="e67e1-293">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="e67e1-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e67e1-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e67e1-295">(30)</span><span class="sxs-lookup"><span data-stu-id="e67e1-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-296">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="e67e1-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e67e1-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e67e1-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e67e1-298">31</span><span class="sxs-lookup"><span data-stu-id="e67e1-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-299">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e67e1-299">Device is not working properly.</span></span> <span data-ttu-id="e67e1-300">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="e67e1-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e67e1-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-302">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-304">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e67e1-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-305">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e67e1-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e67e1-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e67e1-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-310">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e67e1-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-311">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="e67e1-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e67e1-312">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e67e1-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e67e1-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-314">**Description**</span><span class="sxs-lookup"><span data-stu-id="e67e1-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-317">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e67e1-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-318">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e67e1-318">Description of the object.</span></span>

<span data-ttu-id="e67e1-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e67e1-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-323">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="e67e1-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-324">Identificateur unique du port série avec d’autres périphériques sur le système.</span><span class="sxs-lookup"><span data-stu-id="e67e1-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="e67e1-325">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e67e1-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-327">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-329">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="e67e1-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e67e1-330">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e67e1-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-332">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-334">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="e67e1-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="e67e1-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e67e1-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-337">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e67e1-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-339">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-340">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e67e1-340">Date and time the object was installed.</span></span> <span data-ttu-id="e67e1-341">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e67e1-342">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-343">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e67e1-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-344">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67e1-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-346">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e67e1-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e67e1-347">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-348">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="e67e1-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-349">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67e1-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-351">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Ports série DMTF \| 004,6 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits par seconde ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-352">Débit en bauds maximal (en bits par seconde) pris en charge par le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="e67e1-353">Cette propriété est héritée de la [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-354">**MaximumInputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="e67e1-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-355">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67e1-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-357">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| des structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxRxQueue"), [**unités**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e67e1-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-358">Taille maximale de la mémoire tampon d’entrée interne du pilote du port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="e67e1-359">La valeur 0 (zéro) indique qu’aucune valeur maximale n’est imposée par le fournisseur série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-360">**MaximumOutputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="e67e1-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-361">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67e1-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-363">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| des structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxTxQueue"), [**unités**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e67e1-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-364">Taille maximale de la mémoire tampon de sortie interne du pilote du port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="e67e1-365">La valeur 0 (zéro) indique qu’aucune valeur maximale n’est imposée par le fournisseur série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-366">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="e67e1-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-367">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e67e1-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-369">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-370">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="e67e1-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="e67e1-371">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e67e1-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="e67e1-372">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-373">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e67e1-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-376">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e67e1-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-377">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="e67e1-377">Label by which the object is known.</span></span> <span data-ttu-id="e67e1-378">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e67e1-379">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-380">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="e67e1-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-381">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-383">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Hardware \\ \\ description \\ \\ System \\ \\ MultifunctionAdapter »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-384">Si la **valeur est true**, les instances de cette classe ont été détectées automatiquement par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e67e1-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="e67e1-385">Si, par exemple, le matériel a été ajouté par le biais du panneau de configuration, le système d’exploitation trouve les instances de cette classe en interrogeant le matériel à partir des instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e67e1-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e67e1-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-389">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e67e1-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-390">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e67e1-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e67e1-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e67e1-392">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="e67e1-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e67e1-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-394">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67e1-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-396">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="e67e1-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e67e1-397">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="e67e1-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e67e1-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e67e1-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e67e1-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e67e1-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e67e1-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="e67e1-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e67e1-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="e67e1-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-402">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e67e1-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e67e1-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="e67e1-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-404">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="e67e1-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e67e1-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="e67e1-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-406">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e67e1-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e67e1-407">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="e67e1-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e67e1-408">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e67e1-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="e67e1-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-410">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="e67e1-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e67e1-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="e67e1-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-412">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67e1-412">Timed Power-On Supported</span></span>

<span data-ttu-id="e67e1-413">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="e67e1-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-414">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e67e1-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-415">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-417">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="e67e1-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="e67e1-418">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e67e1-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="e67e1-419">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-420">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="e67e1-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-421">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67e1-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-423">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-424">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="e67e1-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="e67e1-425">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="e67e1-426">La liste suivante indique les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="e67e1-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e67e1-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e67e1-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e67e1-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e67e1-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="e67e1-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="e67e1-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="e67e1-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="e67e1-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="e67e1-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="e67e1-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="e67e1-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="e67e1-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e67e1-433">ATA ou ATAPI</span><span class="sxs-lookup"><span data-stu-id="e67e1-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="e67e1-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="e67e1-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="e67e1-435"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="e67e1-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="e67e1-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="e67e1-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="e67e1-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="e67e1-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="e67e1-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="e67e1-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="e67e1-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="e67e1-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="e67e1-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="e67e1-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="e67e1-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="e67e1-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="e67e1-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="e67e1-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="e67e1-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="e67e1-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="e67e1-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="e67e1-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="e67e1-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="e67e1-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="e67e1-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="e67e1-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="e67e1-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="e67e1-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="e67e1-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="e67e1-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="e67e1-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="e67e1-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="e67e1-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="e67e1-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="e67e1-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="e67e1-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="e67e1-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="e67e1-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="e67e1-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="e67e1-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="e67e1-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="e67e1-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="e67e1-455"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="e67e1-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="e67e1-456"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="e67e1-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="e67e1-457"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="e67e1-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="e67e1-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="e67e1-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="e67e1-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="e67e1-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="e67e1-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="e67e1-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="e67e1-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="e67e1-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="e67e1-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="e67e1-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="e67e1-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="e67e1-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="e67e1-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="e67e1-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="e67e1-465"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="e67e1-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="e67e1-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="e67e1-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="e67e1-467"><span id="DSSI"></span><span id="dssi"></span>**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="e67e1-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="e67e1-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="e67e1-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="e67e1-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="e67e1-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="e67e1-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="e67e1-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="e67e1-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="e67e1-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="e67e1-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="e67e1-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="e67e1-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="e67e1-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="e67e1-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="e67e1-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="e67e1-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-476">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-478">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvSubType")</span><span class="sxs-lookup"><span data-stu-id="e67e1-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-479">Type de fournisseur de communications.</span><span class="sxs-lookup"><span data-stu-id="e67e1-479">Communications provider type.</span></span>

<span data-ttu-id="e67e1-480">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="e67e1-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="e67e1-481">« Périphérique de télécopie »</span><span class="sxs-lookup"><span data-stu-id="e67e1-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="e67e1-482">« Protocole LAT »</span><span class="sxs-lookup"><span data-stu-id="e67e1-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="e67e1-483">« Périphérique modem »</span><span class="sxs-lookup"><span data-stu-id="e67e1-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="e67e1-484">« Pont réseau »</span><span class="sxs-lookup"><span data-stu-id="e67e1-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="e67e1-485">« Port parallèle »</span><span class="sxs-lookup"><span data-stu-id="e67e1-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="e67e1-486">« Port série RS232 »</span><span class="sxs-lookup"><span data-stu-id="e67e1-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="e67e1-487">« Port RS422 »</span><span class="sxs-lookup"><span data-stu-id="e67e1-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="e67e1-488">« Port RS423 »</span><span class="sxs-lookup"><span data-stu-id="e67e1-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="e67e1-489">« Port RS449 »</span><span class="sxs-lookup"><span data-stu-id="e67e1-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="e67e1-490">« Périphérique du scanneur »</span><span class="sxs-lookup"><span data-stu-id="e67e1-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="e67e1-491">« TelNet TCP/IP »</span><span class="sxs-lookup"><span data-stu-id="e67e1-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="e67e1-492">« X. 25 »</span><span class="sxs-lookup"><span data-stu-id="e67e1-492">"X.25"</span></span></dd> <dd><span data-ttu-id="e67e1-493">Non spécifié</span><span class="sxs-lookup"><span data-stu-id="e67e1-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="e67e1-494">**Périphérique de télécopie** (« périphérique de télécopie »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="e67e1-495">**Protocole lat** (« protocole LAT »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="e67e1-496">**Périphérique modem** (« périphérique modem »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="e67e1-497">**Pont réseau** (« pont réseau »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="e67e1-498">**Port parallèle** (« port parallèle »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="e67e1-499">**Port série RS232** (« port série RS232 »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="e67e1-500">**Port RS422** (« port RS422 »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="e67e1-501">**Port RS423** (« port RS423 »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="e67e1-502">**Port RS449** (« port RS449 »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="e67e1-503">**Périphérique scanneur** (« périphérique scanneur »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="e67e1-504">**Telnet TCP/IP** (« TCP/IP Telnet »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="e67e1-505">**X. 25** ("x. 25")</span><span class="sxs-lookup"><span data-stu-id="e67e1-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="e67e1-506">**Non spécifié** (« non spécifié »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-507">**SettableBaudRate**</span><span class="sxs-lookup"><span data-stu-id="e67e1-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-508">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-510">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ bauds")</span><span class="sxs-lookup"><span data-stu-id="e67e1-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-511">Si la **valeur est true**, la vitesse en bauds peut être modifiée pour ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-512">**SettableDataBits**</span><span class="sxs-lookup"><span data-stu-id="e67e1-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-513">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-515">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ DATABITS")</span><span class="sxs-lookup"><span data-stu-id="e67e1-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-516">Si la **valeur est true**, les bits de données peuvent être définis pour ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-517">**SettableFlowControl**</span><span class="sxs-lookup"><span data-stu-id="e67e1-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-518">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-520">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams de négociation de \| SP \_ ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-521">Si la **valeur est true**, le contrôle de Flow peut être défini pour ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-522">**SettableParity**</span><span class="sxs-lookup"><span data-stu-id="e67e1-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-523">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-525">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ Parity")</span><span class="sxs-lookup"><span data-stu-id="e67e1-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-526">Si la **valeur est true**, la parité peut être définie pour ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-527">**SettableParityCheck**</span><span class="sxs-lookup"><span data-stu-id="e67e1-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-528">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-529">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-530">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP de contrôle de \_ parité \_ ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-531">Si la **valeur est true**, la vérification de la parité peut être définie pour ce port série (si le contrôle de parité est pris en charge).</span><span class="sxs-lookup"><span data-stu-id="e67e1-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-532">**SettableRLSD**</span><span class="sxs-lookup"><span data-stu-id="e67e1-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-533">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-534">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-535">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="e67e1-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-536">Si la **valeur est true**, la détection de signal de ligne reçue (RLSD) peut être définie pour ce port série (si RLSD est pris en charge).</span><span class="sxs-lookup"><span data-stu-id="e67e1-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-537">**SettableStopBits**</span><span class="sxs-lookup"><span data-stu-id="e67e1-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-538">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-539">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-540">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ arrêt")</span><span class="sxs-lookup"><span data-stu-id="e67e1-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-541">Si la **valeur est true**, les bits d’arrêt peuvent être définis pour ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-542">**État**</span><span class="sxs-lookup"><span data-stu-id="e67e1-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-543">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-544">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-545">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e67e1-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-546">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e67e1-546">Current status of the object.</span></span> <span data-ttu-id="e67e1-547">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="e67e1-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e67e1-548">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="e67e1-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e67e1-549">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e67e1-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e67e1-550">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e67e1-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e67e1-551">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e67e1-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e67e1-552">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e67e1-553">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e67e1-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e67e1-554">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e67e1-555">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e67e1-556">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e67e1-557">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e67e1-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e67e1-558">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e67e1-559">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e67e1-560">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e67e1-561">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e67e1-562">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e67e1-563">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e67e1-564">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e67e1-565">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e67e1-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e67e1-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-567">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e67e1-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-568">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-569">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-570">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e67e1-570">State of the logical device.</span></span> <span data-ttu-id="e67e1-571">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e67e1-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e67e1-572">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e67e1-573">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e67e1-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e67e1-574">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e67e1-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e67e1-575">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="e67e1-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e67e1-576">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="e67e1-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e67e1-577">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="e67e1-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e67e1-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="e67e1-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-579">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-580">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-581">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ 16BITMODE")</span><span class="sxs-lookup"><span data-stu-id="e67e1-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-582">Si la **valeur est true**, le mode 16 bits est pris en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-583">**SupportsDTRDSR**</span><span class="sxs-lookup"><span data-stu-id="e67e1-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-584">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-585">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-586">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ DTRDSR")</span><span class="sxs-lookup"><span data-stu-id="e67e1-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-587">Si la **valeur est true**, les signaux DTR (Data Terminal Ready) et DSR (Data Set Ready) sont pris en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-588">**SupportsElapsedTimeouts**</span><span class="sxs-lookup"><span data-stu-id="e67e1-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-589">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-590">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-591">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ TOTALTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="e67e1-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-592">Si la **valeur est true**, les délais d’expiration écoulés sont pris en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="e67e1-593">Les délais d’expiration écoulés effectuent le suivi de la durée totale entre les transmissions de données.</span><span class="sxs-lookup"><span data-stu-id="e67e1-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-594">**SupportsIntTimeouts**</span><span class="sxs-lookup"><span data-stu-id="e67e1-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-595">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-596">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-597">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ INTTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="e67e1-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-598">Si la **valeur est true**, les délais d’expiration des intervalles sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e67e1-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="e67e1-599">Un délai d’expiration de l’intervalle est la durée autorisée à s’écouler entre l’arrivée de chaque élément de données.</span><span class="sxs-lookup"><span data-stu-id="e67e1-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-600">**SupportsParityCheck**</span><span class="sxs-lookup"><span data-stu-id="e67e1-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-601">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-602">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-603">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| contrôle de parité PCF \_ \_ ")</span><span class="sxs-lookup"><span data-stu-id="e67e1-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-604">Si la **valeur est true**, le contrôle de parité est pris en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-605">**SupportsRLSD**</span><span class="sxs-lookup"><span data-stu-id="e67e1-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-606">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-607">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-608">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="e67e1-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-609">Si la **valeur est true**, la détection de signal de ligne reçue (RLSD) est prise en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-610">**SupportsRTSCTS**</span><span class="sxs-lookup"><span data-stu-id="e67e1-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-611">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-612">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-613">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RTSCTS")</span><span class="sxs-lookup"><span data-stu-id="e67e1-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-614">Si la **valeur est true**, les signaux RTS (Ready to Send) et CTS (Clear to Send) sont pris en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-615">**SupportsSpecialCharacters**</span><span class="sxs-lookup"><span data-stu-id="e67e1-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-616">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-617">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-618">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SPECIALCHARS")</span><span class="sxs-lookup"><span data-stu-id="e67e1-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-619">Si la **valeur est true**, les caractères de contrôle de port série sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e67e1-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="e67e1-620">Ces caractères signalent des événements plutôt que des données.</span><span class="sxs-lookup"><span data-stu-id="e67e1-620">These characters signal events rather than data.</span></span> <span data-ttu-id="e67e1-621">Ces caractères ne peuvent pas être lus et sont définis par le pilote.</span><span class="sxs-lookup"><span data-stu-id="e67e1-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="e67e1-622">Elles incluent EofChar, ErrorChar, BreakChar, EventChar, XonChar et XoffChar.</span><span class="sxs-lookup"><span data-stu-id="e67e1-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-623">**SupportsXOnXOff**</span><span class="sxs-lookup"><span data-stu-id="e67e1-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-624">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-625">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-626">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ XONXOFF")</span><span class="sxs-lookup"><span data-stu-id="e67e1-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-627">Si la **valeur est true**, Xon ou XOFF Flow-Control est pris en charge sur ce port série.</span><span class="sxs-lookup"><span data-stu-id="e67e1-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-628">**SupportsXOnXOffSet**</span><span class="sxs-lookup"><span data-stu-id="e67e1-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-629">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e67e1-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-630">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-631">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SETXCHAR")</span><span class="sxs-lookup"><span data-stu-id="e67e1-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-632">Si la **valeur est true**, le fournisseur de communications prend en charge la configuration du paramètre de contrôle de workflow XOFF XONor.</span><span class="sxs-lookup"><span data-stu-id="e67e1-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-633">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e67e1-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-634">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-635">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-636">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e67e1-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-637">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e67e1-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e67e1-638">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-639">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e67e1-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-640">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e67e1-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-641">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-642">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e67e1-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-643">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e67e1-643">Name of the scoping system.</span></span>

<span data-ttu-id="e67e1-644">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e67e1-645">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="e67e1-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e67e1-646">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e67e1-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e67e1-647">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e67e1-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e67e1-648">Date et heure de la dernière réinitialisation de ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="e67e1-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="e67e1-649">Cela peut signifier que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="e67e1-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="e67e1-650">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e67e1-651">Notes</span><span class="sxs-lookup"><span data-stu-id="e67e1-651">Remarks</span></span>

<span data-ttu-id="e67e1-652">La **classe \_ SerialPort Win32** est dérivée de la [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e67e1-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e67e1-653">Exemples</span><span class="sxs-lookup"><span data-stu-id="e67e1-653">Examples</span></span>

<span data-ttu-id="e67e1-654">Pour obtenir une autre méthode de récupération des informations du port série (à partir du registre), consultez l’exemple [énumérer les Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e67e1-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="e67e1-655">L’exemple PowerShell [list port série Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) retourne des informations sur les ports série installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e67e1-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="e67e1-656">L’exemple VBScript suivant retourne des informations sur les ports série installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e67e1-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="e67e1-657">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e67e1-657">Requirements</span></span>



| <span data-ttu-id="e67e1-658">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e67e1-658">Requirement</span></span> | <span data-ttu-id="e67e1-659">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67e1-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e67e1-660">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67e1-660">Minimum supported client</span></span><br/> | <span data-ttu-id="e67e1-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e67e1-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e67e1-662">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67e1-662">Minimum supported server</span></span><br/> | <span data-ttu-id="e67e1-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e67e1-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e67e1-664">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e67e1-664">Namespace</span></span><br/>                | <span data-ttu-id="e67e1-665">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e67e1-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e67e1-666">MOF</span><span class="sxs-lookup"><span data-stu-id="e67e1-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e67e1-667"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e67e1-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e67e1-668">DLL</span><span class="sxs-lookup"><span data-stu-id="e67e1-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e67e1-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e67e1-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e67e1-670">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e67e1-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e67e1-671">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e67e1-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="e67e1-672">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="e67e1-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
