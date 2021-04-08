---
description: La \_ classe CIM USBDevice représente les caractéristiques de gestion d’un périphérique USB.
ms.assetid: 0ff39701-826a-434b-a628-0af586600a80
ms.tgt_platform: multiple
title: CIM_USBDevice, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.Availability
- CIM_USBDevice.Caption
- CIM_USBDevice.ClassCode
- CIM_USBDevice.ConfigManagerErrorCode
- CIM_USBDevice.ConfigManagerUserConfig
- CIM_USBDevice.CreationClassName
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.Description
- CIM_USBDevice.DeviceID
- CIM_USBDevice.ErrorCleared
- CIM_USBDevice.ErrorDescription
- CIM_USBDevice.InstallDate
- CIM_USBDevice.LastErrorCode
- CIM_USBDevice.Name
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.PNPDeviceID
- CIM_USBDevice.PowerManagementCapabilities
- CIM_USBDevice.PowerManagementSupported
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.Status
- CIM_USBDevice.StatusInfo
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.SystemCreationClassName
- CIM_USBDevice.SystemName
- CIM_USBDevice.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21b927980716d4ee7ee2e22a352c5c3b34b363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110050"
---
# <a name="cim_usbdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="043b2-103">CIM_USBDevice, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="043b2-103">CIM_USBDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="043b2-104">La classe **CIM \_ USBDevice** représente les caractéristiques de gestion d’un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-104">The **CIM\_USBDevice** class represents the management characteristics of a USB device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="043b2-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="043b2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="043b2-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="043b2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="043b2-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="043b2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="043b2-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="043b2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="043b2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="043b2-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="043b2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="043b2-110">Members</span></span>

<span data-ttu-id="043b2-111">La classe **CIM \_ USBDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="043b2-111">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="043b2-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="043b2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="043b2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="043b2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="043b2-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="043b2-114">Methods</span></span>

<span data-ttu-id="043b2-115">La classe **CIM \_ USBDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="043b2-115">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="043b2-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="043b2-116">Method</span></span>                                                               | <span data-ttu-id="043b2-117">Description</span><span class="sxs-lookup"><span data-stu-id="043b2-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="043b2-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="043b2-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md) | <span data-ttu-id="043b2-119">Retourne le descripteur de périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="043b2-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="043b2-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="043b2-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="043b2-121">**Reset**</span></span>](reset-method-in-class-cim-usbdevice.md)                 | <span data-ttu-id="043b2-122">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="043b2-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="043b2-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="043b2-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="043b2-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="043b2-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbdevice.md) | <span data-ttu-id="043b2-125">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="043b2-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="043b2-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="043b2-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="043b2-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="043b2-127">Properties</span></span>

<span data-ttu-id="043b2-128">La classe **CIM \_ USBDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="043b2-128">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="043b2-129">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="043b2-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b2-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="043b2-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-133">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-133">Availability and status of the device.</span></span>

<span data-ttu-id="043b2-134">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="043b2-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="043b2-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b2-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="043b2-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="043b2-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="043b2-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-138">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="043b2-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="043b2-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="043b2-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="043b2-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="043b2-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="043b2-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="043b2-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="043b2-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="043b2-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="043b2-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="043b2-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="043b2-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="043b2-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="043b2-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="043b2-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="043b2-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="043b2-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="043b2-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="043b2-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="043b2-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="043b2-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-149">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="043b2-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="043b2-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="043b2-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-151">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="043b2-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="043b2-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="043b2-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-153">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="043b2-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="043b2-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="043b2-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="043b2-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="043b2-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-156">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="043b2-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="043b2-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="043b2-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-158">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="043b2-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="043b2-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="043b2-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-160">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="043b2-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="043b2-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="043b2-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-162">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="043b2-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="043b2-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="043b2-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-164">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="043b2-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="043b2-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="043b2-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-168">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="043b2-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-169">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043b2-169">Short textual description of the object.</span></span>

