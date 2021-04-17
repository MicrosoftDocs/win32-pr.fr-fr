---
description: La \_ classe ALARMDEVICE CIM est un appareil d’alarme qui émet des indications audibles ou visibles relatives à une situation problématique.
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: Classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523895"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="4b20a-103">\_Classe CIM AlarmDevice</span><span class="sxs-lookup"><span data-stu-id="4b20a-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="4b20a-104">La **classe \_ AlarmDevice CIM** est un appareil d’alarme qui émet des indications audibles ou visibles relatives à une situation problématique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="4b20a-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4b20a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4b20a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4b20a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b20a-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4b20a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b20a-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b20a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4b20a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b20a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="4b20a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4b20a-110">Members</span></span>

<span data-ttu-id="4b20a-111">La classe **CIM \_ AlarmDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4b20a-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4b20a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4b20a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4b20a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b20a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4b20a-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4b20a-114">Methods</span></span>

<span data-ttu-id="4b20a-115">La classe **CIM \_ AlarmDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4b20a-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="4b20a-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="4b20a-116">Method</span></span>                                                                 | <span data-ttu-id="4b20a-117">Description</span><span class="sxs-lookup"><span data-stu-id="4b20a-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b20a-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="4b20a-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="4b20a-119">Demande une réinitialisation d’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-119">Requests a logical device reset.</span></span> <span data-ttu-id="4b20a-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="4b20a-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="4b20a-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4b20a-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="4b20a-122">Définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="4b20a-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="4b20a-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="4b20a-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="4b20a-124">**SetUrgency**</span><span class="sxs-lookup"><span data-stu-id="4b20a-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="4b20a-125">Définit le niveau d’urgence souhaité pour l’alarme.</span><span class="sxs-lookup"><span data-stu-id="4b20a-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="4b20a-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="4b20a-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="4b20a-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b20a-127">Properties</span></span>

<span data-ttu-id="4b20a-128">La classe **CIM \_ AlarmDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b20a-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b20a-129">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="4b20a-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4b20a-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-132">Si la **valeur est true**, l’alarme est audible.</span><span class="sxs-lookup"><span data-stu-id="4b20a-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-133">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="4b20a-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b20a-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-136">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="4b20a-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-137">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4b20a-137">Availability and status of the device.</span></span>

<span data-ttu-id="4b20a-138">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4b20a-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4b20a-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4b20a-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4b20a-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4b20a-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="4b20a-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4b20a-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="4b20a-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4b20a-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="4b20a-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4b20a-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="4b20a-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4b20a-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="4b20a-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4b20a-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="4b20a-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4b20a-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="4b20a-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4b20a-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="4b20a-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4b20a-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="4b20a-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4b20a-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="4b20a-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4b20a-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="4b20a-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-152">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="4b20a-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4b20a-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="4b20a-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-154">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="4b20a-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4b20a-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="4b20a-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-156">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="4b20a-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4b20a-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="4b20a-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4b20a-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="4b20a-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-159">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4b20a-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4b20a-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="4b20a-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-161">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="4b20a-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4b20a-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="4b20a-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-163">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="4b20a-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4b20a-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="4b20a-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-165">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="4b20a-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4b20a-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="4b20a-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-167">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="4b20a-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4b20a-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4b20a-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-171">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-172">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4b20a-172">A short textual description of the object.</span></span>

