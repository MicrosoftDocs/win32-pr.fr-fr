---
description: La \_ classe du tachymètre CIM existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.
ms.assetid: 30b7c23e-05c6-4fd6-80bc-3f729855ab45
ms.tgt_platform: multiple
title: Classe CIM_Tachometer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Tachometer
- CIM_Tachometer.Accuracy
- CIM_Tachometer.Availability
- CIM_Tachometer.Caption
- CIM_Tachometer.ConfigManagerErrorCode
- CIM_Tachometer.ConfigManagerUserConfig
- CIM_Tachometer.CreationClassName
- CIM_Tachometer.CurrentReading
- CIM_Tachometer.Description
- CIM_Tachometer.DeviceID
- CIM_Tachometer.ErrorCleared
- CIM_Tachometer.ErrorDescription
- CIM_Tachometer.InstallDate
- CIM_Tachometer.IsLinear
- CIM_Tachometer.LastErrorCode
- CIM_Tachometer.LowerThresholdCritical
- CIM_Tachometer.LowerThresholdFatal
- CIM_Tachometer.LowerThresholdNonCritical
- CIM_Tachometer.MaxReadable
- CIM_Tachometer.MinReadable
- CIM_Tachometer.Name
- CIM_Tachometer.NominalReading
- CIM_Tachometer.NormalMax
- CIM_Tachometer.NormalMin
- CIM_Tachometer.PNPDeviceID
- CIM_Tachometer.PowerManagementCapabilities
- CIM_Tachometer.PowerManagementSupported
- CIM_Tachometer.Resolution
- CIM_Tachometer.Status
- CIM_Tachometer.StatusInfo
- CIM_Tachometer.SystemCreationClassName
- CIM_Tachometer.SystemName
- CIM_Tachometer.Tolerance
- CIM_Tachometer.UpperThresholdCritical
- CIM_Tachometer.UpperThresholdFatal
- CIM_Tachometer.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f761d7ef18ef7e27a46d6b5e8a5a00442752561
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514956"
---
# <a name="cim_tachometer-class"></a><span data-ttu-id="31fd3-103">\_Classe du tachymètre CIM</span><span class="sxs-lookup"><span data-stu-id="31fd3-103">CIM\_Tachometer class</span></span>

<span data-ttu-id="31fd3-104">La classe du **\_ tachymètre CIM** existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="31fd3-104">The **CIM\_Tachometer** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="31fd3-105">Avec les ajouts [**au \_ capteur CIM**](cim-sensor.md) et aux classes [**\_ NumericSensor CIM**](cim-numericsensor.md) dans la version 2,2, il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="31fd3-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="31fd3-106">Un tachymètre peut être défini en affectant à la propriété **SensorType** héritée du **\_ capteur CIM** la valeur 5 (« Tachymètre »).</span><span class="sxs-lookup"><span data-stu-id="31fd3-106">A tachometer can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 5 ("Tachometer").</span></span> <span data-ttu-id="31fd3-107">Les autres propriétés de cette classe sont codées en dur pour des valeurs constantes qui correspondent aux définitions dans la hiérarchie de capteur.</span><span class="sxs-lookup"><span data-stu-id="31fd3-107">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31fd3-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="31fd3-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31fd3-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31fd3-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31fd3-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="31fd3-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="31fd3-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="31fd3-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fd3-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31fd3-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{237D964F-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_Tachometer : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="31fd3-113">Membres</span><span class="sxs-lookup"><span data-stu-id="31fd3-113">Members</span></span>

<span data-ttu-id="31fd3-114">La classe du **\_ tachymètre CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="31fd3-114">The **CIM\_Tachometer** class has these types of members:</span></span>

