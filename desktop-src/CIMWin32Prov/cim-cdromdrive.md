---
description: La \_ classe CIM CDROMDrive représente un lecteur de CD-ROM sur l’ordinateur.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: CIM_CDROMDrive, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861353"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="bbe7f-103">CIM_CDROMDrive, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="bbe7f-104">La classe **CIM \_ CDROMDrive** représente un lecteur de CD-ROM sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="bbe7f-105">Le nom du lecteur ne correspond pas à la lettre de lecteur logique attribuée à l’appareil, qui est le nom du périphérique de stockage logique qui est dépendant du lecteur.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="bbe7f-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bbe7f-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bbe7f-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bbe7f-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe7f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbe7f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="bbe7f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bbe7f-111">Members</span></span>

<span data-ttu-id="bbe7f-112">La classe **CIM \_ CDROMDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bbe7f-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="bbe7f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bbe7f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="bbe7f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bbe7f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bbe7f-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bbe7f-115">Methods</span></span>

<span data-ttu-id="bbe7f-116">La classe **CIM \_ CDROMDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="bbe7f-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="bbe7f-117">Method</span></span>                                                                | <span data-ttu-id="bbe7f-118">Description</span><span class="sxs-lookup"><span data-stu-id="bbe7f-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbe7f-119">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="bbe7f-120">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="bbe7f-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="bbe7f-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="bbe7f-123">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="bbe7f-124">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bbe7f-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bbe7f-125">Properties</span></span>

<span data-ttu-id="bbe7f-126">La classe **CIM \_ CDROMDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbe7f-127">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-131">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-131">Availability and status of the device.</span></span>

<span data-ttu-id="bbe7f-132">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bbe7f-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbe7f-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bbe7f-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bbe7f-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bbe7f-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bbe7f-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bbe7f-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bbe7f-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bbe7f-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bbe7f-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bbe7f-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bbe7f-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bbe7f-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-146">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bbe7f-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-148">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bbe7f-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-150">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bbe7f-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bbe7f-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-153">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bbe7f-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-155">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bbe7f-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-157">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bbe7f-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-159">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bbe7f-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-161">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-163">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-165">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-166">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="bbe7f-167">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbe7f-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-169">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bbe7f-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-171">Autre.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="bbe7f-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-173">Accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="bbe7f-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-175">Accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="bbe7f-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-177">Écriture.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="bbe7f-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-179">Chiffrement.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="bbe7f-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-181">Compression.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="bbe7f-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-183">Support amovible.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="bbe7f-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-185">Nettoyage manuel.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="bbe7f-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-187">Nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="bbe7f-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-189">Notification intelligente.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="bbe7f-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-191">Distingue un appareil qui peut accéder aux deux côtés d’un média à deux faces à partir d’un appareil qui ne lit qu’un seul côté et requiert le basculement du média.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="bbe7f-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-193">Indique qu’il n’est pas nécessaire d’éjecter explicitement le média de l’appareil avant d’y accéder par un élément sélecteur.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-194">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-195">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-197">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-198">Tableau de chaînes de forme libre qui fournit des explications détaillées pour l’accès aux fonctionnalités d’appareil indiquées dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="bbe7f-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="bbe7f-199">Chaque entrée de ce tableau est liée à l’entrée dans le tableau des **fonctionnalités** , située dans le même index.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="bbe7f-200">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-201">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-204">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-205">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-205">A short textual description of the object.</span></span>

<span data-ttu-id="bbe7f-206">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-210">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="bbe7f-211">S’il n’est pas possible de décrire le schéma de compression (car il est inconnu), utilisez ce qui suit : if, use « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="bbe7f-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="bbe7f-212">Si, utilisez « Compressed ».</span><span class="sxs-lookup"><span data-stu-id="bbe7f-212">If , use "Compressed".</span></span> <span data-ttu-id="bbe7f-213">, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="bbe7f-213">, use "Not Compressed".</span></span>

<span data-ttu-id="bbe7f-214">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="bbe7f-215">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-216">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="bbe7f-217">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-218">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="bbe7f-219">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-220">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="bbe7f-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-221">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-222">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-224">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-225">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="bbe7f-226">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bbe7f-227">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-227">**This device is working properly.**</span></span> <span data-ttu-id="bbe7f-228"> (0)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bbe7f-229">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="bbe7f-230">(1)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bbe7f-231">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bbe7f-232">(2)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bbe7f-233">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bbe7f-234">(3)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bbe7f-235">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bbe7f-236">(4)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bbe7f-237">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bbe7f-238">(5)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bbe7f-239">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bbe7f-240"> (6)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bbe7f-241">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-241">**Cannot filter.**</span></span> <span data-ttu-id="bbe7f-242">(7)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bbe7f-243">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bbe7f-244">(8)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bbe7f-245">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bbe7f-246">(9)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bbe7f-247">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-247">**This device cannot start.**</span></span> <span data-ttu-id="bbe7f-248">(10)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bbe7f-249">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-249">**This device failed.**</span></span> <span data-ttu-id="bbe7f-250">(11)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bbe7f-251">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bbe7f-252">douze</span><span class="sxs-lookup"><span data-stu-id="bbe7f-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bbe7f-253">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bbe7f-254">(13)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bbe7f-255">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bbe7f-256">(14)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bbe7f-257">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bbe7f-258">(15)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bbe7f-259">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bbe7f-260">(16)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bbe7f-261">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bbe7f-262">(17)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bbe7f-263">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bbe7f-264">(18)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bbe7f-265">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="bbe7f-266">(19)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bbe7f-267">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="bbe7f-268">(20)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bbe7f-269">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bbe7f-270">(21)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bbe7f-271">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-271">**This device is disabled.**</span></span> <span data-ttu-id="bbe7f-272">(22)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bbe7f-273">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bbe7f-274">(23)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bbe7f-275">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bbe7f-276">(24)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bbe7f-277">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="bbe7f-278">(25)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bbe7f-279">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="bbe7f-280">(26)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bbe7f-281">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bbe7f-282">(27)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bbe7f-283">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bbe7f-284">(28)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bbe7f-285">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bbe7f-286">(29)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bbe7f-287">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bbe7f-288">(30)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bbe7f-289">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bbe7f-290">31</span><span class="sxs-lookup"><span data-stu-id="bbe7f-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-292">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-294">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-295">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bbe7f-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-300">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-301">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bbe7f-302">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bbe7f-303">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-304">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-305">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-307">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-308">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="bbe7f-309">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="bbe7f-310">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-311">**Description**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-314">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-315">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-315">A textual description of the object.</span></span>

