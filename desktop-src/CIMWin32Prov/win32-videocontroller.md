---
description: Représente les capacités et la capacité de gestion du contrôleur vidéo sur un système informatique exécutant Windows.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Win32_VideoController, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482769"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="fd5a8-103">\_Classe VideoController Win32</span><span class="sxs-lookup"><span data-stu-id="fd5a8-103">Win32\_VideoController class</span></span>

<span data-ttu-id="fd5a8-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VideoController** WMI représente les capacités et la capacité de gestion du contrôleur vidéo sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="fd5a8-105">Le matériel qui n’est pas compatible avec le modèle WDDM (Windows Display Driver Model) retourne des valeurs de propriété inexactes pour les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="fd5a8-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fd5a8-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5a8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd5a8-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
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
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="fd5a8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fd5a8-109">Members</span></span>

<span data-ttu-id="fd5a8-110">La classe **Win32 \_ VideoController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd5a8-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="fd5a8-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd5a8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd5a8-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd5a8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd5a8-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fd5a8-113">Methods</span></span>

<span data-ttu-id="fd5a8-114">La classe **Win32 \_ VideoController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="fd5a8-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="fd5a8-115">Method</span></span>            | <span data-ttu-id="fd5a8-116">Description</span><span class="sxs-lookup"><span data-stu-id="fd5a8-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5a8-117">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-117">**Reset**</span></span>         | <span data-ttu-id="fd5a8-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-118">Not implemented.</span></span> <span data-ttu-id="fd5a8-119">Pour implémenter cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="fd5a8-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-120">**SetPowerState**</span></span> | <span data-ttu-id="fd5a8-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-121">Not implemented.</span></span> <span data-ttu-id="fd5a8-122">Pour implémenter cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fd5a8-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd5a8-123">Properties</span></span>

<span data-ttu-id="fd5a8-124">La classe **Win32 \_ VideoController** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd5a8-125">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-126">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-128">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-129">Tableau de graphiques et de fonctionnalités 3D du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="fd5a8-130">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="fd5a8-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Accélérateur graphique** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="fd5a8-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**accélérateur 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-135">Accélérateur 3D</span><span class="sxs-lookup"><span data-stu-id="fd5a8-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-136">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-139">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-140">Processeur général utilisé par ce contrôleur pour comparer les compatibilités avec le système.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-141">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-144">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. DACType")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-145">Nom ou identificateur de la puce de conversion numérique-analogique (DAC).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="fd5a8-146">Le jeu de caractères de cette propriété est alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-147">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-150">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-151">Taille de la mémoire de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="fd5a8-152">Exemple : 64000</span><span class="sxs-lookup"><span data-stu-id="fd5a8-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-153">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-156">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-157">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-157">Availability and status of the device.</span></span>

<span data-ttu-id="fd5a8-158">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="fd5a8-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-162">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="fd5a8-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="fd5a8-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="fd5a8-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fd5a8-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="fd5a8-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="fd5a8-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-168">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="fd5a8-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="fd5a8-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fd5a8-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="fd5a8-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="fd5a8-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="fd5a8-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-174">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="fd5a8-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-176">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="fd5a8-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-178">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="fd5a8-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="fd5a8-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-181">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="fd5a8-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-183">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="fd5a8-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-185">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="fd5a8-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-187">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="fd5a8-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-189">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-190">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-191">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-193">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-194">Chaînes de forme libre fournissant des explications plus détaillées sur les fonctionnalités de l’accélérateur vidéo indiquées dans le tableau **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fd5a8-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="fd5a8-195">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau **AcceleratorCapabilities** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="fd5a8-196">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-197">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-200">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-201">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-201">Short description of the object.</span></span>

