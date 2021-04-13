---
description: La \_ classe WMI VoltageProbe WMI représente les propriétés d’un capteur de tension (un tensiomètre électronique).
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Classe Win32_VoltageProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200885"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="f4503-103">\_Classe VoltageProbe Win32</span><span class="sxs-lookup"><span data-stu-id="f4503-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="f4503-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VoltageProbe** WMI représente les propriétés d’un capteur de tension (un tensiomètre électronique).</span><span class="sxs-lookup"><span data-stu-id="f4503-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="f4503-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f4503-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f4503-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f4503-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4503-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4503-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="f4503-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f4503-108">Members</span></span>

<span data-ttu-id="f4503-109">La classe **Win32 \_ VoltageProbe** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f4503-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="f4503-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f4503-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f4503-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4503-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f4503-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f4503-112">Methods</span></span>

<span data-ttu-id="f4503-113">La classe **Win32 \_ VoltageProbe** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f4503-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="f4503-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="f4503-114">Method</span></span>            | <span data-ttu-id="f4503-115">Description</span><span class="sxs-lookup"><span data-stu-id="f4503-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4503-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="f4503-116">**Reset**</span></span>         | <span data-ttu-id="f4503-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="f4503-117">Not implemented.</span></span> <span data-ttu-id="f4503-118">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ capteur**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="f4503-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f4503-119">**SetPowerState**</span></span> | <span data-ttu-id="f4503-120">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="f4503-120">Not implemented.</span></span> <span data-ttu-id="f4503-121">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ capteur**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f4503-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4503-122">Properties</span></span>

<span data-ttu-id="f4503-123">La classe **Win32 \_ VoltageProbe** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f4503-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4503-124">**Précision**</span><span class="sxs-lookup"><span data-stu-id="f4503-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-125">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-127">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="f4503-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-128">Précision du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="f4503-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="f4503-129">La valeur de précision est enregistrée comme plus ou moins centièmes de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="f4503-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="f4503-130">La précision, ainsi que la résolution et la tolérance, sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="f4503-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="f4503-131">La précision peut varier et varie selon que l’appareil est linéaire ou non dans sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="f4503-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="f4503-132">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-133">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="f4503-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4503-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-136">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f4503-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-137">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-137">Availability and status of the device.</span></span>

