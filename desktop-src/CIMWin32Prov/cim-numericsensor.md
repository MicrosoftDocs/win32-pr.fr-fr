---
description: La \_ classe CIM NumericSensor représente un capteur numérique qui retourne des lectures numériques et éventuellement prend en charge les paramètres de seuils.
ms.assetid: 9be9ee28-24ee-49d1-871f-73b504c77518
ms.tgt_platform: multiple
title: Classe CIM_NumericSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NumericSensor
- CIM_NumericSensor.Accuracy
- CIM_NumericSensor.Availability
- CIM_NumericSensor.Caption
- CIM_NumericSensor.ConfigManagerErrorCode
- CIM_NumericSensor.ConfigManagerUserConfig
- CIM_NumericSensor.CreationClassName
- CIM_NumericSensor.CurrentReading
- CIM_NumericSensor.Description
- CIM_NumericSensor.DeviceID
- CIM_NumericSensor.ErrorCleared
- CIM_NumericSensor.ErrorDescription
- CIM_NumericSensor.InstallDate
- CIM_NumericSensor.IsLinear
- CIM_NumericSensor.LastErrorCode
- CIM_NumericSensor.LowerThresholdCritical
- CIM_NumericSensor.LowerThresholdFatal
- CIM_NumericSensor.LowerThresholdNonCritical
- CIM_NumericSensor.MaxReadable
- CIM_NumericSensor.MinReadable
- CIM_NumericSensor.Name
- CIM_NumericSensor.NominalReading
- CIM_NumericSensor.NormalMax
- CIM_NumericSensor.NormalMin
- CIM_NumericSensor.PNPDeviceID
- CIM_NumericSensor.PowerManagementCapabilities
- CIM_NumericSensor.PowerManagementSupported
- CIM_NumericSensor.Resolution
- CIM_NumericSensor.Status
- CIM_NumericSensor.StatusInfo
- CIM_NumericSensor.SystemCreationClassName
- CIM_NumericSensor.SystemName
- CIM_NumericSensor.Tolerance
- CIM_NumericSensor.UpperThresholdCritical
- CIM_NumericSensor.UpperThresholdFatal
- CIM_NumericSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2888b56e39184b05484cacd587be140b94dc732e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515148"
---
# <a name="cim_numericsensor-class"></a><span data-ttu-id="deebb-103">\_Classe CIM NumericSensor</span><span class="sxs-lookup"><span data-stu-id="deebb-103">CIM\_NumericSensor class</span></span>

<span data-ttu-id="deebb-104">La classe **CIM \_ NumericSensor** représente un capteur numérique qui retourne des lectures numériques et éventuellement prend en charge les paramètres de seuils.</span><span class="sxs-lookup"><span data-stu-id="deebb-104">The **CIM\_NumericSensor** class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="deebb-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="deebb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="deebb-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="deebb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="deebb-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="deebb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="deebb-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="deebb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="deebb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="deebb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979C-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_NumericSensor : CIM_Sensor
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

## <a name="members"></a><span data-ttu-id="deebb-110">Membres</span><span class="sxs-lookup"><span data-stu-id="deebb-110">Members</span></span>

<span data-ttu-id="deebb-111">La classe **CIM \_ NumericSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="deebb-111">The **CIM\_NumericSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="deebb-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="deebb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="deebb-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="deebb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="deebb-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="deebb-114">Methods</span></span>

<span data-ttu-id="deebb-115">La classe **CIM \_ NumericSensor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="deebb-115">The **CIM\_NumericSensor** class has these methods.</span></span>



| <span data-ttu-id="deebb-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="deebb-116">Method</span></span>                                                                   | <span data-ttu-id="deebb-117">Description</span><span class="sxs-lookup"><span data-stu-id="deebb-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="deebb-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="deebb-118">**Reset**</span></span>](reset-method-in-class-cim-numericsensor.md)                 | <span data-ttu-id="deebb-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="deebb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="deebb-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="deebb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="deebb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="deebb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-numericsensor.md) | <span data-ttu-id="deebb-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="deebb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="deebb-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="deebb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="deebb-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="deebb-124">Properties</span></span>

