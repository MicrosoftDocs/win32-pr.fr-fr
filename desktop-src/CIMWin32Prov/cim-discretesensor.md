---
description: La \_ classe CIM DiscreteSensor possède un ensemble de valeurs de chaîne valides qu’elle peut signaler. Les valeurs sont énumérées dans la propriété PossibleValues du capteur. Un capteur discret a toujours une lecture actuelle qui correspond à l’une des valeurs énumérées.
ms.assetid: 58ab5b4d-ff8b-4981-8f09-c9a255635110
ms.tgt_platform: multiple
title: Classe CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor
- CIM_DiscreteSensor.AcceptableValues
- CIM_DiscreteSensor.Availability
- CIM_DiscreteSensor.Caption
- CIM_DiscreteSensor.ConfigManagerErrorCode
- CIM_DiscreteSensor.ConfigManagerUserConfig
- CIM_DiscreteSensor.CreationClassName
- CIM_DiscreteSensor.CurrentReading
- CIM_DiscreteSensor.Description
- CIM_DiscreteSensor.DeviceID
- CIM_DiscreteSensor.ErrorCleared
- CIM_DiscreteSensor.ErrorDescription
- CIM_DiscreteSensor.InstallDate
- CIM_DiscreteSensor.LastErrorCode
- CIM_DiscreteSensor.Name
- CIM_DiscreteSensor.PNPDeviceID
- CIM_DiscreteSensor.PossibleValues
- CIM_DiscreteSensor.PowerManagementCapabilities
- CIM_DiscreteSensor.PowerManagementSupported
- CIM_DiscreteSensor.Status
- CIM_DiscreteSensor.StatusInfo
- CIM_DiscreteSensor.SystemCreationClassName
- CIM_DiscreteSensor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5211aa8d840384eaf140c1afbeb2fa9c0680cb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523879"
---
# <a name="cim_discretesensor-class"></a><span data-ttu-id="7f890-105">\_Classe CIM DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="7f890-105">CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="7f890-106">La classe **CIM \_ DiscreteSensor** possède un ensemble de valeurs de chaîne valides qu’elle peut signaler.</span><span class="sxs-lookup"><span data-stu-id="7f890-106">The **CIM\_DiscreteSensor** class has a set of legal string values that it can report.</span></span> <span data-ttu-id="7f890-107">Les valeurs sont énumérées dans la propriété **PossibleValues** du capteur.</span><span class="sxs-lookup"><span data-stu-id="7f890-107">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="7f890-108">Un capteur discret a toujours une lecture actuelle qui correspond à l’une des valeurs énumérées.</span><span class="sxs-lookup"><span data-stu-id="7f890-108">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

