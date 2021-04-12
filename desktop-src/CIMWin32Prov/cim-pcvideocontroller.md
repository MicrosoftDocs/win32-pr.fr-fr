---
description: Le \_ PCVIDEOCONTROLLER CIM représente les fonctionnalités et la gestion d’un contrôleur vidéo d’ordinateur personnel, un sous-type d’un contrôleur vidéo.
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: Classe CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393115"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="7758a-103">\_Classe CIM PCVideoController</span><span class="sxs-lookup"><span data-stu-id="7758a-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="7758a-104">Le **\_ PCVideoController CIM** représente les fonctionnalités et la gestion d’un contrôleur vidéo d’ordinateur personnel, un sous-type d’un contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7758a-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7758a-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="7758a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7758a-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7758a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7758a-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7758a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7758a-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7758a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7758a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7758a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="7758a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7758a-110">Members</span></span>

<span data-ttu-id="7758a-111">La classe **CIM \_ PCVideoController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7758a-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="7758a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7758a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7758a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7758a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7758a-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7758a-114">Methods</span></span>

<span data-ttu-id="7758a-115">La classe **CIM \_ PCVideoController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7758a-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="7758a-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="7758a-116">Method</span></span>                                                                       | <span data-ttu-id="7758a-117">Description</span><span class="sxs-lookup"><span data-stu-id="7758a-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7758a-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="7758a-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="7758a-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7758a-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="7758a-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="7758a-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="7758a-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7758a-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="7758a-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="7758a-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7758a-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="7758a-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7758a-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7758a-124">Properties</span></span>

<span data-ttu-id="7758a-125">La classe **CIM \_ PCVideoController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7758a-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7758a-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7758a-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-127">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7758a-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-129">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="7758a-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-130">Graphiques et fonctionnalités 3D du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7758a-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="7758a-131">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="7758a-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="7758a-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Accélérateur graphique** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="7758a-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**accélérateur 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-136">accélérateur 3D</span><span class="sxs-lookup"><span data-stu-id="7758a-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-137">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="7758a-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7758a-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-141">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-141">Availability and status of the device.</span></span>

<span data-ttu-id="7758a-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7758a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-146">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="7758a-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7758a-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7758a-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="7758a-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7758a-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="7758a-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7758a-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="7758a-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7758a-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="7758a-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7758a-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="7758a-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7758a-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="7758a-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7758a-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="7758a-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7758a-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="7758a-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7758a-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="7758a-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-157">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="7758a-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7758a-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="7758a-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-159">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="7758a-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7758a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="7758a-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-161">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="7758a-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7758a-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="7758a-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7758a-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="7758a-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-164">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="7758a-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7758a-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="7758a-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-166">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="7758a-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7758a-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="7758a-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-168">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="7758a-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7758a-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="7758a-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-170">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="7758a-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7758a-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="7758a-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-172">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="7758a-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-173">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7758a-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-174">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7758a-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7758a-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-176">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="7758a-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-177">Chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités d’accélérateur vidéo indiquées dans le tableau **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7758a-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="7758a-178">Chaque entrée de tableau est liée à l’entrée dans le tableau **AcceleratorCapabilities** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="7758a-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="7758a-179">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-180">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7758a-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-183">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="7758a-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-184">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7758a-184">Short textual description of the object.</span></span>