<span data-ttu-id="043b2-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="043b2-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-172">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="043b2-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-174">Code de la classe USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-174">USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="043b2-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="043b2-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-176">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="043b2-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-178">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="043b2-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-179">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="043b2-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="043b2-180">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="043b2-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="043b2-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="043b2-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="043b2-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-183">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="043b2-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="043b2-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="043b2-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="043b2-185">(1)</span><span class="sxs-lookup"><span data-stu-id="043b2-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-186">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="043b2-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="043b2-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="043b2-188">(2)</span><span class="sxs-lookup"><span data-stu-id="043b2-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="043b2-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="043b2-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="043b2-190">(3)</span><span class="sxs-lookup"><span data-stu-id="043b2-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-191">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="043b2-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="043b2-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="043b2-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="043b2-193">(4)</span><span class="sxs-lookup"><span data-stu-id="043b2-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-194">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="043b2-194">Device is not working properly.</span></span> <span data-ttu-id="043b2-195">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="043b2-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="043b2-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="043b2-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="043b2-197">(5)</span><span class="sxs-lookup"><span data-stu-id="043b2-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-198">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="043b2-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="043b2-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="043b2-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="043b2-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="043b2-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-201">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="043b2-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="043b2-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="043b2-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="043b2-203">(7)</span><span class="sxs-lookup"><span data-stu-id="043b2-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="043b2-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="043b2-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="043b2-205">(8)</span><span class="sxs-lookup"><span data-stu-id="043b2-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-206">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="043b2-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="043b2-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="043b2-208">(9)</span><span class="sxs-lookup"><span data-stu-id="043b2-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-209">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="043b2-209">Device is not working properly.</span></span> <span data-ttu-id="043b2-210">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="043b2-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="043b2-212">(10)</span><span class="sxs-lookup"><span data-stu-id="043b2-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-213">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="043b2-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="043b2-215">(11)</span><span class="sxs-lookup"><span data-stu-id="043b2-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-216">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="043b2-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="043b2-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="043b2-218">douze</span><span class="sxs-lookup"><span data-stu-id="043b2-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-219">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="043b2-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="043b2-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="043b2-221">(13)</span><span class="sxs-lookup"><span data-stu-id="043b2-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-222">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="043b2-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="043b2-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="043b2-224">(14)</span><span class="sxs-lookup"><span data-stu-id="043b2-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-225">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="043b2-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="043b2-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="043b2-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="043b2-227">(15)</span><span class="sxs-lookup"><span data-stu-id="043b2-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-228">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="043b2-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="043b2-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="043b2-230">(16)</span><span class="sxs-lookup"><span data-stu-id="043b2-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-231">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="043b2-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="043b2-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="043b2-233">(17)</span><span class="sxs-lookup"><span data-stu-id="043b2-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-234">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="043b2-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="043b2-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="043b2-236">(18)</span><span class="sxs-lookup"><span data-stu-id="043b2-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-237">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="043b2-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="043b2-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="043b2-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="043b2-239">(19)</span><span class="sxs-lookup"><span data-stu-id="043b2-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="043b2-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="043b2-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="043b2-241">(20)</span><span class="sxs-lookup"><span data-stu-id="043b2-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-242">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="043b2-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="043b2-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="043b2-244">(21)</span><span class="sxs-lookup"><span data-stu-id="043b2-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-245">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="043b2-245">System failure.</span></span> <span data-ttu-id="043b2-246">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="043b2-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="043b2-247">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="043b2-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="043b2-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="043b2-249">(22)</span><span class="sxs-lookup"><span data-stu-id="043b2-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-250">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="043b2-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="043b2-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="043b2-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="043b2-252">(23)</span><span class="sxs-lookup"><span data-stu-id="043b2-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-253">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="043b2-253">System failure.</span></span> <span data-ttu-id="043b2-254">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="043b2-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="043b2-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="043b2-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="043b2-256">(24)</span><span class="sxs-lookup"><span data-stu-id="043b2-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-257">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="043b2-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="043b2-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="043b2-259">(25)</span><span class="sxs-lookup"><span data-stu-id="043b2-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-260">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="043b2-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="043b2-262">(26)</span><span class="sxs-lookup"><span data-stu-id="043b2-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-263">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="043b2-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="043b2-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="043b2-265">(27)</span><span class="sxs-lookup"><span data-stu-id="043b2-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-266">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="043b2-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="043b2-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="043b2-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="043b2-268">(28)</span><span class="sxs-lookup"><span data-stu-id="043b2-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-269">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="043b2-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="043b2-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="043b2-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="043b2-271">(29)</span><span class="sxs-lookup"><span data-stu-id="043b2-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-272">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="043b2-272">Device is disabled.</span></span> <span data-ttu-id="043b2-273">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="043b2-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="043b2-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="043b2-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="043b2-275">(30)</span><span class="sxs-lookup"><span data-stu-id="043b2-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-276">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="043b2-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="043b2-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="043b2-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="043b2-278">31</span><span class="sxs-lookup"><span data-stu-id="043b2-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-279">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="043b2-279">Device is not working properly.</span></span> <span data-ttu-id="043b2-280">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="043b2-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="043b2-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="043b2-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-282">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="043b2-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-284">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="043b2-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-285">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="043b2-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="043b2-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043b2-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-290">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b2-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b2-291">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="043b2-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="043b2-292">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="043b2-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="043b2-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-294">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="043b2-294">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-295">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="043b2-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="043b2-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-297">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="043b2-297">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-298">Paramètres USB alternatifs pour chaque interface dans la configuration actuellement sélectionnée (indiquée par la propriété **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="043b2-298">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="043b2-299">Ce tableau possède une entrée pour chaque interface de la configuration.</span><span class="sxs-lookup"><span data-stu-id="043b2-299">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="043b2-300">Si la propriété **CurrentConfigValue** a la valeur 0 (zéro), ce qui indique que l’appareil n’est pas configuré, le tableau n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="043b2-300">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="043b2-301">Pour plus d’informations sur l’analyse de cette chaîne d’octets, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-301">For more information about parsing this octet string, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="043b2-302">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="043b2-302">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-303">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="043b2-303">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-305">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="043b2-305">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-306">Configuration actuellement sélectionnée pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-306">Configuration currently selected for the device.</span></span> <span data-ttu-id="043b2-307">Si la valeur est 0 (zéro), l’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="043b2-307">If the value is 0 (zero), the device is unconfigured.</span></span>