<span data-ttu-id="fd5a8-202">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-203">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-204">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-206">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-207">Taille de la table des couleurs du système.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-207">Size of the system's color table.</span></span> <span data-ttu-id="fd5a8-208">L’appareil doit avoir une profondeur de couleur inférieure ou égale à 8 bits par pixel ; dans le cas contraire, cette propriété n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="fd5a8-209">Exemple : 256</span><span class="sxs-lookup"><span data-stu-id="fd5a8-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-210">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-211">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-213">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-214">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="fd5a8-215">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="fd5a8-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="fd5a8-217"> (0)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-218">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="fd5a8-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="fd5a8-220">(1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-221">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fd5a8-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="fd5a8-223">(2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="fd5a8-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="fd5a8-225">(3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-226">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fd5a8-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="fd5a8-228">(4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-229">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-229">Device is not working properly.</span></span> <span data-ttu-id="fd5a8-230">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="fd5a8-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="fd5a8-232">(5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-233">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="fd5a8-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="fd5a8-235"> (6)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-236">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="fd5a8-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="fd5a8-238">(7)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="fd5a8-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="fd5a8-240">(8)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-241">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="fd5a8-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="fd5a8-243">(9)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-244">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-244">Device is not working properly.</span></span> <span data-ttu-id="fd5a8-245">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="fd5a8-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="fd5a8-247">(10)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-248">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="fd5a8-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="fd5a8-250">(11)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-251">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="fd5a8-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="fd5a8-253">douze</span><span class="sxs-lookup"><span data-stu-id="fd5a8-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-254">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="fd5a8-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="fd5a8-256">(13)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-257">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="fd5a8-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="fd5a8-259">(14)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-260">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="fd5a8-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="fd5a8-262">(15)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-263">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="fd5a8-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="fd5a8-265">(16)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-266">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="fd5a8-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="fd5a8-268">(17)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-269">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fd5a8-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="fd5a8-271">(18)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-272">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="fd5a8-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="fd5a8-274">(19)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fd5a8-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="fd5a8-276">(20)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-277">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="fd5a8-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="fd5a8-279">(21)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-280">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-280">System failure.</span></span> <span data-ttu-id="fd5a8-281">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="fd5a8-282">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="fd5a8-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="fd5a8-284">(22)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-285">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="fd5a8-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="fd5a8-287">(23)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-288">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-288">System failure.</span></span> <span data-ttu-id="fd5a8-289">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="fd5a8-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="fd5a8-291">(24)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-292">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fd5a8-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="fd5a8-294">(25)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-295">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fd5a8-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="fd5a8-297">(26)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-298">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="fd5a8-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="fd5a8-300">(27)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-301">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="fd5a8-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="fd5a8-303">(28)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-304">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="fd5a8-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="fd5a8-306">(29)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-307">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-307">Device is disabled.</span></span> <span data-ttu-id="fd5a8-308">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="fd5a8-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="fd5a8-310">(30)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-311">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fd5a8-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="fd5a8-313">31</span><span class="sxs-lookup"><span data-stu-id="fd5a8-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-314">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-314">Device is not working properly.</span></span> <span data-ttu-id="fd5a8-315">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-316">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-317">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-319">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-320">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="fd5a8-321">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-322">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-325">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-326">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="fd5a8-327">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="fd5a8-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-329">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-330">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-332">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,12 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-333">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="fd5a8-334">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-335">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-336">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-338">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,11 "), [**unités**](../wmisdk/standard-qualifiers.md) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-339">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="fd5a8-340">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-341">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-344">Nombre de couleurs prises en charge à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="fd5a8-345">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="fd5a8-346">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-347">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-348">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-350">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-351">Nombre de colonnes pour ce contrôleur vidéo (en mode caractère).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="fd5a8-352">Sinon, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="fd5a8-353">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-354">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-355">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-357">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-358">Nombre de lignes pour ce contrôleur vidéo (en mode caractère).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="fd5a8-359">Sinon, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="fd5a8-360">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-361">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-362">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-364">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-365">Fréquence à laquelle le contrôleur vidéo actualise l’image de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="fd5a8-366">La valeur 0 (zéro) indique que le taux par défaut est utilisé, tandis que 0xFFFFFFFF indique que le taux optimal est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="fd5a8-367">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-368">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-369">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-371">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-372">Mode d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-372">Current scan mode.</span></span>

<span data-ttu-id="fd5a8-373">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="fd5a8-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelacé** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="fd5a8-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non entrelacé** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-378">Pas entrelacé</span><span class="sxs-lookup"><span data-stu-id="fd5a8-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-379">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-380">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-382">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,10 "), [**unités**](../wmisdk/standard-qualifiers.md) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-383">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="fd5a8-384">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-385">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-386">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-388">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-389">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-389">Description of the object.</span></span>

