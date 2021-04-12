---
description: La \_ classe CIM MagnetoOpticalDrive représente les fonctionnalités et la gestion d’un lecteur magnéto-optique, un sous-type de l’appareil d’accès aux médias.
ms.assetid: 82a4604d-3bef-4378-812b-550849e30b8c
ms.tgt_platform: multiple
title: Classe CIM_MagnetoOpticalDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive
- CIM_MagnetoOpticalDrive.Availability
- CIM_MagnetoOpticalDrive.Capabilities
- CIM_MagnetoOpticalDrive.CapabilityDescriptions
- CIM_MagnetoOpticalDrive.Caption
- CIM_MagnetoOpticalDrive.CompressionMethod
- CIM_MagnetoOpticalDrive.ConfigManagerErrorCode
- CIM_MagnetoOpticalDrive.ConfigManagerUserConfig
- CIM_MagnetoOpticalDrive.CreationClassName
- CIM_MagnetoOpticalDrive.DefaultBlockSize
- CIM_MagnetoOpticalDrive.Description
- CIM_MagnetoOpticalDrive.DeviceID
- CIM_MagnetoOpticalDrive.ErrorCleared
- CIM_MagnetoOpticalDrive.ErrorDescription
- CIM_MagnetoOpticalDrive.ErrorMethodology
- CIM_MagnetoOpticalDrive.InstallDate
- CIM_MagnetoOpticalDrive.LastErrorCode
- CIM_MagnetoOpticalDrive.MaxBlockSize
- CIM_MagnetoOpticalDrive.MaxMediaSize
- CIM_MagnetoOpticalDrive.MinBlockSize
- CIM_MagnetoOpticalDrive.Name
- CIM_MagnetoOpticalDrive.NeedsCleaning
- CIM_MagnetoOpticalDrive.NumberOfMediaSupported
- CIM_MagnetoOpticalDrive.PNPDeviceID
- CIM_MagnetoOpticalDrive.PowerManagementCapabilities
- CIM_MagnetoOpticalDrive.PowerManagementSupported
- CIM_MagnetoOpticalDrive.Status
- CIM_MagnetoOpticalDrive.StatusInfo
- CIM_MagnetoOpticalDrive.SystemCreationClassName
- CIM_MagnetoOpticalDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: abc5acdf25a2920fa53c6315109264180b6e7c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483368"
---
# <a name="cim_magnetoopticaldrive-class"></a><span data-ttu-id="2e826-103">\_Classe CIM MagnetoOpticalDrive</span><span class="sxs-lookup"><span data-stu-id="2e826-103">CIM\_MagnetoOpticalDrive class</span></span>