<span data-ttu-id="7758a-185">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7758a-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-189">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7758a-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-190">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7758a-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="7758a-191">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7758a-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="7758a-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7758a-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="7758a-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-194">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="7758a-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7758a-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="7758a-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7758a-196">(1)</span><span class="sxs-lookup"><span data-stu-id="7758a-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-197">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="7758a-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7758a-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7758a-199">(2)</span><span class="sxs-lookup"><span data-stu-id="7758a-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7758a-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="7758a-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7758a-201">(3)</span><span class="sxs-lookup"><span data-stu-id="7758a-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-202">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="7758a-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7758a-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="7758a-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7758a-204">(4)</span><span class="sxs-lookup"><span data-stu-id="7758a-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-205">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="7758a-205">Device is not working properly.</span></span> <span data-ttu-id="7758a-206">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="7758a-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7758a-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="7758a-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7758a-208">(5)</span><span class="sxs-lookup"><span data-stu-id="7758a-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-209">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="7758a-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7758a-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="7758a-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7758a-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="7758a-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-212">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="7758a-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7758a-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="7758a-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7758a-214">(7)</span><span class="sxs-lookup"><span data-stu-id="7758a-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7758a-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="7758a-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7758a-216">(8)</span><span class="sxs-lookup"><span data-stu-id="7758a-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-217">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="7758a-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7758a-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7758a-219">(9)</span><span class="sxs-lookup"><span data-stu-id="7758a-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-220">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="7758a-220">Device is not working properly.</span></span> <span data-ttu-id="7758a-221">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7758a-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7758a-223">(10)</span><span class="sxs-lookup"><span data-stu-id="7758a-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-224">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7758a-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7758a-226">(11)</span><span class="sxs-lookup"><span data-stu-id="7758a-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-227">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7758a-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="7758a-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7758a-229">douze</span><span class="sxs-lookup"><span data-stu-id="7758a-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-230">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7758a-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7758a-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7758a-232">(13)</span><span class="sxs-lookup"><span data-stu-id="7758a-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-233">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7758a-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="7758a-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7758a-235">(14)</span><span class="sxs-lookup"><span data-stu-id="7758a-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-236">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="7758a-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7758a-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="7758a-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7758a-238">(15)</span><span class="sxs-lookup"><span data-stu-id="7758a-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-239">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="7758a-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7758a-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7758a-241">(16)</span><span class="sxs-lookup"><span data-stu-id="7758a-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-242">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7758a-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="7758a-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7758a-244">(17)</span><span class="sxs-lookup"><span data-stu-id="7758a-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-245">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="7758a-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7758a-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7758a-247">(18)</span><span class="sxs-lookup"><span data-stu-id="7758a-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-248">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="7758a-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7758a-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="7758a-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7758a-250">(19)</span><span class="sxs-lookup"><span data-stu-id="7758a-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7758a-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="7758a-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7758a-252">(20)</span><span class="sxs-lookup"><span data-stu-id="7758a-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-253">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="7758a-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7758a-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7758a-255">(21)</span><span class="sxs-lookup"><span data-stu-id="7758a-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-256">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="7758a-256">System failure.</span></span> <span data-ttu-id="7758a-257">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="7758a-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7758a-258">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7758a-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="7758a-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7758a-260">(22)</span><span class="sxs-lookup"><span data-stu-id="7758a-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-261">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7758a-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7758a-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="7758a-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7758a-263">(23)</span><span class="sxs-lookup"><span data-stu-id="7758a-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-264">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="7758a-264">System failure.</span></span> <span data-ttu-id="7758a-265">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="7758a-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7758a-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="7758a-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7758a-267">(24)</span><span class="sxs-lookup"><span data-stu-id="7758a-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-268">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="7758a-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7758a-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7758a-270">(25)</span><span class="sxs-lookup"><span data-stu-id="7758a-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-271">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7758a-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7758a-273">(26)</span><span class="sxs-lookup"><span data-stu-id="7758a-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-274">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7758a-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7758a-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="7758a-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7758a-276">(27)</span><span class="sxs-lookup"><span data-stu-id="7758a-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-277">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="7758a-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7758a-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="7758a-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7758a-279">(28)</span><span class="sxs-lookup"><span data-stu-id="7758a-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-280">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="7758a-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7758a-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="7758a-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7758a-282">(29)</span><span class="sxs-lookup"><span data-stu-id="7758a-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-283">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="7758a-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7758a-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="7758a-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7758a-285">(30)</span><span class="sxs-lookup"><span data-stu-id="7758a-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-286">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="7758a-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7758a-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="7758a-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7758a-288">31</span><span class="sxs-lookup"><span data-stu-id="7758a-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-289">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="7758a-289">Device is not working properly.</span></span> <span data-ttu-id="7758a-290">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="7758a-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7758a-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-292">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7758a-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-294">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7758a-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-295">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7758a-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7758a-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7758a-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-300">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7758a-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7758a-301">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="7758a-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7758a-302">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7758a-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7758a-303">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-304">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="7758a-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-305">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-307">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,12 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="7758a-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-308">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="7758a-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="7758a-309">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-310">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="7758a-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-311">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-313">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="7758a-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-314">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="7758a-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="7758a-315">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-316">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="7758a-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-317">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7758a-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-319">Nombre de couleurs prises en charge aux résolutions actuelles.</span><span class="sxs-lookup"><span data-stu-id="7758a-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="7758a-320">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="7758a-321">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7758a-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-322">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="7758a-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-323">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-325">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-326">En mode caractère, nombre de colonnes pour le contrôleur vidéo ; Sinon, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="7758a-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="7758a-327">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-328">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="7758a-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-329">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-331">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-332">En mode caractère, nombre de lignes pour ce contrôleur vidéo ; Sinon, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="7758a-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="7758a-333">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-334">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="7758a-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-335">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="7758a-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-338">Taux d’actualisation actuel en Hertz.</span><span class="sxs-lookup"><span data-stu-id="7758a-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="7758a-339">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-340">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="7758a-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-341">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-343">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-344">Mode d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="7758a-344">Current scan mode.</span></span> <span data-ttu-id="7758a-345">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="7758a-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelacé** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="7758a-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non entrelacé** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-350">Non entrelacé</span><span class="sxs-lookup"><span data-stu-id="7758a-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-351">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="7758a-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-352">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-354">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,10 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="7758a-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-355">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="7758a-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="7758a-356">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-357">**Description**</span><span class="sxs-lookup"><span data-stu-id="7758a-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-360">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7758a-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-361">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7758a-361">Textual description of the object.</span></span>

