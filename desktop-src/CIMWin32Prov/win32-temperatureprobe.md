---
description: Le \_ TemperatureProbe Win32&\# 32 ; La classe WMI représente les propriétés d’un capteur de température (thermomètre électronique).
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Classe Win32_TemperatureProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861154"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="e9670-103">\_Classe TemperatureProbe Win32</span><span class="sxs-lookup"><span data-stu-id="e9670-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="e9670-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TemperatureProbe** WMI représente les propriétés d’un capteur de température (thermomètre électronique).</span><span class="sxs-lookup"><span data-stu-id="e9670-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="e9670-105">La plupart des informations fournies par la classe WMI **Win32 \_ TemperatureProbe** proviennent de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="e9670-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="e9670-106">Les lectures en temps réel de la propriété **CurrentReading** ne peuvent pas être extraites des tables SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="e9670-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="e9670-107">Pour cette raison, les implémentations actuelles de WMI ne remplissent pas la propriété **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="e9670-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="e9670-108">La présence de la propriété **CurrentReading** est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e9670-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="e9670-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e9670-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e9670-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e9670-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9670-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9670-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="e9670-112">Membres</span><span class="sxs-lookup"><span data-stu-id="e9670-112">Members</span></span>

<span data-ttu-id="e9670-113">La classe **Win32 \_ TemperatureProbe** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9670-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="e9670-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9670-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9670-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9670-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9670-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9670-116">Methods</span></span>

<span data-ttu-id="e9670-117">La classe **Win32 \_ TemperatureProbe** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e9670-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="e9670-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="e9670-118">Method</span></span>            | <span data-ttu-id="e9670-119">Description</span><span class="sxs-lookup"><span data-stu-id="e9670-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9670-120">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="e9670-120">**Reset**</span></span>         | <span data-ttu-id="e9670-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e9670-121">Not implemented.</span></span> <span data-ttu-id="e9670-122">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-temperaturesensor.md) dans [**CIM \_ capteur**](cim-temperaturesensor.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="e9670-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="e9670-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e9670-123">**SetPowerState**</span></span> | <span data-ttu-id="e9670-124">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e9670-124">Not implemented.</span></span> <span data-ttu-id="e9670-125">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) dans [**CIM \_ capteur**](cim-temperaturesensor.md) pour obtenir de la documentation.</span><span class="sxs-lookup"><span data-stu-id="e9670-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e9670-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9670-126">Properties</span></span>

<span data-ttu-id="e9670-127">La classe **Win32 \_ TemperatureProbe** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e9670-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9670-128">**Précision**</span><span class="sxs-lookup"><span data-stu-id="e9670-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-131">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="e9670-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-132">Précision du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="e9670-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="e9670-133">Sa valeur est enregistrée comme plus ou moins centièmes de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="e9670-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="e9670-134">La précision, la résolution et la tolérance sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="e9670-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e9670-135">La précision peut varier et varie selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="e9670-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="e9670-136">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-137">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="e9670-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9670-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-140">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e9670-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-141">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-141">Availability and status of the device.</span></span>