<span data-ttu-id="2e826-104">La classe **CIM \_ MagnetoOpticalDrive** représente les fonctionnalités et la gestion d’un lecteur magnéto-optique, un sous-type de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="2e826-104">The **CIM\_MagnetoOpticalDrive** class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e826-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2e826-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e826-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e826-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e826-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2e826-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2e826-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2e826-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e826-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e826-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{F62037D8-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_MagnetoOpticalDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="2e826-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2e826-110">Members</span></span>

<span data-ttu-id="2e826-111">La classe **CIM \_ MagnetoOpticalDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e826-111">The **CIM\_MagnetoOpticalDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="2e826-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e826-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e826-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e826-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e826-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e826-114">Methods</span></span>

<span data-ttu-id="2e826-115">La classe **CIM \_ MagnetoOpticalDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2e826-115">The **CIM\_MagnetoOpticalDrive** class has these methods.</span></span>



| <span data-ttu-id="2e826-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2e826-116">Method</span></span>                                                                         | <span data-ttu-id="2e826-117">Description</span><span class="sxs-lookup"><span data-stu-id="2e826-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e826-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="2e826-118">**Reset**</span></span>](reset-method-in-class-cim-magnetoopticaldrive.md)                 | <span data-ttu-id="2e826-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="2e826-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2e826-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2e826-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2e826-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-magnetoopticaldrive.md) | <span data-ttu-id="2e826-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="2e826-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2e826-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2e826-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e826-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e826-124">Properties</span></span>

<span data-ttu-id="2e826-125">La classe **CIM \_ MagnetoOpticalDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e826-125">The **CIM\_MagnetoOpticalDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e826-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="2e826-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e826-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2e826-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-130">Availability and status of the device.</span></span>

<span data-ttu-id="2e826-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e826-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2e826-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e826-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2e826-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2e826-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="2e826-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2e826-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="2e826-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2e826-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="2e826-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2e826-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2e826-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2e826-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="2e826-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2e826-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="2e826-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2e826-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="2e826-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2e826-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="2e826-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2e826-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="2e826-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2e826-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="2e826-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2e826-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="2e826-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2e826-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2e826-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="2e826-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="2e826-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2e826-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="2e826-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-149">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="2e826-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2e826-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="2e826-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2e826-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="2e826-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="2e826-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2e826-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="2e826-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="2e826-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2e826-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="2e826-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="2e826-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2e826-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="2e826-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="2e826-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2e826-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="2e826-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="2e826-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2e826-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-162">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e826-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e826-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-164">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="2e826-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-165">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="2e826-165">Capabilities of the media access device.</span></span>

<span data-ttu-id="2e826-166">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-166">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e826-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2e826-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-168">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="2e826-168">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e826-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2e826-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-170">Autre.</span><span class="sxs-lookup"><span data-stu-id="2e826-170">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="2e826-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="2e826-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-172">Accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="2e826-172">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="2e826-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="2e826-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-174">Accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="2e826-174">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="2e826-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="2e826-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-176">Écriture.</span><span class="sxs-lookup"><span data-stu-id="2e826-176">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="2e826-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="2e826-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-178">Chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2e826-178">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="2e826-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="2e826-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-180">Compression.</span><span class="sxs-lookup"><span data-stu-id="2e826-180">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="2e826-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="2e826-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-182">Support amovible.</span><span class="sxs-lookup"><span data-stu-id="2e826-182">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="2e826-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="2e826-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-184">Nettoyage manuel.</span><span class="sxs-lookup"><span data-stu-id="2e826-184">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="2e826-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="2e826-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-186">Nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="2e826-186">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="2e826-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="2e826-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-188">Notification intelligente.</span><span class="sxs-lookup"><span data-stu-id="2e826-188">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="2e826-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="2e826-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-190">Distingue un appareil qui peut accéder aux deux côtés d’un média à deux faces à partir d’un appareil qui ne lit qu’un seul côté et requiert le basculement du média.</span><span class="sxs-lookup"><span data-stu-id="2e826-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="2e826-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="2e826-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-192">Indique qu’il n’est pas nécessaire d’éjecter explicitement le média de l’appareil avant d’y accéder par un élément sélecteur.</span><span class="sxs-lookup"><span data-stu-id="2e826-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-193">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2e826-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-194">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2e826-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e826-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-196">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="2e826-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-197">Tableau de chaînes de forme libre qui fournit des explications détaillées pour l’accès aux fonctionnalités d’appareil indiquées dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="2e826-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="2e826-198">Chaque entrée de tableau est liée à l’entrée dans le tableau de **fonctionnalités** , située au même index.</span><span class="sxs-lookup"><span data-stu-id="2e826-198">Each array entry is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="2e826-199">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-199">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-200">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2e826-200">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-203">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2e826-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-204">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e826-204">Short textual description of the object.</span></span>

<span data-ttu-id="2e826-205">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-206">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="2e826-206">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-209">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-209">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="2e826-210">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="2e826-210">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="2e826-211">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="2e826-211">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="2e826-212">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="2e826-212">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="2e826-213">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-213">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="2e826-214">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="2e826-214">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="2e826-215">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="2e826-215">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="2e826-216">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="2e826-216">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="2e826-217">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="2e826-217">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="2e826-218">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="2e826-218">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="2e826-219">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="2e826-219">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e826-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-221">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e826-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-223">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2e826-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-224">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2e826-224">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="2e826-225">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2e826-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="2e826-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2e826-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="2e826-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-228">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="2e826-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2e826-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="2e826-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2e826-230">(1)</span><span class="sxs-lookup"><span data-stu-id="2e826-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-231">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="2e826-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e826-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2e826-233">(2)</span><span class="sxs-lookup"><span data-stu-id="2e826-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2e826-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="2e826-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2e826-235">(3)</span><span class="sxs-lookup"><span data-stu-id="2e826-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-236">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="2e826-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2e826-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="2e826-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2e826-238">(4)</span><span class="sxs-lookup"><span data-stu-id="2e826-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-239">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="2e826-239">Device is not working properly.</span></span> <span data-ttu-id="2e826-240">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="2e826-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2e826-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="2e826-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2e826-242">(5)</span><span class="sxs-lookup"><span data-stu-id="2e826-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-243">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="2e826-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2e826-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="2e826-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2e826-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="2e826-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-246">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="2e826-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2e826-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="2e826-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2e826-248">(7)</span><span class="sxs-lookup"><span data-stu-id="2e826-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2e826-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="2e826-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2e826-250">(8)</span><span class="sxs-lookup"><span data-stu-id="2e826-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-251">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="2e826-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2e826-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2e826-253">(9)</span><span class="sxs-lookup"><span data-stu-id="2e826-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-254">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-254">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2e826-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2e826-256">(10)</span><span class="sxs-lookup"><span data-stu-id="2e826-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-257">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2e826-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2e826-259">(11)</span><span class="sxs-lookup"><span data-stu-id="2e826-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-260">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2e826-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="2e826-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2e826-262">douze</span><span class="sxs-lookup"><span data-stu-id="2e826-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-263">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2e826-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2e826-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2e826-265">(13)</span><span class="sxs-lookup"><span data-stu-id="2e826-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-266">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2e826-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="2e826-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2e826-268">(14)</span><span class="sxs-lookup"><span data-stu-id="2e826-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-269">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="2e826-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2e826-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="2e826-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2e826-271">(15)</span><span class="sxs-lookup"><span data-stu-id="2e826-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-272">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="2e826-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2e826-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2e826-274">(16)</span><span class="sxs-lookup"><span data-stu-id="2e826-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-275">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2e826-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="2e826-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2e826-277">(17)</span><span class="sxs-lookup"><span data-stu-id="2e826-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-278">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="2e826-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e826-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2e826-280">(18)</span><span class="sxs-lookup"><span data-stu-id="2e826-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-281">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="2e826-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2e826-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="2e826-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2e826-283">(19)</span><span class="sxs-lookup"><span data-stu-id="2e826-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2e826-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="2e826-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2e826-285">(20)</span><span class="sxs-lookup"><span data-stu-id="2e826-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-286">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="2e826-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2e826-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2e826-288">(21)</span><span class="sxs-lookup"><span data-stu-id="2e826-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-289">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="2e826-289">System failure.</span></span> <span data-ttu-id="2e826-290">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="2e826-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2e826-291">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2e826-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="2e826-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2e826-293">(22)</span><span class="sxs-lookup"><span data-stu-id="2e826-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-294">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2e826-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2e826-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="2e826-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2e826-296">(23)</span><span class="sxs-lookup"><span data-stu-id="2e826-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-297">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="2e826-297">System failure.</span></span> <span data-ttu-id="2e826-298">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="2e826-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2e826-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="2e826-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2e826-300">(24)</span><span class="sxs-lookup"><span data-stu-id="2e826-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-301">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="2e826-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2e826-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2e826-303">(25)</span><span class="sxs-lookup"><span data-stu-id="2e826-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-304">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2e826-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2e826-306">(26)</span><span class="sxs-lookup"><span data-stu-id="2e826-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-307">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2e826-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="2e826-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2e826-309">(27)</span><span class="sxs-lookup"><span data-stu-id="2e826-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-310">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="2e826-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2e826-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="2e826-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2e826-312">(28)</span><span class="sxs-lookup"><span data-stu-id="2e826-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-313">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="2e826-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2e826-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="2e826-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2e826-315">(29)</span><span class="sxs-lookup"><span data-stu-id="2e826-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-316">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="2e826-316">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2e826-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="2e826-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2e826-318">(30)</span><span class="sxs-lookup"><span data-stu-id="2e826-318">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-319">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="2e826-319">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e826-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2e826-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2e826-321">31</span><span class="sxs-lookup"><span data-stu-id="2e826-321">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-322">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="2e826-322">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-323">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2e826-323">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-324">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e826-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-326">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2e826-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-327">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e826-327">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2e826-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-329">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e826-329">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-332">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e826-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e826-333">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="2e826-333">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2e826-334">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="2e826-334">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2e826-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-336">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e826-336">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-337">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e826-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-339">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2e826-339">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-340">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-340">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="2e826-341">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-341">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e826-342">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2e826-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-343">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e826-343">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-346">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2e826-346">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-347">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e826-347">Textual description of the object.</span></span>

<span data-ttu-id="2e826-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2e826-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-352">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e826-352">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e826-353">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-353">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2e826-354">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-355">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2e826-355">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-356">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e826-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-358">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e826-358">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2e826-359">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-360">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2e826-360">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-363">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2e826-363">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2e826-364">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-365">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2e826-365">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-366">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-368">Chaîne de forme libre qui décrit les types de détection d’erreurs et de correction pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-368">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="2e826-369">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-369">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2e826-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-371">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e826-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-373">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2e826-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-374">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e826-374">Date and time the object was installed.</span></span> <span data-ttu-id="2e826-375">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="2e826-375">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2e826-376">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e826-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-378">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e826-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-380">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2e826-381">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-382">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e826-382">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-383">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e826-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-385">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2e826-385">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-386">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-386">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="2e826-387">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-387">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e826-388">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2e826-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-389">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="2e826-389">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-390">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e826-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-392">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="2e826-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-393">Taille maximale, en kilo-octets, des médias pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-393">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="2e826-394">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="2e826-394">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="2e826-395">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-395">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e826-396">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2e826-396">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-397">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e826-397">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-398">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e826-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-400">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2e826-400">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-401">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-401">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="2e826-402">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-402">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e826-403">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2e826-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-404">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2e826-404">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-407">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2e826-407">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-408">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2e826-408">Label by which the object is known.</span></span> <span data-ttu-id="2e826-409">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2e826-409">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2e826-410">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-410">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-411">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="2e826-411">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-412">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e826-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-414">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="2e826-414">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="2e826-415">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété du tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="2e826-415">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="2e826-416">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-416">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-417">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="2e826-417">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-418">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e826-418">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-420">Si l’appareil d’accès aux médias prend en charge plusieurs médias individuels, cette propriété définit le nombre maximal qui peut être pris en charge ou inséré.</span><span class="sxs-lookup"><span data-stu-id="2e826-420">If the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="2e826-421">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-421">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-422">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2e826-422">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-423">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-425">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2e826-425">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-426">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-426">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2e826-427">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2e826-428">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="2e826-428">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2e826-429">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2e826-429">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-430">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e826-430">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e826-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-432">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-432">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2e826-433">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="2e826-433">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e826-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2e826-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2e826-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="2e826-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-436">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2e826-436">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2e826-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="2e826-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2e826-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="2e826-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-439">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2e826-439">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2e826-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="2e826-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-441">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="2e826-441">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2e826-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="2e826-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-443">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2e826-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2e826-444">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="2e826-444">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2e826-445">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2e826-445">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2e826-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="2e826-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-447">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="2e826-447">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2e826-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="2e826-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e826-449">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="2e826-449">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-450">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2e826-450">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-451">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2e826-451">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e826-453">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="2e826-453">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2e826-454">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2e826-454">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2e826-455">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2e826-455">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2e826-456">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2e826-456">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2e826-457">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-458">**État**</span><span class="sxs-lookup"><span data-stu-id="2e826-458">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-459">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-461">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2e826-461">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-462">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e826-462">Current status of the object.</span></span>

<span data-ttu-id="2e826-463">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-463">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2e826-464">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2e826-464">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2e826-465">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2e826-465">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2e826-466">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2e826-466">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2e826-467">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2e826-467">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e826-468">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2e826-468">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2e826-469">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2e826-469">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2e826-470">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2e826-470">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2e826-471">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2e826-471">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2e826-472">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2e826-472">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2e826-473">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2e826-473">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2e826-474">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2e826-474">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2e826-475">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2e826-475">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2e826-476">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2e826-476">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2e826-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-478">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e826-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-480">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2e826-480">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2e826-481">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2e826-481">State of the logical device.</span></span> <span data-ttu-id="2e826-482">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="2e826-482">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2e826-483">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e826-484">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2e826-484">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e826-485">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2e826-485">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2e826-486">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="2e826-486">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2e826-487">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="2e826-487">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2e826-488">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2e826-488">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e826-489">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e826-489">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-490">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-491">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-492">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e826-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e826-493">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2e826-493">Scoping system's creation class name.</span></span>

<span data-ttu-id="2e826-494">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e826-495">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2e826-495">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e826-496">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e826-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e826-497">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e826-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e826-498">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e826-498">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e826-499">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2e826-499">Scoping system's name.</span></span>

<span data-ttu-id="2e826-500">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-500">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e826-501">Notes</span><span class="sxs-lookup"><span data-stu-id="2e826-501">Remarks</span></span>

<span data-ttu-id="2e826-502">La classe **CIM \_ MagnetoOpticalDrive** est dérivée de [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e826-502">The **CIM\_MagnetoOpticalDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="2e826-503">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2e826-503">WMI does not implement this class.</span></span>

<span data-ttu-id="2e826-504">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e826-504">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e826-505">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2e826-505">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e826-506">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e826-506">Requirements</span></span>



| <span data-ttu-id="2e826-507">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e826-507">Requirement</span></span> | <span data-ttu-id="2e826-508">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e826-508">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e826-509">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e826-509">Minimum supported client</span></span><br/> | <span data-ttu-id="2e826-510">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e826-510">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e826-511">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e826-511">Minimum supported server</span></span><br/> | <span data-ttu-id="2e826-512">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e826-512">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e826-513">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e826-513">Namespace</span></span><br/>                | <span data-ttu-id="2e826-514">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2e826-514">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e826-515">MOF</span><span class="sxs-lookup"><span data-stu-id="2e826-515">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e826-516"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e826-516"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e826-517">DLL</span><span class="sxs-lookup"><span data-stu-id="2e826-517">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e826-518"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e826-518"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e826-519">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e826-519">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e826-520">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2e826-520">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

