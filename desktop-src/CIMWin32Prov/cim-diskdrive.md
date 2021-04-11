---
description: La \_ classe CIM DiskDrive représente un lecteur de disque physique tel qu’il est vu par le système d’exploitation.
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: CIM_DiskDrive, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201066"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="6f1c6-103">CIM_DiskDrive, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6f1c6-104">La classe **CIM \_ DiskDrive** représente un lecteur de disque physique tel qu’il est vu par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="6f1c6-105">Les fonctionnalités du lecteur de disque correspondent aux caractéristiques logiques et de gestion du lecteur, et dans certains cas, peuvent ne pas refléter les caractéristiques physiques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="6f1c6-106">Une interface vers un lecteur physique est un membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="6f1c6-107">Toutefois, un objet basé sur un autre périphérique logique n’est pas un membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f1c6-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f1c6-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6f1c6-110">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6f1c6-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1c6-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f1c6-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="6f1c6-113">Membres</span><span class="sxs-lookup"><span data-stu-id="6f1c6-113">Members</span></span>

<span data-ttu-id="6f1c6-114">La classe **CIM \_ DiskDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f1c6-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="6f1c6-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f1c6-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f1c6-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f1c6-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f1c6-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f1c6-117">Methods</span></span>

<span data-ttu-id="6f1c6-118">La classe **CIM \_ DiskDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="6f1c6-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f1c6-119">Method</span></span>                                                                | <span data-ttu-id="6f1c6-120">Description</span><span class="sxs-lookup"><span data-stu-id="6f1c6-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f1c6-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="6f1c6-122">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="6f1c6-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6f1c6-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="6f1c6-125">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6f1c6-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6f1c6-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f1c6-127">Properties</span></span>

<span data-ttu-id="6f1c6-128">La classe **CIM \_ DiskDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f1c6-129">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-133">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-133">Availability and status of the device.</span></span>

<span data-ttu-id="6f1c6-134">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f1c6-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-136">Autre.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f1c6-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-138">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6f1c6-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-140">En cours d’exécution/pleine puissance.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6f1c6-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-142">Avertissement.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6f1c6-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-144">Tests.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6f1c6-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-146">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6f1c6-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-148">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6f1c6-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-150">Déconnecté.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6f1c6-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-152">Hors service.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f1c6-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-154">Détérioré.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6f1c6-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-156">Non installé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6f1c6-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-158">Erreur d’installation.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6f1c6-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-160">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact dans ce mode est inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6f1c6-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-162">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6f1c6-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-164">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance « rapidement ».</span><span class="sxs-lookup"><span data-stu-id="6f1c6-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6f1c6-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-166">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6f1c6-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-168">L’appareil est dans un état d’avertissement et également dans un mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6f1c6-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-170">Suspendu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6f1c6-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-172">Non prêt.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6f1c6-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-174">Non configuré.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6f1c6-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-176">Le lecteur de disque n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-177">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-178">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-180">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-181">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-181">Capabilities of the media access device.</span></span> <span data-ttu-id="6f1c6-182">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f1c6-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-184">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f1c6-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-186">Autre.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="6f1c6-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-188">Accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="6f1c6-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-190">Accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="6f1c6-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-192">Écriture.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="6f1c6-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-194">Chiffrement.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="6f1c6-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-196">Compression.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="6f1c6-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-198">Support amovible.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="6f1c6-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-200">Nettoyage manuel.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="6f1c6-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-202">Nettoyage automatique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="6f1c6-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-204">Notification intelligente.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="6f1c6-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-206">Distingue un appareil qui peut accéder aux deux côtés d’un média à deux faces à partir d’un appareil qui ne lit qu’un seul côté et requiert le basculement du média.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="6f1c6-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-208">Indique qu’il n’est pas nécessaire d’éjecter explicitement le média de l’appareil avant d’y accéder par un élément sélecteur.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-209">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-210">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-212">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-213">Tableau de chaînes de forme libre qui fournissent des explications détaillées pour l’accès aux fonctionnalités d’appareil indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="6f1c6-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="6f1c6-214">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="6f1c6-215">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f1c6-216">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-219">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-220">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-220">Short textual description of the object.</span></span>

