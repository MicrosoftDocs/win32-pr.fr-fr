---
description: La \_ classe WMI Win32 PrinterConfiguration représente la configuration d’un périphérique d’impression. Cela comprend des fonctionnalités telles que la résolution, la couleur, les polices et l’orientation.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Classe Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950757"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="fc77c-104">\_Classe PrinterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="fc77c-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="fc77c-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PrinterConfiguration** représente la configuration d’un périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="fc77c-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="fc77c-106">Cela comprend des fonctionnalités telles que la résolution, la couleur, les polices et l’orientation.</span><span class="sxs-lookup"><span data-stu-id="fc77c-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="fc77c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fc77c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fc77c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fc77c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc77c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc77c-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="fc77c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="fc77c-110">Members</span></span>

<span data-ttu-id="fc77c-111">La classe **Win32 \_ PrinterConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fc77c-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="fc77c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc77c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc77c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc77c-113">Properties</span></span>

<span data-ttu-id="fc77c-114">La classe **Win32 \_ PrinterConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc77c-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc77c-115">**BitsPerPel**</span><span class="sxs-lookup"><span data-stu-id="fc77c-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-118">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc77c-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-119">Nombre de bits utilisés pour représenter la couleur dans cette configuration (bits par pixel).</span><span class="sxs-lookup"><span data-stu-id="fc77c-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="fc77c-120">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fc77c-120">This property is obsolete.</span></span> <span data-ttu-id="fc77c-121">Utilisez plutôt des propriétés dans les classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) pour déterminer comment la couleur est représentée.</span><span class="sxs-lookup"><span data-stu-id="fc77c-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fc77c-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-125">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="fc77c-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-126">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="fc77c-126">Short textual description of the current object.</span></span>

<span data-ttu-id="fc77c-127">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc77c-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-128">**Copies assemblées**</span><span class="sxs-lookup"><span data-stu-id="fc77c-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fc77c-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-131">Si la **valeur est true**, les pages imprimées doivent être assemblées.</span><span class="sxs-lookup"><span data-stu-id="fc77c-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="fc77c-132">Pour assembler est d’imprimer l’intégralité du document avant d’imprimer la copie suivante, au lieu d’imprimer chaque page du document le nombre de fois requis.</span><span class="sxs-lookup"><span data-stu-id="fc77c-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="fc77c-133">Cette propriété est ignorée sauf si le pilote d’imprimante indique la prise en charge du classement.</span><span class="sxs-lookup"><span data-stu-id="fc77c-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-134">**Color**</span><span class="sxs-lookup"><span data-stu-id="fc77c-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-137">Couleur du document.</span><span class="sxs-lookup"><span data-stu-id="fc77c-137">Color of the document.</span></span> <span data-ttu-id="fc77c-138">Certaines imprimantes couleur ont la possibilité d’imprimer à l’aide d’un vrai noir au lieu d’une combinaison de cyan, magenta et jaune (CMJ).</span><span class="sxs-lookup"><span data-stu-id="fc77c-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="fc77c-139">Cela crée généralement un texte plus sombre et plus clair pour les documents.</span><span class="sxs-lookup"><span data-stu-id="fc77c-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="fc77c-140">Cette option est utile uniquement pour les imprimantes couleur qui prennent en charge l’impression noir.</span><span class="sxs-lookup"><span data-stu-id="fc77c-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc77c-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-142">Monochrome (vrai noir)</span><span class="sxs-lookup"><span data-stu-id="fc77c-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc77c-143"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-144">Couleur</span><span class="sxs-lookup"><span data-stu-id="fc77c-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-145">**Copies**</span><span class="sxs-lookup"><span data-stu-id="fc77c-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-148">Nombre de copies à imprimer.</span><span class="sxs-lookup"><span data-stu-id="fc77c-148">Number of copies to be printed.</span></span> <span data-ttu-id="fc77c-149">Le pilote d’imprimante doit prendre en charge l’impression de copies à plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="fc77c-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="fc77c-150">Exemple : 2</span><span class="sxs-lookup"><span data-stu-id="fc77c-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-151">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc77c-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-154">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="fc77c-154">Textual description of the current object.</span></span>

