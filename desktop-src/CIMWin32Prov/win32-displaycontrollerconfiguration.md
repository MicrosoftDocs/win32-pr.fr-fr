---
description: La \_ classe WMI DisplayControllerConfiguration WMI représente les informations de configuration de la carte vidéo d’un système informatique exécutant Windows.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Classe Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111219"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="7bbf7-103">\_Classe DisplayControllerConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="7bbf7-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="7bbf7-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DisplayControllerConfiguration** WMI représente les informations de configuration de la carte vidéo d’un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="7bbf7-105">Cette classe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-105">This class is obsolete.</span></span> <span data-ttu-id="7bbf7-106">À la place de cette classe, vous devez utiliser les propriétés des classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)et [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="7bbf7-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="7bbf7-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7bbf7-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbf7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bbf7-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="7bbf7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7bbf7-110">Members</span></span>

<span data-ttu-id="7bbf7-111">La classe **Win32 \_ DisplayControllerConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7bbf7-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="7bbf7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bbf7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bbf7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bbf7-113">Properties</span></span>

<span data-ttu-id="7bbf7-114">La classe **Win32 \_ DisplayControllerConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bbf7-115">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-118">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-119">Le nombre de bits utilisés pour représenter la couleur dans cette configuration, ou les bits dans chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="7bbf7-120">Exemple : 8</span><span class="sxs-lookup"><span data-stu-id="7bbf7-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-124">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7bbf7-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-125">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-125">Short textual description of the current object.</span></span>

<span data-ttu-id="7bbf7-126">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7bbf7-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-127">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-130">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api des \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| ")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-131">Nombre actuel de plans de couleurs utilisés dans la configuration de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="7bbf7-132">Un plan de couleur est une autre façon de représenter les couleurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="7bbf7-133">Au lieu d’affecter une seule valeur RVB à chaque pixel, les plans de couleurs séparent le graphique dans chacun des composants de couleur primaire (rouge, vert, bleu) et les stocke dans leurs propres plans.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="7bbf7-134">Cela permet d’obtenir une plus grande profondeur de couleurs sur les systèmes vidéo 8 bits et 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="7bbf7-135">Les systèmes graphiques présentent un bitwidth suffisamment grand pour stocker les informations de profondeur de couleur, ce qui signifie qu’un seul plan de couleur est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="7bbf7-136">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="7bbf7-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-140">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-140">Textual description of the current object.</span></span>

<span data-ttu-id="7bbf7-141">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7bbf7-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-142">**DeviceEntriesInAColorTable**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-145">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-146">Nombre d’index de couleurs dans une table des couleurs d’un périphérique d’affichage (si l’appareil a une profondeur de couleur inférieure ou égale à 8 bits par pixel).</span><span class="sxs-lookup"><span data-stu-id="7bbf7-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="7bbf7-147">Pour les appareils dont la profondeur de couleur est supérieure, la valeur-1 est retournée.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="7bbf7-148">Exemple : 256</span><span class="sxs-lookup"><span data-stu-id="7bbf7-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-149">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-152">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-153">Nombre actuel de stylets spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-153">Current number of device-specific pens.</span></span> <span data-ttu-id="7bbf7-154">La valeur 0xFFFFFFFF signifie que l’appareil ne prend pas en charge les stylets.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="7bbf7-155">Les stylets sont des propriétés logiques qui peuvent être attribuées par le contrôleur d’affichage pour afficher des appareils, et sont utilisées pour dessiner des lignes, des bordures de polygones et du texte.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="7bbf7-156">Exemple : 3</span><span class="sxs-lookup"><span data-stu-id="7bbf7-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-158">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-160">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-161">Nombre actuel de pixels dans le sens horizontal (axe x) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="7bbf7-162">Exemple : 1024</span><span class="sxs-lookup"><span data-stu-id="7bbf7-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-163">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-166">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="7bbf7-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-167">Nom de l’adaptateur utilisé dans cette configuration.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-168">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-169">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-171">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-172">Fréquence d’actualisation de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="7bbf7-173">La valeur 0 (zéro) ou 1 (un) indique qu’une fréquence par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="7bbf7-174">La valeur-1 indique qu’un taux optimal est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="7bbf7-175">Exemple : 72</span><span class="sxs-lookup"><span data-stu-id="7bbf7-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-176">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-179">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-180">Nombre actuel d’entrées d’index de couleurs réservées à l’utilisation du système.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="7bbf7-181">Cette valeur est uniquement valide pour les paramètres d’affichage qui utilisent une palette indexée.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="7bbf7-182">Les palettes indexées ne sont pas utilisées pour les profondeurs de couleurs supérieurs à 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="7bbf7-183">Si la profondeur de couleur est supérieure à 8 bits par pixel, cette valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="7bbf7-184">Exemple : 20</span><span class="sxs-lookup"><span data-stu-id="7bbf7-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-188">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7bbf7-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-189">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="7bbf7-190">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7bbf7-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-191">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-192">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-194">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-195">Nombre actuel d’entrées d’index de couleurs réservées à l’utilisation du système.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="7bbf7-196">Cette valeur est uniquement valide pour les paramètres d’affichage qui utilisent une palette indexée.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="7bbf7-197">Les palettes indexées ne sont pas utilisées pour les profondeurs de couleurs supérieurs à 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="7bbf7-198">Si la profondeur de couleur est supérieure à 8 bits par pixel, cette valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="7bbf7-199">Exemple : 20</span><span class="sxs-lookup"><span data-stu-id="7bbf7-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-203">Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| fonctions de contexte de périphérique \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="7bbf7-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-204">Nombre actuel de pixels dans le sens vertical (axe y) de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="7bbf7-205">Exemple : 768</span><span class="sxs-lookup"><span data-stu-id="7bbf7-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="7bbf7-206">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bbf7-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7bbf7-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bbf7-209">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="7bbf7-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7bbf7-210">Description lisible par l’utilisateur de la résolution d’écran actuelle et du paramètre de couleur de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7bbf7-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="7bbf7-211">Exemple : « 1024 768 avec 256 couleurs »</span><span class="sxs-lookup"><span data-stu-id="7bbf7-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bbf7-212">Notes</span><span class="sxs-lookup"><span data-stu-id="7bbf7-212">Remarks</span></span>

<span data-ttu-id="7bbf7-213">La classe **Win32 \_ DisplayControllerConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7bbf7-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbf7-214">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bbf7-214">Requirements</span></span>



| <span data-ttu-id="7bbf7-215">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bbf7-215">Requirement</span></span> | <span data-ttu-id="7bbf7-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bbf7-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbf7-217">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bbf7-217">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbf7-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bbf7-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bbf7-219">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bbf7-219">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbf7-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bbf7-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bbf7-221">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7bbf7-221">Namespace</span></span><br/>                | <span data-ttu-id="7bbf7-222">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7bbf7-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bbf7-223">MOF</span><span class="sxs-lookup"><span data-stu-id="7bbf7-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bbf7-224"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf7-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bbf7-225">DLL</span><span class="sxs-lookup"><span data-stu-id="7bbf7-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bbf7-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf7-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbf7-227">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bbf7-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbf7-228">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="7bbf7-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="7bbf7-229">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="7bbf7-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

