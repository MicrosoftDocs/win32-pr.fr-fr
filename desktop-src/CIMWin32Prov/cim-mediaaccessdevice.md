---
description: La \_ classe CIM MediaAccessDevice représente la possibilité d’accéder à un ou plusieurs médias, puis d’utiliser le média pour stocker et récupérer des données.
ms.assetid: 224a7b08-1566-4b0b-90d8-9991fa188d93
ms.tgt_platform: multiple
title: CIM_MediaAccessDevice, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Caption
- CIM_MediaAccessDevice.Description
- CIM_MediaAccessDevice.InstallDate
- CIM_MediaAccessDevice.Name
- CIM_MediaAccessDevice.Status
- CIM_MediaAccessDevice.Availability
- CIM_MediaAccessDevice.ConfigManagerErrorCode
- CIM_MediaAccessDevice.ConfigManagerUserConfig
- CIM_MediaAccessDevice.CreationClassName
- CIM_MediaAccessDevice.DeviceID
- CIM_MediaAccessDevice.PowerManagementCapabilities
- CIM_MediaAccessDevice.ErrorCleared
- CIM_MediaAccessDevice.ErrorDescription
- CIM_MediaAccessDevice.LastErrorCode
- CIM_MediaAccessDevice.PNPDeviceID
- CIM_MediaAccessDevice.PowerManagementSupported
- CIM_MediaAccessDevice.StatusInfo
- CIM_MediaAccessDevice.SystemCreationClassName
- CIM_MediaAccessDevice.SystemName
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de0b993b4cc1da46b19b1c296fae44e855c5816
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869589"
---
# <a name="cim_mediaaccessdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="63621-103">CIM_MediaAccessDevice, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="63621-103">CIM_MediaAccessDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="63621-104">La classe **CIM \_ MediaAccessDevice** représente la possibilité d’accéder à un ou plusieurs médias, puis d’utiliser le média pour stocker et récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="63621-104">The **CIM\_MediaAccessDevice** class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63621-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="63621-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="63621-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="63621-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="63621-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="63621-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="63621-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="63621-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63621-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63621-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="63621-110">Membres</span><span class="sxs-lookup"><span data-stu-id="63621-110">Members</span></span>

<span data-ttu-id="63621-111">La classe **CIM \_ MediaAccessDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="63621-111">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="63621-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="63621-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="63621-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63621-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63621-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="63621-114">Methods</span></span>

<span data-ttu-id="63621-115">La classe **CIM \_ MediaAccessDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="63621-115">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="63621-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="63621-116">Method</span></span>                                                                       | <span data-ttu-id="63621-117">Description</span><span class="sxs-lookup"><span data-stu-id="63621-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63621-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="63621-118">**Reset**</span></span>](reset-method-in-class-cim-mediaaccessdevice.md)                 | <span data-ttu-id="63621-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="63621-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="63621-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="63621-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="63621-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="63621-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-mediaaccessdevice.md) | <span data-ttu-id="63621-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="63621-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="63621-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="63621-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="63621-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63621-124">Properties</span></span>

<span data-ttu-id="63621-125">La classe **CIM \_ MediaAccessDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="63621-125">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63621-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="63621-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63621-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63621-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="63621-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="63621-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-130">Availability and status of the device.</span></span>

<span data-ttu-id="63621-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63621-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="63621-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63621-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="63621-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="63621-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="63621-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="63621-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="63621-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="63621-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="63621-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="63621-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="63621-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="63621-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="63621-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="63621-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="63621-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="63621-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="63621-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="63621-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="63621-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="63621-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="63621-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="63621-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="63621-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="63621-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="63621-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="63621-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="63621-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="63621-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="63621-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="63621-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="63621-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="63621-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="63621-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="63621-149">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="63621-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="63621-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="63621-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="63621-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="63621-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="63621-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="63621-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="63621-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="63621-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="63621-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="63621-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="63621-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="63621-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="63621-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="63621-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="63621-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="63621-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="63621-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="63621-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="63621-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="63621-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="63621-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="63621-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="63621-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-162">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63621-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="63621-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-164">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="63621-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="63621-165">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="63621-165">Capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63621-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="63621-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="63621-167">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="63621-167">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63621-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="63621-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="63621-169">Autre.</span><span class="sxs-lookup"><span data-stu-id="63621-169">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="63621-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="63621-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="63621-171">Accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="63621-171">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="63621-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="63621-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63621-173">Accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="63621-173">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="63621-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="63621-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="63621-175">Écriture.</span><span class="sxs-lookup"><span data-stu-id="63621-175">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="63621-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="63621-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="63621-177">Chiffrement.</span><span class="sxs-lookup"><span data-stu-id="63621-177">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="63621-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="63621-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="63621-179">Compression.</span><span class="sxs-lookup"><span data-stu-id="63621-179">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="63621-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="63621-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="63621-181">Support amovible.</span><span class="sxs-lookup"><span data-stu-id="63621-181">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="63621-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="63621-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="63621-183">Nettoyage manuel.</span><span class="sxs-lookup"><span data-stu-id="63621-183">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="63621-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="63621-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="63621-185">Nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="63621-185">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="63621-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="63621-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="63621-187">Notification intelligente.</span><span class="sxs-lookup"><span data-stu-id="63621-187">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="63621-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="63621-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="63621-189">Média double face.</span><span class="sxs-lookup"><span data-stu-id="63621-189">Dual-sided media.</span></span>