<span data-ttu-id="4b20a-173">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4b20a-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-175">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b20a-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-177">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4b20a-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-178">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="4b20a-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="4b20a-179">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4b20a-180">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-180">**This device is working properly.**</span></span> <span data-ttu-id="4b20a-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="4b20a-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4b20a-182">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="4b20a-183">(1)</span><span class="sxs-lookup"><span data-stu-id="4b20a-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4b20a-184">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4b20a-185">(2)</span><span class="sxs-lookup"><span data-stu-id="4b20a-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4b20a-186">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4b20a-187">(3)</span><span class="sxs-lookup"><span data-stu-id="4b20a-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4b20a-188">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4b20a-189">(4)</span><span class="sxs-lookup"><span data-stu-id="4b20a-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4b20a-190">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4b20a-191">(5)</span><span class="sxs-lookup"><span data-stu-id="4b20a-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4b20a-192">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4b20a-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="4b20a-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4b20a-194">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-194">**Cannot filter.**</span></span> <span data-ttu-id="4b20a-195">(7)</span><span class="sxs-lookup"><span data-stu-id="4b20a-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4b20a-196">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4b20a-197">(8)</span><span class="sxs-lookup"><span data-stu-id="4b20a-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4b20a-198">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4b20a-199">(9)</span><span class="sxs-lookup"><span data-stu-id="4b20a-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4b20a-200">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-200">**This device cannot start.**</span></span> <span data-ttu-id="4b20a-201">(10)</span><span class="sxs-lookup"><span data-stu-id="4b20a-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4b20a-202">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-202">**This device failed.**</span></span> <span data-ttu-id="4b20a-203">(11)</span><span class="sxs-lookup"><span data-stu-id="4b20a-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4b20a-204">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4b20a-205">douze</span><span class="sxs-lookup"><span data-stu-id="4b20a-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4b20a-206">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4b20a-207">(13)</span><span class="sxs-lookup"><span data-stu-id="4b20a-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4b20a-208">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4b20a-209">(14)</span><span class="sxs-lookup"><span data-stu-id="4b20a-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4b20a-210">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4b20a-211">(15)</span><span class="sxs-lookup"><span data-stu-id="4b20a-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4b20a-212">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4b20a-213">(16)</span><span class="sxs-lookup"><span data-stu-id="4b20a-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4b20a-214">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4b20a-215">(17)</span><span class="sxs-lookup"><span data-stu-id="4b20a-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4b20a-216">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4b20a-217">(18)</span><span class="sxs-lookup"><span data-stu-id="4b20a-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4b20a-218">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="4b20a-219">(19)</span><span class="sxs-lookup"><span data-stu-id="4b20a-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4b20a-220">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="4b20a-221">(20)</span><span class="sxs-lookup"><span data-stu-id="4b20a-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4b20a-222">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4b20a-223">(21)</span><span class="sxs-lookup"><span data-stu-id="4b20a-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4b20a-224">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-224">**This device is disabled.**</span></span> <span data-ttu-id="4b20a-225">(22)</span><span class="sxs-lookup"><span data-stu-id="4b20a-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4b20a-226">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4b20a-227">(23)</span><span class="sxs-lookup"><span data-stu-id="4b20a-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4b20a-228">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4b20a-229">(24)</span><span class="sxs-lookup"><span data-stu-id="4b20a-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4b20a-230">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="4b20a-231">(25)</span><span class="sxs-lookup"><span data-stu-id="4b20a-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4b20a-232">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="4b20a-233">(26)</span><span class="sxs-lookup"><span data-stu-id="4b20a-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4b20a-234">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4b20a-235">(27)</span><span class="sxs-lookup"><span data-stu-id="4b20a-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4b20a-236">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4b20a-237">(28)</span><span class="sxs-lookup"><span data-stu-id="4b20a-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4b20a-238">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4b20a-239">(29)</span><span class="sxs-lookup"><span data-stu-id="4b20a-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4b20a-240">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4b20a-241">(30)</span><span class="sxs-lookup"><span data-stu-id="4b20a-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4b20a-242">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="4b20a-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4b20a-243">31</span><span class="sxs-lookup"><span data-stu-id="4b20a-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4b20a-244">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4b20a-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-245">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4b20a-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-247">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4b20a-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-248">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b20a-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4b20a-249">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-250">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4b20a-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-253">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b20a-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-254">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="4b20a-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4b20a-255">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="4b20a-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4b20a-256">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-257">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b20a-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-260">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4b20a-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-261">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4b20a-261">A textual description of the object.</span></span>

