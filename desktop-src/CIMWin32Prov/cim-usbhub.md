---
description: La \_ classe CIM USBHub représente les fonctionnalités et la gestion d’un concentrateur USB.
ms.assetid: 33618963-3053-4c01-992e-aa6d9774f84b
ms.tgt_platform: multiple
title: Classe CIM_USBHub
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub
- CIM_USBHub.Availability
- CIM_USBHub.Caption
- CIM_USBHub.ClassCode
- CIM_USBHub.ConfigManagerErrorCode
- CIM_USBHub.ConfigManagerUserConfig
- CIM_USBHub.CreationClassName
- CIM_USBHub.CurrentAlternateSettings
- CIM_USBHub.CurrentConfigValue
- CIM_USBHub.Description
- CIM_USBHub.DeviceID
- CIM_USBHub.ErrorCleared
- CIM_USBHub.ErrorDescription
- CIM_USBHub.GangSwitched
- CIM_USBHub.InstallDate
- CIM_USBHub.LastErrorCode
- CIM_USBHub.Name
- CIM_USBHub.NumberOfConfigs
- CIM_USBHub.NumberOfPorts
- CIM_USBHub.PNPDeviceID
- CIM_USBHub.PowerManagementCapabilities
- CIM_USBHub.PowerManagementSupported
- CIM_USBHub.ProtocolCode
- CIM_USBHub.Status
- CIM_USBHub.StatusInfo
- CIM_USBHub.SubclassCode
- CIM_USBHub.SystemCreationClassName
- CIM_USBHub.SystemName
- CIM_USBHub.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9213b155b069b4aa19f2cbe910c0614f511ff8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950401"
---
# <a name="cim_usbhub-class"></a><span data-ttu-id="f304d-103">CIM \_ USBHub (classe)</span><span class="sxs-lookup"><span data-stu-id="f304d-103">CIM\_USBHub class</span></span>

<span data-ttu-id="f304d-104">La classe **CIM \_ USBHub** représente les fonctionnalités et la gestion d’un concentrateur USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-104">The **CIM\_USBHub** class represents the capabilities and management of a USB hub.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f304d-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f304d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f304d-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f304d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f304d-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f304d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f304d-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f304d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f304d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f304d-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBHub : CIM_USBDevice
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
  boolean  GangSwitched;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  uint8    NumberOfPorts;
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

## <a name="members"></a><span data-ttu-id="f304d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f304d-110">Members</span></span>

<span data-ttu-id="f304d-111">La classe **CIM \_ USBHub** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f304d-111">The **CIM\_USBHub** class has these types of members:</span></span>

-   [<span data-ttu-id="f304d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f304d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f304d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f304d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f304d-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f304d-114">Methods</span></span>

<span data-ttu-id="f304d-115">La classe **CIM \_ USBHub** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f304d-115">The **CIM\_USBHub** class has these methods.</span></span>



| <span data-ttu-id="f304d-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="f304d-116">Method</span></span>                                                            | <span data-ttu-id="f304d-117">Description</span><span class="sxs-lookup"><span data-stu-id="f304d-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f304d-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f304d-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbhub.md) | <span data-ttu-id="f304d-119">Retourne le descripteur de périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="f304d-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="f304d-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="f304d-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="f304d-121">**Reset**</span></span>](reset-method-in-class-cim-usbhub.md)                 | <span data-ttu-id="f304d-122">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f304d-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="f304d-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="f304d-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f304d-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f304d-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbhub.md) | <span data-ttu-id="f304d-125">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="f304d-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f304d-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="f304d-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f304d-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f304d-127">Properties</span></span>

<span data-ttu-id="f304d-128">La classe **CIM \_ USBHub** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f304d-128">The **CIM\_USBHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f304d-129">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="f304d-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f304d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f304d-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-133">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-133">Availability and status of the device.</span></span>

<span data-ttu-id="f304d-134">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f304d-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f304d-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f304d-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f304d-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f304d-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="f304d-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-138">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="f304d-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f304d-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="f304d-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f304d-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="f304d-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f304d-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="f304d-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f304d-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="f304d-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f304d-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="f304d-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f304d-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="f304d-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f304d-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="f304d-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f304d-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="f304d-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f304d-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="f304d-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f304d-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="f304d-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-149">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="f304d-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f304d-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="f304d-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-151">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="f304d-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f304d-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="f304d-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-153">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="f304d-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f304d-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="f304d-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f304d-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="f304d-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-156">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f304d-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f304d-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="f304d-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-158">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="f304d-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f304d-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="f304d-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-160">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="f304d-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f304d-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="f304d-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-162">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="f304d-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f304d-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="f304d-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-164">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="f304d-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f304d-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f304d-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-168">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="f304d-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-169">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f304d-169">Short textual description of the object.</span></span>