</dd> <dt>

<span data-ttu-id="043b2-308">**Description**</span><span class="sxs-lookup"><span data-stu-id="043b2-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-311">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="043b2-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-312">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043b2-312">Textual description of the object.</span></span>

<span data-ttu-id="043b2-313">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="043b2-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-317">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b2-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b2-318">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="043b2-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="043b2-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="043b2-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-321">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="043b2-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-323">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="043b2-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="043b2-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="043b2-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-328">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="043b2-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="043b2-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="043b2-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-331">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="043b2-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-333">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="043b2-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-334">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043b2-334">Date and time the object was installed.</span></span> <span data-ttu-id="043b2-335">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="043b2-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="043b2-336">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="043b2-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-338">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="043b2-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-340">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="043b2-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="043b2-341">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-342">**Nom**</span><span class="sxs-lookup"><span data-stu-id="043b2-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-345">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="043b2-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-346">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="043b2-346">Label by which the object is known.</span></span> <span data-ttu-id="043b2-347">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="043b2-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="043b2-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-349">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="043b2-349">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-350">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="043b2-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-352">Nombre de configurations d’appareil définies pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="043b2-352">Number of device configurations that are defined for the device.</span></span>

</dd> <dt>

<span data-ttu-id="043b2-353">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="043b2-353">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-356">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="043b2-356">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-357">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="043b2-357">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="043b2-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="043b2-359">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="043b2-359">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="043b2-360">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="043b2-360">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-361">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b2-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="043b2-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-363">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="043b2-363">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="043b2-364">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="043b2-364">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b2-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="043b2-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="043b2-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="043b2-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="043b2-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="043b2-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="043b2-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="043b2-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-369">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="043b2-369">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="043b2-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="043b2-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-371">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="043b2-371">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="043b2-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="043b2-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-373">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="043b2-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="043b2-374">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="043b2-374">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="043b2-375">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="043b2-375">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="043b2-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="043b2-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-377">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="043b2-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="043b2-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="043b2-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="043b2-379">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="043b2-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="043b2-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="043b2-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-381">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="043b2-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-383">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="043b2-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="043b2-384">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="043b2-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="043b2-385">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="043b2-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="043b2-386">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="043b2-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="043b2-387">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-388">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="043b2-388">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-389">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="043b2-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-391">Code de protocole USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-391">USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="043b2-392">**État**</span><span class="sxs-lookup"><span data-stu-id="043b2-392">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-393">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-395">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="043b2-395">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-396">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043b2-396">Current status of the object.</span></span> <span data-ttu-id="043b2-397">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-397">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="043b2-398">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="043b2-398">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="043b2-399">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="043b2-399">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="043b2-400">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="043b2-400">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="043b2-401">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="043b2-401">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b2-402">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="043b2-402">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="043b2-403">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="043b2-403">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="043b2-404">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="043b2-404">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="043b2-405">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="043b2-405">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="043b2-406">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="043b2-406">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="043b2-407">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="043b2-407">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="043b2-408">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="043b2-408">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="043b2-409">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="043b2-409">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="043b2-410">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="043b2-410">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="043b2-411">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="043b2-411">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-412">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b2-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-414">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="043b2-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="043b2-415">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="043b2-415">State of the logical device.</span></span> <span data-ttu-id="043b2-416">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="043b2-416">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="043b2-417">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="043b2-418">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="043b2-418">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b2-419">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="043b2-419">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="043b2-420">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="043b2-420">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="043b2-421">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="043b2-421">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="043b2-422">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="043b2-422">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="043b2-423">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="043b2-423">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-424">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="043b2-424">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-426">Code de sous-classe USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-426">USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="043b2-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043b2-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-430">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b2-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b2-431">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="043b2-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="043b2-432">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="043b2-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043b2-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b2-436">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b2-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b2-437">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="043b2-437">Scoping system's name.</span></span>