<span data-ttu-id="bbe7f-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-320">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-321">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="bbe7f-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-324">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-326">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="bbe7f-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-331">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="bbe7f-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-333">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-336">Chaîne de forme libre qui décrit les types de détection d’erreurs et de correction pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="bbe7f-337">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-339">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-341">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-342">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-342">Indicates when the object was installed.</span></span> <span data-ttu-id="bbe7f-343">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bbe7f-344">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-346">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-348">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bbe7f-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-350">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-351">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-353">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-354">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="bbe7f-355">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="bbe7f-356">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-357">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-358">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-360">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-361">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="bbe7f-362">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="bbe7f-363">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="bbe7f-364">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-365">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-366">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-368">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-369">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="bbe7f-370">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="bbe7f-371">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-372">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-375">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-376">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-376">Label by which the object is known.</span></span> <span data-ttu-id="bbe7f-377">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="bbe7f-378">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-379">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-380">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-382">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="bbe7f-383">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété du tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="bbe7f-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="bbe7f-384">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-385">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-386">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-388">Nombre maximal de plusieurs supports individuels qui peuvent être pris en charge ou insérés.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="bbe7f-389">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-393">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-394">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="bbe7f-395">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="bbe7f-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="bbe7f-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-397">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-398">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-400">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="bbe7f-401">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbe7f-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-403">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bbe7f-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-405">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bbe7f-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-407">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bbe7f-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-409">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bbe7f-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-411">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bbe7f-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-413">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="bbe7f-414">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="bbe7f-415">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bbe7f-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-417">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bbe7f-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bbe7f-419">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-420">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-421">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-423">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="bbe7f-424">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="bbe7f-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="bbe7f-425">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="bbe7f-426">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="bbe7f-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="bbe7f-427">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-428">**État**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-429">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-431">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-432">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="bbe7f-433">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="bbe7f-434">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="bbe7f-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="bbe7f-435">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="bbe7f-436">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="bbe7f-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bbe7f-437">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bbe7f-438">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bbe7f-439">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bbe7f-440">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbe7f-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bbe7f-441">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bbe7f-442">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bbe7f-443">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbe7f-444">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bbe7f-445">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bbe7f-446">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bbe7f-447">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bbe7f-448">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bbe7f-449">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bbe7f-450">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bbe7f-451">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bbe7f-452">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-456">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bbe7f-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-457">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-457">State of the logical device.</span></span> <span data-ttu-id="bbe7f-458">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="bbe7f-459">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bbe7f-460">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbe7f-461">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bbe7f-462">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bbe7f-463">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bbe7f-464">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbe7f-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-468">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-469">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="bbe7f-470">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbe7f-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe7f-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-473">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbe7f-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe7f-474">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bbe7f-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bbe7f-475">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-475">The scoping system's name.</span></span>

<span data-ttu-id="bbe7f-476">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbe7f-477">Notes</span><span class="sxs-lookup"><span data-stu-id="bbe7f-477">Remarks</span></span>

<span data-ttu-id="bbe7f-478">La classe **CIM \_ CDROMDrive** est dérivée de [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bbe7f-479">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-479">WMI does not implement this class.</span></span> <span data-ttu-id="bbe7f-480">Pour plus d’informations sur les classes dérivées de **CIM \_ CDROMDrive**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bbe7f-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bbe7f-481">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bbe7f-482">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="bbe7f-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe7f-483">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbe7f-483">Requirements</span></span>



| <span data-ttu-id="bbe7f-484">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbe7f-484">Requirement</span></span> | <span data-ttu-id="bbe7f-485">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbe7f-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe7f-486">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbe7f-486">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe7f-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbe7f-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbe7f-488">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbe7f-488">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe7f-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbe7f-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbe7f-490">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bbe7f-490">Namespace</span></span><br/>                | <span data-ttu-id="bbe7f-491">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bbe7f-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bbe7f-492">MOF</span><span class="sxs-lookup"><span data-stu-id="bbe7f-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbe7f-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbe7f-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbe7f-494">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe7f-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe7f-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe7f-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe7f-496">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbe7f-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe7f-497">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="bbe7f-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