<span data-ttu-id="63621-190">Distingue un appareil qui peut accéder aux deux côtés d’un média à deux faces à partir d’un appareil qui ne lit qu’un seul côté et requiert le basculement du média.</span><span class="sxs-lookup"><span data-stu-id="63621-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="63621-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="63621-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="63621-192">Indique qu’il n’est pas nécessaire d’éjecter explicitement le média de l’appareil avant d’y accéder par un élément sélecteur.</span><span class="sxs-lookup"><span data-stu-id="63621-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-193">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="63621-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-194">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="63621-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="63621-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-196">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="63621-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="63621-197">Tableau de chaînes de forme libre qui fournit des explications détaillées pour l’accès aux fonctionnalités d’appareil indiquées dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="63621-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="63621-198">Chaque entrée de ce tableau est liée à l’entrée dans le tableau des **fonctionnalités** , située dans le même index.</span><span class="sxs-lookup"><span data-stu-id="63621-198">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="63621-199">**Caption**</span><span class="sxs-lookup"><span data-stu-id="63621-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-202">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="63621-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="63621-203">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63621-203">A short textual description of the object.</span></span>

<span data-ttu-id="63621-204">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63621-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-205">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="63621-205">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-208">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="63621-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="63621-209">S’il n’est pas possible de décrire le schéma de compression (car il est inconnu), utilisez ce qui suit : if, use « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="63621-209">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="63621-210">Si, utilisez « Compressed ».</span><span class="sxs-lookup"><span data-stu-id="63621-210">If , use "Compressed".</span></span> <span data-ttu-id="63621-211">, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="63621-211">, use "Not Compressed".</span></span>

<dt>

<span data-ttu-id="63621-212">Connue</span><span class="sxs-lookup"><span data-stu-id="63621-212">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="63621-213">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="63621-213">The compression scheme is unknown or not described.</span></span>

</dd> <dt>

<span data-ttu-id="63621-214">Compact</span><span class="sxs-lookup"><span data-stu-id="63621-214">"Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="63621-215">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="63621-215">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>