<span data-ttu-id="fd5a8-390">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-391">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-392">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-394">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« DeviceID »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-395">Identificateur (propre au système informatique) de ce contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="fd5a8-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-397">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-398">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-400">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-401">Nombre actuel de stylets spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-401">Current number of device-specific pens.</span></span> <span data-ttu-id="fd5a8-402">La valeur 0xffff signifie que l’appareil ne prend pas en charge les stylets.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="fd5a8-403">Exemple : 3</span><span class="sxs-lookup"><span data-stu-id="fd5a8-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-404">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-405">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-407">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions de contexte de périphérique \| EnumDisplaySettings")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-408">Type de tramage du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-408">Dither type of the video controller.</span></span> <span data-ttu-id="fd5a8-409">La propriété peut être l’une des valeurs prédéfinies, ou une valeur définie par le pilote supérieure ou égale à 256.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="fd5a8-410">Si le tramage d’art en ligne est choisi, le contrôleur utilise une méthode de tramage qui produit des bordures bien définies entre les mises à l’échelle en noir, blanc et gris.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="fd5a8-411">Le tramage en ligne n’est pas adapté aux images qui incluent des diplômes continus en intensité et en teinte, tels que des photographies numérisées.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="fd5a8-412">**Aucun tramage** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="fd5a8-413">**Tramage à l’aide d’un pinceau épais** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="fd5a8-414">**Tramage avec un pinceau fin** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="fd5a8-415">**Tramage en ligne** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="fd5a8-416">**L’appareil n’effectue pas de mise à l’échelle en gris** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-417">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-418">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-420">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-421">Date et heure de la dernière modification du pilote vidéo actuellement installé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-422">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-423">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-425">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« fonctions de la \| bibliothèque d’installation du fichier win32api \| GetFileVersionInfo »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-426">Numéro de version du pilote vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-428">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-430">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="fd5a8-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-435">Chaîne de forme libre fournissant plus d’informations sur l’erreur enregistrée dans la propriété **LastErrorCode** , ainsi que des informations sur toutes les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="fd5a8-436">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-437">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-438">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-440">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Printing and Print Spooler structures \| DEVMODE \| dmICMIntent")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-441">Valeur spécifique de l’une des trois méthodes ou intentions de correspondance de couleur possibles qui doit être utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="fd5a8-442">Cette propriété est principalement utilisée pour les applications non-ICM.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="fd5a8-443">Les applications ICM établissent des intentions à l’aide des fonctions ICM.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="fd5a8-444">Cette propriété peut être une valeur prédéfinie ou une valeur définie par le pilote supérieure ou égale à 256.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="fd5a8-445">La correspondance des couleurs basée sur la saturation est le choix le plus approprié pour les graphes professionnels lorsque le tramage n’est pas souhaité.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="fd5a8-446">La correspondance des couleurs basée sur le contraste est le choix le plus approprié pour les images numérisées ou photographiques lorsque le tramage est souhaité.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="fd5a8-447">La mise en correspondance des couleurs optimisée pour correspondre à la couleur exacte demandée est la plus appropriée pour une utilisation avec des logos d’entreprise ou d’autres images lorsqu’une correspondance de couleur exacte est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="fd5a8-448">**Saturation** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="fd5a8-449">**Contraste** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="fd5a8-450">**Couleur exacte** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-451">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-452">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-454">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Printing and Print Spooler structures \| DEVMODE \| dmICMMethod")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-455">Méthode de gestion de l’ICM.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-455">Method of handling ICM.</span></span> <span data-ttu-id="fd5a8-456">Pour les applications non-ICM, cette propriété détermine si ICM est activé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="fd5a8-457">Pour les applications ICM, le système examine cette propriété pour déterminer comment gérer la prise en charge d’ICM.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="fd5a8-458">Cette propriété peut être une valeur prédéfinie ou une valeur définie par le pilote supérieure ou égale à 256.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="fd5a8-459">La valeur détermine le système qui gère la correspondance des couleurs de l’image.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fd5a8-460">**Désactivé** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="fd5a8-461">**Windows** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="fd5a8-462">**Pilote de périphérique** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="fd5a8-463">**Appareil de destination** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-464">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-465">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-467">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-468">Chemin d’accès au fichier. inf de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="fd5a8-469">Exemple : « C : \\ \\ pilotes Windows system32 \\ »</span><span class="sxs-lookup"><span data-stu-id="fd5a8-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-470">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-471">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-473">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-474">Section du fichier. inf où se trouvent les informations de vidéo Windows.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-476">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-478">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-479">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-479">Date and time the object was installed.</span></span> <span data-ttu-id="fd5a8-480">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="fd5a8-481">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-482">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-483">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-484">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-485">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-486">Nom du pilote de périphérique d’affichage installé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-487">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-488">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-489">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-490">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="fd5a8-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-492">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-493">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-495">Qualificateurs : [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-496">Quantité maximale de mémoire prise en charge en octets.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="fd5a8-497">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-498">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-499">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-501">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-502">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="fd5a8-503">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="fd5a8-504">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-505">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-506">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-508">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-509">Taux d’actualisation maximal du contrôleur vidéo en Hertz.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="fd5a8-510">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-511">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-512">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-514">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,4 "), [**unités**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-515">Fréquence d’actualisation minimale du contrôleur vidéo en Hertz.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="fd5a8-516">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-517">**Monochrome**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-518">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-520">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-521">Si la **valeur est true**, la mise à l’échelle grise est utilisée pour afficher les images.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-522">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-524">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-525">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-526">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-526">Label by which the object is known.</span></span> <span data-ttu-id="fd5a8-527">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="fd5a8-528">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-529">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-530">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-531">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-532">Nombre actuel de plans de couleurs.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-532">Current number of color planes.</span></span> <span data-ttu-id="fd5a8-533">Si cette valeur n’est pas applicable à la configuration vidéo actuelle, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="fd5a8-534">Cette propriété est héritée de la [**\_ PCVideoController CIM**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-535">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-536">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-537">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-538">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="fd5a8-539">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-541">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-542">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-543">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-544">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="fd5a8-545">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="fd5a8-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="fd5a8-546">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-547">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-548">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-549">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-550">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="fd5a8-551">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fd5a8-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fd5a8-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fd5a8-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-556">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="fd5a8-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-558">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="fd5a8-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-560">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="fd5a8-561">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="fd5a8-562">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="fd5a8-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-564">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="fd5a8-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-566">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5a8-566">Timed Power-On Supported</span></span>

<span data-ttu-id="fd5a8-567">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-568">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-569">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-570">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-571">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="fd5a8-572">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="fd5a8-573">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-574">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-575">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-576">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-577">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-578">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="fd5a8-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="fd5a8-579">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="fd5a8-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="fd5a8-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="fd5a8-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="fd5a8-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fd5a8-586">ATA ou ATAPI</span><span class="sxs-lookup"><span data-stu-id="fd5a8-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="fd5a8-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="fd5a8-588"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="fd5a8-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="fd5a8-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="fd5a8-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="fd5a8-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="fd5a8-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="fd5a8-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="fd5a8-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="fd5a8-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="fd5a8-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="fd5a8-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="fd5a8-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="fd5a8-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="fd5a8-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="fd5a8-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="fd5a8-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="fd5a8-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="fd5a8-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="fd5a8-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="fd5a8-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="fd5a8-608"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="fd5a8-609"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="fd5a8-610"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="fd5a8-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="fd5a8-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="fd5a8-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="fd5a8-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="fd5a8-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="fd5a8-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="fd5a8-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="fd5a8-618"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="fd5a8-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="fd5a8-620"><span id="DSSI"></span><span id="dssi"></span>**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="fd5a8-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="fd5a8-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="fd5a8-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="fd5a8-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="fd5a8-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="fd5a8-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="fd5a8-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-628">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-629">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-630">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-631">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-632">Nombre d’entrées réservées dans la palette système.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="fd5a8-633">Le système d’exploitation peut réserver des entrées pour prendre en charge des couleurs standard pour les barres de tâches et d’autres éléments d’affichage du bureau.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="fd5a8-634">Cet index est valide uniquement si le pilote de périphérique définit le bit de **\_ palette RC** dans l’index RasterCaps et n’est disponible que si le pilote est compatible avec Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="fd5a8-635">Si le système n’utilise pas de palette, **ReservedSystemPaletteEntries** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="fd5a8-636">Exemple : 20</span><span class="sxs-lookup"><span data-stu-id="fd5a8-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-637">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-638">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-639">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-640">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Printing and Print Spooler structures \| DEVMODE \| dmSpecVersion")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-641">Numéro de version de la spécification des données d’initialisation (sur laquelle la structure est basée).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-642">**État**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-643">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-644">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-645">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-646">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-646">Current status of the object.</span></span> <span data-ttu-id="fd5a8-647">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="fd5a8-648">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="fd5a8-649">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="fd5a8-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fd5a8-650">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fd5a8-651">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fd5a8-652">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fd5a8-653">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd5a8-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fd5a8-654">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fd5a8-655">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fd5a8-656">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-657">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fd5a8-658">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fd5a8-659">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fd5a8-660">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fd5a8-661">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fd5a8-662">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fd5a8-663">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fd5a8-664">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fd5a8-665">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-667">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-668">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-669">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-670">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-670">State of the logical device.</span></span> <span data-ttu-id="fd5a8-671">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="fd5a8-672">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-673">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-674">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fd5a8-675">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fd5a8-676">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fd5a8-677">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-678">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-679">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-680">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-681">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-682">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="fd5a8-683">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-684">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-685">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-686">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-687">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-688">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-688">Name of the scoping system.</span></span>