<span data-ttu-id="deebb-125">La classe **CIM \_ NumericSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="deebb-125">The **CIM\_NumericSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="deebb-126">**Précision**</span><span class="sxs-lookup"><span data-stu-id="deebb-126">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-127">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-129">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« centièmes de pourcentage »)</span><span class="sxs-lookup"><span data-stu-id="deebb-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-130">Précision du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="deebb-130">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="deebb-131">Sa valeur est enregistrée comme plus ou moins centièmes de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="deebb-131">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="deebb-132">Cette propriété, ainsi que les propriétés de **résolution** et de **tolérance** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="deebb-132">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="deebb-133">La précision peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="deebb-133">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-134">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="deebb-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="deebb-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="deebb-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-138">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-138">Availability and status of the device.</span></span>

<span data-ttu-id="deebb-139">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="deebb-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="deebb-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="deebb-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="deebb-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="deebb-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="deebb-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="deebb-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="deebb-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="deebb-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="deebb-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="deebb-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="deebb-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="deebb-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="deebb-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="deebb-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="deebb-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="deebb-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="deebb-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="deebb-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="deebb-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="deebb-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="deebb-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="deebb-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="deebb-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="deebb-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="deebb-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-153">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="deebb-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="deebb-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="deebb-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-155">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="deebb-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="deebb-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="deebb-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-157">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="deebb-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="deebb-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="deebb-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="deebb-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="deebb-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-160">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="deebb-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="deebb-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="deebb-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-162">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="deebb-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="deebb-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="deebb-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-164">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="deebb-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="deebb-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="deebb-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-166">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="deebb-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="deebb-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="deebb-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-168">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="deebb-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="deebb-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="deebb-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="deebb-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-173">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="deebb-173">Short textual description of the object.</span></span>

