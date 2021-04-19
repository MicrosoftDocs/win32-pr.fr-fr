---
description: Les périphériques matériels WIA (Windows Image Acquisition) ont des valeurs de propriété qui sont stockées dans le Registre Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Constantes de propriété de périphérique de scanneur (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543458"
---
# <a name="scanner-device-property-constants"></a><span data-ttu-id="2a679-103">Constantes de propriété de périphérique de scanneur</span><span class="sxs-lookup"><span data-stu-id="2a679-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="2a679-104">Les périphériques matériels WIA (Windows Image Acquisition) ont des valeurs de propriété qui sont stockées dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="2a679-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="2a679-105">Pour plus d’informations, consultez [**constantes de propriété d’appareil courantes**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="2a679-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="2a679-106">Les constantes de propriété d’appareil suivantes, avec leurs chaînes associées, sont spécifiques aux scanneurs d’images numériques.</span><span class="sxs-lookup"><span data-stu-id="2a679-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="2a679-107">Le préfixe « WIA \_ DPS \_ » indique une propriété d’appareil pour les périphériques de scanneur et est la Convention d’affectation de noms utilisée dans C/C++.</span><span class="sxs-lookup"><span data-stu-id="2a679-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="2a679-108">À des fins de script, ces constantes utilisent le préfixe « ScannerDevice » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="2a679-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="2a679-109">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="2a679-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2a679-110">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="2a679-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2a679-111">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="2a679-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="2a679-113">Cette propriété est prise en charge uniquement sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="2a679-114">Contient un identificateur d’instance de fonction unique pour un périphérique de scanneur de services Web.</span><span class="sxs-lookup"><span data-stu-id="2a679-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="2a679-115">Cet identificateur représente le service Web sur le périphérique de scanneur avec lequel le mini-pilote WIA communique.</span><span class="sxs-lookup"><span data-stu-id="2a679-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="2a679-116">Aucune hypothèse relative à la forme de cet identificateur ne doit être faite.</span><span class="sxs-lookup"><span data-stu-id="2a679-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="2a679-117">Le mini-pilote WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="2a679-118">Les applications WIA peuvent utiliser la valeur de WIA_DPS_DEVICE_ID pour trouver, à l’aide de l’API de détection de fonction, l’objet d’instance de fonction représentant le périphérique Web services scanner utilisé dans la session WIA 2,0 actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a679-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="2a679-119">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="2a679-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a679-121">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="2a679-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="2a679-122">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="2a679-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a679-124">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="2a679-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="2a679-125">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="2a679-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a679-127">Contient les fonctionnalités du scanneur.</span><span class="sxs-lookup"><span data-stu-id="2a679-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="2a679-128">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="2a679-129">Une application lit cette propriété pour déterminer si le scanneur a un plateau, un chargeur de documents ou un duplexeur installé.</span><span class="sxs-lookup"><span data-stu-id="2a679-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="2a679-130">Cette propriété est également utilisée pour définir plus précisément les fonctionnalités installées.</span><span class="sxs-lookup"><span data-stu-id="2a679-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="2a679-131">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="2a679-132">Le tableau suivant décrit les constantes qui sont valides uniquement avec Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a679-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-133">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2a679-133">Flags</span></span></th>
<th><span data-ttu-id="2a679-134">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="2a679-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="2a679-136">Un gestionnaire de documents automatique est installé sur le scanneur.</span><span class="sxs-lookup"><span data-stu-id="2a679-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-137">Le tableau suivant décrit les constantes qui sont valides uniquement avec Windows 7 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-138">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2a679-138">Flags</span></span></th>
<th><span data-ttu-id="2a679-139">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="2a679-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="2a679-141">L’appareil prend en charge la configuration avancée de l’analyse duplex.</span><span class="sxs-lookup"><span data-stu-id="2a679-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="2a679-142">Utilisez WIA_IPS_DUPLEX_SETTINGS pour basculer entre l’utilisation de configurations duplex de base et avancées.</span><span class="sxs-lookup"><span data-stu-id="2a679-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="2a679-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="2a679-144">Le scanneur peut détecter lorsque la carte de transparence/film est prête à être analysée.</span><span class="sxs-lookup"><span data-stu-id="2a679-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="2a679-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="2a679-146">Le scanneur peut détecter les documents dans le stockage interne.</span><span class="sxs-lookup"><span data-stu-id="2a679-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="2a679-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="2a679-148">Le scanneur est équipé d’un adaptateur d’analyse de transparence/film.</span><span class="sxs-lookup"><span data-stu-id="2a679-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-149">STOR</span><span class="sxs-lookup"><span data-stu-id="2a679-149">STOR</span></span></td>
<td><span data-ttu-id="2a679-150">Le scanneur est équipé d’un dispositif de stockage d’images interne.</span><span class="sxs-lookup"><span data-stu-id="2a679-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-151">Le tableau suivant décrit les constantes qui sont valides avec Windows XP ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2a679-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-152">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2a679-152">Flags</span></span></th>
<th><span data-ttu-id="2a679-153">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="2a679-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="2a679-155">Le scanneur peut détecter un document dans le chargeur.</span><span class="sxs-lookup"><span data-stu-id="2a679-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="2a679-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="2a679-157">Le scanneur peut détecter un document sur le plateau à plat.</span><span class="sxs-lookup"><span data-stu-id="2a679-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="2a679-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="2a679-159">Le scanneur peut détecter un document dans le chargeur uniquement en analysant.</span><span class="sxs-lookup"><span data-stu-id="2a679-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-160">DUP</span><span class="sxs-lookup"><span data-stu-id="2a679-160">DUP</span></span></td>
<td><span data-ttu-id="2a679-161">Le scanneur a un duplex.</span><span class="sxs-lookup"><span data-stu-id="2a679-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-162">ALIMENTAIRE</span><span class="sxs-lookup"><span data-stu-id="2a679-162">FEED</span></span></td>
<td><span data-ttu-id="2a679-163">Un gestionnaire de documents automatique est installé sur le scanneur.</span><span class="sxs-lookup"><span data-stu-id="2a679-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-164">PLATE</span><span class="sxs-lookup"><span data-stu-id="2a679-164">FLAT</span></span></td>
<td><span data-ttu-id="2a679-165">Le scanneur a un plateau à plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-166">Le tableau suivant décrit les constantes qui sont valides uniquement avec Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a679-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="2a679-167">Ces valeurs ont été dépréciées pour Windows 7 et Windows Vista et ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="2a679-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-168">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2a679-168">Flags</span></span></th>
<th><span data-ttu-id="2a679-169">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="2a679-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="2a679-171">Le scanneur peut détecter une demande d’analyse duplex de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a679-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="2a679-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="2a679-173">Le scanneur peut déterminer à quel moment le duplexeur est installé.</span><span class="sxs-lookup"><span data-stu-id="2a679-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="2a679-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="2a679-175">Le scanneur peut déterminer quand le chargeur automatique de documents est installé.</span><span class="sxs-lookup"><span data-stu-id="2a679-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="2a679-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-177">Cette propriété n’est pas prise en charge dans Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="2a679-178">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-179">Contient la source et le mode d’acquisition du scanneur en cours. Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-180">Une application lit cette propriété pour déterminer la source d’acquisition actuelle du scanneur ou pour écrire cette propriété afin de définir la source et le mode du scanneur.</span><span class="sxs-lookup"><span data-stu-id="2a679-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="2a679-181">En outre, les applications utilisent cette propriété pour activer et désactiver les fonctionnalités duplex.</span><span class="sxs-lookup"><span data-stu-id="2a679-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="2a679-182">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="2a679-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="2a679-183">Le tableau suivant contient les dix constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-184">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2a679-184">Flags</span></span></th>
<th><span data-ttu-id="2a679-185">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-186">FEEDER</span><span class="sxs-lookup"><span data-stu-id="2a679-186">FEEDER</span></span></td>
<td><span data-ttu-id="2a679-187">Analyse à l’aide du chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="2a679-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-188">Scanner</span><span class="sxs-lookup"><span data-stu-id="2a679-188">FLATBED</span></span></td>
<td><span data-ttu-id="2a679-189">Numérisez à l’aide du plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-190">DUPLEX</span><span class="sxs-lookup"><span data-stu-id="2a679-190">DUPLEX</span></span></td>
<td><span data-ttu-id="2a679-191">Analyse à l’aide d’opérations duplex.</span><span class="sxs-lookup"><span data-stu-id="2a679-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="2a679-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="2a679-193">Active l’alimentation automatique du document suivant après une analyse.</span><span class="sxs-lookup"><span data-stu-id="2a679-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="2a679-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="2a679-195">Commencez par analyser le recto du document.</span><span class="sxs-lookup"><span data-stu-id="2a679-195">Scan the front of the document first.</span></span> <span data-ttu-id="2a679-196">Cette valeur est valide lorsque DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="2a679-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="2a679-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="2a679-198">Commencez par analyser le verso du document.</span><span class="sxs-lookup"><span data-stu-id="2a679-198">Scan the back of the document first.</span></span> <span data-ttu-id="2a679-199">Cette valeur est valide lorsque DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="2a679-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="2a679-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="2a679-201">Analysez l’avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="2a679-201">Scan the front only.</span></span> <span data-ttu-id="2a679-202">Cette valeur est valide lorsque DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="2a679-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="2a679-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="2a679-204">Analyser l’arrière uniquement.</span><span class="sxs-lookup"><span data-stu-id="2a679-204">Scan the back only.</span></span> <span data-ttu-id="2a679-205">Cette valeur est valide lorsque DUPLEX est défini.</span><span class="sxs-lookup"><span data-stu-id="2a679-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="2a679-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="2a679-207">Analyse la page suivante du document.</span><span class="sxs-lookup"><span data-stu-id="2a679-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-208">Préalimentation</span><span class="sxs-lookup"><span data-stu-id="2a679-208">PREFEED</span></span></td>
<td><span data-ttu-id="2a679-209">Activez le mode de pré-flux.</span><span class="sxs-lookup"><span data-stu-id="2a679-209">Enable pre-feed mode.</span></span> <span data-ttu-id="2a679-210">Prépositionner le document suivant lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a679-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="2a679-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-212">Contient l’état actuel du plateau installé du scanneur, du chargeur de documents ou du duplexeur.</span><span class="sxs-lookup"><span data-stu-id="2a679-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="2a679-213">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-214">Une application lit cette propriété pour déterminer si le périphérique du scanneur est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a679-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="2a679-215">Il s’agit d’une façon idéale de vérifier si le papier est dans le chargeur avant d’acquérir une image.</span><span class="sxs-lookup"><span data-stu-id="2a679-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="2a679-216">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-217">Le tableau suivant contient les constantes qui sont valides avec cette propriété. Un astérisque \* indique que l’indicateur n’est pas pris en charge dans Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2a679-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="2a679-218">Le symbole <strong>V</strong> indique que l’indicateur est pris en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-219">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2a679-219">Flags</span></span></th>
<th><span data-ttu-id="2a679-220">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="2a679-221">FEED_READY</span></span></td>
<td><span data-ttu-id="2a679-222">Le plateau est prêt à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="2a679-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="2a679-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="2a679-224">Le scanneur a un document sur le plateau à plat.</span><span class="sxs-lookup"><span data-stu-id="2a679-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="2a679-225">DUP_READY</span></span></td>
<td><span data-ttu-id="2a679-226">Le duplexeur est activé et prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a679-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="2a679-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="2a679-228">Le cache plat est en place.</span><span class="sxs-lookup"><span data-stu-id="2a679-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="2a679-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="2a679-230">Le chemin d’accès au papier est couvert et empêche le bon fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="2a679-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="2a679-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="2a679-232">Un document est coincé dans le chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="2a679-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="2a679-234">L’adaptateur de transparence est installé et prêt à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="2a679-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="2a679-236">Le dispositif de stockage interne est prêt.</span><span class="sxs-lookup"><span data-stu-id="2a679-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="2a679-238">Le stockage est plein, aucune opération de chargement n’est possible.</span><span class="sxs-lookup"><span data-stu-id="2a679-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="2a679-240">Une condition de flux multiples s’est produite (généralement avec un PAPER_JAM).</span><span class="sxs-lookup"><span data-stu-id="2a679-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="2a679-242">Une erreur nécessite une intervention de l’utilisateur sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a679-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="2a679-244">Le scanneur n’est pas prêt en raison d’un problème de lampe.</span><span class="sxs-lookup"><span data-stu-id="2a679-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="2a679-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-246">Contient tous les caractères valides qu’une application peut utiliser pour créer des chaînes d’endosseur valides.</span><span class="sxs-lookup"><span data-stu-id="2a679-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="2a679-247">Un endosseur est une imprimante installée sur un scanneur qui imprime un message texte sur chaque page analysée.</span><span class="sxs-lookup"><span data-stu-id="2a679-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="2a679-248">Le minipilote doit valider la valeur de la propriété <strong>WIA_DPS_ENDORSER_STRING</strong> par rapport au jeu de caractères valide dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="2a679-249">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-250">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="2a679-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-252">Contient une chaîne qui doit être approuvée (en d’autres termes, imprimée) sur chaque page analysée par le minipilote.</span><span class="sxs-lookup"><span data-stu-id="2a679-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="2a679-253">Une application définit cette propriété à l’aide du jeu de caractères valide signalé dans la propriété <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="2a679-254">Le minipilote doit approuver les documents uniquement si une chaîne est définie dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="2a679-255">Une chaîne vide signifie que la fonctionnalité de l’endosseur est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2a679-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="2a679-256">Étant donné que le pilote est responsable de l’interprétation de la chaîne d’endossement, votre pilote peut utiliser des caractères spéciaux dans <strong>WIA_DPS_ENDORSER_STRING</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a679-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="2a679-257">Toutefois, seules vos applications comprendront ces caractères.</span><span class="sxs-lookup"><span data-stu-id="2a679-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="2a679-258">Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-259">Un pilote qui prend en charge la propriété <strong>WIA_DPS_ENDORSER_STRING</strong> doit prendre en charge la liste de jetons suivante.</span><span class="sxs-lookup"><span data-stu-id="2a679-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-260">par jeton</span><span class="sxs-lookup"><span data-stu-id="2a679-260">Token</span></span></th>
<th><span data-ttu-id="2a679-261">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-262">$DATE $</span><span class="sxs-lookup"><span data-stu-id="2a679-262">$DATE$</span></span></td>
<td><span data-ttu-id="2a679-263">Date au format AAAA/MM/JJ.</span><span class="sxs-lookup"><span data-stu-id="2a679-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-264">$DAY $</span><span class="sxs-lookup"><span data-stu-id="2a679-264">$DAY$</span></span></td>
<td><span data-ttu-id="2a679-265">Jour au format jj.</span><span class="sxs-lookup"><span data-stu-id="2a679-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="2a679-266">$MONTH$</span></span></td>
<td><span data-ttu-id="2a679-267">Mois de l’année au format MM.</span><span class="sxs-lookup"><span data-stu-id="2a679-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-268">$PAGE _COUNT $</span><span class="sxs-lookup"><span data-stu-id="2a679-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="2a679-269">Nombre de pages transférées.</span><span class="sxs-lookup"><span data-stu-id="2a679-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-270">$TIME $</span><span class="sxs-lookup"><span data-stu-id="2a679-270">$TIME$</span></span></td>
<td><span data-ttu-id="2a679-271">Heure de la journée au format HH : MM : SS.</span><span class="sxs-lookup"><span data-stu-id="2a679-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-272">$YEAR $</span><span class="sxs-lookup"><span data-stu-id="2a679-272">$YEAR$</span></span></td>
<td><span data-ttu-id="2a679-273">Année au format YYYY.</span><span class="sxs-lookup"><span data-stu-id="2a679-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="2a679-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-275">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="2a679-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="2a679-276">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="2a679-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-278">Cette propriété est prise en charge uniquement sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-279">Contient l’adresse SOAP d’un périphérique de scanneur de services Web.</span><span class="sxs-lookup"><span data-stu-id="2a679-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="2a679-280">Le mini-pilote WIA 2,0 crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-281">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="2a679-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-283">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-284">Contient l’enregistrement ou l’alignement horizontal pour les documents placés sur le plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="2a679-285">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-286">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-287">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-288">Constante</span><span class="sxs-lookup"><span data-stu-id="2a679-288">Constant</span></span></th>
<th><span data-ttu-id="2a679-289">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="2a679-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="2a679-291">Le papier est justifié à gauche.</span><span class="sxs-lookup"><span data-stu-id="2a679-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-292">PARTANT</span><span class="sxs-lookup"><span data-stu-id="2a679-292">CENTERED</span></span></td>
<td><span data-ttu-id="2a679-293">Le papier est centré.</span><span class="sxs-lookup"><span data-stu-id="2a679-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="2a679-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="2a679-295">Le papier est justifié à droite.</span><span class="sxs-lookup"><span data-stu-id="2a679-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-296"><strong>Voir aussi</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="2a679-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="2a679-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-299">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-300">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-301">Spécifie la largeur maximale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à partir du plateau d’un scanneur à plat dans la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a679-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="2a679-302">Cette propriété s’applique également aux alimentations automatiques de documents qui déplacent des feuilles vers le plateau d’un scanneur à plat pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a679-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="2a679-303">Cette propriété est obligatoire pour les scanneurs qui ont un plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="2a679-304">À la place, les autres types de scanneurs implémentent la propriété <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="2a679-305">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="2a679-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-307">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-308">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-309">Spécifie la largeur maximale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à partir d’un scanneur de papier portable ou de feuille à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a679-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="2a679-310">Cette propriété s’applique également aux alimentations automatiques de documents qui analysent sans déplacer les feuilles vers le plateau d’un scanneur à plat.</span><span class="sxs-lookup"><span data-stu-id="2a679-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="2a679-311">Cette propriété est obligatoire pour les scanneurs de feuilles, le défilement et les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="2a679-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="2a679-312">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="2a679-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-314">Contient la durée maximale d’analyse d’une page unique avec les paramètres de propriété actuels, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2a679-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="2a679-315">Une application lit cette propriété pour estimer le temps nécessaire à l’analyse d’une page.</span><span class="sxs-lookup"><span data-stu-id="2a679-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="2a679-316">Cela est utile lorsque vous déterminez les conditions d’un appareil qui a cessé de répondre.</span><span class="sxs-lookup"><span data-stu-id="2a679-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="2a679-317">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="2a679-318">Cette propriété est obligatoire pour tous les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="2a679-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="2a679-319">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="2a679-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-321">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-322">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-323">Contient les dimensions horizontales physiques de la plus petite page que le chargeur de documents du scanneur peut analyser, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="2a679-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="2a679-324">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-325">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-326"><strong>Voir aussi</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="2a679-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="2a679-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-329">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-330">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-331">Contient les dimensions verticales physiques de la plus petite page que le chargeur de documents du scanneur peut analyser, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="2a679-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="2a679-332">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-333">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-334"><strong>Voir aussi</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="2a679-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="2a679-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-337">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-338">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-339">Résolution optique horizontale.</span><span class="sxs-lookup"><span data-stu-id="2a679-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="2a679-340">Résolution optique horizontale la plus élevée prise en charge en PPP.</span><span class="sxs-lookup"><span data-stu-id="2a679-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="2a679-341">Cette propriété est une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="2a679-341">This property is a single value.</span></span> <span data-ttu-id="2a679-342">Il ne s’agit pas d’une liste de toutes les résolutions qui peuvent être générées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a679-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="2a679-343">Au lieu de cela, il s’agit de la résolution des optiques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a679-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="2a679-344">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="2a679-345">Cette propriété est obligatoire pour tous les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="2a679-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="2a679-346">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="2a679-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-348">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-349">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-350">Résolution optique verticale.</span><span class="sxs-lookup"><span data-stu-id="2a679-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="2a679-351">Résolution optique verticale la plus élevée prise en charge en PPP.</span><span class="sxs-lookup"><span data-stu-id="2a679-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="2a679-352">Cette propriété est une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="2a679-352">This property is a single value.</span></span> <span data-ttu-id="2a679-353">Il ne s’agit pas d’une liste de toutes les résolutions générées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a679-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="2a679-354">Au lieu de cela, il s’agit de la résolution des optiques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a679-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="2a679-355">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="2a679-356">Cette propriété est obligatoire pour tous les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="2a679-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="2a679-357">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="2a679-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-359">Contient le paramètre d’orientation actuel. Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-360">Une application définit la propriété <strong>WIA_DPS_ORIENTATION</strong> pour définir l’orientation d’origine d’une page ou d’une image à acquérir.</span><span class="sxs-lookup"><span data-stu-id="2a679-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="2a679-361">Pour plus d’informations sur l’utilisation de WIA_DPS_ORIENTATION, consultez <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="2a679-362">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2a679-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2a679-363">Le tableau suivant contient les quatre constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-364">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a679-364">Value</span></span></th>
<th><span data-ttu-id="2a679-365">Définitment</span><span class="sxs-lookup"><span data-stu-id="2a679-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-366">JARDIN</span><span class="sxs-lookup"><span data-stu-id="2a679-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="2a679-367">rotation de 90 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</span><span class="sxs-lookup"><span data-stu-id="2a679-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-368">Aperçu</span><span class="sxs-lookup"><span data-stu-id="2a679-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="2a679-369">0 degré.</span><span class="sxs-lookup"><span data-stu-id="2a679-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="2a679-370">ROT180</span></span></td>
<td><span data-ttu-id="2a679-371">rotation de 180 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</span><span class="sxs-lookup"><span data-stu-id="2a679-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="2a679-372">ROT270</span></span></td>
<td><span data-ttu-id="2a679-373">rotation de 270 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</span><span class="sxs-lookup"><span data-stu-id="2a679-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-374"><strong>Voir aussi</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="2a679-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a679-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="2a679-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-377">Couleur utilisée pour remplir le bloc lorsqu’il n’y a pas assez de données image pour remplir une mémoire tampon demandée.</span><span class="sxs-lookup"><span data-stu-id="2a679-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="2a679-378">Cette propriété est implémentée pour les scanneurs qui complètent la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2a679-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="2a679-379">Cette propriété est facultative pour tous les scanneurs.</span><span class="sxs-lookup"><span data-stu-id="2a679-379">This property is optional for all scanners.</span></span> <span data-ttu-id="2a679-380">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-381">Type : <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-382">Le format des informations de couleur est <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="2a679-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-384">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-385">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-386">Contient la hauteur, en millièmes de pouce, de la page actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2a679-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="2a679-387">Le minipilote crée et gère la propriété <strong>WIA_DPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="2a679-388">Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a679-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="2a679-389">Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la hauteur de la page dont la propriété <strong>WIA_DPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM (qui est une valeur de la propriété <strong>WIA_DPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="2a679-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="2a679-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> doit être synchronisé avec <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, qui indique la hauteur, en pixels, de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="2a679-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="2a679-391">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="2a679-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-393">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-394">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-395">Contient la taille de la page actuellement sélectionnée pour être analysée.</span><span class="sxs-lookup"><span data-stu-id="2a679-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="2a679-396">Pour sélectionner les dimensions de la page à analyser, une application définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="2a679-397">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-398">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2a679-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2a679-399">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-400">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a679-400">Value</span></span></th>
<th><span data-ttu-id="2a679-401">Définition</span><span class="sxs-lookup"><span data-stu-id="2a679-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="2a679-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="2a679-403">8267 X 11692 (orientation PORTRAIT)</span><span class="sxs-lookup"><span data-stu-id="2a679-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="2a679-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="2a679-405">Défini par les valeurs des propriétés <strong>WIA_DPS_PAGE_HEIGHT</strong> et <strong>WIA_DPS_PAGE_WIDTH</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="2a679-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="2a679-407">8500 X 11000 (orientation PORTRAIT)</span><span class="sxs-lookup"><span data-stu-id="2a679-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-408">La valeur de la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> détermine l’orientation de la page actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2a679-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="2a679-409">Les propriétés <strong>WIA_DPS_PAGE_WIDTH</strong> et <strong>WIA_DPS_PAGE_HEIGHT</strong> signalent les dimensions de la page, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="2a679-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="2a679-410">Notez que ces propriétés doivent être accordées avec <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong>, qui contiennent les dimensions de la page en pixels.</span><span class="sxs-lookup"><span data-stu-id="2a679-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="2a679-411">Les valeurs valides de type WIA_PROP_LIST doivent dépendre des paramètres valides de la propriété <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="2a679-412">Si l’appareil ne peut pas analyser les documents orientés paysage avec un paramètre WIA_PAGE_A4, WIA_PAGE_A4 ne doit pas apparaître dans la liste des valeurs valides pour la propriété <strong>WIA_DPS_PAGE_SIZE</strong> lorsque <strong>WIA_IPS_ORIENTATION</strong> a la valeur Lanscape.</span><span class="sxs-lookup"><span data-stu-id="2a679-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="2a679-413">Si une application définit <strong>WIA_DPS_PAGE_SIZE</strong> sur une valeur autre que WIA_PAGE_CUSTOM, le minipilote doit ajuster les valeurs de <strong>WIA_DPS_PAGE_WIDTH</strong> et <strong>WIA_DPS_PAGE_HEIGHT</strong> aux dimensions de la page, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="2a679-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="2a679-414">Elle doit également ajuster les valeurs de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> et <strong>WIA_IPS_YEXTENT</strong> sur les dimensions de la page en pixels.</span><span class="sxs-lookup"><span data-stu-id="2a679-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="2a679-415">Si un paramètre d’extension (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> ou <strong>WIA_IPS_YEXTENT</strong>) est changé en une valeur qui ne correspond pas au paramètre de taille de page actuel, le minipilote doit changer la valeur de la propriété <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="2a679-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="2a679-416">Le minipilote doit également modifier <strong>WIA_DPS_PAGE_WIDTH</strong> ou <strong>WIA_DPS_PAGE_HEIGHT</strong> conformément au nouveau paramètre d’extension.</span><span class="sxs-lookup"><span data-stu-id="2a679-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="2a679-417">Si <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> a la valeur Lanscape, les paramètres d’étendue sont &quot; retournés. &quot; Par exemple, si une application définit <strong>WIA_DPS_PAGE_SIZE</strong> sur WIA_PAGE_A4, le minipilote doit définir <strong>WIA_DPS_PAGE_WIDTH</strong> sur 11692 et <strong>WIA_DPS_PAGE_HEIGHT</strong> sur 8267.</span><span class="sxs-lookup"><span data-stu-id="2a679-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="2a679-418">(Le minipilote doit également définir <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> en conséquence). Notez que si <strong>WIA_DPS_PAGE_SIZE</strong> est défini sur WIA_PAGE_CUSTOM, le paramètre d’orientation n’est pas utilisé pour déterminer les dimensions d’étendue de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="2a679-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="2a679-419">Le minipilote est chargé de s’assurer que la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> est en accord avec la zone de sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a679-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="2a679-420">Si une application remplace la valeur de <strong>WIA_IPS_ORIENTATION</strong> par une valeur non valide pour la taille de page actuellement sélectionnée, le minipilote doit changer la valeur de <strong>WIA_DPS_PAGE_SIZE</strong> en une taille de page prise en charge par la nouvelle valeur d’orientation.</span><span class="sxs-lookup"><span data-stu-id="2a679-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="2a679-421">Si une application définit la propriété <strong>WIA_DPS_PAGE_SIZE</strong> sur WIA_PAGE_CUSTOM, la zone de sélection actuelle n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="2a679-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="2a679-422">Le minipilote WIA doit obtenir la disposition actuelle de l’image, en commençant par les paramètres actuels des propriétés <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> et <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="2a679-423">Si le paramètre de taille de page produit une zone de sélection située en dehors de la vitre du scanneur, le minipilote doit automatiquement ajuster les valeurs des propriétés <strong>WIA_IPS_XPOS</strong> et <strong>WIA_IPS_YPOS</strong> aux paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="2a679-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="2a679-424">Si les propriétés <strong>WIA_DPS_PAGE_SIZE</strong> et <strong>WIA_IPS_ORIENTATION</strong> sont définies en même temps et qu’elles ne sont pas valides lorsqu’elles sont appliquées en combinaison, le minipilote doit faire échouer les paramètres de l’application en renvoyant une erreur dans le <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv ::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="2a679-425">.</span><span class="sxs-lookup"><span data-stu-id="2a679-425">.</span></span></p>
<p><span data-ttu-id="2a679-426">Les quatre exemples suivants illustrent différents scénarios de <strong>WIA_DPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="2a679-427">Le pilote signale les paramètres.</span><span class="sxs-lookup"><span data-stu-id="2a679-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="2a679-428">Une application définit la propriété <strong>WIA_DPS_PAGE_SIZE</strong> sur WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="2a679-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="2a679-429">Une application définit la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> sur Lanscape.</span><span class="sxs-lookup"><span data-stu-id="2a679-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="2a679-430">Une application remplace la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> par une valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="2a679-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="2a679-431"><strong>Exemple 1 : le minipilote signale les paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="2a679-432">Dans l’exemple suivant, le minipilote définit une zone de sélection personnalisée avant qu’une application définisse des propriétés WIA.</span><span class="sxs-lookup"><span data-stu-id="2a679-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="2a679-433">Dans ce cas, la zone de sélection représente l’ensemble du plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-433">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><span data-ttu-id="2a679-434"><strong>Exemple 2 : une application définit la</strong> <strong></strong><strong>propriété WIA_DPS_PAGE_SIZE sur WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="2a679-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><span data-ttu-id="2a679-435"><strong>Exemple 3 : une application définit la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propriété WIA_IPS_ORIENTATION sur Lanscape</strong>  </span><span class="sxs-lookup"><span data-stu-id="2a679-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="2a679-436">Le lit physique doit pouvoir acquérir une page qui était à l’origine en orientation paysage.</span><span class="sxs-lookup"><span data-stu-id="2a679-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><span data-ttu-id="2a679-437"><strong>Exemple 4 : une application remplace la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propriété WIA_IPS_XEXTENT par une valeur inférieure</strong>  </span><span class="sxs-lookup"><span data-stu-id="2a679-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="2a679-438">Dans l’exemple suivant, une application remplace la valeur de la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> par 1000.</span><span class="sxs-lookup"><span data-stu-id="2a679-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="2a679-439">Le minipilote doit supposer que la nouvelle valeur contenue dans <strong>WIA_IPS_XEXTENT</strong> n’est plus valide pour la propriété <strong>WIA_DPS_PAGE_SIZE</strong> et doit donc remplacer <strong>WIA_DPS_PAGE_SIZE</strong> par WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="2a679-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="2a679-440">Le minipilote doit également ajuster <strong>WIA_DPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a679-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="2a679-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-442">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-443">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-444">Contient la largeur de la page actuelle sélectionnée, en millièmes de pouce.</span><span class="sxs-lookup"><span data-stu-id="2a679-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="2a679-445">Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a679-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="2a679-446">Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la largeur de la page dont la propriété <strong>WIA_DPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="2a679-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="2a679-447"><strong>WIA_DPS_PAGE_WIDTH</strong> doit être synchronisée avec la valeur de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, qui indique la largeur, en pixels, de la page à analyser.</span><span class="sxs-lookup"><span data-stu-id="2a679-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="2a679-448">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-449">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="2a679-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-451">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-452">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-453">Contient le nombre actuel de pages à acquérir à partir d’un chargeur automatique de documents.</span><span class="sxs-lookup"><span data-stu-id="2a679-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="2a679-454">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-455">Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zéro jusqu’au nombre maximal de pages que le chargeur de documents peut contenir)</span><span class="sxs-lookup"><span data-stu-id="2a679-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="2a679-456">Une application lit cette propriété pour déterminer la capacité de page du chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="2a679-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="2a679-457">L’application définit également cette propriété sur le nombre de pages qu’elle va analyser.</span><span class="sxs-lookup"><span data-stu-id="2a679-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-458">Si le mode duplex est activé (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> est défini sur alimentation | DUPLEX), <strong>WIA_DPS_PAGES</strong> est toujours égal au nombre de pages à analyser.</span><span class="sxs-lookup"><span data-stu-id="2a679-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-459">Une feuille de papier contient automatiquement deux pages si le DUPLEX est activé, même si le côté arrière de la page est vide.</span><span class="sxs-lookup"><span data-stu-id="2a679-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="2a679-460">Si vous affectez la valeur 1 à <strong>WIA_DPS_PAGES</strong> , un scanneur traite l’un des côtés de la page.</span><span class="sxs-lookup"><span data-stu-id="2a679-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="2a679-461">Si un scanneur ne parvient pas à analyser un seul côté d’une page alors qu’il est en mode duplex, le <strong>WIA_DPS_PAGES</strong> valeur valide pour le membre Inc de la structure WIA_PROPERTY_INFO doit être changée en 2.</span><span class="sxs-lookup"><span data-stu-id="2a679-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="2a679-462">Cette valeur signale à l’application qu’elle doit demander des pages par multiples de deux.</span><span class="sxs-lookup"><span data-stu-id="2a679-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="2a679-463">La valeur zéro signifie que <em>toutes les</em> pages qui sont actuellement chargées dans le chargeur de documents doivent être analysées.</span><span class="sxs-lookup"><span data-stu-id="2a679-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="2a679-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-465">Spécifie la couleur du plateau dans l’arrière de la feuille à analyser.</span><span class="sxs-lookup"><span data-stu-id="2a679-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="2a679-466">Cette propriété est facultative pour les scanneurs qui ont un plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="2a679-467">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-468">Type : <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-469">Le format des informations de couleur est <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="2a679-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-471">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-472">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-473">Indique le mode d’aperçu pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="2a679-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="2a679-474">Une application définit cette propriété pour placer l’appareil dans un mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="2a679-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="2a679-475">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="2a679-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="2a679-476">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-477">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a679-477">Value</span></span></th>
<th><span data-ttu-id="2a679-478">Définition</span><span class="sxs-lookup"><span data-stu-id="2a679-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="2a679-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="2a679-480">L’application effectue une analyse finale.</span><span class="sxs-lookup"><span data-stu-id="2a679-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="2a679-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="2a679-482">L’application effectue une analyse de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="2a679-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="2a679-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="2a679-484">Contient une valeur qui indique si le scanneur met en cache des pages dans une mémoire tampon de scanneur avant de les envoyer à l’application.</span><span class="sxs-lookup"><span data-stu-id="2a679-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="2a679-485">Une valeur de zéro désactive l’analyse à l’avance et aucune page n’est analysée.</span><span class="sxs-lookup"><span data-stu-id="2a679-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="2a679-486">Les transferts de données normaux sur l’élément d’analyse mis en mémoire tampon récupèrent les pages mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2a679-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="2a679-487">Les propriétés WIA ne peuvent pas être modifiées lors d’une opération d’analyse anticipée.</span><span class="sxs-lookup"><span data-stu-id="2a679-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="2a679-488">Cette propriété est facultative.</span><span class="sxs-lookup"><span data-stu-id="2a679-488">This property is optional.</span></span></p>
<p><span data-ttu-id="2a679-489">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zéro au nombre maximal de pages que le chargeur de documents peut contenir.</span><span class="sxs-lookup"><span data-stu-id="2a679-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="2a679-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-491">Cette propriété est prise en charge uniquement par Windows 7 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-492">Indique la source d’entrée à partir de laquelle effectuer l’analyse, ou l’emplacement de stockage à partir duquel les données sont transférées.</span><span class="sxs-lookup"><span data-stu-id="2a679-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="2a679-493">Un événement d’analyse informe l’application que l’utilisateur a lancé une analyse, mais l’événement ne fournit pas le nom de l’élément WIA qui représente la source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2a679-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="2a679-494">Le gestionnaire d’événements de l’application peut interroger la propriété de WIA_DPS_SCAN_AVAILABLE_ITEM de l’élément racine pour obtenir le nom de l’élément source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2a679-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="2a679-495">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zéro au nombre maximal de pages que le chargeur de documents peut contenir.</span><span class="sxs-lookup"><span data-stu-id="2a679-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="2a679-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-497">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-498">Contient l’ID de service d’un périphérique de scanneur de services Web.</span><span class="sxs-lookup"><span data-stu-id="2a679-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="2a679-499">Le mini-pilote WIA 2,0 crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-500">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="2a679-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-502">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-503">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-504">Contient les détections d’alignement, d’alignement et de bord pour les documents placés sur le plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="2a679-505">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="2a679-506">Cette propriété indique comment la feuille est positionnée horizontalement sur la tête de numérisation d’un lecteur de poche ou d’un scanneur à feuille.</span><span class="sxs-lookup"><span data-stu-id="2a679-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="2a679-507">La propriété permet de prédire où un document est placé sur l’en-tête d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a679-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="2a679-508">Pour les scanneurs qui prennent en charge plusieurs têtes d’analyse, cette propriété est relative à la tête d’analyse la plus haut.</span><span class="sxs-lookup"><span data-stu-id="2a679-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="2a679-509">Cette propriété est obligatoire pour les scanneurs de feuille, d’alimentation et de défilement.</span><span class="sxs-lookup"><span data-stu-id="2a679-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="2a679-510">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-511">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-512">Constante</span><span class="sxs-lookup"><span data-stu-id="2a679-512">Constant</span></span></th>
<th><span data-ttu-id="2a679-513">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="2a679-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="2a679-515">La feuille est positionnée à gauche par rapport à la tête de numérisation.</span><span class="sxs-lookup"><span data-stu-id="2a679-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-516">PARTANT</span><span class="sxs-lookup"><span data-stu-id="2a679-516">CENTERED</span></span></td>
<td><span data-ttu-id="2a679-517">La feuille est centrée sur la tête de numérisation.</span><span class="sxs-lookup"><span data-stu-id="2a679-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="2a679-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="2a679-519">La feuille est positionnée à droite par rapport à la tête de numérisation.</span><span class="sxs-lookup"><span data-stu-id="2a679-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="2a679-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-521">Cette propriété n’est pas prise en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2a679-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="2a679-522">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-523">Indique si un élément a besoin d’un contrôle d’aperçu affiché pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a679-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="2a679-524">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-525">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-526">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-527">Constante</span><span class="sxs-lookup"><span data-stu-id="2a679-527">Constant</span></span></th>
<th><span data-ttu-id="2a679-528">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="2a679-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="2a679-530">Affichez un contrôle d’aperçu pour l’utilisateur, car ce dernier peut effectuer une préversion.</span><span class="sxs-lookup"><span data-stu-id="2a679-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="2a679-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="2a679-532">N’affiche pas un contrôle d’aperçu pour l’utilisateur, car cet appareil ne peut pas effectuer d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="2a679-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="2a679-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-534">Cette propriété est prise en charge uniquement par Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-535">Utilisé par le service WIA pour informer le mini-pilote du nom du compte d’utilisateur (y compris le nom de domaine réseau, le cas échéant) de la session dans laquelle l’application WIA en cours est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2a679-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="2a679-536">Il s’agit d’une propriété d’élément racine, gérée par le service WIA.</span><span class="sxs-lookup"><span data-stu-id="2a679-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="2a679-537">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="2a679-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-539">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-540">Contient l’inscription, ou l’alignement vertical et la détection des bords, pour les documents placés sur le plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="2a679-541">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="2a679-542">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="2a679-543">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a679-544">Constante</span><span class="sxs-lookup"><span data-stu-id="2a679-544">Constant</span></span></th>
<th><span data-ttu-id="2a679-545">Description</span><span class="sxs-lookup"><span data-stu-id="2a679-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a679-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="2a679-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="2a679-547">Le papier est aligné en haut.</span><span class="sxs-lookup"><span data-stu-id="2a679-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a679-548">PARTANT</span><span class="sxs-lookup"><span data-stu-id="2a679-548">CENTERED</span></span></td>
<td><span data-ttu-id="2a679-549">Le papier est centré.</span><span class="sxs-lookup"><span data-stu-id="2a679-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a679-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="2a679-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="2a679-551">Le papier est justifié en bas.</span><span class="sxs-lookup"><span data-stu-id="2a679-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2a679-552"><strong>Voir aussi</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a679-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="2a679-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="2a679-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="2a679-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-555">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-556">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-557">Spécifie la hauteur maximale, en millièmes de pouce, qui est analysée sur l’axe vertical (Y) à partir du plateau d’un scanneur à plat dans la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a679-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="2a679-558">Cette propriété s’applique également aux alimentations automatiques de documents, qui déplacent les feuilles vers le plateau d’un scanneur à plat à des fins de numérisation.</span><span class="sxs-lookup"><span data-stu-id="2a679-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="2a679-559">Cette propriété est obligatoire pour les scanneurs qui ont un plateau.</span><span class="sxs-lookup"><span data-stu-id="2a679-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="2a679-560">À la place, les autres types de scanneurs implémentent la propriété <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a679-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="2a679-561">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="2a679-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="2a679-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2a679-563">Cette propriété n’est pas prise en charge avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a679-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="2a679-564">Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2a679-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="2a679-565">Spécifie la hauteur maximale, en millièmes de pouce, qui est numérisée sur l’axe vertical (Y) à partir d’un scanneur de papier portable ou de feuille à la résolution actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a679-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="2a679-566">Cette propriété s’applique également aux alimentations automatiques de documents qui analysent sans déplacer les feuilles vers le plateau d’un scanneur à plat.</span><span class="sxs-lookup"><span data-stu-id="2a679-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="2a679-567">Cette propriété est obligatoire pour les scanneurs feuille à alimentation.</span><span class="sxs-lookup"><span data-stu-id="2a679-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="2a679-568">Les scanneurs à défilement et les scanneurs de la main ne doivent pas implémenter cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2a679-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="2a679-569">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="2a679-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="2a679-570">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a679-570">Requirements</span></span>



| <span data-ttu-id="2a679-571">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a679-571">Requirement</span></span> | <span data-ttu-id="2a679-572">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a679-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2a679-573">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a679-573">Minimum supported client</span></span><br/> | <span data-ttu-id="2a679-574">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a679-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2a679-575">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a679-575">Minimum supported server</span></span><br/> | <span data-ttu-id="2a679-576">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a679-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2a679-577">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a679-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a679-578"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a679-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