<span data-ttu-id="7f890-109">Étant donné l’ajout des propriétés **CurrentState** et **PossibleStates** au [**\_ capteur CIM**](cim-sensor.md), la sous-classe de capteur discrète n’est plus nécessaire. Toutefois, elle est conservée pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="7f890-109">Given the addition of the **CurrentState** and **PossibleStates** properties to [**CIM\_Sensor**](cim-sensor.md), the discrete sensor subclass is no longer necessary; however, it is retained for backward compatibility.</span></span> <span data-ttu-id="7f890-110">Les informations des propriétés **CurrentReading** et **PossibleValues** ont généralement les mêmes valeurs et sémantiques que pour les propriétés **CurrentState** et **PossibleStates** , qui sont héritées **du \_ capteur CIM**.</span><span class="sxs-lookup"><span data-stu-id="7f890-110">Information in the **CurrentReading** and **PossibleValues** properties typically has the same values and semantics as for the **CurrentState** and **PossibleStates** properties, which are inherited from **CIM\_Sensor**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f890-111">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="7f890-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7f890-112">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7f890-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7f890-113">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7f890-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7f890-114">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7f890-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f890-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f890-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{1BF00330-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DiscreteSensor : CIM_Sensor
{
  string   AcceptableValues[];
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  string   PossibleValues[];
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="7f890-116">Membres</span><span class="sxs-lookup"><span data-stu-id="7f890-116">Members</span></span>

<span data-ttu-id="7f890-117">La classe **CIM \_ DiscreteSensor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7f890-117">The **CIM\_DiscreteSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="7f890-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f890-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f890-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f890-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f890-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f890-120">Methods</span></span>

<span data-ttu-id="7f890-121">La classe **CIM \_ DiscreteSensor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7f890-121">The **CIM\_DiscreteSensor** class has these methods.</span></span>



| <span data-ttu-id="7f890-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="7f890-122">Method</span></span>                                                                | <span data-ttu-id="7f890-123">Description</span><span class="sxs-lookup"><span data-stu-id="7f890-123">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f890-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="7f890-124">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="7f890-125">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7f890-125">Requests a reset of the logical device.</span></span> <span data-ttu-id="7f890-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="7f890-126">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="7f890-127">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7f890-127">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="7f890-128">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="7f890-128">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7f890-129">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="7f890-129">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f890-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f890-130">Properties</span></span>

<span data-ttu-id="7f890-131">La classe **CIM \_ DiscreteSensor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7f890-131">The **CIM\_DiscreteSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f890-132">**AcceptableValues**</span><span class="sxs-lookup"><span data-stu-id="7f890-132">**AcceptableValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7f890-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f890-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-135">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7f890-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-136">Les chaînes de la propriété **PossibleValues** sont considérées comme acceptables (c’est-à-dire qu’il ne s’agit pas d’erreurs).</span><span class="sxs-lookup"><span data-stu-id="7f890-136">Strings in the **PossibleValues** property are considered acceptable (that is, they are not errors).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-137">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="7f890-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f890-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7f890-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-141">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-141">Availability and status of the device.</span></span>

<span data-ttu-id="7f890-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f890-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7f890-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f890-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7f890-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7f890-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="7f890-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7f890-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="7f890-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7f890-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="7f890-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f890-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="7f890-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7f890-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="7f890-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7f890-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="7f890-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7f890-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="7f890-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7f890-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="7f890-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7f890-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="7f890-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7f890-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="7f890-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7f890-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="7f890-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-156">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="7f890-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7f890-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="7f890-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-158">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="7f890-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7f890-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="7f890-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-160">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="7f890-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7f890-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="7f890-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7f890-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="7f890-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-163">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="7f890-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7f890-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="7f890-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-165">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="7f890-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7f890-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="7f890-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-167">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="7f890-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7f890-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="7f890-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-169">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="7f890-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7f890-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="7f890-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-171">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="7f890-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f890-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7f890-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-175">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="7f890-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-176">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7f890-176">Short textual description of the object.</span></span>

<span data-ttu-id="7f890-177">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7f890-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-179">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f890-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-181">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f890-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-182">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="7f890-182">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7f890-183">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7f890-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="7f890-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7f890-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="7f890-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-186">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="7f890-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7f890-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="7f890-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7f890-188">(1)</span><span class="sxs-lookup"><span data-stu-id="7f890-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-189">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="7f890-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f890-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7f890-191">(2)</span><span class="sxs-lookup"><span data-stu-id="7f890-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7f890-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="7f890-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7f890-193">(3)</span><span class="sxs-lookup"><span data-stu-id="7f890-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-194">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="7f890-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7f890-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="7f890-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7f890-196">(4)</span><span class="sxs-lookup"><span data-stu-id="7f890-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-197">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="7f890-197">Device is not working properly.</span></span> <span data-ttu-id="7f890-198">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="7f890-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7f890-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="7f890-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7f890-200">(5)</span><span class="sxs-lookup"><span data-stu-id="7f890-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-201">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="7f890-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7f890-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="7f890-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7f890-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="7f890-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-204">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="7f890-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7f890-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="7f890-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7f890-206">(7)</span><span class="sxs-lookup"><span data-stu-id="7f890-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7f890-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="7f890-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7f890-208">(8)</span><span class="sxs-lookup"><span data-stu-id="7f890-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-209">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="7f890-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7f890-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7f890-211">(9)</span><span class="sxs-lookup"><span data-stu-id="7f890-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-212">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7f890-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7f890-214">(10)</span><span class="sxs-lookup"><span data-stu-id="7f890-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-215">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7f890-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7f890-217">(11)</span><span class="sxs-lookup"><span data-stu-id="7f890-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-218">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7f890-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="7f890-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7f890-220">douze</span><span class="sxs-lookup"><span data-stu-id="7f890-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-221">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7f890-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7f890-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7f890-223">(13)</span><span class="sxs-lookup"><span data-stu-id="7f890-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-224">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7f890-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="7f890-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7f890-226">(14)</span><span class="sxs-lookup"><span data-stu-id="7f890-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-227">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="7f890-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7f890-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="7f890-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7f890-229">(15)</span><span class="sxs-lookup"><span data-stu-id="7f890-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-230">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="7f890-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7f890-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7f890-232">(16)</span><span class="sxs-lookup"><span data-stu-id="7f890-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-233">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7f890-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="7f890-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7f890-235">(17)</span><span class="sxs-lookup"><span data-stu-id="7f890-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-236">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="7f890-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f890-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7f890-238">(18)</span><span class="sxs-lookup"><span data-stu-id="7f890-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-239">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="7f890-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7f890-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="7f890-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7f890-241">(19)</span><span class="sxs-lookup"><span data-stu-id="7f890-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7f890-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="7f890-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7f890-243">(20)</span><span class="sxs-lookup"><span data-stu-id="7f890-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-244">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="7f890-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7f890-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7f890-246">(21)</span><span class="sxs-lookup"><span data-stu-id="7f890-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-247">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="7f890-247">System failure.</span></span> <span data-ttu-id="7f890-248">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="7f890-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7f890-249">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7f890-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="7f890-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7f890-251">(22)</span><span class="sxs-lookup"><span data-stu-id="7f890-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-252">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7f890-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7f890-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="7f890-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7f890-254">(23)</span><span class="sxs-lookup"><span data-stu-id="7f890-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-255">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="7f890-255">System failure.</span></span> <span data-ttu-id="7f890-256">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="7f890-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7f890-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="7f890-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7f890-258">(24)</span><span class="sxs-lookup"><span data-stu-id="7f890-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-259">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="7f890-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7f890-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7f890-261">(25)</span><span class="sxs-lookup"><span data-stu-id="7f890-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-262">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7f890-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7f890-264">(26)</span><span class="sxs-lookup"><span data-stu-id="7f890-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-265">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f890-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7f890-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="7f890-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7f890-267">(27)</span><span class="sxs-lookup"><span data-stu-id="7f890-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-268">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="7f890-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7f890-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="7f890-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7f890-270">(28)</span><span class="sxs-lookup"><span data-stu-id="7f890-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-271">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="7f890-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7f890-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="7f890-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7f890-273">(29)</span><span class="sxs-lookup"><span data-stu-id="7f890-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-274">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="7f890-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7f890-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="7f890-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7f890-276">(30)</span><span class="sxs-lookup"><span data-stu-id="7f890-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-277">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="7f890-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f890-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7f890-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7f890-279">31</span><span class="sxs-lookup"><span data-stu-id="7f890-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-280">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="7f890-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f890-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7f890-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-282">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7f890-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-284">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f890-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-285">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f890-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7f890-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f890-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-290">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7f890-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-291">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="7f890-291">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="7f890-292">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7f890-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7f890-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="7f890-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-297">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7f890-297">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-298">Valeur actuelle indiquée par le capteur.</span><span class="sxs-lookup"><span data-stu-id="7f890-298">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="7f890-299">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f890-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-302">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7f890-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-303">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7f890-303">Textual description of the object.</span></span>

<span data-ttu-id="7f890-304">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f890-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-306">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-308">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7f890-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-309">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7f890-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7f890-310">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7f890-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-312">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7f890-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f890-314">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="7f890-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7f890-315">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7f890-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f890-319">Chaîne de forme libre qui fournit plus d’informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="7f890-319">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7f890-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7f890-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-322">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f890-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-324">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="7f890-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-325">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7f890-325">Date and time when the object was installed.</span></span> <span data-ttu-id="7f890-326">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="7f890-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7f890-327">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7f890-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-329">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f890-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f890-331">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7f890-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7f890-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-333">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7f890-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-336">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7f890-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-337">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="7f890-337">Label by which the object is known.</span></span> <span data-ttu-id="7f890-338">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="7f890-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7f890-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f890-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-343">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f890-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-344">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="7f890-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="7f890-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7f890-346">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="7f890-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7f890-347">**PossibleValues**</span><span class="sxs-lookup"><span data-stu-id="7f890-347">**PossibleValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-348">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7f890-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f890-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-350">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7f890-350">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-351">Énumère les sorties de chaîne à partir du capteur discret.</span><span class="sxs-lookup"><span data-stu-id="7f890-351">Enumerates the string outputs from the discrete sensor.</span></span>

</dd> <dt>

<span data-ttu-id="7f890-352">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7f890-352">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-353">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f890-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f890-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f890-355">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="7f890-355">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7f890-356">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="7f890-356">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f890-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="7f890-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7f890-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="7f890-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f890-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="7f890-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f890-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="7f890-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-361">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7f890-361">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7f890-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="7f890-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-363">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="7f890-363">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7f890-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="7f890-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-365">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7f890-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7f890-366">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="7f890-366">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7f890-367">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7f890-367">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7f890-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="7f890-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-369">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="7f890-369">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7f890-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="7f890-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7f890-371">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="7f890-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f890-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7f890-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-373">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7f890-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f890-375">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="7f890-375">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7f890-376">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7f890-376">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7f890-377">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7f890-377">This property does not indicate that power management features are currently enabled, or if enabled, what features are supported.</span></span> <span data-ttu-id="7f890-378">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7f890-378">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7f890-379">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-380">**État**</span><span class="sxs-lookup"><span data-stu-id="7f890-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-383">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7f890-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-384">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7f890-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="7f890-385">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="7f890-385">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7f890-386">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="7f890-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7f890-387">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="7f890-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7f890-388">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="7f890-388">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7f890-389">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="7f890-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7f890-390">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="7f890-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7f890-391">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7f890-392">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f890-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7f890-393">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="7f890-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7f890-394">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="7f890-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7f890-395">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="7f890-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f890-396">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="7f890-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7f890-397">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="7f890-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7f890-398">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="7f890-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7f890-399">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="7f890-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7f890-400">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="7f890-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7f890-401">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="7f890-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7f890-402">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="7f890-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7f890-403">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="7f890-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7f890-404">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="7f890-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f890-405">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7f890-405">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-406">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f890-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-408">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7f890-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7f890-409">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7f890-409">State of the logical device.</span></span> <span data-ttu-id="7f890-410">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7f890-410">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7f890-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f890-412">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7f890-412">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f890-413">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7f890-413">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f890-414">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="7f890-414">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f890-415">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="7f890-415">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f890-416">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="7f890-416">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f890-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f890-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-420">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7f890-420">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-421">Propriété **CreationClassName** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="7f890-421">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="7f890-422">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-422">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f890-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7f890-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f890-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f890-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f890-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f890-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f890-426">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7f890-426">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7f890-427">Propriété de **nom** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="7f890-427">Scoping system's **Name** property.</span></span>

<span data-ttu-id="7f890-428">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f890-429">Notes</span><span class="sxs-lookup"><span data-stu-id="7f890-429">Remarks</span></span>

<span data-ttu-id="7f890-430">La classe **CIM \_ DiscreteSensor** est dérivée [**du \_ capteur CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="7f890-430">The **CIM\_DiscreteSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="7f890-431">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="7f890-431">WMI does not implement this class.</span></span>

<span data-ttu-id="7f890-432">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="7f890-432">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7f890-433">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7f890-433">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f890-434">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f890-434">Requirements</span></span>



| <span data-ttu-id="7f890-435">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f890-435">Requirement</span></span> | <span data-ttu-id="7f890-436">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f890-436">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f890-437">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f890-437">Minimum supported client</span></span><br/> | <span data-ttu-id="7f890-438">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f890-438">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f890-439">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f890-439">Minimum supported server</span></span><br/> | <span data-ttu-id="7f890-440">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f890-440">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f890-441">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f890-441">Namespace</span></span><br/>                | <span data-ttu-id="7f890-442">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7f890-442">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f890-443">MOF</span><span class="sxs-lookup"><span data-stu-id="7f890-443">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f890-444"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f890-444"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f890-445">DLL</span><span class="sxs-lookup"><span data-stu-id="7f890-445">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f890-446"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f890-446"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f890-447">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f890-447">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f890-448">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="7f890-448">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