<span data-ttu-id="deebb-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="deebb-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-176">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="deebb-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-178">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="deebb-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-179">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="deebb-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="deebb-180">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="deebb-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="deebb-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="deebb-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="deebb-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-183">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="deebb-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="deebb-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="deebb-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="deebb-185">(1)</span><span class="sxs-lookup"><span data-stu-id="deebb-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-186">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="deebb-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="deebb-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="deebb-188">(2)</span><span class="sxs-lookup"><span data-stu-id="deebb-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="deebb-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="deebb-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="deebb-190">(3)</span><span class="sxs-lookup"><span data-stu-id="deebb-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-191">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="deebb-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="deebb-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="deebb-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="deebb-193">(4)</span><span class="sxs-lookup"><span data-stu-id="deebb-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-194">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="deebb-194">Device is not working properly.</span></span> <span data-ttu-id="deebb-195">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="deebb-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="deebb-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="deebb-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="deebb-197">(5)</span><span class="sxs-lookup"><span data-stu-id="deebb-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-198">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="deebb-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="deebb-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="deebb-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="deebb-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="deebb-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-201">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="deebb-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="deebb-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="deebb-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="deebb-203">(7)</span><span class="sxs-lookup"><span data-stu-id="deebb-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="deebb-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="deebb-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="deebb-205">(8)</span><span class="sxs-lookup"><span data-stu-id="deebb-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-206">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="deebb-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="deebb-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="deebb-208">(9)</span><span class="sxs-lookup"><span data-stu-id="deebb-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-209">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="deebb-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="deebb-211">(10)</span><span class="sxs-lookup"><span data-stu-id="deebb-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-212">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="deebb-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="deebb-214">(11)</span><span class="sxs-lookup"><span data-stu-id="deebb-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-215">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="deebb-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="deebb-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="deebb-217">douze</span><span class="sxs-lookup"><span data-stu-id="deebb-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-218">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="deebb-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="deebb-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="deebb-220">(13)</span><span class="sxs-lookup"><span data-stu-id="deebb-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-221">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="deebb-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="deebb-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="deebb-223">(14)</span><span class="sxs-lookup"><span data-stu-id="deebb-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-224">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="deebb-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="deebb-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="deebb-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="deebb-226">(15)</span><span class="sxs-lookup"><span data-stu-id="deebb-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-227">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="deebb-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="deebb-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="deebb-229">(16)</span><span class="sxs-lookup"><span data-stu-id="deebb-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-230">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="deebb-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="deebb-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="deebb-232">(17)</span><span class="sxs-lookup"><span data-stu-id="deebb-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-233">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="deebb-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="deebb-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="deebb-235">(18)</span><span class="sxs-lookup"><span data-stu-id="deebb-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-236">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="deebb-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="deebb-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="deebb-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="deebb-238">(19)</span><span class="sxs-lookup"><span data-stu-id="deebb-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="deebb-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="deebb-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="deebb-240">(20)</span><span class="sxs-lookup"><span data-stu-id="deebb-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-241">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="deebb-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="deebb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="deebb-243">(21)</span><span class="sxs-lookup"><span data-stu-id="deebb-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="deebb-244">System failure.</span></span> <span data-ttu-id="deebb-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="deebb-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="deebb-246">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="deebb-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="deebb-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="deebb-248">(22)</span><span class="sxs-lookup"><span data-stu-id="deebb-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-249">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="deebb-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="deebb-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="deebb-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="deebb-251">(23)</span><span class="sxs-lookup"><span data-stu-id="deebb-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-252">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="deebb-252">System failure.</span></span> <span data-ttu-id="deebb-253">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="deebb-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="deebb-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="deebb-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="deebb-255">(24)</span><span class="sxs-lookup"><span data-stu-id="deebb-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-256">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="deebb-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="deebb-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="deebb-258">(25)</span><span class="sxs-lookup"><span data-stu-id="deebb-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-259">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="deebb-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="deebb-261">(26)</span><span class="sxs-lookup"><span data-stu-id="deebb-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-262">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="deebb-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="deebb-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="deebb-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="deebb-264">(27)</span><span class="sxs-lookup"><span data-stu-id="deebb-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-265">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="deebb-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="deebb-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="deebb-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="deebb-267">(28)</span><span class="sxs-lookup"><span data-stu-id="deebb-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-268">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="deebb-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="deebb-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="deebb-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="deebb-270">(29)</span><span class="sxs-lookup"><span data-stu-id="deebb-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-271">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="deebb-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="deebb-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="deebb-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="deebb-273">(30)</span><span class="sxs-lookup"><span data-stu-id="deebb-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-274">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="deebb-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="deebb-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="deebb-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="deebb-276">31</span><span class="sxs-lookup"><span data-stu-id="deebb-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-277">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="deebb-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="deebb-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="deebb-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-279">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="deebb-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-281">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="deebb-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-282">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="deebb-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="deebb-283">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="deebb-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-287">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="deebb-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="deebb-288">Classe ou sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="deebb-288">Class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="deebb-289">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="deebb-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="deebb-290">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-291">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="deebb-291">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-292">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-292">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-294">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="deebb-294">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-295">**Description**</span><span class="sxs-lookup"><span data-stu-id="deebb-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-298">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="deebb-298">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-299">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="deebb-299">Textual description of the object.</span></span>