-   [<span data-ttu-id="31fd3-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="31fd3-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="31fd3-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31fd3-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31fd3-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="31fd3-117">Methods</span></span>

<span data-ttu-id="31fd3-118">La classe du **\_ tachymètre CIM** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="31fd3-118">The **CIM\_Tachometer** class has these methods.</span></span>



| <span data-ttu-id="31fd3-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="31fd3-119">Method</span></span>                                                                | <span data-ttu-id="31fd3-120">Description</span><span class="sxs-lookup"><span data-stu-id="31fd3-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31fd3-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="31fd3-121">**Reset**</span></span>](reset-method-in-class-cim-tachometer.md)                 | <span data-ttu-id="31fd3-122">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="31fd3-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="31fd3-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="31fd3-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="31fd3-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tachometer.md) | <span data-ttu-id="31fd3-125">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="31fd3-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="31fd3-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="31fd3-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="31fd3-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31fd3-127">Properties</span></span>

<span data-ttu-id="31fd3-128">La classe du **\_ tachymètre CIM** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="31fd3-128">The **CIM\_Tachometer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31fd3-129">**Précision**</span><span class="sxs-lookup"><span data-stu-id="31fd3-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-130">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-132">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« centièmes de pourcentage »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-132">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-133">Précision du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="31fd3-134">Sa valeur est enregistrée comme plus ou moins centièmes de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="31fd3-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="31fd3-135">Cette propriété, ainsi que les propriétés de **résolution** et de **tolérance** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="31fd3-136">La précision peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="31fd3-137">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="31fd3-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31fd3-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-141">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="31fd3-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-142">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-142">Availability and status of the device.</span></span>

<span data-ttu-id="31fd3-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31fd3-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="31fd3-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31fd3-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="31fd3-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="31fd3-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="31fd3-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-147">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="31fd3-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="31fd3-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="31fd3-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="31fd3-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="31fd3-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="31fd3-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="31fd3-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="31fd3-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="31fd3-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="31fd3-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="31fd3-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="31fd3-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="31fd3-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31fd3-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="31fd3-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="31fd3-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="31fd3-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="31fd3-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="31fd3-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="31fd3-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="31fd3-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-158">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="31fd3-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="31fd3-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="31fd3-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-160">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="31fd3-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="31fd3-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="31fd3-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-162">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="31fd3-162">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="31fd3-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="31fd3-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="31fd3-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="31fd3-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-165">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="31fd3-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="31fd3-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="31fd3-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-167">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="31fd3-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="31fd3-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="31fd3-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-169">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="31fd3-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="31fd3-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="31fd3-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-171">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="31fd3-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="31fd3-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="31fd3-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-173">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="31fd3-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31fd3-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="31fd3-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-177">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-178">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31fd3-178">Short textual description of the object.</span></span>