<span data-ttu-id="f304d-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="f304d-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-172">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-174">Code de la classe USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-174">USB class code.</span></span>

<span data-ttu-id="f304d-175">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-175">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-176">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f304d-176">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f304d-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-179">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f304d-179">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-180">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="f304d-180">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f304d-181">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-181">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f304d-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="f304d-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f304d-183"> (0)</span><span class="sxs-lookup"><span data-stu-id="f304d-183">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-184">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="f304d-184">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f304d-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="f304d-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f304d-186">(1)</span><span class="sxs-lookup"><span data-stu-id="f304d-186">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-187">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="f304d-187">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f304d-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f304d-189">(2)</span><span class="sxs-lookup"><span data-stu-id="f304d-189">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f304d-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="f304d-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f304d-191">(3)</span><span class="sxs-lookup"><span data-stu-id="f304d-191">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-192">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="f304d-192">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f304d-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="f304d-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f304d-194">(4)</span><span class="sxs-lookup"><span data-stu-id="f304d-194">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-195">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f304d-195">Device is not working properly.</span></span> <span data-ttu-id="f304d-196">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="f304d-196">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f304d-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="f304d-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f304d-198">(5)</span><span class="sxs-lookup"><span data-stu-id="f304d-198">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-199">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="f304d-199">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f304d-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="f304d-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f304d-201"> (6)</span><span class="sxs-lookup"><span data-stu-id="f304d-201">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-202">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="f304d-202">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f304d-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="f304d-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f304d-204">(7)</span><span class="sxs-lookup"><span data-stu-id="f304d-204">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f304d-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="f304d-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f304d-206">(8)</span><span class="sxs-lookup"><span data-stu-id="f304d-206">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-207">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="f304d-207">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f304d-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f304d-209">(9)</span><span class="sxs-lookup"><span data-stu-id="f304d-209">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-210">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f304d-210">Device is not working properly.</span></span> <span data-ttu-id="f304d-211">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-211">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f304d-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f304d-213">(10)</span><span class="sxs-lookup"><span data-stu-id="f304d-213">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-214">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-214">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f304d-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f304d-216">(11)</span><span class="sxs-lookup"><span data-stu-id="f304d-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-217">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-217">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f304d-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="f304d-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f304d-219">douze</span><span class="sxs-lookup"><span data-stu-id="f304d-219">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-220">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f304d-220">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f304d-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f304d-222">(13)</span><span class="sxs-lookup"><span data-stu-id="f304d-222">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-223">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-223">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f304d-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="f304d-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f304d-225">(14)</span><span class="sxs-lookup"><span data-stu-id="f304d-225">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-226">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="f304d-226">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f304d-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="f304d-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f304d-228">(15)</span><span class="sxs-lookup"><span data-stu-id="f304d-228">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-229">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="f304d-229">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f304d-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f304d-231">(16)</span><span class="sxs-lookup"><span data-stu-id="f304d-231">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-232">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-232">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f304d-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="f304d-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f304d-234">(17)</span><span class="sxs-lookup"><span data-stu-id="f304d-234">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-235">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="f304d-235">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f304d-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f304d-237">(18)</span><span class="sxs-lookup"><span data-stu-id="f304d-237">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-238">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="f304d-238">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f304d-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="f304d-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f304d-240">(19)</span><span class="sxs-lookup"><span data-stu-id="f304d-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f304d-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="f304d-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f304d-242">(20)</span><span class="sxs-lookup"><span data-stu-id="f304d-242">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-243">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="f304d-243">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f304d-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f304d-245">(21)</span><span class="sxs-lookup"><span data-stu-id="f304d-245">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-246">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="f304d-246">System failure.</span></span> <span data-ttu-id="f304d-247">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="f304d-247">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f304d-248">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-248">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f304d-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="f304d-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f304d-250">(22)</span><span class="sxs-lookup"><span data-stu-id="f304d-250">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-251">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f304d-251">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f304d-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="f304d-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f304d-253">(23)</span><span class="sxs-lookup"><span data-stu-id="f304d-253">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-254">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="f304d-254">System failure.</span></span> <span data-ttu-id="f304d-255">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="f304d-255">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f304d-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="f304d-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f304d-257">(24)</span><span class="sxs-lookup"><span data-stu-id="f304d-257">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-258">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="f304d-258">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f304d-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f304d-260">(25)</span><span class="sxs-lookup"><span data-stu-id="f304d-260">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-261">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f304d-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f304d-263">(26)</span><span class="sxs-lookup"><span data-stu-id="f304d-263">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-264">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f304d-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="f304d-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f304d-266">(27)</span><span class="sxs-lookup"><span data-stu-id="f304d-266">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-267">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="f304d-267">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f304d-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="f304d-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f304d-269">(28)</span><span class="sxs-lookup"><span data-stu-id="f304d-269">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-270">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="f304d-270">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f304d-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="f304d-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f304d-272">(29)</span><span class="sxs-lookup"><span data-stu-id="f304d-272">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-273">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f304d-273">Device is disabled.</span></span> <span data-ttu-id="f304d-274">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="f304d-274">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f304d-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="f304d-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f304d-276">(30)</span><span class="sxs-lookup"><span data-stu-id="f304d-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-277">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="f304d-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f304d-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="f304d-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f304d-279">31</span><span class="sxs-lookup"><span data-stu-id="f304d-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-280">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f304d-280">Device is not working properly.</span></span> <span data-ttu-id="f304d-281">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="f304d-281">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f304d-282">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f304d-282">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-283">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f304d-283">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-285">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f304d-285">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-286">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f304d-286">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f304d-287">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f304d-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-291">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f304d-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f304d-292">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="f304d-292">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f304d-293">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="f304d-293">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f304d-294">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-295">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="f304d-295">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-296">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-296">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f304d-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-298">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ USBDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="f304d-298">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-299">Paramètres USB alternatifs pour chaque interface dans la configuration actuellement sélectionnée (indiquée par la propriété **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="f304d-299">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="f304d-300">Ce tableau possède une entrée pour chaque interface de la configuration.</span><span class="sxs-lookup"><span data-stu-id="f304d-300">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="f304d-301">Si la propriété **CurrentConfigValue** a la valeur 0 (zéro), ce qui indique que l’appareil n’est pas configuré, le tableau n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f304d-301">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="f304d-302">Pour plus d’informations sur l’analyse de cette chaîne d’octets, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-302">For more information about parsing this octet string, see the USB specification.</span></span>