<span data-ttu-id="e9670-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9670-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e9670-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9670-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e9670-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e9670-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="e9670-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e9670-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="e9670-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e9670-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="e9670-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e9670-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="e9670-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e9670-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="e9670-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e9670-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="e9670-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-151">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="e9670-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e9670-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="e9670-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e9670-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="e9670-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e9670-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="e9670-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e9670-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="e9670-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e9670-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="e9670-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-157">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e9670-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e9670-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="e9670-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-159">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="e9670-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e9670-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="e9670-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-161">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="e9670-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e9670-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="e9670-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e9670-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="e9670-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-164">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="e9670-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e9670-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="e9670-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-166">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="e9670-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e9670-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="e9670-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-168">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="e9670-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e9670-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="e9670-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-170">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="e9670-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e9670-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="e9670-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-172">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="e9670-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e9670-173">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e9670-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-176">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="e9670-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-177">Description succincte d’un objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="e9670-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="e9670-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-179">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e9670-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-180">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9670-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-182">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e9670-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-183">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="e9670-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e9670-184">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e9670-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="e9670-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e9670-186"> (0)</span><span class="sxs-lookup"><span data-stu-id="e9670-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-187">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="e9670-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e9670-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="e9670-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e9670-189">(1)</span><span class="sxs-lookup"><span data-stu-id="e9670-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-190">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="e9670-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e9670-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e9670-192">(2)</span><span class="sxs-lookup"><span data-stu-id="e9670-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e9670-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="e9670-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e9670-194">(3)</span><span class="sxs-lookup"><span data-stu-id="e9670-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-195">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="e9670-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e9670-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="e9670-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e9670-197">(4)</span><span class="sxs-lookup"><span data-stu-id="e9670-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-198">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e9670-198">Device is not working properly.</span></span> <span data-ttu-id="e9670-199">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="e9670-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e9670-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="e9670-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e9670-201">(5)</span><span class="sxs-lookup"><span data-stu-id="e9670-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-202">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="e9670-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e9670-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="e9670-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e9670-204"> (6)</span><span class="sxs-lookup"><span data-stu-id="e9670-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-205">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="e9670-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e9670-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="e9670-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e9670-207">(7)</span><span class="sxs-lookup"><span data-stu-id="e9670-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e9670-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="e9670-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e9670-209">(8)</span><span class="sxs-lookup"><span data-stu-id="e9670-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-210">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="e9670-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e9670-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e9670-212">(9)</span><span class="sxs-lookup"><span data-stu-id="e9670-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-213">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e9670-213">Device is not working properly.</span></span> <span data-ttu-id="e9670-214">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e9670-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e9670-216">(10)</span><span class="sxs-lookup"><span data-stu-id="e9670-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-217">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e9670-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e9670-219">(11)</span><span class="sxs-lookup"><span data-stu-id="e9670-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-220">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e9670-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="e9670-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e9670-222">douze</span><span class="sxs-lookup"><span data-stu-id="e9670-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-223">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e9670-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e9670-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e9670-225">(13)</span><span class="sxs-lookup"><span data-stu-id="e9670-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-226">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e9670-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="e9670-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e9670-228">(14)</span><span class="sxs-lookup"><span data-stu-id="e9670-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-229">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="e9670-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e9670-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="e9670-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e9670-231">(15)</span><span class="sxs-lookup"><span data-stu-id="e9670-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-232">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="e9670-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e9670-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e9670-234">(16)</span><span class="sxs-lookup"><span data-stu-id="e9670-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-235">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e9670-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="e9670-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e9670-237">(17)</span><span class="sxs-lookup"><span data-stu-id="e9670-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-238">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="e9670-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e9670-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e9670-240">(18)</span><span class="sxs-lookup"><span data-stu-id="e9670-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-241">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="e9670-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e9670-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="e9670-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e9670-243">(19)</span><span class="sxs-lookup"><span data-stu-id="e9670-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e9670-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="e9670-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e9670-245">(20)</span><span class="sxs-lookup"><span data-stu-id="e9670-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-246">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="e9670-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e9670-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e9670-248">(21)</span><span class="sxs-lookup"><span data-stu-id="e9670-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-249">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="e9670-249">System failure.</span></span> <span data-ttu-id="e9670-250">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="e9670-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e9670-251">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e9670-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="e9670-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e9670-253">(22)</span><span class="sxs-lookup"><span data-stu-id="e9670-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-254">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e9670-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e9670-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="e9670-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e9670-256">(23)</span><span class="sxs-lookup"><span data-stu-id="e9670-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-257">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="e9670-257">System failure.</span></span> <span data-ttu-id="e9670-258">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="e9670-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e9670-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="e9670-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e9670-260">(24)</span><span class="sxs-lookup"><span data-stu-id="e9670-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-261">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="e9670-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e9670-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e9670-263">(25)</span><span class="sxs-lookup"><span data-stu-id="e9670-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-264">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e9670-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e9670-266">(26)</span><span class="sxs-lookup"><span data-stu-id="e9670-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-267">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9670-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e9670-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="e9670-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e9670-269">(27)</span><span class="sxs-lookup"><span data-stu-id="e9670-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-270">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="e9670-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e9670-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="e9670-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e9670-272">(28)</span><span class="sxs-lookup"><span data-stu-id="e9670-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-273">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="e9670-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e9670-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="e9670-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e9670-275">(29)</span><span class="sxs-lookup"><span data-stu-id="e9670-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-276">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e9670-276">Device is disabled.</span></span> <span data-ttu-id="e9670-277">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="e9670-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e9670-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="e9670-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e9670-279">(30)</span><span class="sxs-lookup"><span data-stu-id="e9670-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-280">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="e9670-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e9670-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="e9670-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e9670-282">31</span><span class="sxs-lookup"><span data-stu-id="e9670-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-283">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="e9670-283">Device is not working properly.</span></span> <span data-ttu-id="e9670-284">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="e9670-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e9670-285">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e9670-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-286">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e9670-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-288">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e9670-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-289">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9670-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e9670-290">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-291">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e9670-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-294">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e9670-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e9670-295">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="e9670-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e9670-296">Lorsqu’elle est utilisée avec les autres propriétés de clé d’une classe, cette propriété permet à toutes les instances de la classe et de ses sous-classes d’être identifiées de manière unique.</span><span class="sxs-lookup"><span data-stu-id="e9670-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="e9670-297">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-298">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="e9670-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-299">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-301">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-302">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="e9670-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="e9670-303">Les implémentations actuelles de WMI ne remplissent pas la propriété **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="e9670-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="e9670-304">La présence de la propriété **CurrentReading** est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e9670-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="e9670-305">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-306">**Description**</span><span class="sxs-lookup"><span data-stu-id="e9670-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-309">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e9670-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-310">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9670-310">Description of the object.</span></span>

