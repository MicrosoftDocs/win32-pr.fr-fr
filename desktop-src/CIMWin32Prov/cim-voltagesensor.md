---
description: La \_ classe CIM capteur existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures. Avec les ajouts au \_ capteur CIM et aux \_ classes NumericSensor CIM dans la version 2,2, il n’est plus nécessaire.
ms.assetid: a578c7a2-27d5-4bd8-86d7-3962d5091f14
ms.tgt_platform: multiple
title: Classe CIM_VoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor
- CIM_VoltageSensor.Accuracy
- CIM_VoltageSensor.Availability
- CIM_VoltageSensor.Caption
- CIM_VoltageSensor.ConfigManagerErrorCode
- CIM_VoltageSensor.ConfigManagerUserConfig
- CIM_VoltageSensor.CreationClassName
- CIM_VoltageSensor.CurrentReading
- CIM_VoltageSensor.Description
- CIM_VoltageSensor.DeviceID
- CIM_VoltageSensor.ErrorCleared
- CIM_VoltageSensor.ErrorDescription
- CIM_VoltageSensor.InstallDate
- CIM_VoltageSensor.IsLinear
- CIM_VoltageSensor.LastErrorCode
- CIM_VoltageSensor.LowerThresholdCritical
- CIM_VoltageSensor.LowerThresholdFatal
- CIM_VoltageSensor.LowerThresholdNonCritical
- CIM_VoltageSensor.MaxReadable
- CIM_VoltageSensor.MinReadable
- CIM_VoltageSensor.Name
- CIM_VoltageSensor.NominalReading
- CIM_VoltageSensor.NormalMax
- CIM_VoltageSensor.NormalMin
- CIM_VoltageSensor.PNPDeviceID
- CIM_VoltageSensor.PowerManagementCapabilities
- CIM_VoltageSensor.PowerManagementSupported
- CIM_VoltageSensor.Resolution
- CIM_VoltageSensor.Status
- CIM_VoltageSensor.StatusInfo
- CIM_VoltageSensor.SystemCreationClassName
- CIM_VoltageSensor.SystemName
- CIM_VoltageSensor.Tolerance
- CIM_VoltageSensor.UpperThresholdCritical
- CIM_VoltageSensor.UpperThresholdFatal
- CIM_VoltageSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bd0f3d79415254d0af50429c8f1776d2eb451cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513306"
---
# <a name="cim_voltagesensor-class"></a><span data-ttu-id="6432c-104">\_Classe CIM capteur</span><span class="sxs-lookup"><span data-stu-id="6432c-104">CIM\_VoltageSensor class</span></span>

<span data-ttu-id="6432c-105">La classe **CIM \_ capteur** existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="6432c-105">The **CIM\_VoltageSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="6432c-106">Avec les ajouts [**au \_ capteur CIM**](cim-sensor.md) et aux classes [**\_ NumericSensor CIM**](cim-numericsensor.md) dans la version 2,2, il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6432c-106">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="6432c-107">Un capteur de voltage peut être défini en affectant à la propriété **SensorType** héritée du [**\_ capteur CIM**](cim-sensor.md)la valeur 3 (« voltage »).</span><span class="sxs-lookup"><span data-stu-id="6432c-107">A voltage sensor can be defined by setting the **SensorType** property, inherited from [**CIM\_Sensor**](cim-sensor.md), to 3 ("Voltage").</span></span> <span data-ttu-id="6432c-108">Les autres propriétés de cette classe sont codées en dur pour des valeurs constantes qui correspondent aux définitions dans la hiérarchie de capteur.</span><span class="sxs-lookup"><span data-stu-id="6432c-108">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6432c-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6432c-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6432c-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6432c-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6432c-111">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6432c-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6432c-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6432c-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6432c-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6432c-113">Syntax</span></span>