<span data-ttu-id="f4503-138">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4503-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f4503-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4503-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f4503-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f4503-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="f4503-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f4503-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="f4503-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f4503-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="f4503-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f4503-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="f4503-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f4503-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="f4503-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f4503-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="f4503-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f4503-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="f4503-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f4503-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="f4503-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f4503-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="f4503-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f4503-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="f4503-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f4503-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="f4503-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-152">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="f4503-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f4503-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="f4503-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-154">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="f4503-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f4503-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="f4503-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-156">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="f4503-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f4503-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="f4503-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f4503-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="f4503-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-159">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f4503-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f4503-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="f4503-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-161">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="f4503-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f4503-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="f4503-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-163">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="f4503-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f4503-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="f4503-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-165">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="f4503-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f4503-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="f4503-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-167">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="f4503-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4503-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f4503-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-171">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="f4503-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-172">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="f4503-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="f4503-173">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f4503-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-175">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4503-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-177">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f4503-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-178">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="f4503-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f4503-179">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f4503-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="f4503-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f4503-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="f4503-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-182">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="f4503-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f4503-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="f4503-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f4503-184">(1)</span><span class="sxs-lookup"><span data-stu-id="f4503-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-185">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="f4503-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f4503-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f4503-187">(2)</span><span class="sxs-lookup"><span data-stu-id="f4503-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f4503-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="f4503-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f4503-189">(3)</span><span class="sxs-lookup"><span data-stu-id="f4503-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-190">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="f4503-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f4503-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="f4503-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f4503-192">(4)</span><span class="sxs-lookup"><span data-stu-id="f4503-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-193">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f4503-193">Device is not working properly.</span></span> <span data-ttu-id="f4503-194">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="f4503-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f4503-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="f4503-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f4503-196">(5)</span><span class="sxs-lookup"><span data-stu-id="f4503-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-197">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="f4503-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f4503-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="f4503-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f4503-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="f4503-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-200">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="f4503-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f4503-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="f4503-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f4503-202">(7)</span><span class="sxs-lookup"><span data-stu-id="f4503-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f4503-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="f4503-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f4503-204">(8)</span><span class="sxs-lookup"><span data-stu-id="f4503-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-205">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="f4503-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f4503-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f4503-207">(9)</span><span class="sxs-lookup"><span data-stu-id="f4503-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-208">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f4503-208">Device is not working properly.</span></span> <span data-ttu-id="f4503-209">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f4503-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f4503-211">(10)</span><span class="sxs-lookup"><span data-stu-id="f4503-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-212">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f4503-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f4503-214">(11)</span><span class="sxs-lookup"><span data-stu-id="f4503-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-215">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f4503-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="f4503-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f4503-217">douze</span><span class="sxs-lookup"><span data-stu-id="f4503-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-218">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f4503-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f4503-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f4503-220">(13)</span><span class="sxs-lookup"><span data-stu-id="f4503-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-221">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f4503-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="f4503-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f4503-223">(14)</span><span class="sxs-lookup"><span data-stu-id="f4503-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-224">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="f4503-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f4503-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="f4503-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f4503-226">(15)</span><span class="sxs-lookup"><span data-stu-id="f4503-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-227">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="f4503-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f4503-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f4503-229">(16)</span><span class="sxs-lookup"><span data-stu-id="f4503-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-230">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f4503-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="f4503-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f4503-232">(17)</span><span class="sxs-lookup"><span data-stu-id="f4503-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-233">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="f4503-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f4503-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f4503-235">(18)</span><span class="sxs-lookup"><span data-stu-id="f4503-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-236">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="f4503-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f4503-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="f4503-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f4503-238">(19)</span><span class="sxs-lookup"><span data-stu-id="f4503-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f4503-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="f4503-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f4503-240">(20)</span><span class="sxs-lookup"><span data-stu-id="f4503-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-241">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="f4503-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f4503-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f4503-243">(21)</span><span class="sxs-lookup"><span data-stu-id="f4503-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="f4503-244">System failure.</span></span> <span data-ttu-id="f4503-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="f4503-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f4503-246">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f4503-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="f4503-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f4503-248">(22)</span><span class="sxs-lookup"><span data-stu-id="f4503-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-249">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f4503-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f4503-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="f4503-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f4503-251">(23)</span><span class="sxs-lookup"><span data-stu-id="f4503-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-252">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="f4503-252">System failure.</span></span> <span data-ttu-id="f4503-253">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="f4503-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f4503-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="f4503-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f4503-255">(24)</span><span class="sxs-lookup"><span data-stu-id="f4503-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-256">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="f4503-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f4503-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f4503-258">(25)</span><span class="sxs-lookup"><span data-stu-id="f4503-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-259">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f4503-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f4503-261">(26)</span><span class="sxs-lookup"><span data-stu-id="f4503-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-262">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4503-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f4503-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="f4503-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f4503-264">(27)</span><span class="sxs-lookup"><span data-stu-id="f4503-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-265">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="f4503-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f4503-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="f4503-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f4503-267">(28)</span><span class="sxs-lookup"><span data-stu-id="f4503-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-268">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="f4503-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f4503-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="f4503-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f4503-270">(29)</span><span class="sxs-lookup"><span data-stu-id="f4503-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-271">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f4503-271">Device is disabled.</span></span> <span data-ttu-id="f4503-272">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="f4503-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f4503-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="f4503-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f4503-274">(30)</span><span class="sxs-lookup"><span data-stu-id="f4503-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-275">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="f4503-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f4503-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f4503-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f4503-277">31</span><span class="sxs-lookup"><span data-stu-id="f4503-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-278">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f4503-278">Device is not working properly.</span></span> <span data-ttu-id="f4503-279">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="f4503-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4503-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f4503-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-281">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f4503-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-283">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f4503-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-284">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4503-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f4503-285">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f4503-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-289">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f4503-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f4503-290">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="f4503-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f4503-291">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="f4503-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f4503-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-293">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="f4503-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-294">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-296">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-297">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="f4503-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="f4503-298">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-299">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4503-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-302">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f4503-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-303">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f4503-303">Description of the object.</span></span>

