---
description: La \_ classe CIM CurrentSensor existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.
ms.assetid: d1835b09-4286-4586-92ec-f5f77791aea6
ms.tgt_platform: multiple
title: Classe CIM_CurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor
- CIM_CurrentSensor.Accuracy
- CIM_CurrentSensor.Availability
- CIM_CurrentSensor.Caption
- CIM_CurrentSensor.ConfigManagerErrorCode
- CIM_CurrentSensor.ConfigManagerUserConfig
- CIM_CurrentSensor.CreationClassName
- CIM_CurrentSensor.CurrentReading
- CIM_CurrentSensor.Description
- CIM_CurrentSensor.DeviceID
- CIM_CurrentSensor.ErrorCleared
- CIM_CurrentSensor.ErrorDescription
- CIM_CurrentSensor.InstallDate
- CIM_CurrentSensor.IsLinear
- CIM_CurrentSensor.LastErrorCode
- CIM_CurrentSensor.LowerThresholdCritical
- CIM_CurrentSensor.LowerThresholdFatal
- CIM_CurrentSensor.LowerThresholdNonCritical
- CIM_CurrentSensor.MaxReadable
- CIM_CurrentSensor.MinReadable
- CIM_CurrentSensor.Name
- CIM_CurrentSensor.NominalReading
- CIM_CurrentSensor.NormalMax
- CIM_CurrentSensor.NormalMin
- CIM_CurrentSensor.PNPDeviceID
- CIM_CurrentSensor.PowerManagementCapabilities
- CIM_CurrentSensor.PowerManagementSupported
- CIM_CurrentSensor.Resolution
- CIM_CurrentSensor.Status
- CIM_CurrentSensor.StatusInfo
- CIM_CurrentSensor.SystemCreationClassName
- CIM_CurrentSensor.SystemName
- CIM_CurrentSensor.Tolerance
- CIM_CurrentSensor.UpperThresholdCritical
- CIM_CurrentSensor.UpperThresholdFatal
- CIM_CurrentSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1fe2a34e2e598d5c9655abbf84324dbf9982e416
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110882"
---
# <a name="cim_currentsensor-class"></a><span data-ttu-id="45d80-103">\_Classe CIM CurrentSensor</span><span class="sxs-lookup"><span data-stu-id="45d80-103">CIM\_CurrentSensor class</span></span>

<span data-ttu-id="45d80-104">La classe **CIM \_ CurrentSensor** existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="45d80-104">The **CIM\_CurrentSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span>

<span data-ttu-id="45d80-105">Les ajouts au [**\_ capteur CIM**](cim-sensor.md) et à [**CIM \_ NumericSensor**](cim-numericsensor.md) dans la version 2,2 ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="45d80-105">Additions to [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) in version 2.2 make it no longer necessary.</span></span> <span data-ttu-id="45d80-106">Une classe **CIM \_ CurrentSensor** peut être définie en affectant à la propriété **SensorType** héritée de **\_ capteur CIM** la valeur 4 (« en cours »).</span><span class="sxs-lookup"><span data-stu-id="45d80-106">A **CIM\_CurrentSensor** class can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 4 ("Current").</span></span> <span data-ttu-id="45d80-107">Les autres propriétés de cette classe sont codées en dur vers des valeurs constantes, qui correspondent aux définitions dans la hiérarchie de capteur.</span><span class="sxs-lookup"><span data-stu-id="45d80-107">Other properties of this class are hard-coded to constant values, which correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45d80-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="45d80-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="45d80-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="45d80-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="45d80-110">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="45d80-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="45d80-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="45d80-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d80-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45d80-112">Syntax</span></span>