<span data-ttu-id="f304d-303">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-303">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-304">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="f304d-304">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-305">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-305">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-307">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="f304d-307">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-308">Configuration actuellement sélectionnée pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-308">Configuration currently selected for the device.</span></span> <span data-ttu-id="f304d-309">Si cette valeur est 0 (zéro), l’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="f304d-309">If this value is 0 (zero), the device is unconfigured.</span></span>

<span data-ttu-id="f304d-310">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-310">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-311">**Description**</span><span class="sxs-lookup"><span data-stu-id="f304d-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-314">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f304d-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-315">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f304d-315">Textual description of the object.</span></span>

<span data-ttu-id="f304d-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f304d-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-320">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f304d-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f304d-321">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f304d-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f304d-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f304d-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-324">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f304d-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-326">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="f304d-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f304d-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f304d-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-331">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="f304d-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f304d-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-333">**GangSwitched**</span><span class="sxs-lookup"><span data-stu-id="f304d-333">**GangSwitched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-334">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f304d-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-336">Si la **valeur est true**, l’alimentation est basculée simultanément sur tous les ports du concentrateur.</span><span class="sxs-lookup"><span data-stu-id="f304d-336">If **TRUE**, power is switched to all ports on the hub simultaneously.</span></span> <span data-ttu-id="f304d-337">Si la **valeur est false**, l’alimentation est commutée individuellement pour chaque port.</span><span class="sxs-lookup"><span data-stu-id="f304d-337">If **FALSE**, power is switched individually for each port.</span></span>

</dd> <dt>

<span data-ttu-id="f304d-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f304d-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-339">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f304d-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-341">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="f304d-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-342">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f304d-342">Date and time the object was installed.</span></span> <span data-ttu-id="f304d-343">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="f304d-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f304d-344">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f304d-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-346">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f304d-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-348">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f304d-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f304d-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-350">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f304d-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-351">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-353">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f304d-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-354">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="f304d-354">Label by which the object is known.</span></span> <span data-ttu-id="f304d-355">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="f304d-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f304d-356">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-357">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="f304d-357">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-358">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-358">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-360">Nombre de configurations d’appareil définies pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f304d-360">Number of device configurations that are defined for the device.</span></span>

<span data-ttu-id="f304d-361">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-361">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-362">**NumberOfPorts**</span><span class="sxs-lookup"><span data-stu-id="f304d-362">**NumberOfPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-363">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-363">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-365">Nombre de ports en aval sur le concentrateur, y compris ceux incorporés dans le silicium du concentrateur.</span><span class="sxs-lookup"><span data-stu-id="f304d-365">Number of downstream ports on the hub, including those embedded in the hub's silicon.</span></span>

</dd> <dt>