<span data-ttu-id="7758a-362">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-363">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7758a-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-366">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7758a-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7758a-367">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7758a-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7758a-368">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-369">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7758a-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-370">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7758a-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-372">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="7758a-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7758a-373">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7758a-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-375">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-377">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="7758a-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7758a-378">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7758a-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-380">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7758a-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-382">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="7758a-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-383">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7758a-383">Date and time the object was installed.</span></span> <span data-ttu-id="7758a-384">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="7758a-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7758a-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-386">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7758a-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-387">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-389">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7758a-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7758a-390">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-391">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="7758a-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-392">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-394">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="7758a-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-395">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="7758a-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="7758a-396">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-397">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="7758a-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-398">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-400">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-401">Nombre maximal d’entités directement adressables prises en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="7758a-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="7758a-402">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="7758a-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="7758a-403">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-404">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="7758a-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-405">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-407">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="7758a-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-408">Taux d’actualisation maximal du contrôleur vidéo en Hertz.</span><span class="sxs-lookup"><span data-stu-id="7758a-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="7758a-409">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-410">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="7758a-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-411">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-412">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-413">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="7758a-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-414">Fréquence d’actualisation minimale du contrôleur vidéo en Hertz.</span><span class="sxs-lookup"><span data-stu-id="7758a-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="7758a-415">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-416">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7758a-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-417">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-419">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7758a-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-420">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="7758a-420">Label by which the object is known.</span></span> <span data-ttu-id="7758a-421">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="7758a-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7758a-422">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-423">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="7758a-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-424">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-426">Nombre actuel de plans de couleurs.</span><span class="sxs-lookup"><span data-stu-id="7758a-426">Current number of color planes.</span></span> <span data-ttu-id="7758a-427">Si cette valeur n’est pas applicable à la configuration vidéo actuelle, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="7758a-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="7758a-428">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="7758a-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-429">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7758a-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-431">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="7758a-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="7758a-432">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7758a-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-436">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7758a-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-437">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="7758a-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="7758a-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7758a-439">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="7758a-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7758a-440">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7758a-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-441">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7758a-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-443">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="7758a-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7758a-444">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="7758a-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="7758a-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7758a-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7758a-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7758a-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-449">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7758a-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7758a-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-451">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="7758a-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7758a-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="7758a-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-453">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7758a-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7758a-454">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="7758a-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7758a-455">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7758a-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7758a-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="7758a-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-457">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="7758a-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7758a-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="7758a-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7758a-459">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="7758a-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-460">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7758a-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-461">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7758a-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-462">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-463">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="7758a-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7758a-464">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7758a-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7758a-465">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7758a-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7758a-466">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7758a-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="7758a-467">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-468">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="7758a-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-469">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-471">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-472">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="7758a-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="7758a-473">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="7758a-474">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7758a-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-475">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-476">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="7758a-477">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="7758a-478">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="7758a-479">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="7758a-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="7758a-480">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="7758a-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="7758a-481">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="7758a-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="7758a-482">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="7758a-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="7758a-483">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="7758a-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="7758a-484">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="7758a-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="7758a-485">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="7758a-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="7758a-486">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="7758a-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="7758a-487">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="7758a-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="7758a-488">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="7758a-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="7758a-489">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="7758a-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="7758a-490">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="7758a-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="7758a-491">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="7758a-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="7758a-492">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="7758a-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="7758a-493">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="7758a-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="7758a-494">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="7758a-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="7758a-495">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="7758a-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="7758a-496">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="7758a-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="7758a-497">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="7758a-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="7758a-498">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="7758a-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="7758a-499">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="7758a-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="7758a-500">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="7758a-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="7758a-501">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="7758a-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="7758a-502">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="7758a-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="7758a-503">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="7758a-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="7758a-504">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="7758a-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="7758a-505">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="7758a-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="7758a-506">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="7758a-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="7758a-507">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="7758a-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="7758a-508">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="7758a-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="7758a-509">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="7758a-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="7758a-510">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="7758a-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="7758a-511">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="7758a-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="7758a-512">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="7758a-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="7758a-513">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="7758a-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="7758a-514">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="7758a-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="7758a-515">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="7758a-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="7758a-516">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="7758a-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="7758a-517">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="7758a-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="7758a-518">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="7758a-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="7758a-519">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="7758a-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="7758a-520">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="7758a-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="7758a-521">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="7758a-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-522">**État**</span><span class="sxs-lookup"><span data-stu-id="7758a-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-525">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7758a-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-526">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7758a-526">Current status of the object.</span></span> <span data-ttu-id="7758a-527">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7758a-528">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7758a-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7758a-529">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="7758a-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7758a-530">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="7758a-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7758a-531">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="7758a-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-532">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="7758a-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7758a-533">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="7758a-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7758a-534">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="7758a-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7758a-535">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="7758a-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7758a-536">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="7758a-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7758a-537">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="7758a-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7758a-538">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="7758a-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7758a-539">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="7758a-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7758a-540">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="7758a-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7758a-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-542">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-543">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-544">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-545">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="7758a-545">State of the logical device.</span></span> <span data-ttu-id="7758a-546">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7758a-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7758a-547">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-548">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-549">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7758a-550">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7758a-551">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7758a-552">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="7758a-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-553">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7758a-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-554">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-555">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-556">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7758a-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7758a-557">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="7758a-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="7758a-558">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-559">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7758a-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-560">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-561">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-562">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7758a-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7758a-563">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="7758a-563">Scoping system's name.</span></span>

