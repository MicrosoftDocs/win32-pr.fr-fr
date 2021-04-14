---
description: La \_ classe VideoConfiguration Win32 n’est pas active. Elle ne retourne pas d’instances, car il n’existe aucun fournisseur qui la sauvegarde.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Classe Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523196"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="cd2d8-104">\_Classe VideoConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="cd2d8-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="cd2d8-105">La **classe \_ VideoConfiguration Win32** n’est pas active.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="cd2d8-106">Elle ne retourne pas d’instances, car il n’existe aucun fournisseur qui la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="cd2d8-107">La **classe \_ VideoConfiguration Win32** représente une configuration d’un sous-système vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="cd2d8-108">Cette classe a été dépréciée en faveur des propriétés contenues dans les classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)et [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="cd2d8-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2d8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd2d8-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="cd2d8-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cd2d8-111">Members</span></span>

<span data-ttu-id="cd2d8-112">La classe **Win32 \_ VideoConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cd2d8-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="cd2d8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd2d8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd2d8-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd2d8-114">Properties</span></span>

<span data-ttu-id="cd2d8-115">La classe **Win32 \_ VideoConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd2d8-116">**ActualColorResolution**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-119">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**unités**](../wmisdk/standard-qualifiers.md) (« bits par pixel »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-120">Indique la profondeur de couleur actuelle de l’affichage vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="cd2d8-121">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-122">**AdapterChipType**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-125">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ info \| ChipType")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-126">Contient le nom de la puce de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="cd2d8-127">Exemple : S3</span><span class="sxs-lookup"><span data-stu-id="cd2d8-127">Example: s3</span></span>

<span data-ttu-id="cd2d8-128">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-129">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-132">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-133">Spécifie le nom du fabricant de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="cd2d8-134">Ce nom peut être utilisé pour comparer la compatibilité de cet appareil avec les besoins du système informatique.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="cd2d8-135">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-136">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-139">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ info \| DACType")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-140">Indique le nom du processeur numérique-analogique (DAC) utilisé dans l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="cd2d8-141">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-142">**AdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-145">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-146">Contient une description ou un nom descriptif de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="cd2d8-147">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-148">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-151">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ info \| VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-152">Indique la taille de la mémoire de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="cd2d8-153">Exemple : 16777216</span><span class="sxs-lookup"><span data-stu-id="cd2d8-153">Example: 16777216</span></span>

<span data-ttu-id="cd2d8-154">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-158">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ description \\ \\ System \\ \\ DisplayController \\ \\ 0 \\ \\ identifier")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-159">Indique le type de carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="cd2d8-160">Jeu de caractères : alphanumérique</span><span class="sxs-lookup"><span data-stu-id="cd2d8-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="cd2d8-161">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-162">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-165">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-166">Indique le nombre réel de bits par pixel représentant l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="cd2d8-167">Elle peut être mise à l’échelle vers le paramètre vidéo actuel (représenté par la propriété ActualColorResolution) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="cd2d8-168">Exemple : 8</span><span class="sxs-lookup"><span data-stu-id="cd2d8-168">Example: 8</span></span>

<span data-ttu-id="cd2d8-169">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-170">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-173">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-174">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-174">Short textual description of the current object.</span></span>

<span data-ttu-id="cd2d8-175">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="cd2d8-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-176">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-179">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| ")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-180">Indique le nombre actuel de plans de couleurs utilisés dans l’affichage vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="cd2d8-181">Un plan de couleur est une autre façon de représenter les couleurs des pixels ; au lieu d’affecter une seule valeur RVB à chaque pixel, les plans de couleurs séparent le graphique dans chacun des composants de couleur primaire (rouge vert bleu) et les stockent dans leurs propres plans.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="cd2d8-182">Cela permet d’obtenir une plus grande profondeur de couleurs sur les systèmes vidéo 8 et 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="cd2d8-183">Les systèmes graphiques présentent un bitwidth suffisamment grand pour stocker les informations de profondeur de couleur, ce qui rend nécessaire un seul plan de couleurs.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="cd2d8-184">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="cd2d8-184">Example: 1</span></span>

<span data-ttu-id="cd2d8-185">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-186">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-189">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-190">Indique le nombre d’index de couleur dans une table de couleurs pour un affichage vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="cd2d8-191">Cette propriété est utilisée si l’appareil a une profondeur de couleur inférieure ou égale à 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="cd2d8-192">Pour les appareils dont la profondeur de couleur est supérieure, la valeur-1 est retournée.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="cd2d8-193">Exemple : 256</span><span class="sxs-lookup"><span data-stu-id="cd2d8-193">Example: 256</span></span>

<span data-ttu-id="cd2d8-194">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-195">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-198">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-198">Textual description of the current object.</span></span>

<span data-ttu-id="cd2d8-199">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="cd2d8-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-200">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-203">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-204">Indique le nombre actuel de stylets spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="cd2d8-205">La valeur 0xFFFFFFFF signifie que l’appareil ne prend pas en charge les stylets.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="cd2d8-206">Les stylets permettent de dessiner des lignes et des theborders d’objets polygones.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="cd2d8-207">Exemple : 3</span><span class="sxs-lookup"><span data-stu-id="cd2d8-207">Example: 3</span></span>