<span data-ttu-id="fc77c-155">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc77c-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="fc77c-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-159">Nom convivial de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="fc77c-159">Friendly name of the printer.</span></span> <span data-ttu-id="fc77c-160">Ce nom est unique pour le type d’imprimante et peut être tronqué en raison des limitations de la chaîne à partir de laquelle il est dérivé.</span><span class="sxs-lookup"><span data-stu-id="fc77c-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="fc77c-161">Exemple : « PCL/HP LaserJet »</span><span class="sxs-lookup"><span data-stu-id="fc77c-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-162">**DisplayFlags**</span><span class="sxs-lookup"><span data-stu-id="fc77c-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-165">Indique si le périphérique d’affichage est de couleur ou monochrome et si le type d’analyse est non entrelacé ou entrelacé.</span><span class="sxs-lookup"><span data-stu-id="fc77c-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="fc77c-166">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fc77c-166">This property is obsolete.</span></span> <span data-ttu-id="fc77c-167">Utilisez plutôt des propriétés d’affichage telles que la propriété **DisplayType** de la classe **Win32 \_ desktopmonitor** .</span><span class="sxs-lookup"><span data-stu-id="fc77c-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-168">**DisplayFrequency**</span><span class="sxs-lookup"><span data-stu-id="fc77c-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-169">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-171">Affiche la fréquence de rafraîchissement verticale.</span><span class="sxs-lookup"><span data-stu-id="fc77c-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="fc77c-172">La fréquence d’actualisation d’une analyse est le nombre de fois où l’écran est redessiné par seconde (fréquence).</span><span class="sxs-lookup"><span data-stu-id="fc77c-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="fc77c-173">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fc77c-173">This property is obsolete.</span></span> <span data-ttu-id="fc77c-174">Au lieu de cela, utilisez les propriétés de la classe [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="fc77c-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-175">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="fc77c-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-176">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-178">Type de trame de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="fc77c-178">Dither type of the printer.</span></span> <span data-ttu-id="fc77c-179">Cette propriété peut supposer des valeurs prédéfinies de 1 à 5, ou des valeurs définies par le pilote comprises entre 6 et 256.</span><span class="sxs-lookup"><span data-stu-id="fc77c-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="fc77c-180">Le tramage en ligne est une méthode de tramage spéciale qui produit des bordures bien définies entre les mises à l’échelle en noir, blanc et gris.</span><span class="sxs-lookup"><span data-stu-id="fc77c-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="fc77c-181">Elle ne convient pas aux images qui incluent des diplômes continus en intensité et en teinte, tels que des photographies numérisées.</span><span class="sxs-lookup"><span data-stu-id="fc77c-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc77c-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-183">Aucun tramage</span><span class="sxs-lookup"><span data-stu-id="fc77c-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc77c-184"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-185">Pinceau épais</span><span class="sxs-lookup"><span data-stu-id="fc77c-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="fc77c-186"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="fc77c-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-187">Pinceau fin</span><span class="sxs-lookup"><span data-stu-id="fc77c-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="fc77c-188"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="fc77c-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-189">Art en ligne</span><span class="sxs-lookup"><span data-stu-id="fc77c-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="fc77c-190"><span id="5"></span>**5,5**</span><span class="sxs-lookup"><span data-stu-id="fc77c-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-191">Grayscale (Nuances de gris)</span><span class="sxs-lookup"><span data-stu-id="fc77c-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-192">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="fc77c-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-195">Numéro de version du pilote d’imprimante Windows.</span><span class="sxs-lookup"><span data-stu-id="fc77c-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="fc77c-196">Les numéros de version sont créés et gérés par le fabricant du pilote.</span><span class="sxs-lookup"><span data-stu-id="fc77c-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-197">**Duplex**</span><span class="sxs-lookup"><span data-stu-id="fc77c-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-198">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fc77c-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-200">Si la **valeur est true**, l’impression est effectuée des deux côtés.</span><span class="sxs-lookup"><span data-stu-id="fc77c-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="fc77c-201">Si la **valeur est false**, l’impression est effectuée sur un seul côté du média.</span><span class="sxs-lookup"><span data-stu-id="fc77c-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-202">**NomFormulaire**</span><span class="sxs-lookup"><span data-stu-id="fc77c-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-205">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc77c-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="fc77c-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-209">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (points par pouce)</span><span class="sxs-lookup"><span data-stu-id="fc77c-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-210">Résolution d’impression en points par pouce le long de l’axe x (largeur) du travail d’impression (similaire à la propriété **XResolution** obsolète).</span><span class="sxs-lookup"><span data-stu-id="fc77c-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="fc77c-211">Cette valeur est définie uniquement lorsque la propriété **PrintQuality** de cette classe est positive.</span><span class="sxs-lookup"><span data-stu-id="fc77c-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-212">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="fc77c-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-213">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-215">Valeur spécifique de l’une des trois méthodes de correspondance des couleurs possibles (appelées intentions) qui doit être utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc77c-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="fc77c-216">Les applications ICM établissent des intentions à l’aide des fonctions ICM.</span><span class="sxs-lookup"><span data-stu-id="fc77c-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="fc77c-217">Cette propriété peut supposer des valeurs prédéfinies de 1 à 3, ou des valeurs définies par le pilote, comprises entre 4 et 256.</span><span class="sxs-lookup"><span data-stu-id="fc77c-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="fc77c-218">Les applications non-ICM peuvent utiliser cette valeur pour déterminer comment l’imprimante gère les travaux d’impression couleur.</span><span class="sxs-lookup"><span data-stu-id="fc77c-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc77c-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-220">Saturation</span><span class="sxs-lookup"><span data-stu-id="fc77c-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc77c-221"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-222">Comparez</span><span class="sxs-lookup"><span data-stu-id="fc77c-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="fc77c-223"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="fc77c-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-224">Couleur exacte</span><span class="sxs-lookup"><span data-stu-id="fc77c-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-225">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="fc77c-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-226">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-228">Mode de gestion de l’ICM.</span><span class="sxs-lookup"><span data-stu-id="fc77c-228">How ICM is handled.</span></span> <span data-ttu-id="fc77c-229">Pour une application non-ICM, cette propriété détermine si ICM est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="fc77c-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="fc77c-230">Pour les applications ICM, le système examine cette propriété pour déterminer quelle partie du système d’ordinateur gère la prise en charge d’ICM.</span><span class="sxs-lookup"><span data-stu-id="fc77c-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc77c-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-232">Désactivé</span><span class="sxs-lookup"><span data-stu-id="fc77c-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc77c-233"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-234">Windows</span><span class="sxs-lookup"><span data-stu-id="fc77c-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="fc77c-235"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="fc77c-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-236">Pilote de périphérique</span><span class="sxs-lookup"><span data-stu-id="fc77c-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="fc77c-237"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="fc77c-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-238">Appareil</span><span class="sxs-lookup"><span data-stu-id="fc77c-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-239">**LogPixels**</span><span class="sxs-lookup"><span data-stu-id="fc77c-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-240">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-242">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc77c-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-243">Nombre de pixels par pouce logique.</span><span class="sxs-lookup"><span data-stu-id="fc77c-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="fc77c-244">Cette propriété obsolète est valide uniquement avec les appareils qui fonctionnent avec des pixels, ce qui exclut les appareils tels que les imprimantes.</span><span class="sxs-lookup"><span data-stu-id="fc77c-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="fc77c-245">Aucune valeur de remplacement ne s’applique aux imprimantes.</span><span class="sxs-lookup"><span data-stu-id="fc77c-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-246">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="fc77c-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-247">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-249">Type de support sur lequel l’imprimante imprime.</span><span class="sxs-lookup"><span data-stu-id="fc77c-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="fc77c-250">La propriété peut être définie sur une valeur prédéfinie ou sur une valeur définie par le pilote supérieure ou égale à 256.</span><span class="sxs-lookup"><span data-stu-id="fc77c-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc77c-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-252">standard</span><span class="sxs-lookup"><span data-stu-id="fc77c-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc77c-253"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-254">Transparence</span><span class="sxs-lookup"><span data-stu-id="fc77c-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="fc77c-255"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="fc77c-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-256">Brillance</span><span class="sxs-lookup"><span data-stu-id="fc77c-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-257">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fc77c-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-260">Qualificateurs : [**clé**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="fc77c-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-261">Nom de l’imprimante à laquelle cette configuration est associée.</span><span class="sxs-lookup"><span data-stu-id="fc77c-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="fc77c-262">Cette valeur correspond à la propriété **Name** de l’instance d' [**\_ imprimante Win32**](win32-printer.md) associée.</span><span class="sxs-lookup"><span data-stu-id="fc77c-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-263">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="fc77c-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-264">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-266">Impression de l’orientation du papier.</span><span class="sxs-lookup"><span data-stu-id="fc77c-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="fc77c-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-268">Portrait</span><span class="sxs-lookup"><span data-stu-id="fc77c-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fc77c-269"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-270">Paysage</span><span class="sxs-lookup"><span data-stu-id="fc77c-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-271">**PaperLength**</span><span class="sxs-lookup"><span data-stu-id="fc77c-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-272">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-274">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (dixièmes de millimètre)</span><span class="sxs-lookup"><span data-stu-id="fc77c-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-275">Longueur du papier.</span><span class="sxs-lookup"><span data-stu-id="fc77c-275">Length of the paper.</span></span> <span data-ttu-id="fc77c-276">Pour déterminer la taille du papier en pouces, divisez cette valeur par 254.</span><span class="sxs-lookup"><span data-stu-id="fc77c-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="fc77c-277">Exemple : 2794</span><span class="sxs-lookup"><span data-stu-id="fc77c-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-278">**PaperSize**</span><span class="sxs-lookup"><span data-stu-id="fc77c-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-281">Taille du papier.</span><span class="sxs-lookup"><span data-stu-id="fc77c-281">Size of the paper.</span></span> <span data-ttu-id="fc77c-282">Les tailles possibles se trouvent dans la propriété **PaperSizesSupported** de la classe [**\_ Printer Win32**](win32-printer.md) associée.</span><span class="sxs-lookup"><span data-stu-id="fc77c-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="fc77c-283">Exemple : « a4 ou lettre ».</span><span class="sxs-lookup"><span data-stu-id="fc77c-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-284">**PaperWidth**</span><span class="sxs-lookup"><span data-stu-id="fc77c-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-287">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (dixièmes de millimètre)</span><span class="sxs-lookup"><span data-stu-id="fc77c-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-288">Largeur du papier.</span><span class="sxs-lookup"><span data-stu-id="fc77c-288">Width of the paper.</span></span> <span data-ttu-id="fc77c-289">Pour déterminer la taille du papier en pouces, divisez cette valeur par 254.</span><span class="sxs-lookup"><span data-stu-id="fc77c-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="fc77c-290">Exemple : 2159</span><span class="sxs-lookup"><span data-stu-id="fc77c-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-291">**PelsHeight**</span><span class="sxs-lookup"><span data-stu-id="fc77c-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-292">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-294">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc77c-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-295">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fc77c-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-296">**PelsWidth**</span><span class="sxs-lookup"><span data-stu-id="fc77c-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-297">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-299">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc77c-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-300">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fc77c-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="fc77c-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-302">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-304">Un des quatre niveaux de qualité du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="fc77c-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="fc77c-305">Si une valeur positive est spécifiée, la qualité est mesurée en points par pouce.</span><span class="sxs-lookup"><span data-stu-id="fc77c-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="fc77c-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="fc77c-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-307">Brouillon</span><span class="sxs-lookup"><span data-stu-id="fc77c-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="fc77c-308"><span id="-2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fc77c-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-309">Faible</span><span class="sxs-lookup"><span data-stu-id="fc77c-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="fc77c-310"><span id="-3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="fc77c-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-311">Moyenne</span><span class="sxs-lookup"><span data-stu-id="fc77c-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="fc77c-312"><span id="-4"></span>**-4**</span><span class="sxs-lookup"><span data-stu-id="fc77c-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-313">Élevé</span><span class="sxs-lookup"><span data-stu-id="fc77c-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-314">**Mise à l’échelle**</span><span class="sxs-lookup"><span data-stu-id="fc77c-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-315">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-317">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="fc77c-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-318">Facteur par lequel la sortie imprimée doit être mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="fc77c-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="fc77c-319">Par exemple, une échelle de 75 réduit la sortie d’impression à 3/4 de sa hauteur et de sa largeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="fc77c-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="fc77c-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fc77c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-323">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="fc77c-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-324">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="fc77c-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="fc77c-325">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc77c-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-326">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="fc77c-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-327">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-329">Numéro de version des données d’initialisation pour l’appareil associé à l’imprimante Windows.</span><span class="sxs-lookup"><span data-stu-id="fc77c-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-330">**TTOption**</span><span class="sxs-lookup"><span data-stu-id="fc77c-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-331">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-333">Indique comment les polices TrueType doivent être imprimées.</span><span class="sxs-lookup"><span data-stu-id="fc77c-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="fc77c-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span><span class="sxs-lookup"><span data-stu-id="fc77c-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-335">Imprime les polices TrueType en tant que graphiques.</span><span class="sxs-lookup"><span data-stu-id="fc77c-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="fc77c-336">Il s’agit de l’action par défaut pour les imprimantes matricielles.</span><span class="sxs-lookup"><span data-stu-id="fc77c-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="fc77c-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Télécharger** (2)</span><span class="sxs-lookup"><span data-stu-id="fc77c-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-338">Télécharge les polices TrueType en tant que polices logicielles.</span><span class="sxs-lookup"><span data-stu-id="fc77c-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="fc77c-339">Il s’agit de l’action par défaut pour les imprimantes qui utilisent le langage de contrôle d’imprimante (PCL).</span><span class="sxs-lookup"><span data-stu-id="fc77c-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="fc77c-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Remplacer** (3)</span><span class="sxs-lookup"><span data-stu-id="fc77c-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc77c-341">Remplace les polices de l’appareil par des polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="fc77c-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="fc77c-342">Il s’agit de l’action par défaut pour les imprimantes PostScript.</span><span class="sxs-lookup"><span data-stu-id="fc77c-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc77c-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="fc77c-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-344">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-346">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (points par pouce)</span><span class="sxs-lookup"><span data-stu-id="fc77c-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-347">Résolution d’impression le long de l’axe y (hauteur) du travail d’impression (similaire à la propriété **YResolution** obsolète).</span><span class="sxs-lookup"><span data-stu-id="fc77c-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="fc77c-348">Cette valeur est définie uniquement lorsque la propriété **PrintQuality** de cette classe est positive.</span><span class="sxs-lookup"><span data-stu-id="fc77c-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-349">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="fc77c-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-350">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-352">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc77c-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-353">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fc77c-353">This property is obsolete.</span></span> <span data-ttu-id="fc77c-354">Utilisez la propriété **HorizontalResolution** à la place.</span><span class="sxs-lookup"><span data-stu-id="fc77c-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="fc77c-355">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="fc77c-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc77c-356">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc77c-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc77c-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc77c-358">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fc77c-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fc77c-359">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fc77c-359">This property is obsolete.</span></span> <span data-ttu-id="fc77c-360">Utilisez plutôt la propriété **VerticalResolution** .</span><span class="sxs-lookup"><span data-stu-id="fc77c-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc77c-361">Notes</span><span class="sxs-lookup"><span data-stu-id="fc77c-361">Remarks</span></span>