<span data-ttu-id="6f1c6-221">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-222">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-225">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6f1c6-226">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="6f1c6-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6f1c6-227">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="6f1c6-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6f1c6-228">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="6f1c6-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="6f1c6-229">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="6f1c6-230">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-231">Le schéma de compression est inconnu ou non décrit.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="6f1c6-232">(« Compressé »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-233">Le fichier logique est compressé, mais le schéma de compression est inconnu ou n’est pas décrit.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="6f1c6-234">(« Non compressé »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-235">Si le fichier logique n’est pas compressé</span><span class="sxs-lookup"><span data-stu-id="6f1c6-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-236">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-237">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-239">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-240">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="6f1c6-241">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6f1c6-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6f1c6-243"> (0)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-244">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6f1c6-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6f1c6-246">(1)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-247">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f1c6-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6f1c6-249">(2)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6f1c6-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6f1c6-251">(3)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-252">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6f1c6-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6f1c6-254">(4)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-255">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-255">Device is not working properly.</span></span> <span data-ttu-id="6f1c6-256">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6f1c6-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6f1c6-258">(5)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-259">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6f1c6-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6f1c6-261"> (6)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-262">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6f1c6-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6f1c6-264">(7)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6f1c6-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6f1c6-266">(8)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-267">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6f1c6-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6f1c6-269">(9)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-270">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6f1c6-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6f1c6-272">(10)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-273">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6f1c6-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6f1c6-275">(11)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-276">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6f1c6-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6f1c6-278">douze</span><span class="sxs-lookup"><span data-stu-id="6f1c6-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-279">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6f1c6-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6f1c6-281">(13)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-282">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6f1c6-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6f1c6-284">(14)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-285">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6f1c6-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6f1c6-287">(15)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-288">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6f1c6-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6f1c6-290">(16)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-291">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6f1c6-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6f1c6-293">(17)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-294">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f1c6-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6f1c6-296">(18)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-297">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6f1c6-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6f1c6-299">(19)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6f1c6-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6f1c6-301">(20)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-302">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6f1c6-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6f1c6-304">(21)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-305">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-305">System failure.</span></span> <span data-ttu-id="6f1c6-306">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6f1c6-307">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6f1c6-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6f1c6-309">(22)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-310">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6f1c6-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6f1c6-312">(23)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-313">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-313">System failure.</span></span> <span data-ttu-id="6f1c6-314">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6f1c6-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6f1c6-316">(24)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-317">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6f1c6-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6f1c6-319">(25)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-320">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6f1c6-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6f1c6-322">(26)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-323">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6f1c6-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6f1c6-325">(27)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-326">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6f1c6-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6f1c6-328">(28)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-329">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6f1c6-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6f1c6-331">(29)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-332">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6f1c6-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6f1c6-334">(30)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-335">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f1c6-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6f1c6-337">31</span><span class="sxs-lookup"><span data-stu-id="6f1c6-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-338">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-339">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-340">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-342">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-343">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6f1c6-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-345">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-348">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-349">Nom de la classe (ou sous-classe) utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="6f1c6-350">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6f1c6-351">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-352">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-353">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-355">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-356">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="6f1c6-357">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="6f1c6-358">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-359">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-362">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-363">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-363">Textual description of the object.</span></span>

<span data-ttu-id="6f1c6-364">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-365">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-366">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-368">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-369">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6f1c6-370">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-371">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-372">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-374">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est effacée.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="6f1c6-375">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-377">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-379">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6f1c6-380">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-381">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-384">Chaîne de forme libre qui décrit le type de détection d’erreurs et de correction pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="6f1c6-385">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-387">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-389">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-390">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-390">Date and time when the object was installed.</span></span> <span data-ttu-id="6f1c6-391">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6f1c6-392">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-394">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-396">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6f1c6-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-398">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-399">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-401">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-402">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="6f1c6-403">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="6f1c6-404">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-405">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-406">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-408">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Appareils d’accès séquentiel DMTF \| 001,2 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-409">Taille maximale, en kilo-octets, des médias pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="6f1c6-410">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="6f1c6-411">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="6f1c6-412">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-413">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-414">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-416">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-417">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="6f1c6-418">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="6f1c6-419">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-420">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-423">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-424">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-424">Label by which the object is known.</span></span> <span data-ttu-id="6f1c6-425">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6f1c6-426">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-427">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-428">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-430">Si la **valeur est true**, l’appareil d’accès aux médias doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="6f1c6-431">La possibilité de procéder à un nettoyage manuel ou automatique est indiquée dans la propriété du tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="6f1c6-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="6f1c6-432">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-433">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-434">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-436">Lorsque l’appareil d’accès aux médias prend en charge plusieurs médias individuels, cette propriété définit le nombre maximal qui peut être pris en charge ou inséré.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="6f1c6-437">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-441">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-442">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6f1c6-443">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6f1c6-444">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="6f1c6-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-445">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-446">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-448">Fonctionnalités liées à l’alimentation spécifiques de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="6f1c6-449">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f1c6-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-451">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6f1c6-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-453">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f1c6-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-455">Désactivé.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f1c6-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-457">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6f1c6-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-459">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6f1c6-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-461">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6f1c6-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-463">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6f1c6-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6f1c6-465">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-466">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-467">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-469">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6f1c6-470">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6f1c6-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6f1c6-471">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6f1c6-472">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6f1c6-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6f1c6-473">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-474">**État**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-477">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-478">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-478">Current status of the object.</span></span>

<span data-ttu-id="6f1c6-479">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6f1c6-480">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f1c6-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6f1c6-481">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6f1c6-482">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f1c6-483">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f1c6-484">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6f1c6-485">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6f1c6-486">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6f1c6-487">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6f1c6-488">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6f1c6-489">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6f1c6-490">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6f1c6-491">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6f1c6-492">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-494">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-496">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6f1c6-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-497">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-497">State of the logical device.</span></span> <span data-ttu-id="6f1c6-498">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6f1c6-499">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f1c6-500">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f1c6-501">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f1c6-502">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f1c6-503">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6f1c6-504">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f1c6-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-506">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-508">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-509">Propriété **CreationClassName** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="6f1c6-510">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f1c6-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f1c6-512">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f1c6-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f1c6-514">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f1c6-515">Propriété de **nom** du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="6f1c6-516">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f1c6-517">Notes</span><span class="sxs-lookup"><span data-stu-id="6f1c6-517">Remarks</span></span>

<span data-ttu-id="6f1c6-518">La classe **CIM \_ DiskDrive** est dérivée de [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c6-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="6f1c6-519">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-519">WMI does not implement this class.</span></span> <span data-ttu-id="6f1c6-520">Consultez [classes Win32](win32-provider.md) pour les classes dérivées de **CIM \_ DiskDrive**.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="6f1c6-521">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f1c6-522">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1c6-523">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f1c6-523">Requirements</span></span>



| <span data-ttu-id="6f1c6-524">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f1c6-524">Requirement</span></span> | <span data-ttu-id="6f1c6-525">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f1c6-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1c6-526">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f1c6-526">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1c6-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f1c6-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f1c6-528">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f1c6-528">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1c6-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f1c6-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f1c6-530">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f1c6-530">Namespace</span></span><br/>                | <span data-ttu-id="6f1c6-531">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6f1c6-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f1c6-532">MOF</span><span class="sxs-lookup"><span data-stu-id="6f1c6-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f1c6-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f1c6-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f1c6-534">DLL</span><span class="sxs-lookup"><span data-stu-id="6f1c6-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f1c6-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f1c6-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f1c6-536">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f1c6-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1c6-537">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6f1c6-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