<span data-ttu-id="31fd3-179">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="31fd3-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-181">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-183">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="31fd3-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-184">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="31fd3-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="31fd3-185">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="31fd3-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="31fd3-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="31fd3-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-188">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="31fd3-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="31fd3-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="31fd3-190">(1)</span><span class="sxs-lookup"><span data-stu-id="31fd3-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-191">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="31fd3-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="31fd3-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="31fd3-193">(2)</span><span class="sxs-lookup"><span data-stu-id="31fd3-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="31fd3-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="31fd3-195">(3)</span><span class="sxs-lookup"><span data-stu-id="31fd3-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-196">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="31fd3-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="31fd3-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="31fd3-198">(4)</span><span class="sxs-lookup"><span data-stu-id="31fd3-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-199">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="31fd3-199">Device is not working properly.</span></span> <span data-ttu-id="31fd3-200">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="31fd3-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="31fd3-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="31fd3-202">(5)</span><span class="sxs-lookup"><span data-stu-id="31fd3-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-203">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="31fd3-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="31fd3-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="31fd3-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="31fd3-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-206">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="31fd3-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="31fd3-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="31fd3-208">(7)</span><span class="sxs-lookup"><span data-stu-id="31fd3-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="31fd3-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="31fd3-210">(8)</span><span class="sxs-lookup"><span data-stu-id="31fd3-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-211">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="31fd3-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="31fd3-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="31fd3-213">(9)</span><span class="sxs-lookup"><span data-stu-id="31fd3-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-214">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="31fd3-214">Device is not working properly.</span></span> <span data-ttu-id="31fd3-215">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="31fd3-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="31fd3-217">(10)</span><span class="sxs-lookup"><span data-stu-id="31fd3-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-218">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="31fd3-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="31fd3-220">(11)</span><span class="sxs-lookup"><span data-stu-id="31fd3-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-221">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="31fd3-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="31fd3-223">douze</span><span class="sxs-lookup"><span data-stu-id="31fd3-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-224">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="31fd3-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="31fd3-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="31fd3-226">(13)</span><span class="sxs-lookup"><span data-stu-id="31fd3-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-227">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="31fd3-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="31fd3-229">(14)</span><span class="sxs-lookup"><span data-stu-id="31fd3-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-230">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="31fd3-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="31fd3-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="31fd3-232">(15)</span><span class="sxs-lookup"><span data-stu-id="31fd3-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-233">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="31fd3-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="31fd3-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="31fd3-235">(16)</span><span class="sxs-lookup"><span data-stu-id="31fd3-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-236">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="31fd3-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="31fd3-238">(17)</span><span class="sxs-lookup"><span data-stu-id="31fd3-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-239">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="31fd3-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="31fd3-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="31fd3-241">(18)</span><span class="sxs-lookup"><span data-stu-id="31fd3-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-242">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="31fd3-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="31fd3-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="31fd3-244">(19)</span><span class="sxs-lookup"><span data-stu-id="31fd3-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="31fd3-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="31fd3-246">(20)</span><span class="sxs-lookup"><span data-stu-id="31fd3-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-247">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="31fd3-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="31fd3-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="31fd3-249">(21)</span><span class="sxs-lookup"><span data-stu-id="31fd3-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-250">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="31fd3-250">System failure.</span></span> <span data-ttu-id="31fd3-251">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="31fd3-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="31fd3-252">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="31fd3-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="31fd3-254">(22)</span><span class="sxs-lookup"><span data-stu-id="31fd3-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-255">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="31fd3-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="31fd3-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="31fd3-257">(23)</span><span class="sxs-lookup"><span data-stu-id="31fd3-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-258">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="31fd3-258">System failure.</span></span> <span data-ttu-id="31fd3-259">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="31fd3-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="31fd3-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="31fd3-261">(24)</span><span class="sxs-lookup"><span data-stu-id="31fd3-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-262">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="31fd3-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="31fd3-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="31fd3-264">(25)</span><span class="sxs-lookup"><span data-stu-id="31fd3-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-265">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="31fd3-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="31fd3-267">(26)</span><span class="sxs-lookup"><span data-stu-id="31fd3-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-268">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31fd3-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="31fd3-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="31fd3-270">(27)</span><span class="sxs-lookup"><span data-stu-id="31fd3-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-271">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="31fd3-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="31fd3-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="31fd3-273">(28)</span><span class="sxs-lookup"><span data-stu-id="31fd3-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-274">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="31fd3-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="31fd3-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="31fd3-276">(29)</span><span class="sxs-lookup"><span data-stu-id="31fd3-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-277">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="31fd3-277">Device is disabled.</span></span> <span data-ttu-id="31fd3-278">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="31fd3-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="31fd3-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="31fd3-280">(30)</span><span class="sxs-lookup"><span data-stu-id="31fd3-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-281">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="31fd3-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="31fd3-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="31fd3-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="31fd3-283">31</span><span class="sxs-lookup"><span data-stu-id="31fd3-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-284">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="31fd3-284">Device is not working properly.</span></span> <span data-ttu-id="31fd3-285">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="31fd3-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31fd3-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="31fd3-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-287">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="31fd3-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-289">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="31fd3-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-290">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31fd3-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="31fd3-291">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31fd3-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-295">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31fd3-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-296">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="31fd3-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="31fd3-297">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="31fd3-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="31fd3-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-299">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="31fd3-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-300">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-302">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-303">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="31fd3-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="31fd3-304">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-305">**Description**</span><span class="sxs-lookup"><span data-stu-id="31fd3-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-306">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-308">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="31fd3-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-309">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31fd3-309">Textual description of the object.</span></span>