<span data-ttu-id="f304d-366">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f304d-366">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-369">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f304d-369">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-370">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="f304d-370">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f304d-371">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="f304d-371">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f304d-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-373">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f304d-373">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-374">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f304d-374">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f304d-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-376">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="f304d-376">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f304d-377">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f304d-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f304d-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f304d-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f304d-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f304d-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="f304d-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f304d-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="f304d-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-382">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="f304d-382">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f304d-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="f304d-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-384">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="f304d-384">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f304d-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="f304d-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-386">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f304d-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f304d-387">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="f304d-387">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f304d-388">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f304d-388">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f304d-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="f304d-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-390">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="f304d-390">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f304d-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="f304d-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f304d-392">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="f304d-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f304d-393">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f304d-393">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-394">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f304d-394">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-396">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f304d-396">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f304d-397">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f304d-397">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f304d-398">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f304d-398">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f304d-399">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f304d-399">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f304d-400">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-401">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="f304d-401">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-402">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-402">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-404">Code de protocole USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-404">USB protocol code.</span></span>

<span data-ttu-id="f304d-405">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-405">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-406">**État**</span><span class="sxs-lookup"><span data-stu-id="f304d-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-407">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-409">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f304d-409">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-410">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f304d-410">Current status of the object.</span></span>

<span data-ttu-id="f304d-411">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f304d-412">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f304d-412">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f304d-413">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="f304d-413">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f304d-414">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="f304d-414">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f304d-415">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="f304d-415">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f304d-416">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="f304d-416">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f304d-417">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="f304d-417">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f304d-418">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="f304d-418">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f304d-419">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="f304d-419">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f304d-420">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="f304d-420">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f304d-421">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="f304d-421">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f304d-422">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="f304d-422">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f304d-423">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="f304d-423">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f304d-424">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="f304d-424">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f304d-425">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f304d-425">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-426">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f304d-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-427">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-428">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f304d-428">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f304d-429">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="f304d-429">State of the logical device.</span></span> <span data-ttu-id="f304d-430">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f304d-430">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f304d-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f304d-432">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="f304d-432">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f304d-433">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="f304d-433">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f304d-434">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="f304d-434">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f304d-435">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="f304d-435">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f304d-436">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="f304d-436">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f304d-437">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="f304d-437">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-438">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="f304d-438">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-440">Code de sous-classe USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-440">USB subclass code.</span></span>

<span data-ttu-id="f304d-441">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-441">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-442">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f304d-442">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-445">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f304d-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f304d-446">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f304d-446">Scoping system's creation class name.</span></span>

<span data-ttu-id="f304d-447">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-448">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f304d-448">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-449">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f304d-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f304d-451">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f304d-451">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f304d-452">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f304d-452">Scoping system's name.</span></span>

<span data-ttu-id="f304d-453">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f304d-454">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="f304d-454">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f304d-455">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f304d-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f304d-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f304d-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f304d-457">Version USB la plus récente prise en charge par le périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="f304d-457">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="f304d-458">Cette propriété est exprimée sous la forme d’une valeur décimale codée binaire (BCD) où une virgule décimale est impliquée entre le deuxième et le troisième chiffre.</span><span class="sxs-lookup"><span data-stu-id="f304d-458">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="f304d-459">Par exemple, la valeur 0x201 indique que la version 2,01 est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f304d-459">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

<span data-ttu-id="f304d-460">Cette propriété est héritée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-460">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f304d-461">Notes</span><span class="sxs-lookup"><span data-stu-id="f304d-461">Remarks</span></span>

<span data-ttu-id="f304d-462">La **classe \_ CIM CIM** est dérivée de la [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-462">The **CIM\_USBHub** class is derived from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

<span data-ttu-id="f304d-463">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="f304d-463">WMI does not implement this class.</span></span> <span data-ttu-id="f304d-464">Pour les classes WMI dérivées de **CIM \_ USBHub**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f304d-464">For WMI classes derived from **CIM\_USBHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f304d-465">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f304d-465">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f304d-466">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f304d-466">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f304d-467">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f304d-467">Requirements</span></span>



| <span data-ttu-id="f304d-468">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f304d-468">Requirement</span></span> | <span data-ttu-id="f304d-469">Valeur</span><span class="sxs-lookup"><span data-stu-id="f304d-469">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f304d-470">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f304d-470">Minimum supported client</span></span><br/> | <span data-ttu-id="f304d-471">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f304d-471">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f304d-472">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f304d-472">Minimum supported server</span></span><br/> | <span data-ttu-id="f304d-473">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f304d-473">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f304d-474">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f304d-474">Namespace</span></span><br/>                | <span data-ttu-id="f304d-475">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f304d-475">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f304d-476">MOF</span><span class="sxs-lookup"><span data-stu-id="f304d-476">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f304d-477"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f304d-477"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f304d-478">DLL</span><span class="sxs-lookup"><span data-stu-id="f304d-478">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f304d-479"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f304d-479"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f304d-480">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f304d-480">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f304d-481">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f304d-481">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