``` syntax
[UUID("{DCA1D084-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_CurrentSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="45d80-113">Membres</span><span class="sxs-lookup"><span data-stu-id="45d80-113">Members</span></span>

<span data-ttu-id="45d80-114">La classe **CIM \_ CurrentSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="45d80-114">The **CIM\_CurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="45d80-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45d80-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="45d80-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45d80-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45d80-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45d80-117">Methods</span></span>

<span data-ttu-id="45d80-118">La classe **CIM \_ CurrentSensor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="45d80-118">The **CIM\_CurrentSensor** class has these methods.</span></span>



| <span data-ttu-id="45d80-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="45d80-119">Method</span></span>                                                                   | <span data-ttu-id="45d80-120">Description</span><span class="sxs-lookup"><span data-stu-id="45d80-120">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45d80-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="45d80-121">**Reset**</span></span>](reset-method-in-class-cim-currentsensor.md)                 | <span data-ttu-id="45d80-122">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45d80-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="45d80-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="45d80-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="45d80-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="45d80-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-currentsensor.md) | <span data-ttu-id="45d80-125">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="45d80-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="45d80-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="45d80-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45d80-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45d80-127">Properties</span></span>

<span data-ttu-id="45d80-128">La classe **CIM \_ CurrentSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="45d80-128">The **CIM\_CurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45d80-129">**Précision**</span><span class="sxs-lookup"><span data-stu-id="45d80-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-130">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("précision"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="45d80-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-133">Précision du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="45d80-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="45d80-134">Sa valeur est enregistrée comme plus ou moins centièmes de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="45d80-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="45d80-135">Cette propriété, ainsi que les propriétés de **résolution** et de **tolérance** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="45d80-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="45d80-136">La précision peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="45d80-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="45d80-137">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="45d80-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45d80-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-141">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="45d80-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-142">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-142">Availability and status of the device.</span></span>

<span data-ttu-id="45d80-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45d80-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45d80-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45d80-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="45d80-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="45d80-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="45d80-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="45d80-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="45d80-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="45d80-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="45d80-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="45d80-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="45d80-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="45d80-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="45d80-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="45d80-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="45d80-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="45d80-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="45d80-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45d80-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="45d80-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="45d80-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="45d80-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="45d80-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="45d80-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="45d80-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="45d80-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-157">Économie d’énergie inconnue.</span><span class="sxs-lookup"><span data-stu-id="45d80-157">Power save   unknown.</span></span>

<span data-ttu-id="45d80-158">L’appareil est en mode économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="45d80-158">Device is in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="45d80-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="45d80-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-160">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45d80-160">Power save   low-power mode.</span></span>

<span data-ttu-id="45d80-161">L’appareil est en mode économie d’énergie et continue de fonctionner, mais peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="45d80-161">Device is in a power-save mode and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="45d80-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="45d80-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-163">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="45d80-163">Power save   standby.</span></span>

<span data-ttu-id="45d80-164">L’appareil ne fonctionne pas, mais il peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="45d80-164">Device is not functioning, but it could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="45d80-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="45d80-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="45d80-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="45d80-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-167">Avertissement d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45d80-167">Power save   warning.</span></span>

<span data-ttu-id="45d80-168">L’appareil est dans un état d’avertissement et un mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45d80-168">Device is in a warning state and a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="45d80-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="45d80-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="45d80-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="45d80-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="45d80-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="45d80-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="45d80-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="45d80-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-173">Le capteur actuel n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="45d80-173">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d80-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45d80-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-177">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="45d80-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-178">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d80-178">Short textual description of the object.</span></span>

<span data-ttu-id="45d80-179">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45d80-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-181">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d80-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-183">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45d80-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-184">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="45d80-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="45d80-185">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="45d80-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="45d80-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="45d80-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="45d80-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-188">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="45d80-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="45d80-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="45d80-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="45d80-190">(1)</span><span class="sxs-lookup"><span data-stu-id="45d80-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-191">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="45d80-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45d80-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="45d80-193">(2)</span><span class="sxs-lookup"><span data-stu-id="45d80-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="45d80-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="45d80-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="45d80-195">(3)</span><span class="sxs-lookup"><span data-stu-id="45d80-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-196">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="45d80-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="45d80-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="45d80-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="45d80-198">(4)</span><span class="sxs-lookup"><span data-stu-id="45d80-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-199">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="45d80-199">Device is not working properly.</span></span> <span data-ttu-id="45d80-200">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="45d80-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="45d80-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="45d80-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="45d80-202">(5)</span><span class="sxs-lookup"><span data-stu-id="45d80-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-203">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="45d80-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="45d80-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="45d80-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="45d80-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="45d80-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-206">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="45d80-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="45d80-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="45d80-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="45d80-208">(7)</span><span class="sxs-lookup"><span data-stu-id="45d80-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="45d80-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="45d80-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="45d80-210">(8)</span><span class="sxs-lookup"><span data-stu-id="45d80-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-211">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="45d80-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="45d80-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="45d80-213">(9)</span><span class="sxs-lookup"><span data-stu-id="45d80-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-214">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-214">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="45d80-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="45d80-216">(10)</span><span class="sxs-lookup"><span data-stu-id="45d80-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-217">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="45d80-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="45d80-219">(11)</span><span class="sxs-lookup"><span data-stu-id="45d80-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-220">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="45d80-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="45d80-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="45d80-222">douze</span><span class="sxs-lookup"><span data-stu-id="45d80-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-223">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="45d80-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="45d80-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="45d80-225">(13)</span><span class="sxs-lookup"><span data-stu-id="45d80-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-226">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="45d80-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="45d80-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="45d80-228">(14)</span><span class="sxs-lookup"><span data-stu-id="45d80-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-229">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="45d80-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="45d80-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="45d80-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="45d80-231">(15)</span><span class="sxs-lookup"><span data-stu-id="45d80-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-232">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="45d80-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="45d80-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="45d80-234">(16)</span><span class="sxs-lookup"><span data-stu-id="45d80-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-235">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="45d80-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="45d80-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="45d80-237">(17)</span><span class="sxs-lookup"><span data-stu-id="45d80-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-238">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="45d80-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45d80-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="45d80-240">(18)</span><span class="sxs-lookup"><span data-stu-id="45d80-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-241">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="45d80-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="45d80-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="45d80-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="45d80-243">(19)</span><span class="sxs-lookup"><span data-stu-id="45d80-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="45d80-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="45d80-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="45d80-245">(20)</span><span class="sxs-lookup"><span data-stu-id="45d80-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-246">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="45d80-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="45d80-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="45d80-248">(21)</span><span class="sxs-lookup"><span data-stu-id="45d80-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-249">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="45d80-249">System failure.</span></span> <span data-ttu-id="45d80-250">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="45d80-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="45d80-251">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="45d80-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="45d80-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="45d80-253">(22)</span><span class="sxs-lookup"><span data-stu-id="45d80-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-254">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="45d80-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="45d80-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="45d80-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="45d80-256">(23)</span><span class="sxs-lookup"><span data-stu-id="45d80-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-257">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="45d80-257">System failure.</span></span> <span data-ttu-id="45d80-258">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="45d80-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="45d80-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="45d80-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="45d80-260">(24)</span><span class="sxs-lookup"><span data-stu-id="45d80-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-261">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="45d80-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="45d80-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="45d80-263">(25)</span><span class="sxs-lookup"><span data-stu-id="45d80-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-264">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="45d80-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="45d80-266">(26)</span><span class="sxs-lookup"><span data-stu-id="45d80-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-267">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="45d80-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="45d80-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="45d80-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="45d80-269">(27)</span><span class="sxs-lookup"><span data-stu-id="45d80-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-270">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="45d80-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="45d80-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="45d80-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="45d80-272">(28)</span><span class="sxs-lookup"><span data-stu-id="45d80-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-273">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="45d80-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="45d80-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="45d80-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="45d80-275">(29)</span><span class="sxs-lookup"><span data-stu-id="45d80-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-276">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="45d80-276">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="45d80-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="45d80-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="45d80-278">(30)</span><span class="sxs-lookup"><span data-stu-id="45d80-278">(30)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-279">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="45d80-279">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45d80-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="45d80-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="45d80-281">31</span><span class="sxs-lookup"><span data-stu-id="45d80-281">(31)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-282">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="45d80-282">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d80-283">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="45d80-283">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-284">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45d80-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-286">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45d80-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-287">Indique si l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45d80-287">Indicates whether the device is using a user-defined configuration.</span></span>

<span data-ttu-id="45d80-288">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-289">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45d80-289">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-292">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45d80-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45d80-293">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="45d80-293">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="45d80-294">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="45d80-294">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="45d80-295">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-296">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="45d80-296">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-297">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-297">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-299">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-299">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-300">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="45d80-300">Current value indicated by the sensor.</span></span>

<span data-ttu-id="45d80-301">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-301">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-302">**Description**</span><span class="sxs-lookup"><span data-stu-id="45d80-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-305">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="45d80-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-306">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d80-306">Textual description of the object.</span></span>

<span data-ttu-id="45d80-307">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="45d80-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-311">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45d80-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45d80-312">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45d80-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="45d80-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="45d80-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-315">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45d80-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d80-317">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="45d80-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="45d80-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="45d80-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d80-322">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="45d80-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="45d80-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45d80-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-325">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45d80-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-327">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="45d80-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-328">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d80-328">Date and time when the object was installed.</span></span> <span data-ttu-id="45d80-329">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="45d80-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="45d80-330">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-331">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="45d80-331">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-332">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45d80-332">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d80-334">Si la **valeur est true**, le capteur est linéaire sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="45d80-334">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="45d80-335">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-335">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45d80-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-337">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d80-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d80-339">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45d80-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="45d80-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-341">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="45d80-341">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-342">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-342">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-344">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,13 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-344">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-345">Valeur de seuil qui spécifie si le capteur fonctionne dans des conditions critiques.</span><span class="sxs-lookup"><span data-stu-id="45d80-345">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="45d80-346">Si la propriété **CurrentReading** est comprise entre **LowerThresholdCritical** et **LowerThresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="45d80-346">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="45d80-347">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-347">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-348">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="45d80-348">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-349">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-349">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-351">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-351">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-352">Valeur de seuil qui spécifie si le capteur fonctionne dans des conditions irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="45d80-352">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="45d80-353">Si la propriété **CurrentReading** est en dessous de **LowerThresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="45d80-353">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="45d80-354">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-354">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-355">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="45d80-355">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-356">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-356">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-358">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-358">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-359">Valeur de seuil qui spécifie si le capteur fonctionne dans des conditions normales ou non critiques.</span><span class="sxs-lookup"><span data-stu-id="45d80-359">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="45d80-360">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="45d80-360">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="45d80-361">Si, toutefois, la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **LowerThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="45d80-361">If the **CurrentReading** property, however, is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="45d80-362">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-362">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-363">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="45d80-363">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-364">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-364">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-366">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,9 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-366">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-367">Plus grande valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="45d80-367">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="45d80-368">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-368">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-369">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="45d80-369">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-370">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-370">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-372">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,10 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-372">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-373">Plus petite valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="45d80-373">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="45d80-374">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-374">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-375">**Nom**</span><span class="sxs-lookup"><span data-stu-id="45d80-375">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-378">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="45d80-378">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-379">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="45d80-379">Label by which the object is known.</span></span> <span data-ttu-id="45d80-380">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="45d80-380">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="45d80-381">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-381">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-382">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="45d80-382">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-383">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-383">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-385">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-385">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-386">Valeur attendue pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="45d80-386">Expected value for the numeric sensor.</span></span>

<span data-ttu-id="45d80-387">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-387">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-388">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="45d80-388">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-389">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-389">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-391">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,7 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-391">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-392">Plage maximale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="45d80-392">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="45d80-393">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-393">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-394">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="45d80-394">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-395">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-395">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-397">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,8 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-397">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-398">Plage minimale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="45d80-398">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="45d80-399">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-399">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-400">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="45d80-400">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-403">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45d80-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-404">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="45d80-404">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="45d80-405">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="45d80-405">Example: "\*PNP030b"</span></span>

<span data-ttu-id="45d80-406">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="45d80-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-408">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45d80-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45d80-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d80-410">Fonctionnalités liées à l’alimentation spécifiques de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45d80-410">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="45d80-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45d80-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="45d80-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="45d80-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="45d80-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="45d80-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="45d80-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="45d80-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="45d80-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-416">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="45d80-416">Power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="45d80-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="45d80-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-418">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="45d80-418">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="45d80-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="45d80-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-420">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="45d80-420">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="45d80-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="45d80-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-422">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="45d80-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="45d80-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="45d80-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="45d80-424">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="45d80-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d80-425">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="45d80-425">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-426">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="45d80-426">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-427">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d80-428">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="45d80-428">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="45d80-429">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="45d80-429">This property does not indicate that power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="45d80-430">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="45d80-430">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="45d80-431">Si la valeur est **false**, la valeur entière 1, pour la chaîne « non pris en charge », doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="45d80-431">If **FALSE**, the integer value 1, for the string "Not Supported", should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="45d80-432">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-433">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="45d80-433">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-434">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d80-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-436">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,17 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" dixièmes de milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-436">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-437">Capacité du capteur à résoudre les différences dans la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="45d80-437">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="45d80-438">Cette propriété, ainsi que les propriétés de **précision** et de **tolérance** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="45d80-438">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="45d80-439">Cette valeur peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="45d80-439">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="45d80-440">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-440">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-441">**État**</span><span class="sxs-lookup"><span data-stu-id="45d80-441">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-444">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="45d80-444">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-445">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d80-445">String that indicates the current status of the object.</span></span> <span data-ttu-id="45d80-446">L’état opérationnel et l’état des opérations ne peuvent pas être définis.</span><span class="sxs-lookup"><span data-stu-id="45d80-446">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="45d80-447">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="45d80-447">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="45d80-448">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="45d80-448">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="45d80-449">L’état de fonctionnement peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="45d80-449">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="45d80-450">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="45d80-450">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="45d80-451">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="45d80-451">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="45d80-452">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="45d80-453">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="45d80-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="45d80-454">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="45d80-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="45d80-455">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="45d80-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45d80-456">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="45d80-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45d80-457">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="45d80-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="45d80-458">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="45d80-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="45d80-459">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="45d80-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="45d80-460">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="45d80-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="45d80-461">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="45d80-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="45d80-462">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="45d80-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="45d80-463">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="45d80-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="45d80-464">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="45d80-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="45d80-465">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="45d80-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45d80-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="45d80-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-467">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45d80-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-469">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="45d80-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-470">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="45d80-470">State of the logical device.</span></span> <span data-ttu-id="45d80-471">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="45d80-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="45d80-472">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45d80-473">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="45d80-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45d80-474">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="45d80-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="45d80-475">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="45d80-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="45d80-476">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="45d80-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="45d80-477">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="45d80-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45d80-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45d80-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-479">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-481">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45d80-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45d80-482">Propriété **CreationClassName** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="45d80-482">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="45d80-483">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="45d80-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-485">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d80-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-487">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45d80-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45d80-488">Propriété de **nom** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="45d80-488">Scoping system's **Name** property.</span></span>

<span data-ttu-id="45d80-489">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-490">**Seuil**</span><span class="sxs-lookup"><span data-stu-id="45d80-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-491">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-493">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,18 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-494">Tolérance du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="45d80-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="45d80-495">Cette propriété, ainsi que les propriétés de **résolution** et de **précision** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="45d80-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="45d80-496">La tolérance peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="45d80-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="45d80-497">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="45d80-497">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-498">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-498">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-500">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,14 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-500">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-501">Valeur de seuil qui spécifie si le capteur fonctionne dans des conditions critiques.</span><span class="sxs-lookup"><span data-stu-id="45d80-501">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="45d80-502">Si la propriété **CurrentReading** est comprise entre **UpperThresholdCritical** et **UpperthresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="45d80-502">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="45d80-503">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-503">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-504">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="45d80-504">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-505">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-505">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-506">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-507">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperthresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,16 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-507">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-508">Valeur de seuil qui spécifie si le capteur fonctionne dans des conditions irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="45d80-508">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="45d80-509">Si la propriété **CurrentReading** est au-dessus de **UpperthresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="45d80-509">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="45d80-510">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-510">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d80-511">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="45d80-511">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d80-512">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="45d80-512">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d80-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d80-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d80-514">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonde de courant électrique DMTF \| 001,12 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliampères ")</span><span class="sxs-lookup"><span data-stu-id="45d80-514">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="45d80-515">Valeur de seuil qui spécifie si le capteur fonctionne dans des conditions normales ou non critiques.</span><span class="sxs-lookup"><span data-stu-id="45d80-515">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="45d80-516">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="45d80-516">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="45d80-517">Si, toutefois, la propriété **CurrentReading** est comprise entre **UpperThresholdNonCritical** et **UpperThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="45d80-517">If the **CurrentReading** property, however, is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="45d80-518">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-518">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d80-519">Notes</span><span class="sxs-lookup"><span data-stu-id="45d80-519">Remarks</span></span>

<span data-ttu-id="45d80-520">La classe **CIM \_ CurrentSensor** est dérivée de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-520">The **CIM\_CurrentSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="45d80-521">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="45d80-521">WMI does not implement this class.</span></span> <span data-ttu-id="45d80-522">Pour plus d’informations sur les classes WMI dérivées de **CIM \_ CurrentSensor**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="45d80-522">For more information about WMI classes derived from **CIM\_CurrentSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="45d80-523">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="45d80-523">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="45d80-524">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="45d80-524">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d80-525">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45d80-525">Requirements</span></span>



| <span data-ttu-id="45d80-526">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45d80-526">Requirement</span></span> | <span data-ttu-id="45d80-527">Valeur</span><span class="sxs-lookup"><span data-stu-id="45d80-527">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d80-528">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45d80-528">Minimum supported client</span></span><br/> | <span data-ttu-id="45d80-529">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45d80-529">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45d80-530">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45d80-530">Minimum supported server</span></span><br/> | <span data-ttu-id="45d80-531">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45d80-531">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45d80-532">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45d80-532">Namespace</span></span><br/>                | <span data-ttu-id="45d80-533">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="45d80-533">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45d80-534">MOF</span><span class="sxs-lookup"><span data-stu-id="45d80-534">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45d80-535"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45d80-535"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45d80-536">DLL</span><span class="sxs-lookup"><span data-stu-id="45d80-536">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45d80-537"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45d80-537"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d80-538">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45d80-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d80-539">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="45d80-539">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