<span data-ttu-id="043b2-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b2-439">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="043b2-439">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b2-440">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b2-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043b2-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043b2-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b2-442">Version USB la plus récente prise en charge par le périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="043b2-442">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="043b2-443">Cette propriété est exprimée sous la forme d’une valeur décimale codée binaire (BCD) où une virgule décimale est impliquée entre le deuxième et le troisième chiffre.</span><span class="sxs-lookup"><span data-stu-id="043b2-443">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="043b2-444">Par exemple, la valeur 0x201 indique que la version 2,01 est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="043b2-444">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="043b2-445">Notes</span><span class="sxs-lookup"><span data-stu-id="043b2-445">Remarks</span></span>

<span data-ttu-id="043b2-446">La classe **CIM \_ USBDevice** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-446">The **CIM\_USBDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="043b2-447">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="043b2-447">WMI does not implement this class.</span></span> <span data-ttu-id="043b2-448">Pour les classes WMI qui implémentent **CIM \_ USBDevice**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="043b2-448">For WMI classes that implement **CIM\_USBDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="043b2-449">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="043b2-449">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="043b2-450">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="043b2-450">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="043b2-451">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="043b2-451">Requirements</span></span>



| <span data-ttu-id="043b2-452">Condition requise</span><span class="sxs-lookup"><span data-stu-id="043b2-452">Requirement</span></span> | <span data-ttu-id="043b2-453">Valeur</span><span class="sxs-lookup"><span data-stu-id="043b2-453">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="043b2-454">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="043b2-454">Minimum supported client</span></span><br/> | <span data-ttu-id="043b2-455">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="043b2-455">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="043b2-456">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="043b2-456">Minimum supported server</span></span><br/> | <span data-ttu-id="043b2-457">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="043b2-457">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="043b2-458">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="043b2-458">Namespace</span></span><br/>                | <span data-ttu-id="043b2-459">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="043b2-459">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="043b2-460">MOF</span><span class="sxs-lookup"><span data-stu-id="043b2-460">MOF</span></span><br/>                      | <dl> <span data-ttu-id="043b2-461"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="043b2-461"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="043b2-462">DLL</span><span class="sxs-lookup"><span data-stu-id="043b2-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="043b2-463"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="043b2-463"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="043b2-464">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="043b2-464">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043b2-465">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="043b2-465">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