<span data-ttu-id="deebb-300">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-301">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="deebb-301">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-304">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="deebb-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="deebb-305">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="deebb-305">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="deebb-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-307">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="deebb-307">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-308">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="deebb-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-310">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="deebb-310">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="deebb-311">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-312">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="deebb-312">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-315">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="deebb-315">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="deebb-316">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="deebb-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-318">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="deebb-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-320">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="deebb-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-321">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="deebb-321">Date and time the object was installed.</span></span> <span data-ttu-id="deebb-322">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="deebb-322">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="deebb-323">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-324">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="deebb-324">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-325">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="deebb-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-327">Si la **valeur est true**, le capteur est linéaire sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="deebb-327">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="deebb-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-329">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="deebb-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-331">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="deebb-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="deebb-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-333">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="deebb-333">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-334">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-334">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-336">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="deebb-336">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="deebb-337">Si la propriété **CurrentReading** est comprise entre **LowerThresholdCritical** et **LowerThresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="deebb-337">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="deebb-338">Cette propriété est héritée de la **\_ NumericSensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="deebb-338">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-339">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="deebb-339">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-340">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-342">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="deebb-342">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="deebb-343">Si la propriété **CurrentReading** est en dessous de **LowerThresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="deebb-343">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="deebb-344">Cette propriété est héritée de la **\_ NumericSensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="deebb-344">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-345">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="deebb-345">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-346">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-348">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="deebb-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="deebb-349">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="deebb-349">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="deebb-350">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **LowerThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="deebb-350">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="deebb-351">Cette propriété est héritée de la **\_ NumericSensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="deebb-351">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-352">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="deebb-352">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-353">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-355">Plus grande valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="deebb-355">Largest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-356">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="deebb-356">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-357">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-359">Plus petite valeur de la propriété mesurée qui peut être lue par le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="deebb-359">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-360">**Nom**</span><span class="sxs-lookup"><span data-stu-id="deebb-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-363">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="deebb-363">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-364">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="deebb-364">Label by which the object is known.</span></span> <span data-ttu-id="deebb-365">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="deebb-365">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="deebb-366">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-367">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="deebb-367">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-368">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-370">Valeur attendue ou « normale » pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="deebb-370">Expected or "normal" value for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-371">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="deebb-371">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-372">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-372">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-374">Plage maximale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="deebb-374">Normal maximum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-375">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="deebb-375">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-376">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-376">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-378">Plage minimale normale pour le capteur numérique.</span><span class="sxs-lookup"><span data-stu-id="deebb-378">Normal minimum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-379">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="deebb-379">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-380">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-382">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="deebb-382">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-383">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="deebb-383">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="deebb-384">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="deebb-385">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="deebb-385">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="deebb-386">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="deebb-386">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-387">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="deebb-387">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="deebb-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-389">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="deebb-389">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="deebb-390">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="deebb-390">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="deebb-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="deebb-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="deebb-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="deebb-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="deebb-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="deebb-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="deebb-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="deebb-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-395">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="deebb-395">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="deebb-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="deebb-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-397">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="deebb-397">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="deebb-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="deebb-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-399">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="deebb-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="deebb-400">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="deebb-400">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="deebb-401">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="deebb-401">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="deebb-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="deebb-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-403">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="deebb-403">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="deebb-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="deebb-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="deebb-405">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="deebb-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="deebb-406">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="deebb-406">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-407">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="deebb-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-409">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="deebb-409">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="deebb-410">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="deebb-410">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="deebb-411">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="deebb-411">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="deebb-412">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="deebb-412">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="deebb-413">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-414">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="deebb-414">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-415">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="deebb-415">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-417">Capacité du capteur à résoudre les différences dans la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="deebb-417">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="deebb-418">Cette valeur peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="deebb-418">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-419">**État**</span><span class="sxs-lookup"><span data-stu-id="deebb-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-422">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="deebb-422">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-423">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="deebb-423">Current status of the object.</span></span>

<span data-ttu-id="deebb-424">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-424">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="deebb-425">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="deebb-425">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="deebb-426">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="deebb-426">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="deebb-427">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="deebb-427">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="deebb-428">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="deebb-428">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="deebb-429">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="deebb-429">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="deebb-430">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="deebb-430">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="deebb-431">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="deebb-431">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="deebb-432">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="deebb-432">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="deebb-433">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="deebb-433">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="deebb-434">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="deebb-434">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="deebb-435">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="deebb-435">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="deebb-436">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="deebb-436">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="deebb-437">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="deebb-437">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="deebb-438">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="deebb-438">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-439">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="deebb-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-441">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="deebb-441">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="deebb-442">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="deebb-442">State of the logical device.</span></span> <span data-ttu-id="deebb-443">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="deebb-443">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="deebb-444">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="deebb-445">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="deebb-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="deebb-446">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="deebb-446">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="deebb-447">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="deebb-447">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="deebb-448">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="deebb-448">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="deebb-449">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="deebb-449">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="deebb-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="deebb-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-451">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-453">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="deebb-453">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="deebb-454">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="deebb-454">Scoping system's creation class name.</span></span>

<span data-ttu-id="deebb-455">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-455">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-456">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="deebb-456">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="deebb-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deebb-459">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="deebb-459">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="deebb-460">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="deebb-460">Scoping system's name.</span></span>