<span data-ttu-id="cd2d8-208">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-209">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-210">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-212">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-213">Indique la date et l’heure d’installation du pilote vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="cd2d8-214">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-216">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-218">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-219">Indique le nombre actuel de pixels dans le sens horizontal (axe X) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="cd2d8-220">Exemple : 1024</span><span class="sxs-lookup"><span data-stu-id="cd2d8-220">Example: 1024</span></span>

<span data-ttu-id="cd2d8-221">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-222">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-225">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-226">Spécifie le chemin d’accès au fichier. inf du pilote vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="cd2d8-227">Exemple : C : \\ \\ pilotes Windows system32 \\</span><span class="sxs-lookup"><span data-stu-id="cd2d8-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="cd2d8-228">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-229">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-232">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-233">Indique la section du fichier. inf où se trouvent les informations de vidéo Win32.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="cd2d8-234">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-235">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-238">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ Class \\ \\ Defaule \| DRV")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-239">Indique le nom du pilote vidéo installé.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="cd2d8-240">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-241">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-244">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-245">Indique le nom du fabricant du périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="cd2d8-246">Exemple : NEC</span><span class="sxs-lookup"><span data-stu-id="cd2d8-246">Example: NEC</span></span>

<span data-ttu-id="cd2d8-247">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-248">**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-251">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ description \\ \\ System \\ \\ MonitorPeripheral \\ \\ 0 \| identifier")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-252">Indique le nom du modèle du périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="cd2d8-253">Exemple : NEC 5FGp</span><span class="sxs-lookup"><span data-stu-id="cd2d8-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="cd2d8-254">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-255">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-258">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-259">Contient un nom d’identification pour la classe de configuration vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="cd2d8-260">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-261">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-262">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-264">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-265">Indique le nombre de pixels par pouce logique le long de l’axe X (sens horizontal) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="cd2d8-266">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-267">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-268">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-270">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-271">Indique le nombre de pixels par pouce logique le long de l’axe Y (direction verticale) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="cd2d8-272">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-273">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-274">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-276">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-277">Indique la fréquence d’actualisation de la configuration vidéo.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="cd2d8-278">Une valeur de 0 ou 1 indique qu’une fréquence par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="cd2d8-279">Exemple : 72</span><span class="sxs-lookup"><span data-stu-id="cd2d8-279">Example: 72</span></span>

<span data-ttu-id="cd2d8-280">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-281">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-284">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \| Device0 \| DefaultSettings. entrelacé")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-285">Indique si le périphérique d’affichage est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="cd2d8-286">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="cd2d8-287">**Non entrelacé** (« non entrelacé »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="cd2d8-288">**Entrelacé** (« entrelacé »)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd2d8-289">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-290">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-292">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unités**](../wmisdk/standard-qualifiers.md) ("millimètres")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-293">Spécifie la hauteur de l’écran physique.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="cd2d8-294">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-295">**Largeur**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-296">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-298">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unités**](../wmisdk/standard-qualifiers.md) ("millimètres")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-299">Spécifie la largeur de l’écran physique.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="cd2d8-300">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-304">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cd2d8-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-305">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="cd2d8-306">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="cd2d8-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-307">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-308">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-310">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-311">Indique le nombre actuel d’entrées d’index de couleurs réservées à l’utilisation du système.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="cd2d8-312">Cette valeur est uniquement valide pour les paramètres d’affichage qui utilisent une palette indexée.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="cd2d8-313">Les palettes indexées ne sont pas utilisées pour les profondeurs de couleurs supérieurs à 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="cd2d8-314">Si la profondeur de couleur est supérieure à 8 bits par pixel, cette valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="cd2d8-315">Exemple : 20</span><span class="sxs-lookup"><span data-stu-id="cd2d8-315">Example: 20</span></span>

<span data-ttu-id="cd2d8-316">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2d8-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2d8-318">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd2d8-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2d8-320">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")</span><span class="sxs-lookup"><span data-stu-id="cd2d8-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="cd2d8-321">Indique le nombre actuel de pixels dans le sens vertical (axe Y) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="cd2d8-322">Exemple : 768</span><span class="sxs-lookup"><span data-stu-id="cd2d8-322">Example: 768</span></span>

<span data-ttu-id="cd2d8-323">Cette propriété est dépréciée en faveur d’une ou plusieurs propriétés correspondantes contenues dans les [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md) et//ou CIM.</span><span class="sxs-lookup"><span data-stu-id="cd2d8-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd2d8-324">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd2d8-324">Requirements</span></span>



| <span data-ttu-id="cd2d8-325">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd2d8-325">Requirement</span></span> | <span data-ttu-id="cd2d8-326">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd2d8-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2d8-327">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd2d8-327">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2d8-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd2d8-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd2d8-329">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd2d8-329">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2d8-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd2d8-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd2d8-331">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd2d8-331">Namespace</span></span><br/>                | <span data-ttu-id="cd2d8-332">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cd2d8-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd2d8-333">MOF</span><span class="sxs-lookup"><span data-stu-id="cd2d8-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd2d8-334"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd2d8-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd2d8-335">DLL</span><span class="sxs-lookup"><span data-stu-id="cd2d8-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd2d8-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd2d8-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd2d8-337">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd2d8-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2d8-338">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="cd2d8-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