<span data-ttu-id="4b20a-262">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-263">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4b20a-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-266">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b20a-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-267">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="4b20a-268">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-269">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4b20a-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-270">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4b20a-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-272">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="4b20a-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="4b20a-273">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4b20a-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-277">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="4b20a-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="4b20a-278">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4b20a-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-280">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4b20a-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-282">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="4b20a-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-283">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="4b20a-283">Indicates when the object was installed.</span></span> <span data-ttu-id="4b20a-284">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="4b20a-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4b20a-285">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-286">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4b20a-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-287">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b20a-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-289">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4b20a-290">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-291">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4b20a-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-294">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4b20a-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-295">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4b20a-295">Label by which the object is known.</span></span> <span data-ttu-id="4b20a-296">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="4b20a-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4b20a-297">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4b20a-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-301">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4b20a-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-302">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4b20a-303">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="4b20a-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="4b20a-304">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-305">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4b20a-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-306">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b20a-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-308">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="4b20a-309">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4b20a-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4b20a-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-311">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="4b20a-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4b20a-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4b20a-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-313">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4b20a-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4b20a-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="4b20a-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-315">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="4b20a-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4b20a-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="4b20a-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-317">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="4b20a-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4b20a-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="4b20a-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-319">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="4b20a-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4b20a-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="4b20a-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-321">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4b20a-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="4b20a-322">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="4b20a-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="4b20a-323">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4b20a-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4b20a-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="4b20a-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-325">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="4b20a-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4b20a-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="4b20a-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-327">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="4b20a-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4b20a-328">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4b20a-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-329">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4b20a-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-331">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="4b20a-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="4b20a-332">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4b20a-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4b20a-333">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4b20a-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="4b20a-334">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4b20a-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4b20a-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-336">**État**</span><span class="sxs-lookup"><span data-stu-id="4b20a-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-339">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4b20a-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-340">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4b20a-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="4b20a-341">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="4b20a-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4b20a-342">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="4b20a-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4b20a-343">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="4b20a-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4b20a-344">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="4b20a-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4b20a-345">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="4b20a-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4b20a-346">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="4b20a-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4b20a-347">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4b20a-348">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4b20a-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4b20a-349">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4b20a-350">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4b20a-351">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4b20a-352">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="4b20a-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4b20a-353">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4b20a-354">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4b20a-355">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4b20a-356">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4b20a-357">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4b20a-358">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4b20a-359">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4b20a-360">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="4b20a-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4b20a-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4b20a-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-362">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b20a-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-364">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4b20a-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-365">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-365">State of the logical device.</span></span> <span data-ttu-id="4b20a-366">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="4b20a-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="4b20a-367">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4b20a-368">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4b20a-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4b20a-369">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="4b20a-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4b20a-370">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="4b20a-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4b20a-371">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="4b20a-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4b20a-372">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="4b20a-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4b20a-373">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4b20a-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-376">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b20a-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-377">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4b20a-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="4b20a-378">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-379">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4b20a-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-380">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b20a-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-382">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4b20a-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-383">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4b20a-383">The scoping system's name.</span></span>

<span data-ttu-id="4b20a-384">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b20a-385">**Urgence**</span><span class="sxs-lookup"><span data-stu-id="4b20a-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-386">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b20a-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-388">Valeur énumérée qui indique la fréquence relative à laquelle l’alarme clignote, vibre ou émet des tonalités audibles.</span><span class="sxs-lookup"><span data-stu-id="4b20a-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4b20a-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4b20a-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-390">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="4b20a-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4b20a-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4b20a-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-392">Autre.</span><span class="sxs-lookup"><span data-stu-id="4b20a-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4b20a-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="4b20a-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-394">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4b20a-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="4b20a-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informations** (3)</span><span class="sxs-lookup"><span data-stu-id="4b20a-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-396">Informatif.</span><span class="sxs-lookup"><span data-stu-id="4b20a-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="4b20a-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non critique** (4)</span><span class="sxs-lookup"><span data-stu-id="4b20a-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-398">Non critique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4b20a-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (5)</span><span class="sxs-lookup"><span data-stu-id="4b20a-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-400">Critique.</span><span class="sxs-lookup"><span data-stu-id="4b20a-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="4b20a-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Irrécupérable** (6)</span><span class="sxs-lookup"><span data-stu-id="4b20a-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4b20a-402">Irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="4b20a-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4b20a-403">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="4b20a-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b20a-404">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4b20a-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b20a-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b20a-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b20a-406">Si la **valeur est true**, l’alarme est visible.</span><span class="sxs-lookup"><span data-stu-id="4b20a-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b20a-407">Notes</span><span class="sxs-lookup"><span data-stu-id="4b20a-407">Remarks</span></span>

<span data-ttu-id="4b20a-408">La classe **CIM \_ AlarmDevice** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="4b20a-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4b20a-409">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4b20a-409">WMI does not implement this class.</span></span>

<span data-ttu-id="4b20a-410">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b20a-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b20a-411">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4b20a-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b20a-412">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b20a-412">Requirements</span></span>



| <span data-ttu-id="4b20a-413">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b20a-413">Requirement</span></span> | <span data-ttu-id="4b20a-414">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b20a-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b20a-415">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b20a-415">Minimum supported client</span></span><br/> | <span data-ttu-id="4b20a-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b20a-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b20a-417">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b20a-417">Minimum supported server</span></span><br/> | <span data-ttu-id="4b20a-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b20a-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b20a-419">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b20a-419">Namespace</span></span><br/>                | <span data-ttu-id="4b20a-420">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4b20a-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b20a-421">MOF</span><span class="sxs-lookup"><span data-stu-id="4b20a-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b20a-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b20a-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b20a-423">DLL</span><span class="sxs-lookup"><span data-stu-id="4b20a-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b20a-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b20a-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b20a-425">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b20a-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b20a-426">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4b20a-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

