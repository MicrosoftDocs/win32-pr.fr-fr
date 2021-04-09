---
description: La \_ classe CIM VideoController représente les fonctionnalités et la gestion du contrôleur vidéo.
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: Classe CIM_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861529"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="c9f87-103">\_Classe CIM VideoController</span><span class="sxs-lookup"><span data-stu-id="c9f87-103">CIM\_VideoController class</span></span>

<span data-ttu-id="c9f87-104">La classe **CIM \_ VideoController** représente les fonctionnalités et la gestion du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9f87-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9f87-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c9f87-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c9f87-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c9f87-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c9f87-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c9f87-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c9f87-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c9f87-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f87-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9f87-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="c9f87-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c9f87-110">Members</span></span>

<span data-ttu-id="c9f87-111">La classe **CIM \_ VideoController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c9f87-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="c9f87-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c9f87-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c9f87-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9f87-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c9f87-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c9f87-114">Methods</span></span>

<span data-ttu-id="c9f87-115">La classe **CIM \_ VideoController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c9f87-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="c9f87-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="c9f87-116">Method</span></span>                                                                     | <span data-ttu-id="c9f87-117">Description</span><span class="sxs-lookup"><span data-stu-id="c9f87-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9f87-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="c9f87-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="c9f87-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c9f87-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c9f87-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="c9f87-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c9f87-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c9f87-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="c9f87-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="c9f87-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c9f87-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="c9f87-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c9f87-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9f87-124">Properties</span></span>

<span data-ttu-id="c9f87-125">La classe **CIM \_ VideoController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9f87-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9f87-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c9f87-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-127">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-129">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="c9f87-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-130">Graphiques et fonctionnalités 3D du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9f87-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-131">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c9f87-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9f87-132">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="c9f87-133">**Accélérateur graphique** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="c9f87-134">**accélérateur 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-135">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="c9f87-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-136">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-139">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-139">Availability and status of the device.</span></span>

<span data-ttu-id="c9f87-140">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9f87-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c9f87-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c9f87-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c9f87-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="c9f87-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c9f87-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="c9f87-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c9f87-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="c9f87-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c9f87-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="c9f87-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c9f87-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="c9f87-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c9f87-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="c9f87-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c9f87-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="c9f87-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c9f87-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="c9f87-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c9f87-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="c9f87-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-154">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="c9f87-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c9f87-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="c9f87-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-156">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="c9f87-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c9f87-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="c9f87-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-158">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="c9f87-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c9f87-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="c9f87-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c9f87-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="c9f87-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-161">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="c9f87-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c9f87-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="c9f87-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-163">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="c9f87-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c9f87-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="c9f87-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-165">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="c9f87-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c9f87-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="c9f87-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-167">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="c9f87-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c9f87-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="c9f87-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-169">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="c9f87-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-170">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c9f87-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-171">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="c9f87-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-173">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="c9f87-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-174">Chaînes de forme libre qui fournissent des descriptions détaillées des fonctionnalités d’accélérateur vidéo indiquées dans le tableau **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c9f87-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="c9f87-175">Chaque entrée de ce tableau est liée à l’entrée dans le tableau **AcceleratorCapabilities** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="c9f87-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="c9f87-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c9f87-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-179">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-180">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9f87-180">Short textual description of the object.</span></span>