<span data-ttu-id="31fd3-310">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-311">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="31fd3-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-314">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31fd3-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-315">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="31fd3-316">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-317">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="31fd3-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-318">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="31fd3-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-320">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="31fd3-321">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="31fd3-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-325">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="31fd3-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="31fd3-326">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31fd3-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-328">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31fd3-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-330">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="31fd3-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-331">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31fd3-331">Date and time the object was installed.</span></span> <span data-ttu-id="31fd3-332">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="31fd3-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="31fd3-333">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-334">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="31fd3-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-335">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="31fd3-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-337">Si la **valeur est true**, le capteur est linéaire sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="31fd3-338">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="31fd3-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-340">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-342">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="31fd3-343">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-344">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="31fd3-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-345">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-347">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-348">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="31fd3-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="31fd3-349">Si la propriété **CurrentReading** est comprise entre **LowerThresholdCritical** et **LowerThresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="31fd3-350">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-351">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="31fd3-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-352">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-354">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-355">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="31fd3-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="31fd3-356">Si la propriété **CurrentReading** est en dessous de **LowerThresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="31fd3-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="31fd3-357">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-358">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="31fd3-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-359">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-361">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-362">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="31fd3-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="31fd3-363">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="31fd3-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="31fd3-364">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **LowerThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="31fd3-365">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-366">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="31fd3-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-367">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-369">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-370">Plus grande valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="31fd3-371">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-372">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="31fd3-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-373">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-375">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-376">Plus petite valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="31fd3-377">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-378">**Nom**</span><span class="sxs-lookup"><span data-stu-id="31fd3-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-381">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="31fd3-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-382">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="31fd3-382">Label by which the object is known.</span></span> <span data-ttu-id="31fd3-383">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="31fd3-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="31fd3-384">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-385">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="31fd3-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-386">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-388">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-389">Valeur attendue ou normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="31fd3-390">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-391">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="31fd3-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-392">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-394">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-395">Plage maximale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="31fd3-396">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-397">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="31fd3-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-398">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-400">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-401">Plage minimale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="31fd3-402">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="31fd3-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-404">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-406">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="31fd3-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-407">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="31fd3-408">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="31fd3-409">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="31fd3-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-410">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="31fd3-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-411">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31fd3-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-413">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="31fd3-414">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="31fd3-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31fd3-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="31fd3-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="31fd3-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="31fd3-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="31fd3-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="31fd3-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="31fd3-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="31fd3-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-419">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="31fd3-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="31fd3-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="31fd3-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-421">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="31fd3-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="31fd3-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="31fd3-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-423">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="31fd3-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="31fd3-424">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="31fd3-425">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="31fd3-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="31fd3-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="31fd3-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-427">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="31fd3-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="31fd3-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="31fd3-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="31fd3-429">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="31fd3-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31fd3-430">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="31fd3-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-431">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="31fd3-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-433">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="31fd3-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="31fd3-434">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="31fd3-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="31fd3-435">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="31fd3-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="31fd3-436">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="31fd3-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="31fd3-437">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-438">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="31fd3-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-439">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-441">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("dixièmes de tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-442">Capacité du capteur à résoudre les différences dans la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="31fd3-443">Cette valeur peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="31fd3-444">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-445">**État**</span><span class="sxs-lookup"><span data-stu-id="31fd3-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-446">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-448">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="31fd3-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-449">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31fd3-449">Current status of the object.</span></span> <span data-ttu-id="31fd3-450">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="31fd3-451">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="31fd3-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="31fd3-452">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="31fd3-453">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31fd3-454">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31fd3-455">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="31fd3-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="31fd3-456">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="31fd3-457">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="31fd3-458">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="31fd3-459">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="31fd3-460">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="31fd3-461">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="31fd3-462">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="31fd3-463">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31fd3-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="31fd3-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-465">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31fd3-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-467">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="31fd3-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-468">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-468">State of the logical device.</span></span> <span data-ttu-id="31fd3-469">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="31fd3-470">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31fd3-471">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="31fd3-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31fd3-472">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="31fd3-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="31fd3-473">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="31fd3-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="31fd3-474">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="31fd3-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="31fd3-475">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="31fd3-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31fd3-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31fd3-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-477">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-478">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-479">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31fd3-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-480">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="31fd3-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="31fd3-481">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="31fd3-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-483">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31fd3-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-484">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-485">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31fd3-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-486">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="31fd3-486">Scoping system's name.</span></span>

<span data-ttu-id="31fd3-487">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-488">**Seuil**</span><span class="sxs-lookup"><span data-stu-id="31fd3-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-489">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-490">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-491">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Tolerance »), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« tours par minute »)</span><span class="sxs-lookup"><span data-stu-id="31fd3-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-492">Tolérance du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="31fd3-493">Cette propriété, ainsi que les propriétés de **résolution** et de **précision** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="31fd3-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="31fd3-494">La tolérance peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="31fd3-495">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-496">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="31fd3-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-497">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-498">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-499">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-500">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="31fd3-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="31fd3-501">Si la propriété **CurrentReading** est comprise entre **UpperThresholdCritical** et **UpperthresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="31fd3-502">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-503">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="31fd3-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-504">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-505">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-506">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperthresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-507">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="31fd3-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="31fd3-508">Si la propriété **CurrentReading** est au-dessus de **UpperthresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="31fd3-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="31fd3-509">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="31fd3-510">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="31fd3-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31fd3-511">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="31fd3-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31fd3-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31fd3-513">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tours par minute")</span><span class="sxs-lookup"><span data-stu-id="31fd3-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="31fd3-514">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="31fd3-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="31fd3-515">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="31fd3-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="31fd3-516">Si la propriété **CurrentReading** est comprise entre **UpperThresholdNonCritical** et **UpperThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="31fd3-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="31fd3-517">Cette propriété est héritée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31fd3-518">Notes</span><span class="sxs-lookup"><span data-stu-id="31fd3-518">Remarks</span></span>