<span data-ttu-id="fc77c-362">La classe **Win32 \_ PrinterConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fc77c-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="fc77c-363">**Vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="fc77c-363">**Overview**</span></span>

<span data-ttu-id="fc77c-364">Avant de pouvoir déterminer comment distribuer et utiliser au mieux vos ressources d’impression, vous devez avoir une connaissance détaillée de ces ressources.</span><span class="sxs-lookup"><span data-stu-id="fc77c-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="fc77c-365">Par exemple, le service A peut avoir seulement trois imprimantes par rapport à cinq imprimantes dans le département B. Toutefois, si les imprimantes du service A peuvent imprimer 20 pages par minute et que les imprimantes du département B peuvent imprimer seulement 5 pages par minute, les utilisateurs du service A ont en fait davantage de capacité d’impression.</span><span class="sxs-lookup"><span data-stu-id="fc77c-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="fc77c-366">Sans connaître les fonctionnalités détaillées de ces imprimantes, vous pouvez conclure par erreur que le service A est limité à la capacité d’impression et, par conséquent, acheter des imprimantes supplémentaires qui finissent par ne plus être utilisées.</span><span class="sxs-lookup"><span data-stu-id="fc77c-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="fc77c-367">WMI comprend deux classes, [**Win32 \_ Printer**](win32-printer.md) et **Win32 \_ PrinterConfiguration**, qui peuvent être utilisées pour retourner des informations détaillées sur toutes les imprimantes installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fc77c-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="fc77c-368">Exemples</span><span class="sxs-lookup"><span data-stu-id="fc77c-368">Examples</span></span>

<span data-ttu-id="fc77c-369">L’exemple de code suivant récupère des informations sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="fc77c-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="fc77c-370">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc77c-370">Requirements</span></span>



| <span data-ttu-id="fc77c-371">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc77c-371">Requirement</span></span> | <span data-ttu-id="fc77c-372">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc77c-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc77c-373">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc77c-373">Minimum supported client</span></span><br/> | <span data-ttu-id="fc77c-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc77c-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="fc77c-375">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc77c-375">Minimum supported server</span></span><br/> | <span data-ttu-id="fc77c-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc77c-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="fc77c-377">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fc77c-377">Namespace</span></span><br/>                | <span data-ttu-id="fc77c-378">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fc77c-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="fc77c-379">MOF</span><span class="sxs-lookup"><span data-stu-id="fc77c-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc77c-380"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc77c-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc77c-381">DLL</span><span class="sxs-lookup"><span data-stu-id="fc77c-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc77c-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc77c-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fc77c-383">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc77c-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc77c-384">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="fc77c-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="fc77c-385">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="fc77c-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