<span data-ttu-id="c9f87-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-182">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c9f87-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-185">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c9f87-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-186">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c9f87-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="c9f87-187">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c9f87-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c9f87-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="c9f87-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-190">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="c9f87-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c9f87-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c9f87-192">(1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-193">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="c9f87-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c9f87-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c9f87-195">(2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c9f87-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c9f87-197">(3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-198">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="c9f87-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c9f87-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c9f87-200">(4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-201">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c9f87-201">Device is not working properly.</span></span> <span data-ttu-id="c9f87-202">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c9f87-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c9f87-204">(5)</span><span class="sxs-lookup"><span data-stu-id="c9f87-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-205">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="c9f87-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c9f87-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c9f87-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="c9f87-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-208">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="c9f87-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c9f87-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c9f87-210">(7)</span><span class="sxs-lookup"><span data-stu-id="c9f87-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c9f87-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c9f87-212">(8)</span><span class="sxs-lookup"><span data-stu-id="c9f87-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-213">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="c9f87-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c9f87-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c9f87-215">(9)</span><span class="sxs-lookup"><span data-stu-id="c9f87-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-216">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c9f87-216">Device is not working properly.</span></span> <span data-ttu-id="c9f87-217">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c9f87-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c9f87-219">(10)</span><span class="sxs-lookup"><span data-stu-id="c9f87-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-220">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c9f87-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c9f87-222">(11)</span><span class="sxs-lookup"><span data-stu-id="c9f87-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-223">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c9f87-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c9f87-225">douze</span><span class="sxs-lookup"><span data-stu-id="c9f87-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-226">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c9f87-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c9f87-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c9f87-228">(13)</span><span class="sxs-lookup"><span data-stu-id="c9f87-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-229">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c9f87-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c9f87-231">(14)</span><span class="sxs-lookup"><span data-stu-id="c9f87-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-232">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="c9f87-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c9f87-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c9f87-234">(15)</span><span class="sxs-lookup"><span data-stu-id="c9f87-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-235">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="c9f87-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c9f87-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c9f87-237">(16)</span><span class="sxs-lookup"><span data-stu-id="c9f87-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-238">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c9f87-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c9f87-240">(17)</span><span class="sxs-lookup"><span data-stu-id="c9f87-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-241">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="c9f87-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c9f87-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c9f87-243">(18)</span><span class="sxs-lookup"><span data-stu-id="c9f87-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-244">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="c9f87-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c9f87-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c9f87-246">(19)</span><span class="sxs-lookup"><span data-stu-id="c9f87-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c9f87-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c9f87-248">(20)</span><span class="sxs-lookup"><span data-stu-id="c9f87-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-249">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c9f87-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c9f87-251">(21)</span><span class="sxs-lookup"><span data-stu-id="c9f87-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-252">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="c9f87-252">System failure.</span></span> <span data-ttu-id="c9f87-253">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="c9f87-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c9f87-254">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c9f87-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c9f87-256">(22)</span><span class="sxs-lookup"><span data-stu-id="c9f87-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-257">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c9f87-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c9f87-259">(23)</span><span class="sxs-lookup"><span data-stu-id="c9f87-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-260">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="c9f87-260">System failure.</span></span> <span data-ttu-id="c9f87-261">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="c9f87-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c9f87-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c9f87-263">(24)</span><span class="sxs-lookup"><span data-stu-id="c9f87-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-264">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="c9f87-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c9f87-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c9f87-266">(25)</span><span class="sxs-lookup"><span data-stu-id="c9f87-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-267">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c9f87-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c9f87-269">(26)</span><span class="sxs-lookup"><span data-stu-id="c9f87-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-270">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9f87-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c9f87-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c9f87-272">(27)</span><span class="sxs-lookup"><span data-stu-id="c9f87-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-273">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="c9f87-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c9f87-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c9f87-275">(28)</span><span class="sxs-lookup"><span data-stu-id="c9f87-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-276">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="c9f87-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c9f87-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c9f87-278">(29)</span><span class="sxs-lookup"><span data-stu-id="c9f87-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-279">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-279">Device is disabled.</span></span> <span data-ttu-id="c9f87-280">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="c9f87-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c9f87-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c9f87-282">(30)</span><span class="sxs-lookup"><span data-stu-id="c9f87-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-283">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="c9f87-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c9f87-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="c9f87-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c9f87-285">31</span><span class="sxs-lookup"><span data-stu-id="c9f87-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-286">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c9f87-286">Device is not working properly.</span></span> <span data-ttu-id="c9f87-287">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="c9f87-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c9f87-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-289">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c9f87-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-291">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c9f87-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-292">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9f87-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c9f87-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c9f87-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-297">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c9f87-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-298">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="c9f87-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c9f87-299">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="c9f87-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c9f87-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-301">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="c9f87-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-302">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-304">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,12 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-305">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="c9f87-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-306">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="c9f87-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-307">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-309">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,11 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-310">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="c9f87-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-311">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="c9f87-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-312">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9f87-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-314">Nombre de couleurs prises en charge à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="c9f87-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="c9f87-315">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c9f87-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-316">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="c9f87-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-317">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-319">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-320">En mode caractère, nombre de colonnes pour le contrôleur vidéo ; Sinon, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="c9f87-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-321">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="c9f87-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-322">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-324">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-325">En mode caractère, nombre de lignes pour le contrôleur vidéo ; Sinon, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="c9f87-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-326">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c9f87-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-327">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-329">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,15 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-330">Fréquence d’actualisation actuelle, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="c9f87-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-331">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="c9f87-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-332">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-334">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-335">Mode d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="c9f87-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9f87-336">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-337">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="c9f87-338">**Entrelacé** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="c9f87-339">**Non entrelacé** (4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-340">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="c9f87-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-341">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-343">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,10 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-344">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="c9f87-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-345">**Description**</span><span class="sxs-lookup"><span data-stu-id="c9f87-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-348">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c9f87-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-349">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9f87-349">Textual description of the object.</span></span>

<span data-ttu-id="c9f87-350">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c9f87-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-354">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c9f87-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-355">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c9f87-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c9f87-356">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-357">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c9f87-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-358">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c9f87-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-360">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="c9f87-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c9f87-361">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c9f87-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-363">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-365">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="c9f87-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c9f87-366">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c9f87-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-368">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c9f87-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-370">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-371">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9f87-371">Date and time the object was installed.</span></span> <span data-ttu-id="c9f87-372">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c9f87-373">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-374">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c9f87-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-375">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-377">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c9f87-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c9f87-378">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-379">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="c9f87-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-380">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-382">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c9f87-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-383">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="c9f87-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-384">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="c9f87-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-385">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-387">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-388">Nombre maximal d’entités directement adressables prises en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="c9f87-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="c9f87-389">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="c9f87-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="c9f87-390">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-391">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c9f87-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-392">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-395">Taux de rafraîchissement maximal du contrôleur vidéo, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="c9f87-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-396">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="c9f87-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-397">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-399">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-400">Taux d’actualisation minimal du contrôleur vidéo, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="c9f87-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-401">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c9f87-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-402">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-404">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c9f87-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-405">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="c9f87-405">Label by which the object is known.</span></span> <span data-ttu-id="c9f87-406">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c9f87-407">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-408">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="c9f87-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-409">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9f87-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-411">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="c9f87-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c9f87-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-413">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-415">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c9f87-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-416">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c9f87-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="c9f87-417">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c9f87-418">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="c9f87-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-419">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c9f87-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-420">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-422">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="c9f87-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c9f87-423">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="c9f87-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c9f87-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c9f87-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c9f87-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c9f87-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-428">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="c9f87-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c9f87-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-430">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="c9f87-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c9f87-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="c9f87-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-432">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c9f87-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c9f87-433">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="c9f87-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c9f87-434">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c9f87-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c9f87-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="c9f87-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-436">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="c9f87-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c9f87-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="c9f87-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c9f87-438">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="c9f87-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-439">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c9f87-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-440">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c9f87-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-442">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="c9f87-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c9f87-443">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c9f87-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c9f87-444">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c9f87-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c9f87-445">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c9f87-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="c9f87-446">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-447">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="c9f87-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-448">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-450">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-451">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="c9f87-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="c9f87-452">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="c9f87-453">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9f87-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9f87-454">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-455">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="c9f87-456">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="c9f87-457">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="c9f87-458">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="c9f87-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="c9f87-459">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="c9f87-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="c9f87-460">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="c9f87-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="c9f87-461">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="c9f87-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="c9f87-462">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="c9f87-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="c9f87-463">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="c9f87-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="c9f87-464">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="c9f87-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="c9f87-465">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="c9f87-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="c9f87-466">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="c9f87-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="c9f87-467">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="c9f87-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="c9f87-468">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="c9f87-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="c9f87-469">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="c9f87-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="c9f87-470">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="c9f87-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="c9f87-471">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="c9f87-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="c9f87-472">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="c9f87-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="c9f87-473">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="c9f87-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c9f87-474">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="c9f87-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="c9f87-475">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="c9f87-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="c9f87-476">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="c9f87-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="c9f87-477">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="c9f87-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="c9f87-478">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="c9f87-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="c9f87-479">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="c9f87-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="c9f87-480">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="c9f87-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="c9f87-481">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="c9f87-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="c9f87-482">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="c9f87-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="c9f87-483">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="c9f87-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="c9f87-484">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="c9f87-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="c9f87-485">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="c9f87-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="c9f87-486">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="c9f87-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="c9f87-487">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="c9f87-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="c9f87-488">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="c9f87-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="c9f87-489">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="c9f87-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="c9f87-490">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="c9f87-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="c9f87-491">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="c9f87-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="c9f87-492">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="c9f87-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="c9f87-493">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="c9f87-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="c9f87-494">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="c9f87-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="c9f87-495">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="c9f87-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="c9f87-496">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="c9f87-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="c9f87-497">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="c9f87-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="c9f87-498">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="c9f87-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="c9f87-499">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="c9f87-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="c9f87-500">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="c9f87-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-501">**État**</span><span class="sxs-lookup"><span data-stu-id="c9f87-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-502">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-504">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c9f87-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-505">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c9f87-505">Current status of the object.</span></span> <span data-ttu-id="c9f87-506">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c9f87-507">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9f87-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c9f87-508">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c9f87-509">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c9f87-510">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-511">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="c9f87-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c9f87-512">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c9f87-513">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c9f87-514">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c9f87-515">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c9f87-516">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c9f87-517">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c9f87-518">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c9f87-519">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="c9f87-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c9f87-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-521">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-522">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-523">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-524">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="c9f87-524">State of the logical device.</span></span> <span data-ttu-id="c9f87-525">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c9f87-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c9f87-526">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9f87-527">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-528">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c9f87-529">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c9f87-530">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c9f87-531">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="c9f87-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c9f87-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-533">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-534">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-535">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c9f87-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-536">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c9f87-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="c9f87-537">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-538">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c9f87-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-539">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-540">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-541">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c9f87-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-542">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c9f87-542">Scoping system's name.</span></span>

<span data-ttu-id="c9f87-543">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-544">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c9f87-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-545">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c9f87-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-546">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-547">Date et heure de la dernière réinitialisation du contrôleur, ce qui signifie que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="c9f87-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="c9f87-548">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9f87-549">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="c9f87-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-550">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9f87-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-551">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-552">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vidéo DMTF \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="c9f87-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-553">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9f87-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c9f87-554">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c9f87-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c9f87-555">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="c9f87-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="c9f87-556">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="c9f87-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="c9f87-557">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="c9f87-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="c9f87-558">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="c9f87-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="c9f87-559">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="c9f87-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="c9f87-560">**Mémoire vive Edo** (7)</span><span class="sxs-lookup"><span data-stu-id="c9f87-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="c9f87-561">**DRAM synchrone en rafale** (8)</span><span class="sxs-lookup"><span data-stu-id="c9f87-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="c9f87-562">**SRAM en rafales pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="c9f87-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="c9f87-563">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="c9f87-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="c9f87-564">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="c9f87-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="c9f87-565">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="c9f87-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="c9f87-566">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="c9f87-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9f87-567">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="c9f87-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9f87-568">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9f87-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9f87-569">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f87-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9f87-570">Chaîne de forme libre qui décrit le processeur vidéo ou le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="c9f87-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9f87-571">Notes</span><span class="sxs-lookup"><span data-stu-id="c9f87-571">Remarks</span></span>

<span data-ttu-id="c9f87-572">La classe **CIM \_ VideoController** est dérivée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="c9f87-573">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="c9f87-573">WMI does not implement this class.</span></span> <span data-ttu-id="c9f87-574">Pour les classes WMI dérivées de **CIM \_ VideoController**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c9f87-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c9f87-575">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c9f87-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c9f87-576">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c9f87-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f87-577">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9f87-577">Requirements</span></span>



| <span data-ttu-id="c9f87-578">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9f87-578">Requirement</span></span> | <span data-ttu-id="c9f87-579">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9f87-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f87-580">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9f87-580">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f87-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9f87-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9f87-582">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9f87-582">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f87-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9f87-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9f87-584">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9f87-584">Namespace</span></span><br/>                | <span data-ttu-id="c9f87-585">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c9f87-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9f87-586">MOF</span><span class="sxs-lookup"><span data-stu-id="c9f87-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9f87-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9f87-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9f87-588">DLL</span><span class="sxs-lookup"><span data-stu-id="c9f87-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9f87-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9f87-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9f87-590">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9f87-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f87-591">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="c9f87-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