<span data-ttu-id="e9670-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e9670-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-315">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="e9670-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-316">Identificateur unique de la sonde actuelle.</span><span class="sxs-lookup"><span data-stu-id="e9670-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="e9670-317">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e9670-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-319">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e9670-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9670-321">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="e9670-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e9670-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e9670-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9670-326">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="e9670-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="e9670-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9670-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-329">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9670-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-331">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e9670-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-332">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9670-332">Date and time the object is installed.</span></span> <span data-ttu-id="e9670-333">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="e9670-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e9670-334">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-335">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="e9670-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-336">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e9670-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9670-338">Si la **valeur est true**, le capteur est linéaire sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="e9670-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="e9670-339">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e9670-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-341">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9670-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9670-343">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e9670-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e9670-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="e9670-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-346">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-348">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,13 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-349">Valeur du seuil du capteur pour spécifier les plages (valeurs minimales et maximales) qui identifient les conditions de fonctionnement du capteur, qui peuvent être des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="e9670-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="e9670-350">Si **CurrentReading** est compris entre **LowerThresholdCritical** et **LowerThresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="e9670-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="e9670-351">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="e9670-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-353">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-355">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,15 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-356">Valeur du seuil du capteur pour spécifier les plages (valeurs minimales et maximales) qui identifient les conditions de fonctionnement du capteur, qui peuvent être des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="e9670-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="e9670-357">Si **CurrentReading** est en dessous de **LowerThresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="e9670-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="e9670-358">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="e9670-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-360">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-362">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,11 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-363">Valeur du seuil du capteur pour spécifier les plages (valeurs minimales et maximales) qui identifient les conditions de fonctionnement du capteur, qui peuvent être des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="e9670-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="e9670-364">Si **CurrentReading** est compris entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="e9670-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="e9670-365">Si **CurrentReading** est compris entre **LowerThresholdNonCritical** et **LowerThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="e9670-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="e9670-366">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="e9670-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-368">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-370">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,9 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-371">Plus grande valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="e9670-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="e9670-372">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="e9670-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-374">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-376">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,10 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-377">Plus petite valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="e9670-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="e9670-378">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-379">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e9670-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-380">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-382">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e9670-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-383">Étiquette de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9670-383">Label for the object.</span></span> <span data-ttu-id="e9670-384">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="e9670-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e9670-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="e9670-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-387">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-389">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,6 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-390">Valeur normale ou attendue pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="e9670-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="e9670-391">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="e9670-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-393">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-395">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,7 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-396">Valeur normale ou attendue pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="e9670-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="e9670-397">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="e9670-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-399">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-401">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,8 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-402">Aide pour l’utilisateur en ce qui concerne la plage minimale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="e9670-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="e9670-403">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e9670-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-407">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e9670-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-408">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e9670-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e9670-409">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="e9670-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="e9670-410">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e9670-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-412">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9670-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9670-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9670-414">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="e9670-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e9670-415">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9670-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e9670-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e9670-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e9670-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e9670-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="e9670-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e9670-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="e9670-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-420">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e9670-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e9670-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="e9670-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-422">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="e9670-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e9670-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="e9670-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-424">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e9670-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e9670-425">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="e9670-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e9670-426">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e9670-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="e9670-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-428">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="e9670-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e9670-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="e9670-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e9670-430">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="e9670-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e9670-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e9670-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-432">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e9670-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-433">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9670-434">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="e9670-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="e9670-435">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e9670-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="e9670-436">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-437">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="e9670-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-438">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9670-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-440">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,17 "), [**unités**](../wmisdk/standard-qualifiers.md) (" centièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-441">Capacité du capteur à résoudre les différences dans la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="e9670-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="e9670-442">Cette valeur peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="e9670-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="e9670-443">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-444">**État**</span><span class="sxs-lookup"><span data-stu-id="e9670-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-447">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e9670-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-448">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9670-448">Current status of the object.</span></span> <span data-ttu-id="e9670-449">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="e9670-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e9670-450">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="e9670-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e9670-451">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e9670-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e9670-452">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e9670-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e9670-453">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e9670-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e9670-454">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e9670-455">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9670-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e9670-456">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e9670-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e9670-457">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e9670-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e9670-458">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e9670-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9670-459">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e9670-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e9670-460">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e9670-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e9670-461">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e9670-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e9670-462">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e9670-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e9670-463">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e9670-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e9670-464">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e9670-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e9670-465">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e9670-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e9670-466">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e9670-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e9670-467">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e9670-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9670-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e9670-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-469">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9670-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-471">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e9670-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-472">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e9670-472">State of the logical device.</span></span> <span data-ttu-id="e9670-473">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e9670-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e9670-474">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9670-475">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e9670-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9670-476">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="e9670-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e9670-477">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="e9670-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e9670-478">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="e9670-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e9670-479">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="e9670-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9670-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e9670-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-483">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e9670-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e9670-484">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e9670-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e9670-485">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e9670-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9670-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-489">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e9670-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e9670-490">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e9670-490">Name of the scoping system.</span></span>

<span data-ttu-id="e9670-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-492">**Seuil**</span><span class="sxs-lookup"><span data-stu-id="e9670-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-493">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-495">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,18 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-496">Tolérance du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="e9670-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="e9670-497">La tolérance, ainsi que la résolution et la précision, sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="e9670-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e9670-498">La tolérance peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="e9670-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="e9670-499">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-500">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="e9670-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-501">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-502">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-503">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,14 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-504">Les valeurs de seuil du capteur spécifient les plages (valeurs minimales et maximales) qui identifient les conditions de fonctionnement du capteur, qui peuvent être des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="e9670-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="e9670-505">Si **CurrentReading** est compris entre **UpperThresholdCritical** et **UpperthresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="e9670-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="e9670-506">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-507">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="e9670-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-508">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-510">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,16 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-511">Les valeurs de seuil du capteur spécifient les plages (valeurs minimales et maximales) qui identifient les conditions de fonctionnement du capteur, qui peuvent être des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="e9670-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="e9670-512">Si **CurrentReading** est au-dessus de **UpperthresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="e9670-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="e9670-513">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9670-514">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="e9670-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9670-515">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9670-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9670-516">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9670-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9670-517">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de température DMTF \| 001,12 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de degrés centigrade ")</span><span class="sxs-lookup"><span data-stu-id="e9670-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="e9670-518">Les valeurs de seuil du capteur spécifient les plages (valeurs minimales et maximales) qui identifient les conditions de fonctionnement du capteur, qui peuvent être des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="e9670-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="e9670-519">Si **CurrentReading** est compris entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="e9670-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="e9670-520">Si **CurrentReading** est compris entre **UpperThresholdNonCritical** et **UpperThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="e9670-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="e9670-521">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9670-522">Notes</span><span class="sxs-lookup"><span data-stu-id="e9670-522">Remarks</span></span>

<span data-ttu-id="e9670-523">La classe **Win32 \_ TemperatureProbe** est dérivée de [**CIM \_ capteur**](cim-temperaturesensor.md).</span><span class="sxs-lookup"><span data-stu-id="e9670-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e9670-524">Exemples</span><span class="sxs-lookup"><span data-stu-id="e9670-524">Examples</span></span>

<span data-ttu-id="e9670-525">L’exemple suivant retourne des données de sonde de température pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e9670-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="e9670-526">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9670-526">Requirements</span></span>



| <span data-ttu-id="e9670-527">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9670-527">Requirement</span></span> | <span data-ttu-id="e9670-528">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9670-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9670-529">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9670-529">Minimum supported client</span></span><br/> | <span data-ttu-id="e9670-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9670-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9670-531">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9670-531">Minimum supported server</span></span><br/> | <span data-ttu-id="e9670-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9670-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9670-533">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e9670-533">Namespace</span></span><br/>                | <span data-ttu-id="e9670-534">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e9670-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9670-535">MOF</span><span class="sxs-lookup"><span data-stu-id="e9670-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9670-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9670-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9670-537">DLL</span><span class="sxs-lookup"><span data-stu-id="e9670-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9670-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9670-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9670-539">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9670-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9670-540">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="e9670-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="e9670-541">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="e9670-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