<span data-ttu-id="63621-216">« Non compressé »</span><span class="sxs-lookup"><span data-stu-id="63621-216">"Not Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="63621-217">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="63621-217">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-218">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="63621-218">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-219">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63621-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63621-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-221">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="63621-221">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="63621-222">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="63621-222">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="63621-223">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-223">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="63621-224">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="63621-224">**This device is working properly.**</span></span> <span data-ttu-id="63621-225"> (0)</span><span class="sxs-lookup"><span data-stu-id="63621-225">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="63621-226">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="63621-226">**This device is not configured correctly.**</span></span> <span data-ttu-id="63621-227">(1)</span><span class="sxs-lookup"><span data-stu-id="63621-227">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="63621-228">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-228">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="63621-229">(2)</span><span class="sxs-lookup"><span data-stu-id="63621-229">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="63621-230">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="63621-230">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="63621-231">(3)</span><span class="sxs-lookup"><span data-stu-id="63621-231">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="63621-232">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="63621-232">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="63621-233">(4)</span><span class="sxs-lookup"><span data-stu-id="63621-233">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="63621-234">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="63621-234">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="63621-235">(5)</span><span class="sxs-lookup"><span data-stu-id="63621-235">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="63621-236">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="63621-236">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="63621-237"> (6)</span><span class="sxs-lookup"><span data-stu-id="63621-237">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="63621-238">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="63621-238">**Cannot filter.**</span></span> <span data-ttu-id="63621-239">(7)</span><span class="sxs-lookup"><span data-stu-id="63621-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="63621-240">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="63621-240">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="63621-241">(8)</span><span class="sxs-lookup"><span data-stu-id="63621-241">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="63621-242">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-242">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="63621-243">(9)</span><span class="sxs-lookup"><span data-stu-id="63621-243">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="63621-244">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-244">**This device cannot start.**</span></span> <span data-ttu-id="63621-245">(10)</span><span class="sxs-lookup"><span data-stu-id="63621-245">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="63621-246">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-246">**This device failed.**</span></span> <span data-ttu-id="63621-247">(11)</span><span class="sxs-lookup"><span data-stu-id="63621-247">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="63621-248">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="63621-248">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="63621-249">douze</span><span class="sxs-lookup"><span data-stu-id="63621-249">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="63621-250">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-250">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="63621-251">(13)</span><span class="sxs-lookup"><span data-stu-id="63621-251">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="63621-252">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="63621-252">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="63621-253">(14)</span><span class="sxs-lookup"><span data-stu-id="63621-253">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="63621-254">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="63621-254">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="63621-255">(15)</span><span class="sxs-lookup"><span data-stu-id="63621-255">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="63621-256">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-256">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="63621-257">(16)</span><span class="sxs-lookup"><span data-stu-id="63621-257">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="63621-258">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="63621-258">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="63621-259">(17)</span><span class="sxs-lookup"><span data-stu-id="63621-259">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="63621-260">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-260">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="63621-261">(18)</span><span class="sxs-lookup"><span data-stu-id="63621-261">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="63621-262">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="63621-262">**Failure using the VxD loader.**</span></span> <span data-ttu-id="63621-263">(19)</span><span class="sxs-lookup"><span data-stu-id="63621-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="63621-264">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="63621-264">**Your registry might be corrupted.**</span></span> <span data-ttu-id="63621-265">(20)</span><span class="sxs-lookup"><span data-stu-id="63621-265">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="63621-266">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-266">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="63621-267">(21)</span><span class="sxs-lookup"><span data-stu-id="63621-267">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="63621-268">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="63621-268">**This device is disabled.**</span></span> <span data-ttu-id="63621-269">(22)</span><span class="sxs-lookup"><span data-stu-id="63621-269">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="63621-270">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="63621-270">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="63621-271">(23)</span><span class="sxs-lookup"><span data-stu-id="63621-271">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="63621-272">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="63621-272">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="63621-273">(24)</span><span class="sxs-lookup"><span data-stu-id="63621-273">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="63621-274">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-274">**Windows is still setting up this device.**</span></span> <span data-ttu-id="63621-275">(25)</span><span class="sxs-lookup"><span data-stu-id="63621-275">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="63621-276">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-276">**Windows is still setting up this device.**</span></span> <span data-ttu-id="63621-277">(26)</span><span class="sxs-lookup"><span data-stu-id="63621-277">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="63621-278">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="63621-278">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="63621-279">(27)</span><span class="sxs-lookup"><span data-stu-id="63621-279">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="63621-280">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="63621-280">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="63621-281">(28)</span><span class="sxs-lookup"><span data-stu-id="63621-281">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="63621-282">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="63621-282">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="63621-283">(29)</span><span class="sxs-lookup"><span data-stu-id="63621-283">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="63621-284">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="63621-284">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="63621-285">(30)</span><span class="sxs-lookup"><span data-stu-id="63621-285">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="63621-286">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="63621-286">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="63621-287">31</span><span class="sxs-lookup"><span data-stu-id="63621-287">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="63621-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-289">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63621-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63621-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-291">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="63621-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="63621-292">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63621-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="63621-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63621-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-297">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63621-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63621-298">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="63621-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="63621-299">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="63621-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="63621-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-301">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="63621-301">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-302">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63621-302">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63621-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-304">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="63621-304">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="63621-305">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-305">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="63621-306">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63621-306">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63621-307">**Description**</span><span class="sxs-lookup"><span data-stu-id="63621-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-310">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="63621-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="63621-311">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63621-311">A textual description of the object.</span></span>

<span data-ttu-id="63621-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63621-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="63621-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-316">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63621-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63621-317">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="63621-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="63621-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="63621-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-320">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63621-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63621-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-322">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="63621-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="63621-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="63621-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-327">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="63621-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="63621-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="63621-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-332">Chaîne de forme libre qui décrit les types de détection d’erreurs et de correction pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-332">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="63621-333">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="63621-333">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-334">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="63621-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63621-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-336">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="63621-336">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="63621-337">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="63621-337">Indicates when the object was installed.</span></span> <span data-ttu-id="63621-338">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="63621-338">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="63621-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63621-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="63621-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-341">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63621-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63621-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-343">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="63621-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="63621-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-345">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="63621-345">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-346">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63621-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63621-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-348">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="63621-348">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="63621-349">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-349">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="63621-350">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63621-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63621-351">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="63621-351">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-352">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63621-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63621-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-354">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="63621-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="63621-355">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-355">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="63621-356">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="63621-356">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="63621-357">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63621-357">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63621-358">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="63621-358">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-359">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="63621-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="63621-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-361">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="63621-361">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="63621-362">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-362">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="63621-363">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="63621-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="63621-364">**Nom**</span><span class="sxs-lookup"><span data-stu-id="63621-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-367">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="63621-367">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="63621-368">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="63621-368">Label by which the object is known.</span></span> <span data-ttu-id="63621-369">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="63621-369">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="63621-370">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63621-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-371">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="63621-371">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-372">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63621-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63621-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-374">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="63621-374">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="63621-375">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété du tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="63621-375">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

