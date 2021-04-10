---
description: La \_ classe WMI Win32 FloppyDrive gère les fonctions d’un lecteur de disquette.
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Classe Win32_FloppyDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111215"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="98317-103">\_Classe FloppyDrive Win32</span><span class="sxs-lookup"><span data-stu-id="98317-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="98317-104">\[**Win32 \_ FloppyDrive** n’est plus disponible pour une utilisation à partir de Windows 10 et Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="98317-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="98317-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ FloppyDrive** gère les fonctions d’un lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="98317-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="98317-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="98317-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="98317-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="98317-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98317-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98317-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="98317-109">Membres</span><span class="sxs-lookup"><span data-stu-id="98317-109">Members</span></span>

<span data-ttu-id="98317-110">La classe **Win32 \_ FloppyDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98317-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="98317-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98317-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="98317-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98317-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98317-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98317-113">Methods</span></span>

<span data-ttu-id="98317-114">La classe **Win32 \_ FloppyDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="98317-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="98317-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="98317-115">Method</span></span>            | <span data-ttu-id="98317-116">Description</span><span class="sxs-lookup"><span data-stu-id="98317-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98317-117">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="98317-117">**Reset**</span></span>         | <span data-ttu-id="98317-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="98317-118">Not implemented.</span></span> <span data-ttu-id="98317-119">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="98317-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="98317-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="98317-120">**SetPowerState**</span></span> | <span data-ttu-id="98317-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="98317-121">Not implemented.</span></span> <span data-ttu-id="98317-122">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="98317-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="98317-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98317-123">Properties</span></span>

<span data-ttu-id="98317-124">La classe **Win32 \_ FloppyDrive** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="98317-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98317-125">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="98317-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98317-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98317-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="98317-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="98317-129">État de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-129">Status of the device.</span></span>

<span data-ttu-id="98317-130">Cette propriété est héritée de [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="98317-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98317-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="98317-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98317-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="98317-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="98317-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="98317-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="98317-134">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="98317-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="98317-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="98317-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="98317-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="98317-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="98317-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="98317-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="98317-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="98317-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="98317-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="98317-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="98317-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="98317-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="98317-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="98317-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="98317-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="98317-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="98317-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="98317-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="98317-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="98317-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="98317-145">Économie d’énergie-inconnu</span><span class="sxs-lookup"><span data-stu-id="98317-145">Power Save - Unknown</span></span>

<span data-ttu-id="98317-146">L’appareil est en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="98317-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="98317-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="98317-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="98317-148">Économie d’énergie-mode faible puissance</span><span class="sxs-lookup"><span data-stu-id="98317-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="98317-149">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="98317-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="98317-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="98317-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="98317-151">Économie d’énergie-veille</span><span class="sxs-lookup"><span data-stu-id="98317-151">Power Save - Standby</span></span>

<span data-ttu-id="98317-152">L’appareil ne fonctionne pas, mais peut être rapidement restauré en mode plein-énergie.</span><span class="sxs-lookup"><span data-stu-id="98317-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="98317-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="98317-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="98317-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="98317-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="98317-155">Économie d’énergie-Avertissement</span><span class="sxs-lookup"><span data-stu-id="98317-155">Power Save - Warning</span></span>

<span data-ttu-id="98317-156">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="98317-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="98317-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="98317-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="98317-158">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="98317-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="98317-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="98317-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="98317-160">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="98317-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="98317-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="98317-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="98317-162">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="98317-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="98317-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="98317-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="98317-164">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="98317-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-165">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="98317-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-166">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98317-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98317-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-168">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="98317-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="98317-169">Tableau de fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="98317-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="98317-170">Par exemple, l’appareil peut prendre en charge l’accès aléatoire, le support amovible et le nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="98317-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="98317-171">Dans ce cas, les valeurs 3, 7 et 9 sont écrites dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="98317-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="98317-172">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98317-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="98317-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98317-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="98317-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="98317-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="98317-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="98317-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="98317-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="98317-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="98317-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="98317-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="98317-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="98317-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="98317-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="98317-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="98317-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="98317-181">Prend en charge les supports amovibles</span><span class="sxs-lookup"><span data-stu-id="98317-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="98317-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="98317-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="98317-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="98317-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="98317-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="98317-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="98317-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="98317-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="98317-186">Prend en charge Dual-Sided support</span><span class="sxs-lookup"><span data-stu-id="98317-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="98317-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="98317-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-188">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="98317-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-189">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="98317-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="98317-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-191">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="98317-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="98317-192">Tableau de chaînes de forme libre fournissant des explications plus détaillées sur les fonctionnalités du contrôleur série indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="98317-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="98317-193">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="98317-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="98317-194">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-195">**Caption**</span><span class="sxs-lookup"><span data-stu-id="98317-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-198">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="98317-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="98317-199">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98317-199">Short description of the object.</span></span>

<span data-ttu-id="98317-200">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98317-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-201">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="98317-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-204">Chaîne de forme libre indiquant l’algorithme ou l’outil utilisé par l’appareil pour prendre en charge la compression.</span><span class="sxs-lookup"><span data-stu-id="98317-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="98317-205">S’il n’est pas possible de décrire le schéma de compression (peut-être parce qu’il n’est pas connu), utilisez « Unknown » pour indiquer qu’il n’est pas connu que l’appareil prenne en charge les fonctionnalités de compression. « Compressed » pour représenter que l’appareil prend en charge les fonctionnalités de compression, mais que son schéma de compression n’est pas connu ou n’est pas divulgué ; et « non compressés » pour représenter que l’appareil ne prend pas en charge les fonctionnalités de compression.</span><span class="sxs-lookup"><span data-stu-id="98317-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="98317-206">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="98317-207">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="98317-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="98317-208">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="98317-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="98317-209">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="98317-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="98317-210">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="98317-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="98317-211">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="98317-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="98317-212">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="98317-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="98317-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-214">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98317-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98317-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-216">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="98317-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="98317-217">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="98317-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="98317-218">Cette propriété est héritée de [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="98317-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="98317-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="98317-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="98317-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="98317-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="98317-221">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="98317-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="98317-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="98317-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="98317-223">(1)</span><span class="sxs-lookup"><span data-stu-id="98317-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="98317-224">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="98317-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="98317-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="98317-226">(2)</span><span class="sxs-lookup"><span data-stu-id="98317-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="98317-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="98317-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="98317-228">(3)</span><span class="sxs-lookup"><span data-stu-id="98317-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="98317-229">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="98317-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="98317-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="98317-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="98317-231">(4)</span><span class="sxs-lookup"><span data-stu-id="98317-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="98317-232">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="98317-232">Device is not working properly.</span></span> <span data-ttu-id="98317-233">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="98317-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="98317-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="98317-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="98317-235">(5)</span><span class="sxs-lookup"><span data-stu-id="98317-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="98317-236">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="98317-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="98317-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="98317-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="98317-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="98317-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="98317-239">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="98317-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="98317-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="98317-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="98317-241">(7)</span><span class="sxs-lookup"><span data-stu-id="98317-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="98317-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="98317-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="98317-243">(8)</span><span class="sxs-lookup"><span data-stu-id="98317-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="98317-244">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="98317-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="98317-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="98317-246">(9)</span><span class="sxs-lookup"><span data-stu-id="98317-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="98317-247">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="98317-247">Device is not working properly.</span></span> <span data-ttu-id="98317-248">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="98317-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="98317-250">(10)</span><span class="sxs-lookup"><span data-stu-id="98317-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="98317-251">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="98317-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="98317-253">(11)</span><span class="sxs-lookup"><span data-stu-id="98317-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="98317-254">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="98317-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="98317-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="98317-256">douze</span><span class="sxs-lookup"><span data-stu-id="98317-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="98317-257">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="98317-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="98317-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="98317-259">(13)</span><span class="sxs-lookup"><span data-stu-id="98317-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="98317-260">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="98317-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="98317-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="98317-262">(14)</span><span class="sxs-lookup"><span data-stu-id="98317-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="98317-263">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="98317-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="98317-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="98317-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="98317-265">(15)</span><span class="sxs-lookup"><span data-stu-id="98317-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="98317-266">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="98317-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="98317-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="98317-268">(16)</span><span class="sxs-lookup"><span data-stu-id="98317-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="98317-269">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="98317-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="98317-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="98317-271">(17)</span><span class="sxs-lookup"><span data-stu-id="98317-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="98317-272">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="98317-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="98317-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="98317-274">(18)</span><span class="sxs-lookup"><span data-stu-id="98317-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="98317-275">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="98317-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="98317-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="98317-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="98317-277">(19)</span><span class="sxs-lookup"><span data-stu-id="98317-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="98317-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="98317-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="98317-279">(20)</span><span class="sxs-lookup"><span data-stu-id="98317-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="98317-280">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="98317-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="98317-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="98317-282">(21)</span><span class="sxs-lookup"><span data-stu-id="98317-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="98317-283">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="98317-283">System failure.</span></span> <span data-ttu-id="98317-284">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="98317-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="98317-285">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="98317-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="98317-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="98317-287">(22)</span><span class="sxs-lookup"><span data-stu-id="98317-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="98317-288">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="98317-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="98317-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="98317-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="98317-290">(23)</span><span class="sxs-lookup"><span data-stu-id="98317-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="98317-291">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="98317-291">System failure.</span></span> <span data-ttu-id="98317-292">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="98317-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="98317-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="98317-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="98317-294">(24)</span><span class="sxs-lookup"><span data-stu-id="98317-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="98317-295">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="98317-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="98317-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="98317-297">(25)</span><span class="sxs-lookup"><span data-stu-id="98317-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="98317-298">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="98317-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="98317-300">(26)</span><span class="sxs-lookup"><span data-stu-id="98317-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="98317-301">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="98317-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="98317-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="98317-303">(27)</span><span class="sxs-lookup"><span data-stu-id="98317-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="98317-304">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="98317-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="98317-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="98317-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="98317-306">(28)</span><span class="sxs-lookup"><span data-stu-id="98317-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="98317-307">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="98317-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="98317-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="98317-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="98317-309">(29)</span><span class="sxs-lookup"><span data-stu-id="98317-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="98317-310">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="98317-310">Device is disabled.</span></span> <span data-ttu-id="98317-311">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="98317-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="98317-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="98317-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="98317-313">(30)</span><span class="sxs-lookup"><span data-stu-id="98317-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="98317-314">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="98317-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="98317-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="98317-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="98317-316">31</span><span class="sxs-lookup"><span data-stu-id="98317-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="98317-317">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="98317-317">Device is not working properly.</span></span> <span data-ttu-id="98317-318">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="98317-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="98317-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-320">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="98317-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98317-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-322">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="98317-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="98317-323">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98317-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="98317-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-325">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="98317-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-328">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98317-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98317-329">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="98317-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="98317-330">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="98317-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="98317-331">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-332">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="98317-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-333">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98317-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98317-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-335">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="98317-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="98317-336">Taille de bloc par défaut, en octets, pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="98317-337">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="98317-338">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="98317-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="98317-339">**Description**</span><span class="sxs-lookup"><span data-stu-id="98317-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-342">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="98317-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="98317-343">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98317-343">Description of the object.</span></span>

<span data-ttu-id="98317-344">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98317-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="98317-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-348">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98317-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98317-349">Identificateur unique du lecteur de disquette avec les autres périphériques du système.</span><span class="sxs-lookup"><span data-stu-id="98317-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="98317-350">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="98317-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-352">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="98317-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98317-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-354">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="98317-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="98317-355">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="98317-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-357">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-359">Chaîne de forme libre qui fournit plus d’informations sur l’erreur enregistrée dans **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="98317-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="98317-360">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-361">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="98317-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-364">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="98317-365">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="98317-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-367">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98317-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="98317-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-369">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="98317-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="98317-370">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98317-370">Date and time the object was installed.</span></span> <span data-ttu-id="98317-371">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="98317-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="98317-372">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98317-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-373">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="98317-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-374">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98317-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98317-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-376">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="98317-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="98317-377">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-378">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="98317-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-381">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="98317-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="98317-382">Nom du fabricant du lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="98317-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="98317-383">Exemple : « Acme »</span><span class="sxs-lookup"><span data-stu-id="98317-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="98317-384">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="98317-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-385">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98317-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98317-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-387">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="98317-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="98317-388">Taille maximale de bloc, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="98317-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="98317-389">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="98317-390">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="98317-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="98317-391">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="98317-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-392">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98317-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98317-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="98317-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="98317-395">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="98317-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="98317-396">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="98317-397">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="98317-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="98317-398">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="98317-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-399">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98317-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98317-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-401">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="98317-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="98317-402">Taille de bloc minimale, en octets, pour les médias auxquels ce périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="98317-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="98317-403">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="98317-404">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="98317-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="98317-405">**Nom**</span><span class="sxs-lookup"><span data-stu-id="98317-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-408">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="98317-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="98317-409">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="98317-409">Label by which the object is known.</span></span> <span data-ttu-id="98317-410">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="98317-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="98317-411">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98317-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-412">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="98317-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-413">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="98317-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98317-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-415">Si la **valeur est true**, l’appareil d’accès aux médias nécessite un nettoyage.</span><span class="sxs-lookup"><span data-stu-id="98317-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="98317-416">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété **capacités** .</span><span class="sxs-lookup"><span data-stu-id="98317-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="98317-417">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-418">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="98317-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-419">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98317-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98317-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-421">Nombre maximal de médias individuels qui peuvent être pris en charge ou insérés dans l’appareil d’accès aux médias (en cas de prise en charge).</span><span class="sxs-lookup"><span data-stu-id="98317-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="98317-422">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="98317-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-426">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="98317-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="98317-427">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="98317-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="98317-428">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="98317-429">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="98317-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="98317-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="98317-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-431">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98317-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98317-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-433">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="98317-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="98317-434">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="98317-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98317-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="98317-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="98317-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="98317-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="98317-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="98317-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="98317-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="98317-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="98317-439">activé</span><span class="sxs-lookup"><span data-stu-id="98317-439">Enabled</span></span>

<span data-ttu-id="98317-440">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="98317-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="98317-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="98317-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="98317-442">Modes d’économie d’énergie entrés automatiquement</span><span class="sxs-lookup"><span data-stu-id="98317-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="98317-443">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="98317-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="98317-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="98317-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="98317-445">État d’alimentation définissable</span><span class="sxs-lookup"><span data-stu-id="98317-445">Power State Settable</span></span>

<span data-ttu-id="98317-446">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="98317-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="98317-447">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="98317-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="98317-448">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="98317-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="98317-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="98317-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="98317-450">Cycle d’alimentation pris en charge</span><span class="sxs-lookup"><span data-stu-id="98317-450">Power Cycling Supported</span></span>

<span data-ttu-id="98317-451">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="98317-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="98317-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="98317-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="98317-453">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="98317-453">Timed Power-On Supported</span></span>

<span data-ttu-id="98317-454">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="98317-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-455">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="98317-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-456">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="98317-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98317-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98317-458">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="98317-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="98317-459">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="98317-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="98317-460">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="98317-461">**État**</span><span class="sxs-lookup"><span data-stu-id="98317-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-462">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-463">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-464">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="98317-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="98317-465">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98317-465">Current status of the object.</span></span> <span data-ttu-id="98317-466">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="98317-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="98317-467">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prédit » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="98317-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="98317-468">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="98317-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="98317-469">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="98317-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="98317-470">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="98317-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="98317-471">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98317-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="98317-472">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="98317-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="98317-473">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="98317-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="98317-474">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="98317-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="98317-475">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="98317-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98317-476">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="98317-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="98317-477">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="98317-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="98317-478">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="98317-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="98317-479">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="98317-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="98317-480">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="98317-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="98317-481">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="98317-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="98317-482">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="98317-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="98317-483">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="98317-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="98317-484">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="98317-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="98317-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-486">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98317-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98317-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-488">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="98317-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="98317-489">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="98317-489">State of the logical device.</span></span> <span data-ttu-id="98317-490">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="98317-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="98317-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="98317-492">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="98317-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="98317-493">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="98317-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="98317-494">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="98317-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="98317-495">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="98317-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="98317-496">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="98317-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98317-497">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="98317-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-498">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-500">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98317-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98317-501">Valeur de la propriété de l’étendue **CreationClassName** de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="98317-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="98317-502">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="98317-503">Cette propriété est héritée de [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="98317-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="98317-504">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="98317-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98317-505">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98317-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98317-506">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98317-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98317-507">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98317-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98317-508">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="98317-508">Name of the scoping system.</span></span>

<span data-ttu-id="98317-509">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98317-510">Notes</span><span class="sxs-lookup"><span data-stu-id="98317-510">Remarks</span></span>

<span data-ttu-id="98317-511">La classe **Win32 \_ FloppyDrive** est dérivée de [**CIM \_ DisketteDrive**](cim-diskettedrive.md) qui dérive de [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="98317-512">La classe **CIM \_ MediaAccessDevice** dérive de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="98317-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98317-513">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98317-513">Requirements</span></span>



| <span data-ttu-id="98317-514">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98317-514">Requirement</span></span> | <span data-ttu-id="98317-515">Valeur</span><span class="sxs-lookup"><span data-stu-id="98317-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98317-516">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98317-516">Minimum supported client</span></span><br/> | <span data-ttu-id="98317-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98317-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98317-518">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98317-518">Minimum supported server</span></span><br/> | <span data-ttu-id="98317-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98317-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98317-520">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="98317-520">End of client support</span></span><br/>    | <span data-ttu-id="98317-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="98317-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="98317-522">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="98317-522">End of server support</span></span><br/>    | <span data-ttu-id="98317-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="98317-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="98317-524">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98317-524">Namespace</span></span><br/>                | <span data-ttu-id="98317-525">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="98317-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98317-526">MOF</span><span class="sxs-lookup"><span data-stu-id="98317-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98317-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98317-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98317-528">DLL</span><span class="sxs-lookup"><span data-stu-id="98317-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98317-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98317-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98317-530">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98317-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98317-531">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="98317-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="98317-532">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="98317-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

