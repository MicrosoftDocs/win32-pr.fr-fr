---
description: Windows Les appareils mobiles prennent en charge les propriétés d’appareil suivantes.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Propriétés de l’appareil (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5490323e60d353fade6dfb7f517533ecb5fa26ca9e78ae221b9ff584d8c13a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430977"
---
# <a name="device-properties-portabledeviceh"></a>Propriétés de l’appareil (PortableDevice. h)

Windows Les appareils mobiles prennent en charge les propriétés d’appareil suivantes.



<table>
<thead>
<tr class="header">
<th>Property</th>
<th>VarType</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>Date et heure actuelles sur l’appareil.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Version du microprogramme de l’appareil.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Identificateur unique de 16 octets qui est commun entre plusieurs transports pris en charge par l’appareil. Si un seul appareil prend en charge plusieurs transports, cette propriété peut être utilisée pour associer les différents pilotes WPD de transport à cet appareil.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Nom de fabricant de l’appareil lisible par l’utilisateur.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Modèle de l'appareil.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Identificateur unique de 16 octets utilisé pour faire la distinction entre les différents modèles d’un appareil.</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>Valeur qui spécifie l’identificateur réseau EUI-64 de l’appareil ; Cette propriété est utilisée pour les opérations réseau hors bande. Si l’appareil possède des adresses réseau physiques MAC-48 (en général des réseaux IPv4), l’adresse MAC-48 est encodée dans l’adresse EUI-64, car les deux moitiés de l’adresse MAC-48 sont séparées par FF-FF. La valeur EUI-64 est stockée &quot; dans &quot; &quot; un ordre réseau ou Big endian &quot; , où une adresse eui-64 de 01-02-03-ff-ff-04-05-06 serait placée dans le VT_UI8 de manière à ce que la valeur décimale soit 72624942021346566. Cette propriété est requise sur tous les appareils qui prennent en charge l’authentification nominale ou sécurisée. Cette propriété est recommandée sur les appareils qui prennent uniquement en charge l’authentification zéro. La valeur peut être utilisée par l’hôte pour établir automatiquement l’accès à l’appareil sans intervention de l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valeur comprise entre 0 et 100 qui spécifie le niveau de puissance de la batterie de l’appareil, 0 étant aucun et 100 entièrement facturé.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Énumération <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> qui spécifie la source d’alimentation de l’appareil.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Protocole d’appareil utilisé.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Numéro de série de l’appareil.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Valeur qui spécifie si les formats pris en charge retournés par l’appareil sont dans un ordre de préférence. Le premier format de la liste est préféré par l’appareil, tandis que le dernier est le moins recommandé. Les applications peuvent utiliser cette propriété pour déterminer si les formats pris en charge par un appareil sont répertoriés dans un ordre de préférence.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valeur booléenne qui spécifie si les formats pris en charge retournés par l’appareil sont dans un ordre de préférence. autrement dit, le premier format retourné est plus préféré, tandis que le dernier format retourné est le moins recommandé.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valeur booléenne qui spécifie si l’appareil prend en charge les objets non consommables. Il s’agit d’objets que l’appareil est destiné uniquement à stocker, à ne pas lire ou à utiliser de quelque manière que ce soit.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Description explicite du <em>partenaire de synchronisation</em>d’un appareil. Il s’agit d’un périphérique, d’une application ou d’un serveur avec lequel l’appareil communique pour maintenir un État commun ou un groupe de fichiers entre les deux partenaires. Les programmes de messagerie électronique et les bibliothèques musicales en sont des exemples.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valeur qui représente le nom convivial défini par l’utilisateur sur l’appareil.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>transport pris en charge par l’appareil, tel que USB, IP ou Bluetooth. Les valeurs valides sont du type d’énumération <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valeur qui spécifie le type d’appareil ; les applications utilisent cette propriété à des fins de représentation uniquement. Les caractéristiques fonctionnelles de l’appareil sont choisies par le biais d’objets fonctionnels. Les appareils qui ne fournissent pas d’icône d’appareil, par exemple, une <strong>WPD_RESOURCE_ICON</strong> pour l’objet appareil, sont représentés dans l’espace de noms wpd avec une icône générique. Cette icône dépend du type de périphérique spécifié, par exemple, si le type d’appareil est un téléphone mobile, l’icône de téléphone générique est utilisée. Lors de la première installation de l’appareil, le programme d’installation de la classe WPD interroge cette valeur de propriété et le stocke dans le registre de l’appareil sous la valeur PORTABLE_DEVICE_TYPE en tant que REG_DWORD.<br/> Les valeurs possibles de ce paramètre proviennent de l’énumération <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> définie dans PortableDevice. h. Les valeurs sont les suivantes :<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Si cette propriété existe et qu’elle a la valeur <strong>true</strong>, l’appareil peut être utilisé avec l’étape de l’appareil. Cela est destiné aux appareils qui ne peuvent pas stocker les métadonnées à l’aide de l' <strong>Metadata service d’appareil</strong>, mais qui fournissent des métadonnées sur les serveurs Microsoft.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