``` syntax
[UUID("{A998F9B4-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VoltageSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="6432c-114">Membres</span><span class="sxs-lookup"><span data-stu-id="6432c-114">Members</span></span>

<span data-ttu-id="6432c-115">La classe **CIM \_ capteur** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6432c-115">The **CIM\_VoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="6432c-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6432c-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="6432c-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6432c-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6432c-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6432c-118">Methods</span></span>

<span data-ttu-id="6432c-119">La classe **CIM \_ capteur** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6432c-119">The **CIM\_VoltageSensor** class has these methods.</span></span>



| <span data-ttu-id="6432c-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="6432c-120">Method</span></span>                                                                   | <span data-ttu-id="6432c-121">Description</span><span class="sxs-lookup"><span data-stu-id="6432c-121">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6432c-122">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="6432c-122">**Reset**</span></span>](reset-method-in-class-cim-voltagesensor.md)                 | <span data-ttu-id="6432c-123">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6432c-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="6432c-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6432c-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6432c-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6432c-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md) | <span data-ttu-id="6432c-126">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="6432c-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6432c-127">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6432c-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6432c-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6432c-128">Properties</span></span>

<span data-ttu-id="6432c-129">La classe **CIM \_ capteur** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6432c-129">The **CIM\_VoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6432c-130">**Précision**</span><span class="sxs-lookup"><span data-stu-id="6432c-130">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-133">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("précision"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="6432c-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-134">Précision du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="6432c-134">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="6432c-135">Sa valeur est enregistrée comme plus ou moins centièmes de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="6432c-135">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="6432c-136">Cette propriété, ainsi que les propriétés de **résolution** et de **tolérance** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="6432c-136">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6432c-137">La précision peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="6432c-137">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6432c-138">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-138">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-139">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="6432c-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6432c-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-142">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6432c-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-143">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-143">Availability and status of the device.</span></span>

<span data-ttu-id="6432c-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6432c-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6432c-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6432c-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6432c-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6432c-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="6432c-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-148">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="6432c-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6432c-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="6432c-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6432c-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="6432c-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6432c-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="6432c-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6432c-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="6432c-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6432c-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="6432c-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6432c-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="6432c-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6432c-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="6432c-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6432c-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="6432c-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6432c-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="6432c-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6432c-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="6432c-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-159">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="6432c-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6432c-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="6432c-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-161">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="6432c-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6432c-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="6432c-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-163">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="6432c-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6432c-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="6432c-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6432c-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="6432c-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-166">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6432c-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6432c-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="6432c-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-168">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="6432c-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6432c-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="6432c-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-170">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="6432c-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6432c-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="6432c-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-172">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="6432c-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6432c-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="6432c-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-174">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="6432c-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6432c-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6432c-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-178">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6432c-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-179">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6432c-179">Short textual description of the object.</span></span>

<span data-ttu-id="6432c-180">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6432c-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6432c-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-184">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6432c-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-185">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="6432c-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6432c-186">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6432c-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="6432c-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6432c-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="6432c-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-189">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="6432c-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6432c-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="6432c-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6432c-191">(1)</span><span class="sxs-lookup"><span data-stu-id="6432c-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-192">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="6432c-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6432c-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6432c-194">(2)</span><span class="sxs-lookup"><span data-stu-id="6432c-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6432c-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="6432c-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6432c-196">(3)</span><span class="sxs-lookup"><span data-stu-id="6432c-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-197">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="6432c-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6432c-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="6432c-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6432c-199">(4)</span><span class="sxs-lookup"><span data-stu-id="6432c-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-200">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="6432c-200">Device is not working properly.</span></span> <span data-ttu-id="6432c-201">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="6432c-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6432c-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="6432c-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6432c-203">(5)</span><span class="sxs-lookup"><span data-stu-id="6432c-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-204">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="6432c-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6432c-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="6432c-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6432c-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="6432c-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-207">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="6432c-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6432c-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="6432c-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6432c-209">(7)</span><span class="sxs-lookup"><span data-stu-id="6432c-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6432c-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="6432c-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6432c-211">(8)</span><span class="sxs-lookup"><span data-stu-id="6432c-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-212">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="6432c-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6432c-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6432c-214">(9)</span><span class="sxs-lookup"><span data-stu-id="6432c-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-215">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="6432c-215">Device is not working properly.</span></span> <span data-ttu-id="6432c-216">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6432c-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6432c-218">(10)</span><span class="sxs-lookup"><span data-stu-id="6432c-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-219">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6432c-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6432c-221">(11)</span><span class="sxs-lookup"><span data-stu-id="6432c-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-222">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6432c-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="6432c-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6432c-224">douze</span><span class="sxs-lookup"><span data-stu-id="6432c-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-225">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6432c-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6432c-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6432c-227">(13)</span><span class="sxs-lookup"><span data-stu-id="6432c-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-228">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6432c-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="6432c-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6432c-230">(14)</span><span class="sxs-lookup"><span data-stu-id="6432c-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-231">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="6432c-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6432c-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="6432c-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6432c-233">(15)</span><span class="sxs-lookup"><span data-stu-id="6432c-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-234">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="6432c-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6432c-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6432c-236">(16)</span><span class="sxs-lookup"><span data-stu-id="6432c-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-237">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6432c-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="6432c-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6432c-239">(17)</span><span class="sxs-lookup"><span data-stu-id="6432c-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-240">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="6432c-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6432c-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6432c-242">(18)</span><span class="sxs-lookup"><span data-stu-id="6432c-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-243">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="6432c-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6432c-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="6432c-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6432c-245">(19)</span><span class="sxs-lookup"><span data-stu-id="6432c-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6432c-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="6432c-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6432c-247">(20)</span><span class="sxs-lookup"><span data-stu-id="6432c-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-248">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="6432c-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6432c-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6432c-250">(21)</span><span class="sxs-lookup"><span data-stu-id="6432c-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-251">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="6432c-251">System failure.</span></span> <span data-ttu-id="6432c-252">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="6432c-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6432c-253">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6432c-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="6432c-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6432c-255">(22)</span><span class="sxs-lookup"><span data-stu-id="6432c-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-256">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6432c-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6432c-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="6432c-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6432c-258">(23)</span><span class="sxs-lookup"><span data-stu-id="6432c-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-259">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="6432c-259">System failure.</span></span> <span data-ttu-id="6432c-260">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="6432c-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6432c-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="6432c-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6432c-262">(24)</span><span class="sxs-lookup"><span data-stu-id="6432c-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-263">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="6432c-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6432c-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6432c-265">(25)</span><span class="sxs-lookup"><span data-stu-id="6432c-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-266">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6432c-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6432c-268">(26)</span><span class="sxs-lookup"><span data-stu-id="6432c-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-269">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6432c-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6432c-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="6432c-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6432c-271">(27)</span><span class="sxs-lookup"><span data-stu-id="6432c-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-272">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="6432c-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6432c-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="6432c-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6432c-274">(28)</span><span class="sxs-lookup"><span data-stu-id="6432c-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-275">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="6432c-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6432c-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="6432c-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6432c-277">(29)</span><span class="sxs-lookup"><span data-stu-id="6432c-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-278">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6432c-278">Device is disabled.</span></span> <span data-ttu-id="6432c-279">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="6432c-279">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6432c-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="6432c-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6432c-281">(30)</span><span class="sxs-lookup"><span data-stu-id="6432c-281">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-282">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="6432c-282">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6432c-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6432c-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6432c-284">31</span><span class="sxs-lookup"><span data-stu-id="6432c-284">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-285">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="6432c-285">Device is not working properly.</span></span> <span data-ttu-id="6432c-286">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="6432c-286">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6432c-287">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6432c-287">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-288">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6432c-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-290">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6432c-290">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-291">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6432c-291">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6432c-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-293">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6432c-293">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-296">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6432c-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6432c-297">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6432c-297">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6432c-298">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="6432c-298">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6432c-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-300">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="6432c-300">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-301">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-301">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-303">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-303">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-304">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="6432c-304">Current value indicated by the sensor.</span></span>

<span data-ttu-id="6432c-305">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-306">**Description**</span><span class="sxs-lookup"><span data-stu-id="6432c-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-309">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6432c-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-310">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6432c-310">Textual description of the object.</span></span>

<span data-ttu-id="6432c-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6432c-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-315">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6432c-315">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6432c-316">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6432c-316">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6432c-317">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6432c-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-319">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6432c-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6432c-321">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="6432c-321">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6432c-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6432c-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6432c-326">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="6432c-326">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6432c-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6432c-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-329">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6432c-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-331">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6432c-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-332">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6432c-332">Date and time the object was installed.</span></span> <span data-ttu-id="6432c-333">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="6432c-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6432c-334">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-335">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="6432c-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-336">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6432c-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6432c-338">Si la **valeur est true**, le capteur est linéaire sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="6432c-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="6432c-339">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6432c-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-341">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6432c-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6432c-343">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6432c-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6432c-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="6432c-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-346">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-348">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,13 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-348">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-349">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="6432c-349">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6432c-350">Si la propriété **CurrentReading** est comprise entre **LowerThresholdCritical** et **LowerThresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="6432c-350">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="6432c-351">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="6432c-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-353">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-355">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-355">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-356">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="6432c-356">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="6432c-357">Si la propriété **CurrentReading** est en dessous de **LowerThresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="6432c-357">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="6432c-358">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="6432c-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-360">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-362">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-362">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-363">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="6432c-363">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6432c-364">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="6432c-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="6432c-365">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **LowerThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="6432c-365">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="6432c-366">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="6432c-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-368">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-370">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,9 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-371">Plus grande valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="6432c-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="6432c-372">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="6432c-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-374">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-376">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,10 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-376">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-377">Plus petite valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="6432c-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="6432c-378">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-379">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6432c-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-380">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-382">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6432c-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-383">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6432c-383">Label by which the object is known.</span></span> <span data-ttu-id="6432c-384">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="6432c-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6432c-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="6432c-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-387">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-389">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-390">Valeur attendue ou normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="6432c-390">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="6432c-391">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="6432c-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-393">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-395">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-395">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-396">Plage maximale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="6432c-396">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="6432c-397">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="6432c-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-399">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-401">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-401">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-402">Plage minimale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="6432c-402">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="6432c-403">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6432c-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-407">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6432c-407">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-408">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="6432c-408">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="6432c-409">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6432c-410">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="6432c-410">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6432c-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6432c-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-412">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6432c-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6432c-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6432c-414">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="6432c-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6432c-415">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="6432c-415">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6432c-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6432c-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6432c-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6432c-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6432c-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="6432c-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6432c-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6432c-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-420">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="6432c-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6432c-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="6432c-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-422">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="6432c-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6432c-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="6432c-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-424">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6432c-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6432c-425">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="6432c-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6432c-426">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6432c-426">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6432c-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="6432c-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-428">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="6432c-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6432c-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="6432c-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6432c-430">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="6432c-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6432c-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6432c-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-432">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6432c-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-433">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6432c-434">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6432c-434">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6432c-435">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6432c-435">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6432c-436">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6432c-436">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6432c-437">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6432c-437">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6432c-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-439">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="6432c-439">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-440">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6432c-440">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-442">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,17 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" dixièmes de millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-443">Capacité du capteur à résoudre les différences dans la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="6432c-443">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="6432c-444">Cette propriété, ainsi que les propriétés de **précision** et de **tolérance** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="6432c-444">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6432c-445">Cette valeur peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="6432c-445">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6432c-446">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-446">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-447">**État**</span><span class="sxs-lookup"><span data-stu-id="6432c-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-450">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6432c-450">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-451">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6432c-451">Current status of the object.</span></span>

<span data-ttu-id="6432c-452">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6432c-453">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6432c-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6432c-454">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6432c-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6432c-455">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6432c-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6432c-456">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6432c-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6432c-457">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6432c-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6432c-458">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6432c-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6432c-459">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6432c-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6432c-460">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6432c-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6432c-461">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6432c-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6432c-462">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6432c-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6432c-463">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6432c-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6432c-464">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6432c-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6432c-465">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6432c-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6432c-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6432c-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-467">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6432c-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-469">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6432c-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-470">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6432c-470">State of the logical device.</span></span> <span data-ttu-id="6432c-471">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6432c-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6432c-472">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6432c-473">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6432c-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6432c-474">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6432c-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6432c-475">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6432c-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6432c-476">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="6432c-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6432c-477">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="6432c-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6432c-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6432c-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-479">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-481">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6432c-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6432c-482">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6432c-482">Scoping system's creation class name.</span></span>

<span data-ttu-id="6432c-483">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6432c-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-485">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6432c-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-487">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6432c-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6432c-488">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6432c-488">Scoping system's name.</span></span>

<span data-ttu-id="6432c-489">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-490">**Seuil**</span><span class="sxs-lookup"><span data-stu-id="6432c-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-491">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-493">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,18 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-494">Tolérance du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="6432c-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="6432c-495">Cette propriété, ainsi que les propriétés de **résolution** et de **précision** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="6432c-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6432c-496">La tolérance peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="6432c-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6432c-497">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-497">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-498">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="6432c-498">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-499">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-499">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-501">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,14 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-501">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-502">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="6432c-502">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6432c-503">Si la propriété **CurrentReading** est comprise entre **UpperThresholdCritical** et **UpperthresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="6432c-503">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="6432c-504">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-504">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-505">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="6432c-505">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-506">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-506">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-508">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperthresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,16 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-508">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-509">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="6432c-509">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6432c-510">Si la propriété **CurrentReading** est au-dessus de **UpperthresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="6432c-510">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="6432c-511">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-511">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6432c-512">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="6432c-512">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6432c-513">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6432c-513">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6432c-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6432c-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6432c-515">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de tension DMTF \| 001,12 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" millivolts ")</span><span class="sxs-lookup"><span data-stu-id="6432c-515">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6432c-516">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="6432c-516">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6432c-517">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="6432c-517">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="6432c-518">Si la propriété **CurrentReading** est comprise entre **UpperThresholdNonCritical** et **UpperThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="6432c-518">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="6432c-519">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-519">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6432c-520">Notes</span><span class="sxs-lookup"><span data-stu-id="6432c-520">Remarks</span></span>

<span data-ttu-id="6432c-521">La classe **CIM \_ capteur** est dérivée de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-521">The **CIM\_VoltageSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="6432c-522">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6432c-522">WMI does not implement this class.</span></span> <span data-ttu-id="6432c-523">Pour les classes WMI dérivées de **CIM \_ capteur**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6432c-523">For WMI classes derived from **CIM\_VoltageSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6432c-524">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6432c-524">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6432c-525">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6432c-525">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6432c-526">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6432c-526">Requirements</span></span>



| <span data-ttu-id="6432c-527">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6432c-527">Requirement</span></span> | <span data-ttu-id="6432c-528">Valeur</span><span class="sxs-lookup"><span data-stu-id="6432c-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6432c-529">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6432c-529">Minimum supported client</span></span><br/> | <span data-ttu-id="6432c-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6432c-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6432c-531">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6432c-531">Minimum supported server</span></span><br/> | <span data-ttu-id="6432c-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6432c-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6432c-533">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6432c-533">Namespace</span></span><br/>                | <span data-ttu-id="6432c-534">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6432c-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6432c-535">MOF</span><span class="sxs-lookup"><span data-stu-id="6432c-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6432c-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6432c-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6432c-537">DLL</span><span class="sxs-lookup"><span data-stu-id="6432c-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6432c-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6432c-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6432c-539">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6432c-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6432c-540">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="6432c-540">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