<span data-ttu-id="31fd3-519">La classe du **\_ tachymètre CIM** est dérivée de la [**\_ NumericSensor CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="31fd3-519">The **CIM\_Tachometer** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="31fd3-520">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="31fd3-520">WMI does not implement this class.</span></span>

<span data-ttu-id="31fd3-521">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="31fd3-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31fd3-522">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="31fd3-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fd3-523">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31fd3-523">Requirements</span></span>



| <span data-ttu-id="31fd3-524">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31fd3-524">Requirement</span></span> | <span data-ttu-id="31fd3-525">Valeur</span><span class="sxs-lookup"><span data-stu-id="31fd3-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31fd3-526">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31fd3-526">Minimum supported client</span></span><br/> | <span data-ttu-id="31fd3-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31fd3-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31fd3-528">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31fd3-528">Minimum supported server</span></span><br/> | <span data-ttu-id="31fd3-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31fd3-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31fd3-530">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="31fd3-530">Namespace</span></span><br/>                | <span data-ttu-id="31fd3-531">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="31fd3-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31fd3-532">MOF</span><span class="sxs-lookup"><span data-stu-id="31fd3-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31fd3-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31fd3-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31fd3-534">DLL</span><span class="sxs-lookup"><span data-stu-id="31fd3-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31fd3-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31fd3-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31fd3-536">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31fd3-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fd3-537">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="31fd3-537">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