<span data-ttu-id="deebb-461">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="deebb-462">**Seuil**</span><span class="sxs-lookup"><span data-stu-id="deebb-462">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-463">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-463">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-465">Tolérance du capteur pour la propriété mesurée.</span><span class="sxs-lookup"><span data-stu-id="deebb-465">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="deebb-466">Cette propriété, ainsi que les propriétés de **résolution** et de **précision** , sont utilisées pour calculer la valeur réelle de la propriété physique mesurée.</span><span class="sxs-lookup"><span data-stu-id="deebb-466">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="deebb-467">La tolérance peut varier selon que l’appareil est linéaire ou non sur sa plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="deebb-467">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-468">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="deebb-468">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-469">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-469">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-471">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="deebb-471">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="deebb-472">Si la propriété **CurrentReading** est comprise entre **UpperThresholdCritical** et **UpperthresholdFatal**, l’état actuel est critique.</span><span class="sxs-lookup"><span data-stu-id="deebb-472">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="deebb-473">Cette propriété est héritée de la **\_ NumericSensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="deebb-473">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-474">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="deebb-474">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-475">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-475">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-477">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="deebb-477">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="deebb-478">Si la propriété **CurrentReading** est au-dessus de **UpperthresholdFatal**, l’état actuel est fatal.</span><span class="sxs-lookup"><span data-stu-id="deebb-478">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="deebb-479">Cette propriété est héritée de la **\_ NumericSensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="deebb-479">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="deebb-480">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="deebb-480">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deebb-481">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="deebb-481">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="deebb-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="deebb-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deebb-483">Valeur de seuil qui spécifie les plages (valeurs minimales et maximales) pour déterminer si le capteur fonctionne dans des conditions normales, non critiques, critiques ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="deebb-483">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="deebb-484">Si la propriété **CurrentReading** est comprise entre **LowerThresholdNonCritical** et **UpperThresholdNonCritical**, le capteur signale une valeur normale.</span><span class="sxs-lookup"><span data-stu-id="deebb-484">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="deebb-485">Si la propriété **CurrentReading** est comprise entre **UpperThresholdNonCritical** et **UpperThresholdCritical**, l’état actuel n’est pas critique.</span><span class="sxs-lookup"><span data-stu-id="deebb-485">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="deebb-486">Cette propriété est héritée de la **\_ NumericSensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="deebb-486">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="deebb-487">Notes</span><span class="sxs-lookup"><span data-stu-id="deebb-487">Remarks</span></span>

<span data-ttu-id="deebb-488">La classe **CIM \_ NumericSensor** est dérivée [**du \_ capteur CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-488">The **CIM\_NumericSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="deebb-489">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="deebb-489">WMI does not implement this class.</span></span> <span data-ttu-id="deebb-490">Pour les classes dérivées de **CIM \_ NumericSensor**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="deebb-490">For classes derived from **CIM\_NumericSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="deebb-491">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="deebb-491">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="deebb-492">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="deebb-492">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="deebb-493">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="deebb-493">Requirements</span></span>



| <span data-ttu-id="deebb-494">Condition requise</span><span class="sxs-lookup"><span data-stu-id="deebb-494">Requirement</span></span> | <span data-ttu-id="deebb-495">Valeur</span><span class="sxs-lookup"><span data-stu-id="deebb-495">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deebb-496">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="deebb-496">Minimum supported client</span></span><br/> | <span data-ttu-id="deebb-497">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="deebb-497">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="deebb-498">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="deebb-498">Minimum supported server</span></span><br/> | <span data-ttu-id="deebb-499">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="deebb-499">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="deebb-500">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="deebb-500">Namespace</span></span><br/>                | <span data-ttu-id="deebb-501">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="deebb-501">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="deebb-502">MOF</span><span class="sxs-lookup"><span data-stu-id="deebb-502">MOF</span></span><br/>                      | <dl> <span data-ttu-id="deebb-503"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="deebb-503"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="deebb-504">DLL</span><span class="sxs-lookup"><span data-stu-id="deebb-504">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deebb-505"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deebb-505"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deebb-506">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deebb-506">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deebb-507">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="deebb-507">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

