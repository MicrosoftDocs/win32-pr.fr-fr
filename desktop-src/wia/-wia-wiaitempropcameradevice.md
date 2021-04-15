---
description: Les périphériques matériels WIA (Windows Image Acquisition) ont des valeurs de propriété qui sont stockées dans le Registre Windows. Pour plus d’informations, consultez constantes de propriété d’appareil courantes.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Constantes de propriété de périphérique d’appareil photo (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485041"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="e562d-104">Constantes de propriété de périphérique d’appareil photo</span><span class="sxs-lookup"><span data-stu-id="e562d-104">Camera Device Property Constants</span></span>

<span data-ttu-id="e562d-105">Les périphériques matériels WIA (Windows Image Acquisition) ont des valeurs de propriété qui sont stockées dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="e562d-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="e562d-106">Pour plus d’informations, consultez [**constantes de propriété d’appareil courantes**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="e562d-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="e562d-107">Les constantes de propriété d’appareil suivantes, avec leurs chaînes associées, sont spécifiques aux appareils photo numériques.</span><span class="sxs-lookup"><span data-stu-id="e562d-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="e562d-108">Le préfixe « WIA \_ DPC \_ » indique une propriété d’appareil pour les appareils photo et est la Convention d’affectation de noms utilisée en C/C++.</span><span class="sxs-lookup"><span data-stu-id="e562d-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="e562d-109">À des fins de script, ces constantes utilisent le préfixe « CameraDevice » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="e562d-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="e562d-110">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="e562d-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="e562d-111">WIA ne prend pas en charge les caméras dans Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e562d-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="e562d-112">Pour ces versions de Windows, utilisez l’API Windows Mobile Device (WPD) décrite dans le kit de développement de pilotes (DDK) Windows pour obtenir des images à partir d’appareils photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e562d-113">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e562d-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e562d-114">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="e562d-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e562d-116">Nombre d’images prises par l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="e562d-117">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="e562d-118">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="e562d-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e562d-120">Nombre d’images pouvant être prises, en fonction des paramètres de propriété actuels.</span><span class="sxs-lookup"><span data-stu-id="e562d-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="e562d-121">Si ces paramètres changent et que les modifications affectent la taille des images générées par l’appareil photo, le minipilote WIA doit mettre à jour le nombre d’images restantes.</span><span class="sxs-lookup"><span data-stu-id="e562d-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="e562d-122">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="e562d-123">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="e562d-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e562d-125">Indique le mode d’exposition actuel de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="e562d-126">Une application modifie cette propriété pour contrôler le mode d’exposition de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="e562d-127">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="e562d-128">Le tableau suivant contient les sept constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-129">Mode exposition</span><span class="sxs-lookup"><span data-stu-id="e562d-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="e562d-130">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="e562d-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="e562d-132">La vitesse et l’ouverture de l’obturateur sont définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e562d-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="e562d-134">La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="e562d-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="e562d-136">L’ouverture est définie par l’utilisateur et l’appareil photo définit automatiquement la vitesse d’obturation.</span><span class="sxs-lookup"><span data-stu-id="e562d-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="e562d-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="e562d-138">La vitesse d’obturation est définie par l’utilisateur et l’appareil photo définit automatiquement l’ouverture.</span><span class="sxs-lookup"><span data-stu-id="e562d-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="e562d-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="e562d-140">La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo, optimisée pour les sujets toujours sujets.</span><span class="sxs-lookup"><span data-stu-id="e562d-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="e562d-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="e562d-142">La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo, optimisée pour les scènes contenant un mouvement rapide.</span><span class="sxs-lookup"><span data-stu-id="e562d-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="e562d-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="e562d-144">La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo, optimisé pour la photographie en portrait.</span><span class="sxs-lookup"><span data-stu-id="e562d-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="e562d-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-146">Permet d’ajuster le point d’ensemble du contrôle d’exposition automatique de l’appareil photo numérique.</span><span class="sxs-lookup"><span data-stu-id="e562d-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="e562d-147">Par exemple, un paramètre de zéro ne change pas le niveau d’exposition automatique défini par l’usine.</span><span class="sxs-lookup"><span data-stu-id="e562d-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="e562d-148">Les unités sont des &quot; arrêts &quot; mis à l’échelle à l’aide d’un facteur de 1000, afin d’autoriser les valeurs d’arrêt fractionnaires.</span><span class="sxs-lookup"><span data-stu-id="e562d-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="e562d-149">Un paramètre de 2000 correspond à deux arrêts supplémentaires (quatre fois plus d’énergie sur le capteur), ce qui génère des images plus claires.</span><span class="sxs-lookup"><span data-stu-id="e562d-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="e562d-150">Un paramètre de-1000 correspond à une exposition moins faible (une demie de l’énergie sur le capteur) produisant des images plus sombres.</span><span class="sxs-lookup"><span data-stu-id="e562d-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="e562d-151">Les valeurs des paramètres sont dans le système additif d’unités d’exposition photographique (APEX).</span><span class="sxs-lookup"><span data-stu-id="e562d-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="e562d-152">Cette propriété peut être exprimée sous la forme d’une liste ou d’une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="e562d-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="e562d-153">Cette propriété est généralement utilisée uniquement lorsque la propriété <strong>WIA_DPC_EXPOSURE_MODE</strong> de l’appareil est définie sur EXPOSUREMODE_MANUAL.</span><span class="sxs-lookup"><span data-stu-id="e562d-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="e562d-154">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="e562d-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="e562d-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-156">Correspond à la vitesse d’obturation, en secondes, mise à l’échelle par 10 000.</span><span class="sxs-lookup"><span data-stu-id="e562d-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="e562d-157">En règle générale, l’appareil utilise cette propriété uniquement lorsque la propriété <strong>WIA_DPC_EXPOSURE_MODE</strong> est définie sur EXPOSUREMODE_MANUAL ou EXPOSUREMODE_SHUTTER_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="e562d-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="e562d-158">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="e562d-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="e562d-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-160">Correspond à l’ouverture de la lentille, en unités du numéro d’arrêt f mis à l’échelle par 100.</span><span class="sxs-lookup"><span data-stu-id="e562d-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="e562d-161">La valeur de cette propriété est généralement valide uniquement lorsque la propriété <strong>WIA_DPC_EXPOSURE_MODE</strong> a la valeur EXPOSUREMODE_MANUAL ou EXPOSUREMODE_APERTURE_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="e562d-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="e562d-162">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="e562d-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-164">Définit le paramètre de mode flash en cours pour le périphérique de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="e562d-165">Le pilote de périphérique énumère les valeurs prises en charge de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="e562d-166">Une application écrit cette propriété pour définir le mode flash de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="e562d-167">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e562d-168">Le tableau suivant contient les six constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-169">Mode flash</span><span class="sxs-lookup"><span data-stu-id="e562d-169">Flash Mode</span></span></th>
<th><span data-ttu-id="e562d-170">Définition</span><span class="sxs-lookup"><span data-stu-id="e562d-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="e562d-172">L’appareil photo détermine les paramètres de Flash appropriés.</span><span class="sxs-lookup"><span data-stu-id="e562d-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="e562d-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="e562d-174">L’appareil photo est configuré pour clignoter indépendamment des conditions d’éclairage actuelles.</span><span class="sxs-lookup"><span data-stu-id="e562d-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="e562d-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="e562d-176">L’appareil photo est configuré pour <em>ne pas</em> clignoter pour une image prise.</span><span class="sxs-lookup"><span data-stu-id="e562d-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="e562d-178">L’appareil photo détermine les paramètres de Flash appropriés à l’aide d’une réduction des yeux rouges, indépendamment des conditions d’éclairage actuelles.</span><span class="sxs-lookup"><span data-stu-id="e562d-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="e562d-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="e562d-180">L’appareil photo est configuré pour utiliser la réduction des yeux rouges et les clignotements, indépendamment des conditions d’éclairage actuelles.</span><span class="sxs-lookup"><span data-stu-id="e562d-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="e562d-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="e562d-182">L’appareil photo est configuré pour se synchroniser avec des unités flash externes.</span><span class="sxs-lookup"><span data-stu-id="e562d-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="e562d-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-184">Définit le paramètre de mode Focus actuel pour le périphérique de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="e562d-185">Le pilote de périphérique énumère les valeurs prises en charge de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="e562d-186">Une application écrit cette propriété pour définir le mode focus pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="e562d-187">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e562d-188">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-189">Mode focus</span><span class="sxs-lookup"><span data-stu-id="e562d-189">Focus Mode</span></span></th>
<th><span data-ttu-id="e562d-190">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="e562d-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="e562d-192">L’appareil photo est configuré pour permettre à l’utilisateur de se concentrer manuellement.</span><span class="sxs-lookup"><span data-stu-id="e562d-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="e562d-194">L’appareil photo est configuré pour se concentrer automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e562d-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="e562d-196">L’appareil photo est configuré pour se concentrer automatiquement à l’aide des paramètres de macro de plage abrégée.</span><span class="sxs-lookup"><span data-stu-id="e562d-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="e562d-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-198">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-199">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="e562d-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-201">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-202">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="e562d-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-204">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-205">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="e562d-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-207">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-208">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="e562d-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-210">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-211">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="e562d-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-213">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-214">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="e562d-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-216">Définit la source d’alimentation actuelle pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="e562d-217">Une application lit cette propriété pour déterminer la source d’alimentation utilisée par l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="e562d-218">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e562d-219">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-220">Mode d'alimentation</span><span class="sxs-lookup"><span data-stu-id="e562d-220">Power Mode</span></span></th>
<th><span data-ttu-id="e562d-221">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="e562d-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="e562d-223">L’appareil photo fonctionne sur un adaptateur d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="e562d-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="e562d-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="e562d-225">L’appareil photo fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="e562d-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="e562d-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-227">Pourcentage de la puissance de la batterie restant pour le fonctionnement de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="e562d-228">Cette valeur doit être un entier compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="e562d-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="e562d-229">Une application lit cette propriété pour déterminer la durée de vie restante de la batterie de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="e562d-230">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="e562d-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-232">Largeur, en pixels, d’une image miniature à utiliser pour les images nouvellement capturées.</span><span class="sxs-lookup"><span data-stu-id="e562d-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="e562d-233">Une application lit cette valeur pour obtenir une taille estimée pour l’affichage des miniatures dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e562d-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="e562d-234">Type : <strong>VT_I4</strong>, Access : lecture/écriture (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou lecture seule (WIA_PROP_NONE), valeurs valides : WIA_PROP_LIST ou WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="e562d-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="e562d-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-236">Largeur, en pixels, d’une image miniature à utiliser pour les images nouvellement capturées.</span><span class="sxs-lookup"><span data-stu-id="e562d-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="e562d-237">Une application lit cette valeur pour obtenir une taille estimée pour l’affichage des miniatures dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e562d-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="e562d-238">Type : <strong>VT_I4</strong>, Access : lecture/écriture (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou lecture seule (WIA_PROP_NONE), valeurs valides : WIA_PROP_LIST ou WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="e562d-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="e562d-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-240">Largeur en pixels à utiliser pour les images nouvellement capturées.</span><span class="sxs-lookup"><span data-stu-id="e562d-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="e562d-241">La liste des valeurs valides pour cette propriété a une correspondance un-à-un avec la liste des valeurs valides pour la propriété <strong>WIA_DPC_PICT_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="e562d-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="e562d-242">Si la largeur et la hauteur individuelles sont définissables de manière linéaire et orthogonales les unes avec les autres, elles peuvent être exprimées sous la forme d’une plage.</span><span class="sxs-lookup"><span data-stu-id="e562d-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="e562d-243">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="e562d-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-245">Hauteur en pixels à utiliser pour les images nouvellement capturées.</span><span class="sxs-lookup"><span data-stu-id="e562d-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="e562d-246">La liste des valeurs valides pour cette propriété a une correspondance un-à-un avec la liste des valeurs valides pour la propriété <strong>WIA_DPC_PICT_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="e562d-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="e562d-247">Si la largeur et la hauteur individuelles sont définissables de manière linéaire et orthogonales les unes avec les autres, elles peuvent être exprimées sous la forme d’une plage.</span><span class="sxs-lookup"><span data-stu-id="e562d-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="e562d-248">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="e562d-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-250">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-251">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="e562d-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-253">Conçue pour être approximativement linéaire en ce qui concerne la qualité d’image perçue sur un large éventail de contenu de scène, elle contient une plage ou une liste d’entiers.</span><span class="sxs-lookup"><span data-stu-id="e562d-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="e562d-254">Des entiers plus petits sont utilisés pour représenter une qualité inférieure (c’est-à-dire, une compression maximale), tandis que les entiers plus grands sont utilisés pour représenter une qualité supérieure (c’est-à-dire, compression minimale).</span><span class="sxs-lookup"><span data-stu-id="e562d-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="e562d-255">Tous les paramètres disponibles sur un appareil sont relatifs uniquement à ce périphérique et sont donc spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e562d-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="e562d-256">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="e562d-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-258">Réservé, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e562d-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="e562d-259">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="e562d-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-261">Durée, en millisecondes, entre les captures d’images dans une opération de capture temporelle.</span><span class="sxs-lookup"><span data-stu-id="e562d-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="e562d-262">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="e562d-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-264">Nombre d’images que l’appareil tente de capturer pendant une capture temporelle.</span><span class="sxs-lookup"><span data-stu-id="e562d-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="e562d-265">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="e562d-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-267">Durée, en millisecondes, entre les captures d’images au cours d’une opération de rafale.</span><span class="sxs-lookup"><span data-stu-id="e562d-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="e562d-268">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="e562d-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-270">Nombre d’images que l’appareil tente de capturer pendant une opération de rafale.</span><span class="sxs-lookup"><span data-stu-id="e562d-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="e562d-271">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="e562d-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-273">Spécifie le mode spécial d’acquisition d’image de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="e562d-274">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e562d-275">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-276">Mode d’effet</span><span class="sxs-lookup"><span data-stu-id="e562d-276">Effect Mode</span></span></th>
<th><span data-ttu-id="e562d-277">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="e562d-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="e562d-279">Capturez une image en mode standard pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="e562d-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="e562d-281">Capturez une image en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="e562d-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="e562d-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="e562d-283">Capturez une image sépia.</span><span class="sxs-lookup"><span data-stu-id="e562d-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="e562d-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-285">Taux de zoom effectif de l’image acquise de l’appareil photo numérique, mis à l’échelle d’un facteur de 10.</span><span class="sxs-lookup"><span data-stu-id="e562d-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="e562d-286">La valeur 10 correspond à l’absence de zoom numérique (1X), qui est la taille de scène standard capturée par l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="e562d-287">La valeur 20 correspond à un zoom 2X, où un quart de la taille de la scène standard est capturé par l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="e562d-288">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="e562d-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-290">La netteté perçue d’une image capturée.</span><span class="sxs-lookup"><span data-stu-id="e562d-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="e562d-291">Cette propriété peut utiliser une liste de valeurs ou une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="e562d-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="e562d-292">La valeur minimale représente le moins de précision, tandis que la valeur maximale représente la netteté maximale.</span><span class="sxs-lookup"><span data-stu-id="e562d-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="e562d-293">En général, une valeur au milieu de la plage représente la netteté normale ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="e562d-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="e562d-294">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="e562d-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-296">Contraste perçu d’une image capturée.</span><span class="sxs-lookup"><span data-stu-id="e562d-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="e562d-297">Cette propriété peut contenir une liste de valeurs ou une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="e562d-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="e562d-298">La valeur minimale prise en charge représente le moins de contraste, tandis que la valeur maximale représente le contraste le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="e562d-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="e562d-299">En règle générale, une valeur au milieu de la plage représente le contraste normal ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="e562d-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="e562d-300">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="e562d-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-302">Définit le mode de capture de l’image.</span><span class="sxs-lookup"><span data-stu-id="e562d-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="e562d-303">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e562d-304">Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-305">Mode de capture</span><span class="sxs-lookup"><span data-stu-id="e562d-305">Capture Mode</span></span></th>
<th><span data-ttu-id="e562d-306">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="e562d-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="e562d-308">Mode normal de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e562d-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="e562d-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="e562d-310">Capturez plus d’une image en succession rapide, comme défini par les valeurs des propriétés <strong>WIA_DPC_BURST_NUMBER</strong> et <strong>WIA_DPC_BURST_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="e562d-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="e562d-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="e562d-312">Capturez plusieurs images successivement, comme défini par les propriétés <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> et <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="e562d-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="e562d-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-314">Valeur représentant le délai, en millisecondes, à insérer entre le déclencheur de capture et le lancement réel de la capture de données.</span><span class="sxs-lookup"><span data-stu-id="e562d-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="e562d-315">Cette propriété n’est pas destinée à décrire le temps entre les frames pour une initialisation unique, plusieurs captures telles qu’une rafale ou un laps de temps, qui ont des propriétés d’intervalle distinctes <strong>WIA_DPC_BURST_INTERVAL</strong> et <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="e562d-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="e562d-316">Dans ce cas, il sert toujours de délai initial avant la capture de la première image de la série, indépendamment du temps entre les frames.</span><span class="sxs-lookup"><span data-stu-id="e562d-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="e562d-317">Pour aucun délai de précapture, cette propriété doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="e562d-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="e562d-318">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="e562d-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-320">Permet l’émulation des paramètres de vitesse de la pellicule sur un appareil photo numérique.</span><span class="sxs-lookup"><span data-stu-id="e562d-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="e562d-321">Les paramètres correspondent aux désignations ISO (ASA/DIN).</span><span class="sxs-lookup"><span data-stu-id="e562d-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="e562d-322">En règle générale, un appareil prend en charge des valeurs énumérées discrètes, mais le contrôle continu sur une plage de valeurs est possible.</span><span class="sxs-lookup"><span data-stu-id="e562d-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="e562d-323">La valeur 0xFFFF correspond au paramètre ISO automatique.</span><span class="sxs-lookup"><span data-stu-id="e562d-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="e562d-324">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="e562d-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-326">Spécifie le mode utilisé par l’appareil photo pour ajuster automatiquement le paramètre d’exposition.</span><span class="sxs-lookup"><span data-stu-id="e562d-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="e562d-327">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-328">Mode de contrôle d’exposition</span><span class="sxs-lookup"><span data-stu-id="e562d-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="e562d-329">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="e562d-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="e562d-331">Définissez l’exposition en fonction de la moyenne de la scène entière.</span><span class="sxs-lookup"><span data-stu-id="e562d-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="e562d-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="e562d-333">Définissez l’exposition en fonction d’une moyenne pondérée au centre.</span><span class="sxs-lookup"><span data-stu-id="e562d-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="e562d-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="e562d-335">Définissez l’exposition en fonction d’un modèle à points.</span><span class="sxs-lookup"><span data-stu-id="e562d-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="e562d-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="e562d-337">Définissez l’exposition en fonction d’une zone centrale.</span><span class="sxs-lookup"><span data-stu-id="e562d-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="e562d-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-339">Spécifie le mode utilisé par l’appareil photo pour ajuster automatiquement le focus.</span><span class="sxs-lookup"><span data-stu-id="e562d-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="e562d-340">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e562d-341">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-342">Mode de contrôle du focus</span><span class="sxs-lookup"><span data-stu-id="e562d-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="e562d-343">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="e562d-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="e562d-345">Ajustez le focus en fonction d’un point central.</span><span class="sxs-lookup"><span data-stu-id="e562d-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="e562d-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="e562d-347">Ajustez le focus en fonction d’un modèle à points.</span><span class="sxs-lookup"><span data-stu-id="e562d-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="e562d-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-349">Distance, en millimètres, entre le plan de capture d’image de l’appareil photo numérique et le point de focus.</span><span class="sxs-lookup"><span data-stu-id="e562d-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="e562d-350">La valeur 0xFFFF correspond à un paramètre supérieur à 655 mètres.</span><span class="sxs-lookup"><span data-stu-id="e562d-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="e562d-351">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="e562d-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="e562d-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-353">Longueur focale équivalente à 35mm.</span><span class="sxs-lookup"><span data-stu-id="e562d-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="e562d-354">Les valeurs de cette propriété correspondent à la longueur focale, en millimètres, multipliée par 100.</span><span class="sxs-lookup"><span data-stu-id="e562d-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="e562d-355">La longueur focale détermine le zoom optique.</span><span class="sxs-lookup"><span data-stu-id="e562d-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="e562d-356">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="e562d-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-358">Chaîne Unicode terminée par le caractère null qui représente l’avantage rouge, vert et bleu appliqué aux données d’image, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e562d-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="e562d-359">Par exemple, &quot; 4:25:50 &quot; représente un gain rouge de 4, un gain vert de 25 et un gain bleu de 50.</span><span class="sxs-lookup"><span data-stu-id="e562d-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="e562d-360">Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="e562d-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-362">Spécifie la façon dont l’appareil photo numérique pèse les canaux de couleur.</span><span class="sxs-lookup"><span data-stu-id="e562d-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="e562d-363">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="e562d-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="e562d-364">La liste suivante répertorie les valeurs possibles de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e562d-365">Équilibre des blancs</span><span class="sxs-lookup"><span data-stu-id="e562d-365">White Balance</span></span></th>
<th><span data-ttu-id="e562d-366">Description</span><span class="sxs-lookup"><span data-stu-id="e562d-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e562d-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="e562d-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="e562d-368">L’équilibre des blancs est défini directement à l’aide de la propriété <strong>WIA_DPC_RGB_GAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="e562d-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="e562d-370">L’appareil photo utilise un mécanisme automatique pour définir l’équilibre du blanc.</span><span class="sxs-lookup"><span data-stu-id="e562d-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="e562d-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="e562d-372">L’appareil photo détermine le réglage de l’équilibre des blancs lorsqu’un utilisateur appuie sur le bouton de capture tout en pointant la caméra sur une surface blanche.</span><span class="sxs-lookup"><span data-stu-id="e562d-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="e562d-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="e562d-374">L’appareil photo définit l’équilibre des blancs sur une valeur appropriée pour une utilisation dans les conditions d’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="e562d-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="e562d-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="e562d-376">L’appareil photo définit l’équilibre des blancs sur une valeur appropriée pour une utilisation avec une source de lumière fluorescente.</span><span class="sxs-lookup"><span data-stu-id="e562d-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e562d-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="e562d-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="e562d-378">L’appareil photo définit l’équilibre blanc sur une valeur appropriée pour une utilisation avec une source de lumière tungstène.</span><span class="sxs-lookup"><span data-stu-id="e562d-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e562d-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="e562d-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="e562d-380">L’appareil photo définit l’équilibre des blancs sur une valeur appropriée pour une utilisation avec un Flash électronique.</span><span class="sxs-lookup"><span data-stu-id="e562d-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="e562d-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-382">Décrit une URL.</span><span class="sxs-lookup"><span data-stu-id="e562d-382">Describes a URL.</span></span> <span data-ttu-id="e562d-383">L’URL décrite par ce proroperty est l’une des images ou des objets qui, une fois qu’ils sont acquis à partir du périphérique, peuvent être téléchargés vers, conformément à l’un des scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="e562d-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="e562d-384">Une application WIA lit cette propriété et permet à l’utilisateur de télécharger automatiquement des images vers l’URL.</span><span class="sxs-lookup"><span data-stu-id="e562d-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="e562d-385">Une application définit l’URL et d’autres périphériques (bornes, etc.) utilisent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e562d-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="e562d-386">Microsoft Windows ne charge pas les images par lui-même.</span><span class="sxs-lookup"><span data-stu-id="e562d-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="e562d-387">Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="e562d-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-389">Nom du propriétaire (qui est l’utilisateur actuel) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e562d-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="e562d-390">L’appareil utilise cette propriété pour remplir le champ Artist dans chaque image EXIF capturée.</span><span class="sxs-lookup"><span data-stu-id="e562d-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="e562d-391">Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="e562d-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span><span class="sxs-lookup"><span data-stu-id="e562d-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e562d-393">Notification de droits d’auteur.</span><span class="sxs-lookup"><span data-stu-id="e562d-393">The copyright notification.</span></span> <span data-ttu-id="e562d-394">L’appareil utilise cette propriété pour renseigner le champ de copyright dans chaque image EXIF capturée.</span><span class="sxs-lookup"><span data-stu-id="e562d-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="e562d-395">Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e562d-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e562d-396">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e562d-396">Requirements</span></span>



| <span data-ttu-id="e562d-397">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e562d-397">Requirement</span></span> | <span data-ttu-id="e562d-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="e562d-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e562d-399">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e562d-399">Minimum supported client</span></span><br/> | <span data-ttu-id="e562d-400">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e562d-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e562d-401">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e562d-401">Minimum supported server</span></span><br/> | <span data-ttu-id="e562d-402">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e562d-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e562d-403">En-tête</span><span class="sxs-lookup"><span data-stu-id="e562d-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="e562d-404"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="e562d-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




