---
description: Windows les périphériques matériels d’Acquisition d’images (WIA) ont des valeurs de propriété qui sont stockées dans le registre Windows. Pour plus d’informations, consultez constantes de propriété d’appareil courantes.
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
ms.openlocfilehash: f33e7f2dfd17e535e47026aee173feccb7c69584
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624195"
---
# <a name="camera-device-property-constants"></a>Constantes de propriété de périphérique d’appareil photo

Windows les périphériques matériels d’Acquisition d’images (WIA) ont des valeurs de propriété qui sont stockées dans le registre Windows. Pour plus d’informations, consultez [**constantes de propriété d’appareil courantes**](-wia-wiaitempropcommondevice.md).

Les constantes de propriété d’appareil suivantes, avec leurs chaînes associées, sont spécifiques aux appareils photo numériques. Le préfixe « WIA \_ DPC \_ » indique une propriété d’appareil pour les appareils photo et est la Convention d’affectation de noms utilisée en C/C++. À des fins de script, ces constantes utilisent le préfixe « CameraDevice » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.

> [!Note]  
> WIA ne prend pas en charge les caméras dans Windows Vista ou version ultérieure. pour ces versions du Windows, utilisez l’API de l’appareil Portable Windows (WPD) décrite dans le kit de développement de pilotes (DDK) Windows pour obtenir des images à partir d’appareils photo.

 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante/valeur</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td >Nombre d’images prises par l’appareil photo. Le minipilote crée et gère cette propriété.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td >Nombre d’images pouvant être prises, en fonction des paramètres de propriété actuels. Si ces paramètres changent et que les modifications affectent la taille des images générées par l’appareil photo, le minipilote WIA doit mettre à jour le nombre d’images restantes. Le minipilote crée et gère cette propriété.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td >Indique le mode d’exposition actuel de l’appareil photo. Une application modifie cette propriété pour contrôler le mode d’exposition de l’appareil photo.<br/> Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> Le tableau suivant contient les sept constantes qui sont valides avec cette propriété.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode exposition</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>La vitesse et l’ouverture de l’obturateur sont définies par l’utilisateur.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>L’ouverture est définie par l’utilisateur et l’appareil photo définit automatiquement la vitesse d’obturation.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>La vitesse d’obturation est définie par l’utilisateur et l’appareil photo définit automatiquement l’ouverture.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo, optimisée pour les sujets toujours sujets.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo, optimisée pour les scènes contenant un mouvement rapide.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>La vitesse et l’ouverture de l’obturateur sont automatiquement définies par l’appareil photo, optimisé pour la photographie en portrait.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td ><p>Permet d’ajuster le point d’ensemble du contrôle d’exposition automatique de l’appareil photo numérique. Par exemple, un paramètre de zéro ne change pas le niveau d’exposition automatique défini par l’usine. Les unités sont des &quot; arrêts &quot; mis à l’échelle à l’aide d’un facteur de 1000, afin d’autoriser les valeurs d’arrêt fractionnaires. Un paramètre de 2000 correspond à deux arrêts supplémentaires (quatre fois plus d’énergie sur le capteur), ce qui génère des images plus claires. Un paramètre de-1000 correspond à une exposition moins faible (une demie de l’énergie sur le capteur) produisant des images plus sombres. Les valeurs des paramètres sont dans le système additif d’unités d’exposition photographique (APEX). Cette propriété peut être exprimée sous la forme d’une liste ou d’une plage de valeurs. Cette propriété est généralement utilisée uniquement lorsque la propriété <strong>WIA_DPC_EXPOSURE_MODE</strong> de l’appareil est définie sur EXPOSUREMODE_MANUAL.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td ><p>Correspond à la vitesse d’obturation, en secondes, mise à l’échelle par 10 000. En règle générale, l’appareil utilise cette propriété uniquement lorsque la propriété <strong>WIA_DPC_EXPOSURE_MODE</strong> est définie sur EXPOSUREMODE_MANUAL ou EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td ><p>Correspond à l’ouverture de la lentille, en unités du numéro d’arrêt f mis à l’échelle par 100. La valeur de cette propriété est généralement valide uniquement lorsque la propriété <strong>WIA_DPC_EXPOSURE_MODE</strong> a la valeur EXPOSUREMODE_MANUAL ou EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td ><p>Définit le paramètre de mode flash en cours pour le périphérique de l’appareil photo. Le pilote de périphérique énumère les valeurs prises en charge de cette propriété. Une application écrit cette propriété pour définir le mode flash de l’appareil photo.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les six constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Mode flash</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>L’appareil photo détermine les paramètres de Flash appropriés.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>L’appareil photo est configuré pour clignoter indépendamment des conditions d’éclairage actuelles.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>L’appareil photo est configuré pour <em>ne pas</em> clignoter pour une image prise.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>L’appareil photo détermine les paramètres de Flash appropriés à l’aide d’une réduction des yeux rouges, indépendamment des conditions d’éclairage actuelles.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>L’appareil photo est configuré pour utiliser la réduction des yeux rouges et les clignotements, indépendamment des conditions d’éclairage actuelles.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>L’appareil photo est configuré pour se synchroniser avec des unités flash externes.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td ><p>Définit le paramètre de mode Focus actuel pour le périphérique de l’appareil photo. Le pilote de périphérique énumère les valeurs prises en charge de cette propriété. Une application écrit cette propriété pour définir le mode focus pour l’appareil photo.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Mode focus</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>L’appareil photo est configuré pour permettre à l’utilisateur de se concentrer manuellement.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>L’appareil photo est configuré pour se concentrer automatiquement.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>L’appareil photo est configuré pour se concentrer automatiquement à l’aide des paramètres de macro de plage abrégée.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td ><p>Définit la source d’alimentation actuelle pour l’appareil photo. Une application lit cette propriété pour déterminer la source d’alimentation utilisée par l’appareil photo.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Mode d'alimentation</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>L’appareil photo fonctionne sur un adaptateur d’alimentation.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>L’appareil photo fonctionne sur batterie.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td ><p>Pourcentage de la puissance de la batterie restant pour le fonctionnement de l’appareil photo. Cette valeur doit être un entier compris entre 0 et 100. Une application lit cette propriété pour déterminer la durée de vie restante de la batterie de l’appareil photo.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td ><p>Largeur, en pixels, d’une image miniature à utiliser pour les images nouvellement capturées. Une application lit cette valeur pour obtenir une taille estimée pour l’affichage des miniatures dans son interface utilisateur.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou lecture seule (WIA_PROP_NONE), valeurs valides : WIA_PROP_LIST ou WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td ><p>Largeur, en pixels, d’une image miniature à utiliser pour les images nouvellement capturées. Une application lit cette valeur pour obtenir une taille estimée pour l’affichage des miniatures dans son interface utilisateur.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) ou lecture seule (WIA_PROP_NONE), valeurs valides : WIA_PROP_LIST ou WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td ><p>Largeur en pixels à utiliser pour les images nouvellement capturées. La liste des valeurs valides pour cette propriété a une correspondance un-à-un avec la liste des valeurs valides pour la propriété <strong>WIA_DPC_PICT_HEIGHT</strong> . Si la largeur et la hauteur individuelles sont définissables de manière linéaire et orthogonales les unes avec les autres, elles peuvent être exprimées sous la forme d’une plage.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td ><p>Hauteur en pixels à utiliser pour les images nouvellement capturées. La liste des valeurs valides pour cette propriété a une correspondance un-à-un avec la liste des valeurs valides pour la propriété <strong>WIA_DPC_PICT_WIDTH</strong> . Si la largeur et la hauteur individuelles sont définissables de manière linéaire et orthogonales les unes avec les autres, elles peuvent être exprimées sous la forme d’une plage.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td ><p>Conçue pour être approximativement linéaire en ce qui concerne la qualité d’image perçue sur un large éventail de contenu de scène, elle contient une plage ou une liste d’entiers. Des entiers plus petits sont utilisés pour représenter une qualité inférieure (c’est-à-dire, une compression maximale), tandis que les entiers plus grands sont utilisés pour représenter une qualité supérieure (c’est-à-dire, compression minimale). Tous les paramètres disponibles sur un appareil sont relatifs uniquement à ce périphérique et sont donc spécifiques à l’appareil.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td ><p>Durée, en millisecondes, entre les captures d’images dans une opération de capture temporelle.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td ><p>Nombre d’images que l’appareil tente de capturer pendant une capture temporelle.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td ><p>Durée, en millisecondes, entre les captures d’images au cours d’une opération de rafale.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td ><p>Nombre d’images que l’appareil tente de capturer pendant une opération de rafale.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td ><p>Spécifie le mode spécial d’acquisition d’image de l’appareil photo.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Mode d’effet</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Capturez une image en mode standard pour l’appareil photo.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Capturez une image en nuances de gris.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Capturez une image sépia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td ><p>Taux de zoom effectif de l’image acquise de l’appareil photo numérique, mis à l’échelle d’un facteur de 10. La valeur 10 correspond à l’absence de zoom numérique (1X), qui est la taille de scène standard capturée par l’appareil photo. La valeur 20 correspond à un zoom 2X, où un quart de la taille de la scène standard est capturé par l’appareil photo.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td ><p>La netteté perçue d’une image capturée. Cette propriété peut utiliser une liste de valeurs ou une plage de valeurs. La valeur minimale représente le moins de précision, tandis que la valeur maximale représente la netteté maximale. En général, une valeur au milieu de la plage représente la netteté normale ou par défaut.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td ><p>Contraste perçu d’une image capturée. Cette propriété peut contenir une liste de valeurs ou une plage de valeurs. La valeur minimale prise en charge représente le moins de contraste, tandis que la valeur maximale représente le contraste le plus élevé. En règle générale, une valeur au milieu de la plage représente le contraste normal ou par défaut.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td ><p>Définit le mode de capture de l’image.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Mode de capture</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Mode normal de l’appareil photo.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Capturez plus d’une image en succession rapide, comme défini par les valeurs des propriétés <strong>WIA_DPC_BURST_NUMBER</strong> et <strong>WIA_DPC_BURST_INTERVAL</strong> .</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Capturez plusieurs images successivement, comme défini par les propriétés <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> et <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td ><p>Valeur représentant le délai, en millisecondes, à insérer entre le déclencheur de capture et le lancement réel de la capture de données. Cette propriété n’est pas destinée à décrire le temps entre les frames pour une initialisation unique, plusieurs captures telles qu’une rafale ou un laps de temps, qui ont des propriétés d’intervalle distinctes <strong>WIA_DPC_BURST_INTERVAL</strong> et <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. Dans ce cas, il sert toujours de délai initial avant la capture de la première image de la série, indépendamment du temps entre les frames. Pour aucun délai de précapture, cette propriété doit être définie sur zéro.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td ><p>Permet l’émulation des paramètres de vitesse de la pellicule sur un appareil photo numérique. Les paramètres correspondent aux désignations ISO (ASA/DIN). En règle générale, un appareil prend en charge des valeurs énumérées discrètes, mais le contrôle continu sur une plage de valeurs est possible. La valeur 0xFFFF correspond au paramètre ISO automatique.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td ><p>Spécifie le mode utilisé par l’appareil photo pour ajuster automatiquement le paramètre d’exposition.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Mode de contrôle d’exposition</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Définissez l’exposition en fonction de la moyenne de la scène entière.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Définissez l’exposition en fonction d’une moyenne pondérée au centre.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Définissez l’exposition en fonction d’un modèle à points.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Définissez l’exposition en fonction d’une zone centrale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td ><p>Spécifie le mode utilisé par l’appareil photo pour ajuster automatiquement le focus.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Mode de contrôle du focus</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Ajustez le focus en fonction d’un point central.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Ajustez le focus en fonction d’un modèle à points.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td ><p>Distance, en millimètres, entre le plan de capture d’image de l’appareil photo numérique et le point de focus. La valeur 0xFFFF correspond à un paramètre supérieur à 655 mètres.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td ><p>Longueur focale équivalente à 35mm. Les valeurs de cette propriété correspondent à la longueur focale, en millimètres, multipliée par 100. La longueur focale détermine le zoom optique.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td ><p>Chaîne Unicode terminée par le caractère null qui représente l’avantage rouge, vert et bleu appliqué aux données d’image, respectivement. Par exemple, &quot; 4:25:50 &quot; représente un gain rouge de 4, un gain vert de 25 et un gain bleu de 50.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td ><p>Spécifie la façon dont l’appareil photo numérique pèse les canaux de couleur.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La liste suivante répertorie les valeurs possibles de cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Équilibre des blancs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>L’équilibre des blancs est défini directement à l’aide de la propriété <strong>WIA_DPC_RGB_GAIN</strong> .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>L’appareil photo utilise un mécanisme automatique pour définir l’équilibre du blanc.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>L’appareil photo détermine le réglage de l’équilibre des blancs lorsqu’un utilisateur appuie sur le bouton de capture tout en pointant la caméra sur une surface blanche.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>L’appareil photo définit l’équilibre des blancs sur une valeur appropriée pour une utilisation dans les conditions d’heure d’été.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>L’appareil photo définit l’équilibre des blancs sur une valeur appropriée pour une utilisation avec une source de lumière fluorescente.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>L’appareil photo définit l’équilibre blanc sur une valeur appropriée pour une utilisation avec une source de lumière tungstène.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>L’appareil photo définit l’équilibre des blancs sur une valeur appropriée pour une utilisation avec un Flash électronique.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td ><p>Décrit une URL. L’URL décrite par ce proroperty est l’une des images ou des objets qui, une fois qu’ils sont acquis à partir du périphérique, peuvent être téléchargés vers, conformément à l’un des scénarios suivants.</p>
<ul>
<li>Une application WIA lit cette propriété et permet à l’utilisateur de télécharger automatiquement des images vers l’URL.</li>
<li>Une application définit l’URL et d’autres périphériques (bornes, etc.) utilisent cette propriété.</li>
</ul>
<p>Microsoft Windows ne charge pas les images par lui-même.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td ><p>Nom du propriétaire (qui est l’utilisateur actuel) de l’appareil. L’appareil utilise cette propriété pour remplir le champ Artist dans chaque image EXIF capturée.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td ><p>Notification de droits d’auteur. L’appareil utilise cette propriété pour renseigner le champ de copyright dans chaque image EXIF capturée.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