</dd> <dt>

<span data-ttu-id="63621-376">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="63621-376">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-377">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63621-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63621-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-379">Nombre maximal de plusieurs supports individuels qui peuvent être pris en charge ou insérés.</span><span class="sxs-lookup"><span data-stu-id="63621-379">Maximum number of multiple individual media that can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="63621-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="63621-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-383">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="63621-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="63621-384">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="63621-384">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="63621-385">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="63621-385">Example: "\*PNP030b"</span></span>

<span data-ttu-id="63621-386">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="63621-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-388">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63621-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="63621-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-390">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="63621-390">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="63621-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63621-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="63621-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="63621-393">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="63621-393">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="63621-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="63621-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="63621-395">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="63621-395">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="63621-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="63621-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="63621-397">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="63621-397">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="63621-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="63621-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63621-399">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="63621-399">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="63621-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="63621-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="63621-401">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="63621-401">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="63621-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="63621-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="63621-403">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="63621-403">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="63621-404">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="63621-404">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="63621-405">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="63621-405">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="63621-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="63621-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="63621-407">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="63621-407">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="63621-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="63621-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="63621-409">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="63621-409">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-410">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="63621-410">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-411">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63621-411">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63621-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63621-413">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="63621-413">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="63621-414">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="63621-414">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="63621-415">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="63621-415">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="63621-416">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="63621-416">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="63621-417">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-418">**État**</span><span class="sxs-lookup"><span data-stu-id="63621-418">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-419">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-421">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="63621-421">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="63621-422">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63621-422">String that indicates the current status of the object.</span></span> <span data-ttu-id="63621-423">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="63621-423">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="63621-424">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="63621-424">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="63621-425">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="63621-425">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="63621-426">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="63621-426">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="63621-427">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="63621-427">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="63621-428">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="63621-428">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="63621-429">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63621-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="63621-430">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="63621-430">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="63621-431">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="63621-431">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="63621-432">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="63621-432">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="63621-433">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="63621-433">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63621-434">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63621-434">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="63621-435">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="63621-435">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="63621-436">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63621-436">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="63621-437">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="63621-437">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="63621-438">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="63621-438">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="63621-439">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="63621-439">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="63621-440">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="63621-440">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="63621-441">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="63621-441">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="63621-442">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="63621-442">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-443">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="63621-443">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-444">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63621-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63621-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-446">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="63621-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="63621-447">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="63621-447">State of the logical device.</span></span> <span data-ttu-id="63621-448">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="63621-448">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="63621-449">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63621-450">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="63621-450">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63621-451">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="63621-451">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="63621-452">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="63621-452">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="63621-453">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="63621-453">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="63621-454">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="63621-454">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63621-455">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63621-455">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-456">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-458">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63621-458">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63621-459">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="63621-459">The scoping system's creation class name.</span></span>

<span data-ttu-id="63621-460">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63621-461">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="63621-461">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63621-462">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63621-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63621-463">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63621-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63621-464">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63621-464">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63621-465">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="63621-465">The scoping system's name.</span></span>

<span data-ttu-id="63621-466">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-466">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63621-467">Notes</span><span class="sxs-lookup"><span data-stu-id="63621-467">Remarks</span></span>

<span data-ttu-id="63621-468">La classe **CIM \_ MediaAccessDevice** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="63621-468">The **CIM\_MediaAccessDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="63621-469">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="63621-469">WMI does not implement this class.</span></span> <span data-ttu-id="63621-470">Pour les classes dérivées de **CIM \_ MediaAccessDevice**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="63621-470">For classes derived from **CIM\_MediaAccessDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="63621-471">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="63621-471">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="63621-472">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="63621-472">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="63621-473">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63621-473">Requirements</span></span>



| <span data-ttu-id="63621-474">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63621-474">Requirement</span></span> | <span data-ttu-id="63621-475">Valeur</span><span class="sxs-lookup"><span data-stu-id="63621-475">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63621-476">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63621-476">Minimum supported client</span></span><br/> | <span data-ttu-id="63621-477">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63621-477">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63621-478">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63621-478">Minimum supported server</span></span><br/> | <span data-ttu-id="63621-479">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63621-479">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63621-480">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63621-480">Namespace</span></span><br/>                | <span data-ttu-id="63621-481">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="63621-481">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63621-482">MOF</span><span class="sxs-lookup"><span data-stu-id="63621-482">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63621-483"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63621-483"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63621-484">DLL</span><span class="sxs-lookup"><span data-stu-id="63621-484">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63621-485"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63621-485"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63621-486">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63621-486">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63621-487">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="63621-487">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