<span data-ttu-id="7758a-564">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-565">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="7758a-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-566">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7758a-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-567">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-568">Date et heure de la dernière réinitialisation de ce contrôleur, c’est-à-dire que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="7758a-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="7758a-569">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7758a-570">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="7758a-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-571">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-572">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-573">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-574">Architecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="7758a-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-575">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-576">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="7758a-577">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="7758a-578">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="7758a-579">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="7758a-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="7758a-580">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="7758a-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="7758a-581">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="7758a-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="7758a-582">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="7758a-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="7758a-583">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="7758a-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="7758a-584">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="7758a-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="7758a-585">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="7758a-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="7758a-586">**Mémoire tampon de trame linéaire** (12)</span><span class="sxs-lookup"><span data-stu-id="7758a-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="7758a-587">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="7758a-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-588">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="7758a-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-589">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-590">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-591">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-592">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="7758a-592">Type of video memory.</span></span>

<span data-ttu-id="7758a-593">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7758a-594">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7758a-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7758a-595">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="7758a-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="7758a-596">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="7758a-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="7758a-597">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="7758a-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="7758a-598">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="7758a-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="7758a-599">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="7758a-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="7758a-600">**Mémoire vive Edo** (7)</span><span class="sxs-lookup"><span data-stu-id="7758a-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="7758a-601">**DRAM synchrone en rafale** (8)</span><span class="sxs-lookup"><span data-stu-id="7758a-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="7758a-602">**SRAM en rafales pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="7758a-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="7758a-603">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="7758a-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="7758a-604">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="7758a-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="7758a-605">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="7758a-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="7758a-606">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="7758a-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7758a-607">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="7758a-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-608">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7758a-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-609">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7758a-610">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7758a-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7758a-611">Mode vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="7758a-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="7758a-612">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="7758a-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7758a-613">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7758a-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7758a-614">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7758a-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7758a-615">Chaîne de forme libre qui décrit le processeur/contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7758a-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="7758a-616">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7758a-617">Notes</span><span class="sxs-lookup"><span data-stu-id="7758a-617">Remarks</span></span>

<span data-ttu-id="7758a-618">La classe **CIM \_ PCVideoController** est dérivée de [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="7758a-619">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="7758a-619">WMI does not implement this class.</span></span> <span data-ttu-id="7758a-620">Pour les classes WMI dérivées de [**CIM \_ PCVideoController**](cim-videocontroller.md), consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7758a-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7758a-621">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="7758a-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7758a-622">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7758a-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7758a-623">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7758a-623">Requirements</span></span>



| <span data-ttu-id="7758a-624">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7758a-624">Requirement</span></span> | <span data-ttu-id="7758a-625">Valeur</span><span class="sxs-lookup"><span data-stu-id="7758a-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7758a-626">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7758a-626">Minimum supported client</span></span><br/> | <span data-ttu-id="7758a-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7758a-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7758a-628">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7758a-628">Minimum supported server</span></span><br/> | <span data-ttu-id="7758a-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7758a-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7758a-630">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7758a-630">Namespace</span></span><br/>                | <span data-ttu-id="7758a-631">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7758a-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7758a-632">MOF</span><span class="sxs-lookup"><span data-stu-id="7758a-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7758a-633"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7758a-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7758a-634">DLL</span><span class="sxs-lookup"><span data-stu-id="7758a-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7758a-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7758a-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7758a-636">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7758a-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7758a-637">**\_VIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="7758a-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