<span data-ttu-id="f4503-304">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f4503-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-306">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-308">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="f4503-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-309">Identificateur unique de la sonde de tension.</span><span class="sxs-lookup"><span data-stu-id="f4503-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="f4503-310">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f4503-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-312">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f4503-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4503-314">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="f4503-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="f4503-315">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f4503-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4503-319">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="f4503-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="f4503-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f4503-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-322">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f4503-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-324">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="f4503-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-325">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f4503-325">Date and time the object is installed.</span></span> <span data-ttu-id="f4503-326">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="f4503-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f4503-327">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-328">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="f4503-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-329">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f4503-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4503-331">Si la **valeur est true**, le capteur est linéaire sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="f4503-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="f4503-332">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-333">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f4503-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-334">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4503-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4503-336">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f4503-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f4503-337">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-338">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="f4503-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-339">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-341">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,13 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-342">Les valeurs de seuil de capteur spécifient les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="f4503-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="f4503-343">Si **CurrentReading** est compris entre **LowerThresholdCritical** et **LowerThresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="f4503-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="f4503-344">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-345">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="f4503-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-346">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-348">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,15 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-349">Les valeurs de seuil de capteur spécifient les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="f4503-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="f4503-350">Si **CurrentReading** est en dessous de **LowerThresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="f4503-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="f4503-351">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-352">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="f4503-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-353">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-355">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,11 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-356">Les valeurs de seuil de capteur spécifient les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="f4503-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="f4503-357">Si **CurrentReading** est compris entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="f4503-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="f4503-358">Si **CurrentReading** est compris entre **LowerThresholdNonCritical** et **LowerThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="f4503-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="f4503-359">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-360">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="f4503-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-361">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-363">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,9 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-364">Plus grande valeur de la propriété mesurée que le capteur numérique peut lire.</span><span class="sxs-lookup"><span data-stu-id="f4503-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="f4503-365">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-366">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="f4503-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-367">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-369">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,10 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-370">Plus petite valeur de la propriété mesurée que le capteur numérique peut lire.</span><span class="sxs-lookup"><span data-stu-id="f4503-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="f4503-371">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-372">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f4503-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-375">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f4503-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-376">Étiquette pour un objet.</span><span class="sxs-lookup"><span data-stu-id="f4503-376">Label for an object.</span></span> <span data-ttu-id="f4503-377">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="f4503-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f4503-378">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-379">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="f4503-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-380">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-382">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,6 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-383">Valeur normale ou attendue pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="f4503-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="f4503-384">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-385">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="f4503-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-386">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-388">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,7 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-389">Valeur normale ou attendue pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="f4503-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="f4503-390">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-391">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="f4503-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-392">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-394">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,8 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-395">Instructions permettant à l’utilisateur d’indiquer la plage minimale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="f4503-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="f4503-396">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f4503-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-400">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f4503-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-401">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f4503-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f4503-402">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f4503-403">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="f4503-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f4503-404">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f4503-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-405">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4503-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4503-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4503-407">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="f4503-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f4503-408">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="f4503-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4503-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f4503-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f4503-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f4503-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f4503-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="f4503-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f4503-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="f4503-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-413">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="f4503-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f4503-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="f4503-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-415">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="f4503-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f4503-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="f4503-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-417">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f4503-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f4503-418">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="f4503-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f4503-419">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f4503-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="f4503-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-421">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="f4503-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f4503-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="f4503-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f4503-423">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="f4503-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4503-424">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f4503-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-425">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f4503-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4503-427">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, ce qui signifie qu’il peut être mis en mode de suspension, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f4503-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="f4503-428">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais elle indique que l’appareil logique est capable d’effectuer la gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="f4503-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="f4503-429">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-430">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="f4503-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-431">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4503-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-433">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,17 "), [**unités**](../wmisdk/standard-qualifiers.md) (" dixièmes de millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-434">Capacité du capteur à résoudre les différences dans la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="f4503-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="f4503-435">Cette valeur peut varier et varie selon que l’appareil est linéaire ou non dans sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="f4503-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="f4503-436">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-437">**État**</span><span class="sxs-lookup"><span data-stu-id="f4503-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-438">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-440">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f4503-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-441">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f4503-441">Current status of the object.</span></span> <span data-ttu-id="f4503-442">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="f4503-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f4503-443">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="f4503-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f4503-444">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="f4503-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f4503-445">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="f4503-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f4503-446">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="f4503-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f4503-447">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f4503-448">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4503-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f4503-449">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="f4503-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f4503-450">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="f4503-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f4503-451">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="f4503-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4503-452">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="f4503-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f4503-453">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="f4503-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f4503-454">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="f4503-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f4503-455">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="f4503-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f4503-456">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="f4503-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f4503-457">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="f4503-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f4503-458">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="f4503-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f4503-459">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="f4503-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f4503-460">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="f4503-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4503-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f4503-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-462">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4503-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-463">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-464">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f4503-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-465">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f4503-465">State of the logical device.</span></span> <span data-ttu-id="f4503-466">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f4503-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f4503-467">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4503-468">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f4503-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4503-469">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f4503-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f4503-470">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="f4503-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f4503-471">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="f4503-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f4503-472">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="f4503-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4503-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f4503-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-476">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f4503-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f4503-477">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f4503-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="f4503-478">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f4503-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-480">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f4503-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-482">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f4503-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f4503-483">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f4503-483">Name of the scoping system.</span></span>

<span data-ttu-id="f4503-484">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-485">**Seuil**</span><span class="sxs-lookup"><span data-stu-id="f4503-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-486">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-488">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,18 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-489">Tolérance du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="f4503-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="f4503-490">La tolérance, ainsi que la résolution et la précision, sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="f4503-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="f4503-491">La tolérance peut varier et varie selon que l’appareil est linéaire ou non dans sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="f4503-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="f4503-492">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-493">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="f4503-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-494">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-496">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,14 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-497">Les valeurs de seuil de capteur spécifient les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="f4503-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="f4503-498">Si **CurrentReading** est compris entre **UpperThresholdCritical** et **UpperthresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="f4503-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="f4503-499">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-500">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="f4503-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-501">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-502">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-503">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,16 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-504">Les valeurs de seuil de capteur spécifient les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="f4503-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="f4503-505">Si **CurrentReading** est au-dessus de **UpperthresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="f4503-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="f4503-506">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4503-507">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="f4503-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4503-508">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4503-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4503-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4503-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4503-510">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonde de tension DMTF \| 001,12 "), [**unités**](../wmisdk/standard-qualifiers.md) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="f4503-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="f4503-511">Les valeurs de seuil de capteur spécifient les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="f4503-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="f4503-512">Si **CurrentReading** est compris entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="f4503-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="f4503-513">Si **CurrentReading** est compris entre **UpperThresholdNonCritical** et **UpperThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="f4503-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="f4503-514">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4503-515">Notes</span><span class="sxs-lookup"><span data-stu-id="f4503-515">Remarks</span></span>

<span data-ttu-id="f4503-516">La classe **Win32 \_ VoltageProbe** est dérivée de [**CIM \_ capteur**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="f4503-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4503-517">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4503-517">Requirements</span></span>



| <span data-ttu-id="f4503-518">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4503-518">Requirement</span></span> | <span data-ttu-id="f4503-519">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4503-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4503-520">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4503-520">Minimum supported client</span></span><br/> | <span data-ttu-id="f4503-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4503-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4503-522">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4503-522">Minimum supported server</span></span><br/> | <span data-ttu-id="f4503-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4503-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4503-524">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4503-524">Namespace</span></span><br/>                | <span data-ttu-id="f4503-525">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f4503-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4503-526">MOF</span><span class="sxs-lookup"><span data-stu-id="f4503-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4503-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4503-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4503-528">DLL</span><span class="sxs-lookup"><span data-stu-id="f4503-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4503-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4503-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4503-530">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4503-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4503-531">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="f4503-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="f4503-532">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="f4503-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