<span data-ttu-id="fd5a8-689">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-690">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-691">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-692">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-693">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-694">Nombre actuel d’entrées d’index de couleur dans la palette système.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="fd5a8-695">Cet index est valide uniquement si le pilote de périphérique définit le bit de **\_ palette RC** dans l’index RasterCaps et n’est disponible que si le pilote est compatible avec Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="fd5a8-696">Si le système n’utilise pas de palette, **SystemPaletteEntries** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="fd5a8-697">Exemple : 20</span><span class="sxs-lookup"><span data-stu-id="fd5a8-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-698">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-699">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-700">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-701">Date et heure de la dernière réinitialisation de ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="fd5a8-702">Cela peut signifier que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="fd5a8-703">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-704">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-705">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-706">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-707">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-708">Type d’architecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-708">Type of video architecture.</span></span>

<span data-ttu-id="fd5a8-709">Cette propriété est héritée de la [**\_ PCVideoController CIM**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-710">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-711">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="fd5a8-712">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="fd5a8-713">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="fd5a8-714">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="fd5a8-715">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="fd5a8-716">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="fd5a8-717">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="fd5a8-718">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="fd5a8-719">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="fd5a8-720">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="fd5a8-721">**Mémoire tampon de trame linéaire** (12)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="fd5a8-722">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-723">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-724">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-725">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-726">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-727">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-727">Type of video memory.</span></span>

<span data-ttu-id="fd5a8-728">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fd5a8-729">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd5a8-730">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="fd5a8-731">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="fd5a8-732">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="fd5a8-733">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="fd5a8-734">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="fd5a8-735">**Mémoire vive Edo** (7)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="fd5a8-736">**DRAM synchrone en rafale** (8)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="fd5a8-737">**SRAM en rafales pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="fd5a8-738">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="fd5a8-739">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="fd5a8-740">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="fd5a8-741">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="fd5a8-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd5a8-742">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-743">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-744">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-745">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vidéo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-746">Mode vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-746">Current video mode.</span></span>

<span data-ttu-id="fd5a8-747">Cette propriété est héritée de la [**\_ PCVideoController CIM**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-748">**VideoModeDescription**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-749">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-750">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-751">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="fd5a8-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-752">Paramètres actuels de résolution, de couleur et de numérisation du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="fd5a8-753">Exemple : « 1024 x 768 x 256 couleurs »</span><span class="sxs-lookup"><span data-stu-id="fd5a8-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="fd5a8-754">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5a8-755">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5a8-756">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd5a8-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd5a8-757">Chaîne de forme libre décrivant le processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="fd5a8-758">Cette propriété est héritée de la [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd5a8-759">Notes</span><span class="sxs-lookup"><span data-stu-id="fd5a8-759">Remarks</span></span>

<span data-ttu-id="fd5a8-760">La classe **Win32 \_ VideoController** est dérivée de [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="fd5a8-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="fd5a8-761">Pour plus d’informations sur l’utilisation de cette classe, par exemple la récupération d’informations à partir de plusieurs moniteurs, consultez [Utiliser PowerShell pour découvrir des informations à plusieurs](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)écrans.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="fd5a8-762">Exemples</span><span class="sxs-lookup"><span data-stu-id="fd5a8-762">Examples</span></span>

<span data-ttu-id="fd5a8-763">L’exemple VBScript de la [liste des propriétés du contrôleur vidéo](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) répertorie les propriétés du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="fd5a8-764">L’exemple PowerShell suivant répertorie les propriétés du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="fd5a8-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="fd5a8-765">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd5a8-765">Requirements</span></span>



| <span data-ttu-id="fd5a8-766">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd5a8-766">Requirement</span></span> | <span data-ttu-id="fd5a8-767">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd5a8-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5a8-768">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5a8-768">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5a8-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd5a8-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd5a8-770">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd5a8-770">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5a8-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd5a8-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd5a8-772">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd5a8-772">Namespace</span></span><br/>                | <span data-ttu-id="fd5a8-773">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fd5a8-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd5a8-774">MOF</span><span class="sxs-lookup"><span data-stu-id="fd5a8-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd5a8-775"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd5a8-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd5a8-776">DLL</span><span class="sxs-lookup"><span data-stu-id="fd5a8-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd5a8-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd5a8-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd5a8-778">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd5a8-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5a8-779">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fd5a8-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="fd5a8-780">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="fd5a8-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
