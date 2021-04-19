---
description: Les constantes suivantes spécifient le jeu valide de propriétés d’élément du scanneur WIA (Windows Image Acquisition).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Constantes de propriété d’élément WIA du scanneur (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544672"
---
# <a name="scanner-wia-item-property-constants"></a><span data-ttu-id="e1cbf-103">Constantes de propriété d’élément WIA du scanneur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-103">Scanner WIA Item Property Constants</span></span>

<span data-ttu-id="e1cbf-104">Les constantes suivantes spécifient le jeu valide de propriétés d’élément du scanneur WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-104">The following constants specify the valid set of Windows Image Acquisition (WIA) scanner item properties.</span></span>

<span data-ttu-id="e1cbf-105">Le préfixe « WIA \_ IPS \_ » indique une propriété d’élément pour les périphériques de scanneur et est la Convention d’affectation de noms utilisée dans C/C++.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-105">The prefix "WIA\_IPS\_" indicates an Item Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="e1cbf-106">À des fins de script, ces constantes utilisent le préfixe « ScannerPicture » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-106">For scripting purposes these constants use the prefix "ScannerPicture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="e1cbf-107">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e1cbf-108">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e1cbf-109">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <span data-ttu-id="e1cbf-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-111">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-111">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="e1cbf-112">Active ou désactive la réalignement automatique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-112">Turns automatic deskew on or off.</span></span><br/> <span data-ttu-id="e1cbf-113">Facultatif pour WIA_CATEGORY_FEEDER uniquement.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-113">Optional for WIA_CATEGORY_FEEDER only.</span></span><br/> <span data-ttu-id="e1cbf-114">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-114">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="e1cbf-115">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-115">The following table has the constants that are valid with this property.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-116">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-116">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-117">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-118">WIA_AUTO_DESKEW_ON</span><span class="sxs-lookup"><span data-stu-id="e1cbf-118">WIA_AUTO_DESKEW_ON</span></span></td>
<td><span data-ttu-id="e1cbf-119">Activez la réalignement automatique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-119">Turn on automatic deskew.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-120">WIA_AUTO_DESKEW_OFF</span><span class="sxs-lookup"><span data-stu-id="e1cbf-120">WIA_AUTO_DESKEW_OFF</span></span></td>
<td><span data-ttu-id="e1cbf-121">Désactivez la réalignement automatique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-121">Turn off automatic deskew.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <span data-ttu-id="e1cbf-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-123">Valeurs de luminosité de l’image disponibles dans le scanneur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-123">The image brightness values available within the scanner.</span></span></p>
<p><span data-ttu-id="e1cbf-124">Contient le paramètre de luminosité matérielle actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-124">Contains the current hardware brightness setting for the device.</span></span> <span data-ttu-id="e1cbf-125">Une application définit cette propriété sur la valeur de luminosité du matériel.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-125">An application sets this property to the hardware's brightness value.</span></span> <span data-ttu-id="e1cbf-126">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-126">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-127">Les valeurs doivent être mappées dans une plage comprise entre-1000 et 1000, où 1000 correspond à la luminosité maximale, 0 correspond à la luminosité normale et-1000 correspond à la luminosité minimale.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-127">Values should be mapped in a range from -1000 through 1000, where 1000 corresponds to the maximum brightness, 0 corresponds to normal brightness, and -1000 corresponds to the minimum brightness.</span></span></p>
<p><span data-ttu-id="e1cbf-128">Obligatoire pour tous les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-128">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-129">Facultatif, mais recommandé, pour les éléments de WIA_CATEGORY_FINISHED_FILE prenant en charge les aperçus.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-129">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="e1cbf-130">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-130">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <span data-ttu-id="e1cbf-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-132">Contient le paramètre de contraste matériel actuel pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-132">Contains the current hardware contrast setting for a device.</span></span> <span data-ttu-id="e1cbf-133">Une application définit cette propriété sur la valeur de contraste du matériel.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-133">An application sets this property to the hardware's contrast value.</span></span> <span data-ttu-id="e1cbf-134">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-134">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-135">Les valeurs doivent être mappées dans une plage comprise entre-1000 et 1000, où-1000 correspond au contraste minimal, 0 correspond au contraste normal et 1000 correspond au contraste maximal.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-135">Values should be mapped in a range from -1000 through 1000, where -1000 corresponds to the minimum contrast, 0 corresponds to normal contrast, and 1000 corresponds to the maximum contrast.</span></span></p>
<p><span data-ttu-id="e1cbf-136">Obligatoire pour tous les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-136">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-137">Facultatif, mais recommandé, pour les éléments de WIA_CATEGORY_FINISHED_FILE prenant en charge les aperçus.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-137">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="e1cbf-138">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-138">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <span data-ttu-id="e1cbf-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-140">Contient les paramètres d’intention actuels.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-140">Contains the current intent settings.</span></span> <span data-ttu-id="e1cbf-141">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-141">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-142">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-142">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-143">Elle n’est pas prise en charge pour les éléments WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-143">It is not supported for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-144">Type : <strong>VT_I4</strong> accès : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-144">Type: <strong>VT_I4</strong> Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span></span></p>
<p><span data-ttu-id="e1cbf-145">Le pilote les utilise pour prédéfinir les propriétés d’élément en fonction de l’utilisation prévue de l’image par une application.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-145">The driver uses these to preset item properties based on an application's intended use of the image.</span></span> <span data-ttu-id="e1cbf-146">Cela peut inclure, par exemple, la qualité maximale, la taille minimale, etc.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-146">This might include, for example, maximum quality, minimum size, and so on.</span></span></p>
<p><span data-ttu-id="e1cbf-147">Le pilote choisit la profondeur de bit, en points par pouce, et d’autres paramètres qu’il détermine sont appropriés pour l’intention sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-147">The driver chooses the bit depth, in dots per inch, and other settings that it determines are appropriate for the selected intent.</span></span> <span data-ttu-id="e1cbf-148">Il revient à l’application de lire les paramètres actuels pour déterminer les propriétés qui ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-148">It is up to the application to read the current settings to determine which properties were changed.</span></span> <span data-ttu-id="e1cbf-149">Une application définit cette propriété pour définir automatiquement les propriétés WIA pour une intention d’acquisition spécifique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-149">An application sets this property to auto-set the WIA properties for specific acquisition intent.</span></span> <span data-ttu-id="e1cbf-150">Cette propriété est obligatoire pour tous les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-150">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="e1cbf-151">Une application définit cette propriété pour définir automatiquement les propriétés WIA pour une intention d’acquisition spécifique</span><span class="sxs-lookup"><span data-stu-id="e1cbf-151">An application sets this property to auto-set the WIA properties for specific acquisition intent</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-152">Les indicateurs peuvent être combinés avec <strong>un opérateur or</strong> au niveau du bit, mais une image ne peut pas être à la fois des nuances de gris et des couleurs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-152">The flags can be combined with a bitwise <strong>OR</strong> operator, but an image cannot be both grayscale and color.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-153">Cette propriété est obligatoire pour tous les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-153">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="e1cbf-154">Le tableau suivant contient les indicateurs de type image et leurs définitions.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-154">The following table contains the image-type flags and their definitions.</span></span> <span data-ttu-id="e1cbf-155">Ces indicateurs permettent de définir le type d’image prévu : couleur, nuances de gris, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-155">These flags are used to set which type of image is intended: color, grayscale, and so on.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-156">Indicateurs de type d’image prévu</span><span class="sxs-lookup"><span data-stu-id="e1cbf-156">Intended image type flags</span></span></th>
<th><span data-ttu-id="e1cbf-157">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-158">WIA_INTENT_NONE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-158">WIA_INTENT_NONE</span></span></td>
<td><span data-ttu-id="e1cbf-159">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-159">Default value.</span></span> <span data-ttu-id="e1cbf-160">Aucun objectif n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-160">No intent is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-161">WIA_INTENT_IMAGE_TYPE_COLOR</span><span class="sxs-lookup"><span data-stu-id="e1cbf-161">WIA_INTENT_IMAGE_TYPE_COLOR</span></span></td>
<td><span data-ttu-id="e1cbf-162">L’application envisage de préparer l’appareil pour une analyse des couleurs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-162">The application intends to prepare the device for a color scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span></span></td>
<td><span data-ttu-id="e1cbf-164">L’application envisage de préparer l’appareil pour une analyse en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-164">The application intends to prepare the device for a grayscale scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-165">WIA_INTENT_IMAGE_TYPE_TEXT</span><span class="sxs-lookup"><span data-stu-id="e1cbf-165">WIA_INTENT_IMAGE_TYPE_TEXT</span></span></td>
<td><span data-ttu-id="e1cbf-166">L’application envisage de préparer l’appareil pour l’analyse du texte.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-166">The application intends to prepare the device for scanning text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-167">WIA_INTENT_IMAGE_TYPE_MASK</span><span class="sxs-lookup"><span data-stu-id="e1cbf-167">WIA_INTENT_IMAGE_TYPE_MASK</span></span></td>
<td><span data-ttu-id="e1cbf-168">Masque pour tous les indicateurs de type image.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-168">Mask for all of the image-type flags.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="e1cbf-169">Le tableau suivant contient les indicateurs de qualité et de taille et leurs définitions.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-169">The following table contains the quality and size flags and their definitions.</span></span> <span data-ttu-id="e1cbf-170">Ces indicateurs sont utilisés pour définir le niveau de qualité souhaité.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-170">These flags are used to set which level of quality is intended.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-171">Indicateurs de qualité/taille d’image prévus</span><span class="sxs-lookup"><span data-stu-id="e1cbf-171">Intended image size/quality flags</span></span></th>
<th><span data-ttu-id="e1cbf-172">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-172">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-173">WIA_INTENT_MINIMIZE_SIZE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-173">WIA_INTENT_MINIMIZE_SIZE</span></span></td>
<td><span data-ttu-id="e1cbf-174">L’application envisage de préparer l’appareil pour l’analyse d’une image qui résulte dans une analyse de petite taille.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-174">The application intends to prepare the device for scanning an image that result's in a small scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-175">WIA_INTENT_MAXIMIZE_QUALITY</span><span class="sxs-lookup"><span data-stu-id="e1cbf-175">WIA_INTENT_MAXIMIZE_QUALITY</span></span></td>
<td><span data-ttu-id="e1cbf-176">L’application envisage de préparer l’appareil pour l’analyse d’une image de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-176">The application intends to prepare the device for scanning a high-quality image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-177">WIA_INTENT_SIZE_MASK</span><span class="sxs-lookup"><span data-stu-id="e1cbf-177">WIA_INTENT_SIZE_MASK</span></span></td>
<td><span data-ttu-id="e1cbf-178">Cet indicateur est un masque pour tous les indicateurs de taille/qualité.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-178">This flag is a mask for all of the size/quality flags.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-179">WIA_INTENT_BEST_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="e1cbf-179">WIA_INTENT_BEST_PREVIEW</span></span></td>
<td><span data-ttu-id="e1cbf-180">L’application envisage de préparer l’appareil pour l’analyse d’une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-180">The application intends to prepare the device for scanning a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <span data-ttu-id="e1cbf-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-182">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-182">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-183">Contient le nombre de pixels de l’axe x à partir WIA_IPS_XPOS jusqu’à la coordonnée x du coin supérieur de l’image à décroiser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-183">Contains the number of pixels in the x-direction from WIA_IPS_XPOS to the x-coordinate of the uppermost corner of the image to be deskewed.</span></span> <span data-ttu-id="e1cbf-184">Par conséquent, il décrit, conjointement avec WIA_IPS_DESKEW_Y, où les deux coins supérieurs de l’image inclinée se trouvent dans le rectangle englobant défini par WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT et WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-184">Hence, it describes, in conjunction with WIA_IPS_DESKEW_Y, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="e1cbf-185">sa propriété est implémentée par le pilote du scanneur si elle prend en charge la réalignement.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-185">his property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="e1cbf-186">Les valeurs valides pour WIA_IPS_DESKEW_X doivent être comprises entre 0 et (WIA_IPS_XEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-186">The valid values for WIA_IPS_DESKEW_X must be between 0 and (WIA_IPS_XEXTENT - 1).</span></span> <span data-ttu-id="e1cbf-187">La valeur 0 signifie qu’il n’est pas possible d’effectuer une détorsion.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-187">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="e1cbf-188">Cette propriété est facultative pour les éléments des catégories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM ; elle n’est pas disponible pour les éléments WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-188">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-189">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-189">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <span data-ttu-id="e1cbf-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-191">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-191">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-192">Contient le nombre de pixels de l’axe y de WIA_IPS_YPOS à la coordonnée y du coin le plus à gauche de l’image à décroiser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-192">Contains the number of pixels in the y-direction from WIA_IPS_YPOS to the y-coordinate of the leftmost corner of the image to be deskewed.</span></span> <span data-ttu-id="e1cbf-193">Par conséquent, il décrit, conjointement avec WIA_IPS_DESKEW_X, où les deux coins supérieurs de l’image inclinée se trouvent dans le rectangle englobant défini par WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT et WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-193">Hence, it describes, in conjunction with WIA_IPS_DESKEW_X, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="e1cbf-194">Cette propriété est implémentée par le pilote du scanneur si elle prend en charge la réalignement.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-194">This property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="e1cbf-195">Les valeurs valides pour WIA_IPS_DESKEW_Y doivent être comprises entre 0 et (WIA_IPS_YEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-195">The valid values for WIA_IPS_DESKEW_Y must be between 0 and (WIA_IPS_YEXTENT - 1).</span></span> <span data-ttu-id="e1cbf-196">La valeur 0 signifie qu’il n’est pas possible d’effectuer une détorsion.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-196">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="e1cbf-197">Cette propriété est facultative pour les éléments des catégories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM ; elle n’est pas disponible pour les éléments WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-197">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-198">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-198">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <span data-ttu-id="e1cbf-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-200">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-200">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-201">Contient la source et le mode d’acquisition du scanneur en cours.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-201">Contains the current scanner acquisition source and mode.</span></span> <span data-ttu-id="e1cbf-202">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-202">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-203">Une application lit cette propriété pour déterminer la source d’acquisition actuelle du scanneur ou pour écrire cette propriété afin de définir la source et le mode du scanneur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-203">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="e1cbf-204">En outre, les applications utilisent cette propriété pour activer et désactiver les fonctionnalités duplex.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-204">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="e1cbf-205">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-205">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="e1cbf-206">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-206">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-207">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="e1cbf-207">Flags</span></span></th>
<th><span data-ttu-id="e1cbf-208">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-209">DUPLEX</span><span class="sxs-lookup"><span data-stu-id="e1cbf-209">DUPLEX</span></span></td>
<td><span data-ttu-id="e1cbf-210">Analyse à l’aide d’opérations duplex.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-210">Scan using duplexer operations.</span></span> <span data-ttu-id="e1cbf-211">Analyser les deux côtés du document à l’aide des paramètres communs configurés pour l’élément du chargeur (WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-211">Scan both document sides using common settings configured for the feeder item (WIA_CATEGORY_FEEDER).</span></span> <span data-ttu-id="e1cbf-212">Les modes DUPLEX et ADVANCE_DUPLEX ne peuvent pas être définis.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-212">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-213">ADVANCED_DUPLEX</span><span class="sxs-lookup"><span data-stu-id="e1cbf-213">ADVANCED_DUPLEX</span></span></td>
<td><span data-ttu-id="e1cbf-214">Analyse en utilisant des paramètres individuels configurés pour chaque élément du chargeur d’enfants (WIA_CATEGORY_FEEDER_FRONT et WIA_CATEGORY_FEEDER_BACK).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-214">Scan using individual settings configured for each child feeder item (WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK).</span></span> <span data-ttu-id="e1cbf-215">Les modes DUPLEX et ADVANCE_DUPLEX ne peuvent pas être définis.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-215">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-216">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="e1cbf-216">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="e1cbf-217">Commencez par analyser le recto du document.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-217">Scan the front of the document first.</span></span> <span data-ttu-id="e1cbf-218">Cette valeur est valide lorsque DUPLEX ou ADVANCED_DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-218">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-219">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="e1cbf-219">BACK_FIRST</span></span></td>
<td><span data-ttu-id="e1cbf-220">Commencez par analyser le verso du document.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-220">Scan the back of the document first.</span></span> <span data-ttu-id="e1cbf-221">Cette valeur est valide lorsque DUPLEX ou ADVANCED_DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-221">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-222">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="e1cbf-222">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="e1cbf-223">Analysez l’avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-223">Scan the front only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-224">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="e1cbf-224">BACK_ONLY</span></span></td>
<td><span data-ttu-id="e1cbf-225">Analyser l’arrière uniquement.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-225">Scan the back only.</span></span> <span data-ttu-id="e1cbf-226">Cette valeur est valide lorsque DUPLEX ou ADVANCED_DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-226">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <span data-ttu-id="e1cbf-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-228">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-228">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-229">Permet la spécification d’une pièce jointe d’analyse de film particulière lorsqu’il en existe plusieurs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-229">Enables specification of a particular film scanning attachment when there is more than one.</span></span></p>
<p><span data-ttu-id="e1cbf-230">Cette propriété est requise pour les éléments de WIA_CATEGORY_FILM lorsqu’il y a plusieurs éléments de numérisation de film.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-230">This property is required for the WIA_CATEGORY_FILM items when there are multiple film scan items.</span></span> <span data-ttu-id="e1cbf-231">Si l’appareil ne prend en charge qu’un seul élément de film de scanneur racine, cette propriété est facultative.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-231">If the device supports only one root scanner film item then this property is optional.</span></span></p>
<p><span data-ttu-id="e1cbf-232">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-232">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e1cbf-233">Valeurs autorisées : le BSTR doit se présenter sous la forme de @ResourceBinary ,- <ResourceID> pour permettre la localisation, car cette chaîne sera exposée à l’utilisateur par le biais de l’interface utilisateur d’analyse des films.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-233">Allowed values: The BSTR should be in the form of @ResourceBinary,-<ResourceID> to allow localization as this string would be exposed to the user through the film scanning UI.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <span data-ttu-id="e1cbf-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-235">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-235">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-236">Active la configuration de l’analyse de pellicule actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-236">Enables configuration of the current film scan.</span></span></p>
<p><span data-ttu-id="e1cbf-237">Cette propriété est obligatoire pour l’élément WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-237">This property is required for the WIA_CATEGORY_FILM item.</span></span></p>
<p><span data-ttu-id="e1cbf-238">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-238">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e1cbf-239">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-239">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-240">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-240">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-241">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-241">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-242">WIA_FILM_COLOR_SLIDE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-242">WIA_FILM_COLOR_SLIDE</span></span></td>
<td><span data-ttu-id="e1cbf-243">Recherchez une diapositive de couleur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-243">Scan for a color slide.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-244">WIA_FILM_COLOR_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-244">WIA_FILM_COLOR_NEGATIVE</span></span></td>
<td><span data-ttu-id="e1cbf-245">Rechercher une couleur négative.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-245">Scan for a color negative.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-246">WIA_FILM_BW_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-246">WIA_FILM_BW_NEGATIVE</span></span></td>
<td><span data-ttu-id="e1cbf-247">Recherche un négatif noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-247">Scan for a black and white negative.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <span data-ttu-id="e1cbf-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-249">Réservé à une utilisation future et n’est pas mis en œuvre pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-249">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="e1cbf-250">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-250">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="e1cbf-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-252">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-252">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-253">Spécifie le nombre d’éléments stockés dans l’élément WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-253">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="e1cbf-254">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-254">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <span data-ttu-id="e1cbf-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-256">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-256">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-257">Active ou désactive la lampe du scanneur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-257">Turns the scanner lamp on or off.</span></span></p>
<p><span data-ttu-id="e1cbf-258">Facultatif pour les éléments WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM et recommandé pour WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-258">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-259">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-259">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e1cbf-260">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-260">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-261">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-261">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-262">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-263">WIA_LAMP_ON</span><span class="sxs-lookup"><span data-stu-id="e1cbf-263">WIA_LAMP_ON</span></span></td>
<td><span data-ttu-id="e1cbf-264">Activez la lampe.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-264">Turn on the lamp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-265">WIA_LAMP_OFF</span><span class="sxs-lookup"><span data-stu-id="e1cbf-265">WIA_LAMP_OFF</span></span></td>
<td><span data-ttu-id="e1cbf-266">Désactivez la lampe.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-266">Turn off the lamp.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <span data-ttu-id="e1cbf-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-268">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-268">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-269">Définit la durée maximale de conservation de la lampe lorsque le scanneur n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-269">Sets the maximum time to keep the lamp on when the scanner is not being used.</span></span></p>
<p><span data-ttu-id="e1cbf-270">Facultatif pour les éléments WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM et recommandé pour WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-270">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-271">Type : <strong>VT_UI4</strong>, Access : lecture/écriture, valeurs valides : 0-0xFFF secondes</span><span class="sxs-lookup"><span data-stu-id="e1cbf-271">Type: <strong>VT_UI4</strong>, Access: Read/Write, Valid Values: 0 - 0xFFF seconds</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <span data-ttu-id="e1cbf-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-273">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-273">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-274">Spécifie la largeur maximale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-274">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span> <span data-ttu-id="e1cbf-275">Il peut s’agir de la largeur du chargeur de feuille ou de la vitre de numérisation, en fonction du type d’élément.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-275">This may be the width of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="e1cbf-276">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <span data-ttu-id="e1cbf-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-278">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-278">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-279">Spécifie la hauteur maximale, en millièmes de pouce, qui est analysée sur l’axe vertical (Y) à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-279">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span> <span data-ttu-id="e1cbf-280">Il peut s’agir de la hauteur du chargeur de feuille ou de la vitre de numérisation, en fonction du type d’élément.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-280">This may be the height of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="e1cbf-281">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-281">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <span data-ttu-id="e1cbf-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-283">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-283">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-284">Spécifie la largeur minimale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-284">Specifies the minimum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="e1cbf-285">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-285">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <span data-ttu-id="e1cbf-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-287">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-287">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-288">Spécifie la hauteur minimale, en millièmes de pouce, qui est analysée sur l’axe vertical (Y) à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-288">Specifies the minimum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="e1cbf-289">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-289">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <span data-ttu-id="e1cbf-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-291">Réservé à une utilisation future et n’est pas mis en œuvre pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-291">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="e1cbf-292">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-292">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <span data-ttu-id="e1cbf-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-294">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-294">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-295">Résolution optique horizontale.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-295">Horizontal Optical Resolution.</span></span> <span data-ttu-id="e1cbf-296">Résolution optique horizontale la plus élevée prise en charge en PPP.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-296">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="e1cbf-297">Cette propriété est une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-297">This property is a single value.</span></span> <span data-ttu-id="e1cbf-298">Il ne s’agit pas d’une liste de toutes les résolutions qui peuvent être générées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-298">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="e1cbf-299">Au lieu de cela, il s’agit de la résolution des optiques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-299">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="e1cbf-300">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-300">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="e1cbf-301">Cette propriété est obligatoire pour tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-301">This property is required for all items.</span></span></p>
<p><span data-ttu-id="e1cbf-302">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-302">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <span data-ttu-id="e1cbf-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-304">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-304">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-305">Résolution optique verticale.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-305">Vertical Optical Resolution.</span></span> <span data-ttu-id="e1cbf-306">Résolution optique verticale la plus élevée prise en charge en PPP.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-306">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="e1cbf-307">Cette propriété est une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-307">This property is a single value.</span></span> <span data-ttu-id="e1cbf-308">Il ne s’agit pas d’une liste de toutes les résolutions générées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-308">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="e1cbf-309">Au lieu de cela, il s’agit de la résolution des optiques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-309">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="e1cbf-310">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-310">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="e1cbf-311">Cette propriété est obligatoire pour tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-311">This property is required for all items.</span></span></p>
<p><span data-ttu-id="e1cbf-312">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <span data-ttu-id="e1cbf-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-314">Spécifie l’orientation actuelle des documents à analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-314">Specifies the current orientation of the documents to be scanned.</span></span> <span data-ttu-id="e1cbf-315">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-315">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-316">Une application définit cette propriété pour définir l’orientation d’origine d’une page ou d’une image à acquérir.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-316">An application sets this property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="e1cbf-317">Pour plus d’informations sur l’utilisation de WIA_IPS_ORIENTATION, consultez <strong>WIA_IPS_PAGE_SIZE</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-317">For information on how to use WIA_IPS_ORIENTATION, see <strong>WIA_IPS_PAGE_SIZE</strong>.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-318">WIA_IPS_ORIENTATION fait référence à la position du document à analyser sur la vitre ou le chargeur du scanneur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-318">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="e1cbf-319">Il s’agit de l’orientation du document par rapport à la direction de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-319">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="e1cbf-320">WIA_IPS_ROTATION fait référence à la rotation appliquée à l’image après son analyse, juste avant que l’image ne soit transférée à l’application.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-320">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-321">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-321">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e1cbf-322">Le tableau suivant contient les quatre constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-322">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-323">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-323">Value</span></span></th>
<th><span data-ttu-id="e1cbf-324">Définition</span><span class="sxs-lookup"><span data-stu-id="e1cbf-324">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-325">Aperçu</span><span class="sxs-lookup"><span data-stu-id="e1cbf-325">PORTRAIT</span></span></td>
<td><span data-ttu-id="e1cbf-326">0 degré.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-326">0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-327">JARDIN</span><span class="sxs-lookup"><span data-stu-id="e1cbf-327">LANDSCAPE</span></span></td>
<td><span data-ttu-id="e1cbf-328">rotation de 90 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-328">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-329">ROT180</span><span class="sxs-lookup"><span data-stu-id="e1cbf-329">ROT180</span></span></td>
<td><span data-ttu-id="e1cbf-330">rotation de 180 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-330">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-331">ROT270</span><span class="sxs-lookup"><span data-stu-id="e1cbf-331">ROT270</span></span></td>
<td><span data-ttu-id="e1cbf-332">rotation de 270 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-332">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <span data-ttu-id="e1cbf-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-334">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-334">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-335">Contient la taille de la page qui est actuellement configurée pour être analysée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-335">Contains the size of the page that is currently set to be scanned.</span></span> <span data-ttu-id="e1cbf-336">Une application définit cette propriété pour sélectionner les dimensions de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-336">An application sets this property to select the dimensions of the page to scan.</span></span> <span data-ttu-id="e1cbf-337">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-337">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-338">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-338">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e1cbf-339">Pour connaître les constantes qui peuvent être utilisées avec cette propriété, consultez <a href="-wia-wia2-pagesizeconstants.md"><strong>constantes de taille de page WIA 2,0</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-339">For the constants that can be used with this property, see <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 Page Size Constants</strong></a>.</span></span> <span data-ttu-id="e1cbf-340">Notez ces tailles non fixes, en particulier :</span><span class="sxs-lookup"><span data-stu-id="e1cbf-340">Note these non-fixed sizes, in particular:</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-341">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-341">Value</span></span></th>
<th><span data-ttu-id="e1cbf-342">Définition</span><span class="sxs-lookup"><span data-stu-id="e1cbf-342">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-343">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="e1cbf-343">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="e1cbf-344">Défini par les valeurs des propriétés <strong>WIA_IPS_PAGE_HEIGHT</strong> et <strong>WIA_IPS_PAGE_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-344">Defined by the values of the <strong>WIA_IPS_PAGE_HEIGHT</strong> and <strong>WIA_IPS_PAGE_WIDTH</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-345">WIA_PAGE_AUTO</span><span class="sxs-lookup"><span data-stu-id="e1cbf-345">WIA_PAGE_AUTO</span></span></td>
<td><span data-ttu-id="e1cbf-346">La taille de la page est automatiquement déterminée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-346">Page size is automatically determined by the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-347">WIA_PAGE_CUSTOM_BASE</span><span class="sxs-lookup"><span data-stu-id="e1cbf-347">WIA_PAGE_CUSTOM_BASE</span></span></td>
<td><span data-ttu-id="e1cbf-348">Taille de page personnalisée dont les dimensions sont déjà connues de l’application et du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-348">A custom page size whose dimensions are already known to the application and the device driver.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="e1cbf-349">La valeur de la propriété <strong>WIA_IPS_ORIENTATION</strong> détermine l’orientation de la page actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-349">The value of the <strong>WIA_IPS_ORIENTATION</strong> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="e1cbf-350">Les propriétés <strong>WIA_IPS_PAGE_WIDTH</strong> et <strong>WIA_IPS_PAGE_HEIGHT</strong> signalent les dimensions de la page, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-350">The <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="e1cbf-351">Ces propriétés doivent être accordées avec <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong>, qui contiennent les dimensions de la page en pixels.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-351">These properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-352">Les valeurs valides de type WIA_PROP_LIST dépendent des paramètres valides de la propriété <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-352">Valid values of type WIA_PROP_LIST depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="e1cbf-353">Si, par exemple, l’appareil ne peut pas analyser les documents orientés paysage avec un paramètre WIA_PAGE_A4, WIA_PAGE_A4 n’est pas une valeur valide pour la propriété <strong>WIA_IPS_PAGE_SIZE</strong> lorsque <strong>WIA_IPS_ORIENTATION</strong> est défini sur paysage.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-353">If, for example, the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 is not a valid value for the <strong>WIA_IPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-354">Si une application définit <strong>WIA_IPS_PAGE_SIZE</strong> sur une valeur autre que les trois dans le tableau ci-dessus, le minipilote doit ajuster les valeurs de <strong>WIA_IPS_PAGE_WIDTH</strong> et <strong>WIA_IPS_PAGE_HEIGHT</strong> aux dimensions de la page, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-354">If an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to any value other than the three in the table above, the minidriver should adjust the values of <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="e1cbf-355">Elle doit également ajuster les valeurs de <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> sur les dimensions de la page en pixels.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-355">It should also adjust the values of <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="e1cbf-356">Si un paramètre d’extension (<strong>WIA_IPS_XEXTENT</strong> ou <strong>WIA_IPS_YEXTENT</strong>) est remplacé par une valeur qui ne correspond pas au paramètre de taille de page actuel, le minipilote doit remplacer la valeur de la propriété <strong>WIA_IPS_PAGE_SIZE</strong> par WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-356">If an extent setting (<strong>WIA_IPS_XEXTENT</strong> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page size setting, the minidriver should change the value of the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="e1cbf-357">Le minipilote doit également modifier <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> ou <strong>WIA_IPS_PAGE_HEIGHT</strong> conformément au nouveau paramètre d’extension.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-357">The minidriver should also modify <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> or <strong>WIA_IPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="e1cbf-358">Si <strong>WIA_IPS_ORIENTATION</strong> est défini sur paysage, les paramètres d’étendue sont échangés par rapport à leurs valeurs habituelles.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-358">If <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE, the extent settings will be exchanged relative to their usual values.</span></span> <span data-ttu-id="e1cbf-359">Par exemple, si une application définit <strong>WIA_IPS_PAGE_SIZE</strong> sur WIA_PAGE_A4, le minipilote définit <strong>WIA_IPS_PAGE_WIDTH</strong> sur 11692 et <strong>WIA_IPS_PAGE_HEIGHT</strong> sur 8267.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-359">For example, if an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver sets <strong>WIA_IPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_IPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="e1cbf-360">(Le minipilote doit également ajuster <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> en conséquence.)</span><span class="sxs-lookup"><span data-stu-id="e1cbf-360">(The minidriver should also adjust <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.)</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-361">Si <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> est défini sur WIA_PAGE_CUSTOM, le paramètre d’orientation n’est pas utilisé pour déterminer les dimensions d’étendue de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-361">If <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-362">Le minipilote est chargé de s’assurer que la propriété <strong>WIA_IPS_ORIENTATION</strong> est en accord avec la zone de sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-362">The minidriver is responsible for ensuring that the <strong>WIA_IPS_ORIENTATION</strong> property is in agreement with the current selection area.</span></span> <span data-ttu-id="e1cbf-363">Si une application remplace la valeur de <strong>WIA_IPS_ORIENTATION</strong> par une valeur non valide pour la taille de page actuellement sélectionnée, le minipilote doit changer la valeur de <strong>WIA_IPS_PAGE_SIZE</strong> en une taille de page prise en charge par la nouvelle valeur d’orientation.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-363">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_IPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="e1cbf-364">Si une application définit la propriété <strong>WIA_IPS_PAGE_SIZE</strong> sur WIA_PAGE_CUSTOM, la zone de sélection actuelle n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-364">If an application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="e1cbf-365">Le minipilote WIA doit obtenir la disposition actuelle de l’image, en commençant par les paramètres actuels des propriétés <strong>WIA_IPS_XPOS</strong> et <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-365">The WIA minidriver should obtain the current image layout, starting from the current settings of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="e1cbf-366">Si le paramètre taille de la page se trouve dans une zone de sélection située en dehors de la vitre du scanneur, le minipilote doit automatiquement ajuster les valeurs des propriétés <strong>WIA_IPS_XPOS</strong> et <strong>WIA_IPS_YPOS</strong> aux paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-366">If the page size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="e1cbf-367">Si les propriétés <strong>WIA_IPS_PAGE_SIZE</strong> et <strong>WIA_IPS_ORIENTATION</strong> sont définies en même temps et qu’elles ne sont pas valides lorsqu’elles sont appliquées en combinaison, le minipilote doit faire échouer les paramètres de l’application en renvoyant une erreur dans le <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv ::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-367">If the <strong>WIA_IPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span></p>
<p><span data-ttu-id="e1cbf-368">Les quatre exemples suivants illustrent différents scénarios de <strong>WIA_IPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-368">The following four examples show different <strong>WIA_IPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="e1cbf-369">Le pilote signale les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-369">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="e1cbf-370">Une application définit la propriété <strong>WIA_IPS_PAGE_SIZE</strong> sur WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-370">An application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="e1cbf-371">Une application définit la propriété <strong>WIA_IPS_ORIENTATION</strong> sur paysage.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-371">An application sets the <strong>WIA_IPS_ORIENTATION</strong> property to LANDSCAPE.</span></span></li>
<li><span data-ttu-id="e1cbf-372">Une application remplace la propriété <strong>WIA_IPS_XEXTENT</strong> par une valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-372">An application changes the <strong>WIA_IPS_XEXTENT</strong> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="e1cbf-373"><strong>Exemple 1 : le minipilote signale les paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="e1cbf-373"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="e1cbf-374">Dans l’exemple suivant, le minipilote définit une zone de sélection personnalisée avant qu’une application définisse des propriétés WIA.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-374">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="e1cbf-375">Dans ce cas, la zone de sélection représente l’ensemble du plateau.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-375">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="e1cbf-376"><strong>Exemple 2 : une application définit la</strong> <strong></strong><strong>propriété WIA_IPS_PAGE_SIZE sur WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="e1cbf-376"><strong>Example 2: An application sets the</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="e1cbf-377"><strong>Exemple 3 : une application définit la</strong> <strong></strong><strong>propriété WIA_IPS_ORIENTATION sur paysage</strong>  </span><span class="sxs-lookup"><span data-stu-id="e1cbf-377"><strong>Example 3: An application sets the</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>property to LANDSCAPE</strong></span></span></p>
<p><span data-ttu-id="e1cbf-378">Le lit physique doit pouvoir acquérir une page qui était à l’origine en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-378">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="e1cbf-379"><strong>Exemple 4 : une application remplace la</strong> <strong></strong> <strong>propriété WIA_IPS_XEXTENT par une valeur inférieure</strong></span><span class="sxs-lookup"><span data-stu-id="e1cbf-379"><strong>Example 4: An application changes the</strong> <strong>WIA_IPS_XEXTENT</strong> <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="e1cbf-380">Dans l’exemple suivant, une application remplace la valeur de la propriété <strong>WIA_IPS_XEXTENT</strong> par 1000.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-380">In the following example, an application changes the <strong>WIA_IPS_XEXTENT</strong> property to 1000.</span></span> <span data-ttu-id="e1cbf-381">Le minipilote doit supposer que la nouvelle valeur contenue dans <strong>WIA_IPS_XEXTENT</strong> n’est plus valide pour la propriété <strong>WIA_IPS_PAGE_SIZE</strong> et doit donc remplacer <strong>WIA_IPS_PAGE_SIZE</strong> par WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-381">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_IPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="e1cbf-382">Le minipilote doit également ajuster <strong>WIA_IPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-382">The minidriver must also adjust <strong>WIA_IPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <span data-ttu-id="e1cbf-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-384">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-384">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-385">Contient la hauteur, en millièmes de pouce, de la page actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-385">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="e1cbf-386">Le minipilote crée et gère la propriété <strong>WIA_IPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-386">The minidriver creates and maintains the <strong>WIA_IPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="e1cbf-387">Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-387">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="e1cbf-388">Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la hauteur de la page dont la propriété <strong>WIA_IPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM (qui est une valeur de la propriété <strong>WIA_IPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-388">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_IPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="e1cbf-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> doit être synchronisé avec <strong>WIA_IPS_XEXTENT</strong>, qui indique la hauteur, en pixels, de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> must be in sync with <strong>WIA_IPS_XEXTENT</strong>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="e1cbf-390">Cette propriété est requise pour les éléments de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-390">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-391">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <span data-ttu-id="e1cbf-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-393">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-393">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-394">Contient la largeur de la page actuelle sélectionnée, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-394">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="e1cbf-395">Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-395">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="e1cbf-396">Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la largeur de la page dont la propriété <strong>WIA_IPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-396">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="e1cbf-397"><strong>WIA_IPS_PAGE_WIDTH</strong> doit être synchronisée avec la valeur de <strong>WIA_IPS_XEXTENT</strong>, qui indique la largeur, en pixels, de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-397"><strong>WIA_IPS_PAGE_WIDTH</strong> must be in sync with the value of <strong>WIA_IPS_XEXTENT</strong>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="e1cbf-398">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-398">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-399">Cette propriété est requise pour les éléments de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-399">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-400">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-400">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <span data-ttu-id="e1cbf-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-402">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-402">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-403">Contient le nombre actuel de pages à acquérir à partir d’un chargeur automatique de documents.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-403">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="e1cbf-404">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-404">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-405">Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> il s’agit de zéro dans le nombre maximal de pages que le scanneur peut analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-405">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> This is zero through the maximum number of pages that the scanner can scan.</span></span> <span data-ttu-id="e1cbf-406">La valeur est ALL_PAGES (= 0) si le scanneur peut effectuer une analyse continue.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-406">The value is ALL_PAGES (= 0) if the scanner can scan continuously.</span></span></p>
<p><span data-ttu-id="e1cbf-407">Une application lit cette propriété pour déterminer la capacité de page du chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-407">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="e1cbf-408">L’application définit également cette propriété sur le nombre de pages qu’elle va analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-408">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-409">Si le mode duplex est activé (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> est défini sur alimentation | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> est toujours égal au nombre de pages à analyser.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-409">If duplex mode is enabled (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-410">Une feuille de papier contient automatiquement deux pages si le DUPLEX est activé, même si le côté arrière de la page est vide.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-410">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="e1cbf-411">Si vous affectez la valeur 1 à <strong>WIA_IPS_PAGES</strong> , un scanneur traite un côté de la page.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-411">Setting <strong>WIA_IPS_PAGES</strong> to 1 causes a scanner to process one side of the page.</span></span> <span data-ttu-id="e1cbf-412">Si un scanneur ne parvient pas à analyser un seul côté d’une page en mode duplex, il est recommandé de remplacer la valeur <strong>WIA_IPS_PAGES</strong> pour le membre Inc du membre de la plage de la structure WIA_PROPERTY_INFO par 2.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-412">We recommend that, if a scanner is unable to scan only one side of a page while in duplex mode, you change the <strong>WIA_IPS_PAGES</strong> value for the Inc member of the Range member of the WIA_PROPERTY_INFO structure to 2.</span></span> <span data-ttu-id="e1cbf-413">Cette valeur signale à l’application qu’elle doit demander des pages par multiples de deux.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-413">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="e1cbf-414">La valeur ALL_PAGES (= 0) signifie que <em>toutes les</em> pages qui sont actuellement chargées dans le chargeur de documents doivent être analysées.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-414">A value of ALL_PAGES (= 0) means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <span data-ttu-id="e1cbf-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-416">Contient la valeur actuelle pour les pixels blancs et noirs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-416">Contains the current setting for white and black pixels.</span></span> <span data-ttu-id="e1cbf-417">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-417">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-418">Une application lit cette valeur pour déterminer la valeur du blanc ou du noir (en fonction de ce que l’application fait).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-418">An application reads this value to determine the value of WHITE or BLACK (depending on what the application is doing).</span></span></p>
<p><span data-ttu-id="e1cbf-419">Obligatoire pour toutes les acquisitions activées ou éléments stockés ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-419">Required for all acquisition enabled or stored items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-420">Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-420">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-421">Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-421">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="e1cbf-422">Si l’appareil peut être défini sur une seule valeur, créez un WIA_PROP_LIST type et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-422">If the device can be set to only a single value, create a WIA_PROP_LIST type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="e1cbf-423">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-423">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-424">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-424">Value</span></span></th>
<th><span data-ttu-id="e1cbf-425">Définition</span><span class="sxs-lookup"><span data-stu-id="e1cbf-425">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-426">WIA_PHOTO_WHITE_0</span><span class="sxs-lookup"><span data-stu-id="e1cbf-426">WIA_PHOTO_WHITE_0</span></span></td>
<td><span data-ttu-id="e1cbf-427">Le blanc est 0 et le noir est 1.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-427">WHITE is 0, and BLACK is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-428">WIA_PHOTO_WHITE_1</span><span class="sxs-lookup"><span data-stu-id="e1cbf-428">WIA_PHOTO_WHITE_1</span></span></td>
<td><span data-ttu-id="e1cbf-429">Le blanc est 1 et le noir est 0.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-429">WHITE is 1, and BLACK is 0.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <span data-ttu-id="e1cbf-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-431">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-431">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-432">Indique le mode d’aperçu pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-432">Indicates the preview mode for a device.</span></span> <span data-ttu-id="e1cbf-433">Une application définit cette propriété pour placer l’appareil dans un mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-433">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="e1cbf-434">Cette propriété est requise pour les éléments WIA_CATEGORY_FLATBED et WIA_CATEGORY_FILM, facultatifs pour l’élément WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-434">This property is required for the WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items, optional for the WIA_CATEGORY_FEEDER item.</span></span></p>
<p><span data-ttu-id="e1cbf-435">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-435">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e1cbf-436">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-436">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-437">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-437">Value</span></span></th>
<th><span data-ttu-id="e1cbf-438">Définition</span><span class="sxs-lookup"><span data-stu-id="e1cbf-438">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-439">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="e1cbf-439">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="e1cbf-440">L’application effectue une analyse finale.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-440">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-441">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="e1cbf-441">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="e1cbf-442">L’application effectue une analyse de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-442">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <span data-ttu-id="e1cbf-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-444">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-444">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-445">Spécifie si l’image d’aperçu existante peut être mise à jour au cours d’une préversion d’image (en réponse à une modification dans les propriétés de WIA_IPA_DATATYPE ou de WIA_IPA_DEPTH).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-445">Specifies whether the existing preview image can be updated during an image preview (in response to a change in the WIA_IPA_DATATYPE or WIA_IPA_DEPTH properties).</span></span></p>
<p><span data-ttu-id="e1cbf-446">Cette propriété est facultative pour tous les éléments activés pour l’acquisition qui prennent en charge les analyses d’aperçu. autrement dit, WIA_IPS_PREVIEW est pris en charge avec WIA_PREVIEW_SCAN.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-446">This property is optional for all acquisition enabled items that support preview scans; that is, WIA_IPS_PREVIEW is supported with WIA_PREVIEW_SCAN.</span></span> <span data-ttu-id="e1cbf-447">Cela comprend les éléments de type WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-447">This includes items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-448">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-448">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e1cbf-449">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-449">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-450">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-450">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-451">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-451">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-452">WIA_ADVANCED_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="e1cbf-452">WIA_ADVANCED_PREVIEW</span></span></td>
<td><span data-ttu-id="e1cbf-453">La mise à jour de l’image existante est possible.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-453">Updating the existing image is possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-454">WIA_BASIC_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="e1cbf-454">WIA_BASIC_PREVIEW</span></span></td>
<td><span data-ttu-id="e1cbf-455">Une autre analyse préliminaire doit être exécutée, car la mise à jour de l’image existante n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-455">Another preview scan must be executed because updating the existing image is not possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <span data-ttu-id="e1cbf-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-457">Contient le paramètre de rotation actuel, s’il est implémenté.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-457">Contains the current rotation setting, if it is implemented.</span></span> <span data-ttu-id="e1cbf-458">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-458">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-459">Une application définit cette propriété pour informer le pilote de la quantité (le cas) de rotation de l’image avant que le pilote le renvoie à l’application.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-459">An application sets this property to inform the driver how much (if at all) to rotate the image before the driver returns it to the application.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-460">WIA_IPS_ORIENTATION fait référence à la position du document à analyser sur la vitre ou le chargeur du scanneur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-460">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="e1cbf-461">Il s’agit de l’orientation du document par rapport à la direction de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-461">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="e1cbf-462">WIA_IPS_ROTATION fait référence à la rotation appliquée à l’image après son analyse, juste avant que l’image ne soit transférée à l’application.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-462">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-463">Le minipilote WIA est chargé de faire pivoter les données de l’image avant de les renvoyer à l’application.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-463">The WIA minidriver is responsible for rotating the image data before sending it back to the application.</span></span> <span data-ttu-id="e1cbf-464">L’application est chargée de vérifier les en-têtes d’image pour voir les valeurs qui viennent d’être pivotées.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-464">The application is responsible for checking the image headers to see the newly rotated values.</span></span></p>
<p><span data-ttu-id="e1cbf-465">Il existe une certaine confusion quant à la résolution de l’effet de la rotation sur la zone de sélection de l’image actuelle (qui est définie par les propriétés <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> ).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-465">Considerable confusion exists about resolving the effect of rotation on the current image's selection area (which is defined by the <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> properties).</span></span></p>
<p><span data-ttu-id="e1cbf-466">La <em>zone de sélection</em> fait référence à la zone sélectionnée sur la vitre du scanneur physique à partir de laquelle une image est acquise.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-466"><em>Selection area</em> refers to the selected area on the physical scanner bed that an image is be acquired from.</span></span> <span data-ttu-id="e1cbf-467"><strong>WIA_IPS_ROTATION</strong> ne modifie pas la zone de sélection.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-467"><strong>WIA_IPS_ROTATION</strong> does not modify the selection area.</span></span> <span data-ttu-id="e1cbf-468">Le pilote applique une rotation dans le sens inverse des aiguilles d’une passe en fonction de <strong>WIA_IPS_ROTATION</strong> uniquement après que le pilote a acquis la zone de sélection appropriée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-468">The driver applies a counterclockwise rotation according to <strong>WIA_IPS_ROTATION</strong> only after the driver has acquired the appropriate selection area.</span></span> <span data-ttu-id="e1cbf-469"><strong>WIA_IPS_ROTATION</strong> affecte les dimensions de l’image de sortie, ces dimensions doivent donc être reflétées dans l’en-tête de données de l’image résultante.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-469"><strong>WIA_IPS_ROTATION</strong> does affect the dimensions of the output image, so these dimensions must be reflected in the resulting image's data header.</span></span></p>
<p><span data-ttu-id="e1cbf-470">Facultatif pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-470">Optional for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-471">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-471">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e1cbf-472">Les constantes de rotation suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-472">The following rotation constants are defined.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-473">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-473">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-474">Définition</span><span class="sxs-lookup"><span data-stu-id="e1cbf-474">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-475">Aperçu</span><span class="sxs-lookup"><span data-stu-id="e1cbf-475">PORTRAIT</span></span></td>
<td><span data-ttu-id="e1cbf-476">Le pilote ne fait pas pivoter l’image.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-476">The driver will not rotate the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-477">JARDIN</span><span class="sxs-lookup"><span data-stu-id="e1cbf-477">LANDSCAPE</span></span></td>
<td><span data-ttu-id="e1cbf-478">Le pilote fait pivoter l’image de 90 degrés dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-478">TThe driver rotates the image 90 degrees counterclockwise.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-479">ROT180</span><span class="sxs-lookup"><span data-stu-id="e1cbf-479">ROT180</span></span></td>
<td><span data-ttu-id="e1cbf-480">Le pilote fait pivoter l’image de 180 degrés dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-480">The driver rotates the image 180 degrees counterclockwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-481">ROT270</span><span class="sxs-lookup"><span data-stu-id="e1cbf-481">ROT270</span></span></td>
<td><span data-ttu-id="e1cbf-482">Le pilote fait pivoter l’image de 270 degrés dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-482">The driver rotates the image 270 degrees counterclockwise.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <span data-ttu-id="e1cbf-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-484">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-484">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-485">Spécifie si l’application doit utiliser le filtre de segmentation du pilote pour l’analyse sur plusieurs régions.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-485">Specifies whether the application should use the driver's segmentation filter for multi-region scanning.</span></span> <span data-ttu-id="e1cbf-486">WIA_IPS_SEGMENTATION doit être implémenté pour les éléments WIA_CATEGORY_FLATBED et WIA_CATEGORY_FILM s’ils prennent en charge la création d’éléments enfants avec un filtre de segmentation ou si le pilote lui-même crée des éléments enfants pour les frames fixes.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-486">WIA_IPS_SEGMENTATION must be implemented for WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items if they support either the creation of child items with a segmentation filter or if the driver itself creates child items for fixed frames.</span></span></p>
<p><span data-ttu-id="e1cbf-487">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-487">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e1cbf-488">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-488">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-489">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-489">Value</span></span></th>
<th><span data-ttu-id="e1cbf-490">Définition</span><span class="sxs-lookup"><span data-stu-id="e1cbf-490">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-491">WIA_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="e1cbf-491">WIA_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="e1cbf-492">L’application doit utiliser le filtre de segmentation pour l’analyse sur plusieurs régions.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-492">The application should use the segmentation filter for multi-region scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-493">WIA_DONT_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="e1cbf-493">WIA_DONT_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="e1cbf-494">Le pilote crée les éléments enfants lui-même pour l’analyse sur plusieurs régions.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-494">The driver creates the child items itself for multi-region scanning.</span></span> <span data-ttu-id="e1cbf-495">C’est généralement le cas si le scanneur utilise des frames fixes à cet effet.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-495">This is usually the case if the scanner uses fixed frames for this purpose.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-496">Il est possible qu’un pilote soit fourni avec un filtre de segmentation, mais qu’il ait toujours WIA_IPS_SEGMENTATION défini sur WIA_DONT_USE_SEGMENTATION_FILTER pour l’un de ses éléments (par exemple, l’élément WIA_CATEGORY_FILM).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-496">It is possible for a driver to come with a segmentation filter, but still have WIA_IPS_SEGMENTATION set to WIA_DONT_USE_SEGMENTATION_FILTER for one of its items (such as, the WIA_CATEGORY_FILM item).</span></span> <span data-ttu-id="e1cbf-497">Cela peut être le cas si le scanneur utilise des images fixes pour l’analyse des films, mais pas pour une analyse régulière à partir des éléments de WIA_CATEGORY_FLATBED.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-497">This could be the case if the scanner uses fixed frames for film scanning, but not for regular scanning from WIA_CATEGORY_FLATBED items.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <span data-ttu-id="e1cbf-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-499">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-499">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-500">Contient les détections d’alignement, d’alignement et de bord pour les documents placés sur le plateau.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-500">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="e1cbf-501">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-501">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="e1cbf-502">Cette propriété indique comment la feuille est positionnée horizontalement sur la tête de numérisation d’un lecteur de poche ou d’un scanneur à feuille.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-502">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="e1cbf-503">La propriété permet de prédire où un document est placé sur l’en-tête d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-503">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="e1cbf-504">Pour les scanneurs qui prennent en charge plusieurs têtes d’analyse, cette propriété est relative à la tête d’analyse la plus haut.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-504">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="e1cbf-505">Cette propriété est obligatoire pour les scanneurs de feuille, d’alimentation et de défilement.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-505">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="e1cbf-506">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-506">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e1cbf-507">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-507">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-508">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-508">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-509">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-509">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-510">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="e1cbf-510">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="e1cbf-511">La feuille est positionnée à gauche par rapport à la tête de numérisation.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-511">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-512">PARTANT</span><span class="sxs-lookup"><span data-stu-id="e1cbf-512">CENTERED</span></span></td>
<td><span data-ttu-id="e1cbf-513">La feuille est centrée sur la tête de numérisation.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-513">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1cbf-514">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="e1cbf-514">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="e1cbf-515">La feuille est positionnée à droite par rapport à la tête de numérisation.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-515">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <span data-ttu-id="e1cbf-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-517">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-517">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-518">Indique si un élément a besoin d’un contrôle d’aperçu affiché pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-518">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="e1cbf-519">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-519">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-520">Facultatif pour tous les éléments activés pour le transfert.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-520">Optional for all transfer enabled items.</span></span> <span data-ttu-id="e1cbf-521">Il s’agit généralement simplement d’éléments des catégories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM et WIA_CATEGORY_FINISHED_FILE.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-521">This is usually just items of the categories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM, and WIA_CATEGORY_FINISHED_FILE.</span></span></p>
<p><span data-ttu-id="e1cbf-522">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-522">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e1cbf-523">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-523">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1cbf-524">Constante</span><span class="sxs-lookup"><span data-stu-id="e1cbf-524">Constant</span></span></th>
<th><span data-ttu-id="e1cbf-525">Description</span><span class="sxs-lookup"><span data-stu-id="e1cbf-525">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1cbf-526">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="e1cbf-526">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="e1cbf-527">Affichez un contrôle d’aperçu pour l’utilisateur, car ce dernier peut effectuer une préversion.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-527">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1cbf-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="e1cbf-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="e1cbf-529">N’affiche pas un contrôle d’aperçu pour l’utilisateur, car cet appareil ne peut pas effectuer d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-529">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <span data-ttu-id="e1cbf-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-531">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-531">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-532">Spécifie si l’application (ou les filtres) peut créer des éléments enfants sous l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-532">Specifies whether the application (or the filters) can create child items under the current item.</span></span></p>
<p><span data-ttu-id="e1cbf-533">Facultatif pour toutes les catégories d’éléments activées pour le transfert : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM et même WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-533">Optional for all transfer enabled item categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM and even WIA_CATEGORY_FOLDER.</span></span> <span data-ttu-id="e1cbf-534">(Si le stockage ne prend pas en charge le chargement de nouveaux éléments, cette propriété doit être non prise en charge ou prise en charge avec la valeur <strong>false</strong> .)</span><span class="sxs-lookup"><span data-stu-id="e1cbf-534">(If the storage won't support upload of new items then this property should be either unsupported or supported with the <strong>FALSE</strong> value.)</span></span></p>
<p><span data-ttu-id="e1cbf-535">Les éléments qui prennent en charge WIA_IPS_SEGMENTATION et WIA_USE_SEGMENTATION_FILTER doivent également prendre en charge WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION et avoir la valeur <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-535">Items supporting WIA_IPS_SEGMENTATION and WIA_USE_SEGMENTATION_FILTER must also support WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION and have it set to <strong>TRUE</strong>.</span></span></p>
<p><span data-ttu-id="e1cbf-536">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <strong>true</strong> et <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="e1cbf-536">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <strong>TRUE</strong> and <strong>FALSE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <span data-ttu-id="e1cbf-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-538">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-538">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-539">Spécifie la valeur de nuances de gris qui détermine si un pixel est converti en blanc ou noir quand une image est convertie en monochromatique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-539">Specifies the grayscale value that determines whether a pixel will be converted to white or black when an image is converted to monochromatic.</span></span> <span data-ttu-id="e1cbf-540">Les pixels situés au-dessus du seuil deviennent blancs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-540">Pixels above the threshold become white.</span></span> <span data-ttu-id="e1cbf-541">Les pixels situés en dessous du seuil deviennent blancs.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-541">Pixels below the threshold become white.</span></span></p>
<p><span data-ttu-id="e1cbf-542">Cette propriété est requise pour les éléments d’acquisition qui prennent en charge les analyses 1-BPP et dont la propriété WIA_IPA_DATATYPE est définie sur WIA_DATA_THRESHOLD.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-542">This property is required for acquisition items that support 1-bpp scans and that have the WIA_IPA_DATATYPE property set to WIA_DATA_THRESHOLD.</span></span></p>
<p><span data-ttu-id="e1cbf-543">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-543">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <span data-ttu-id="e1cbf-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-545">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-545">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-546">Spécifie si le pilote peut transférer plusieurs éléments enfants dans un appel de transfert unique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-546">Specifies whether the driver is capable of transferring multiple child items in single transfer call.</span></span></p>
<p><span data-ttu-id="e1cbf-547">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-547">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="e1cbf-548">La seule valeur possible pour cette propriété est WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-548">The only possible value for this property is WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span></span> <span data-ttu-id="e1cbf-549">Si cet indicateur est défini, le pilote est en charge du transfert de plusieurs éléments enfants dans un appel de transfert unique.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-549">If this flag is set, then the driver is capable of transfering multiple child items in single transfer call.</span></span> <span data-ttu-id="e1cbf-550">Si l’indicateur n’est pas défini, le service WIA parcourt les éléments enfants de manière récursive, puis transfère chacun de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-550">If the flag is not set, the WIA Service will walk through the child items recursively and then transfer each of those items.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="e1cbf-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-552">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-552">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-553">Spécifie le nombre d’octets à charger pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-553">Specifies the number of bytes to upload for the item.</span></span></p>
<p><span data-ttu-id="e1cbf-554">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-554">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <span data-ttu-id="e1cbf-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-556">Spécifie la durée de préchauffage maximale, en millisecondes, nécessaire à l’appareil avant de démarrer l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-556">Specifies the maximum warm-up time, in milliseconds, that the device needs before starting the scanning operation.</span></span> <span data-ttu-id="e1cbf-557">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-557">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-558">Une application peut lire cette propriété pour déterminer le temps de préchauffage maximal pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-558">An application can read this property to determine the maximum warm-up time for this device.</span></span> <span data-ttu-id="e1cbf-559">Il peut alors présenter une &quot; boîte de dialogue en attente de préchauffage de l’appareil pour &quot; permettre à l’utilisateur de savoir qu’une attente ou une pause peut se produire avant tout problème.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-559">It can then present a &quot;waiting for the device to warm up&quot; dialog box, to let the user know that a wait or pause might occur before anything happens.</span></span></p>
<p><span data-ttu-id="e1cbf-560">Cette propriété est obligatoire pour tous les éléments d’acquisition activés ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-560">This property is required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-561">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <span data-ttu-id="e1cbf-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-563">Contient la largeur actuelle, en pixels, de l’image sélectionnée à acquérir.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-563">Contains the current width, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="e1cbf-564">Une application définit cette propriété pour marquer la largeur d’une zone de sélection à acquérir.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-564">An application sets this property to mark the width of a selection area to acquire.</span></span> <span data-ttu-id="e1cbf-565">Cette propriété doit accepter la propriété <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-565">This property must agree with the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="e1cbf-566">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-566">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-567">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-567">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-568">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-568">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <span data-ttu-id="e1cbf-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-570">Contient la coordonnée x, en pixels, de l’angle supérieur gauche de l’image sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-570">Contains the x coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="e1cbf-571">Une application définit cette propriété pour marquer l’angle supérieur gauche de la zone de sélection.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-571">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="e1cbf-572">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-572">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-573">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-573">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-574">Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-574">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-575">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-575">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <span data-ttu-id="e1cbf-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-577">Contient la résolution horizontale actuelle, en pixels par pouce, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-577">Contains the current horizontal resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="e1cbf-578">Une application définit cette propriété pour définir la résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-578">An application sets this property to set the horizontal resolution.</span></span> <span data-ttu-id="e1cbf-579">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-579">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-580">Si l’appareil peut être défini sur une seule valeur, créez un type de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-580">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="e1cbf-581">C’est également le cas lorsque l’un des paramètres de résolution dépend d’une autre résolution.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-581">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="e1cbf-582">(La résolution verticale peut dépendre de la résolution horizontale.)</span><span class="sxs-lookup"><span data-stu-id="e1cbf-582">(The vertical resolution can depend on the horizontal resolution.)</span></span></p>
<p><span data-ttu-id="e1cbf-583">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-583">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-584">Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-584">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-585">Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="e1cbf-585">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <span data-ttu-id="e1cbf-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-587">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-587">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-588">Définit la mise à l’échelle horizontale, sous la forme d’un pourcentage, qui peut être appliquée aux images numérisées au sein du périphérique du scanneur ou de son pilote.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-588">Sets the horizontal scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="e1cbf-589">Cette propriété est facultative pour tous les éléments d’acquisition activés ; autrement dit, les éléments de type WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-589">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-590">Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-590">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="e1cbf-591">Les valeurs peuvent être comprises entre 1 et maximum VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-591">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="e1cbf-592">Par exemple, 100 signifie aucune mise à l’échelle, 050 signifie la mise à l’échelle jusqu’à 50% de la taille de la replacer, et 200 signifie la mise à l’échelle jusqu’à 200% de la taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-592">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <span data-ttu-id="e1cbf-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-594">Contient la hauteur actuelle, en pixels, de l’image sélectionnée à acquérir.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-594">Contains the current height, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="e1cbf-595">Une application définit cette propriété pour marquer la hauteur d’une zone de sélection.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-595">An application sets this property to mark the height of a selection area.</span></span> <span data-ttu-id="e1cbf-596">Cette propriété doit être conforme à la valeur de la propriété <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-596">This property must be agree with the value of the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="e1cbf-597">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-597">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-598">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-598">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-599">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-599">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <span data-ttu-id="e1cbf-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-601">Coordonnée y actuelle, en pixels, de l’angle supérieur gauche de l’image sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-601">Current y coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="e1cbf-602">Une application définit cette propriété pour marquer l’angle supérieur gauche de la zone de sélection.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-602">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="e1cbf-603">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-603">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-604">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-604">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-605">Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-605">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-606">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="e1cbf-606">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <span data-ttu-id="e1cbf-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e1cbf-608">Contient la résolution verticale actuelle, en pixels par pouce, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-608">Contains the current vertical resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="e1cbf-609">Une application définit cette propriété pour définir la résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-609">An application sets this property to set the vertical resolution.</span></span> <span data-ttu-id="e1cbf-610">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-610">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="e1cbf-611">Si l’appareil peut être défini sur une seule valeur, créez un type de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-611">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="e1cbf-612">C’est également le cas lorsque l’un des paramètres de résolution dépend d’une autre résolution.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-612">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="e1cbf-613">(La résolution horizontale peut dépendre de la résolution verticale.)</span><span class="sxs-lookup"><span data-stu-id="e1cbf-613">(The horizontal resolution can depend on the vertical resolution.)</span></span></p>
<p><span data-ttu-id="e1cbf-614">Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-614">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="e1cbf-615">Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-615">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="e1cbf-616">Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="e1cbf-616">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <span data-ttu-id="e1cbf-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="e1cbf-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cbf-618">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-618">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="e1cbf-619">Définit la mise à l’échelle verticale, sous la forme d’un pourcentage, qui peut être appliquée aux images numérisées au sein du périphérique du scanneur ou de son pilote.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-619">Sets the vertical scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="e1cbf-620">Cette propriété est facultative pour tous les éléments d’acquisition activés ; autrement dit, les éléments de type WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-620">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="e1cbf-621">Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-621">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="e1cbf-622">Les valeurs peuvent être comprises entre 1 et maximum VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-622">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="e1cbf-623">Par exemple, 100 signifie aucune mise à l’échelle, 050 signifie la mise à l’échelle jusqu’à 50% de la taille de la replacer, et 200 signifie la mise à l’échelle jusqu’à 200% de la taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-623">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e1cbf-624">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1cbf-624">Requirements</span></span>



| <span data-ttu-id="e1cbf-625">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1cbf-625">Requirement</span></span> | <span data-ttu-id="e1cbf-626">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1cbf-626">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cbf-627">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1cbf-627">Minimum supported client</span></span><br/> | <span data-ttu-id="e1cbf-628">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1cbf-628">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e1cbf-629">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1cbf-629">Minimum supported server</span></span><br/> | <span data-ttu-id="e1cbf-630">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1cbf-630">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e1cbf-631">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1cbf-631">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1cbf-632"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cbf-632"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




