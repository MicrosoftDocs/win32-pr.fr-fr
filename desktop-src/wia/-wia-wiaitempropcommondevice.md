---
description: en plus des propriétés d’informations de périphérique, les périphériques d’Acquisition d’images Windows (WIA) ont des valeurs de propriété stockées dans le registre que les applications lisent et écrivent.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Constantes de propriété d’appareil courantes (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c5eda1266c8c99f1125e03dfbacc3eb325a69d1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293255"
---
# <a name="common-device-property-constants"></a>Constantes de propriété d’appareil courantes

en plus des propriétés d’informations de périphérique, les périphériques d’Acquisition d’images Windows (WIA) ont des valeurs de propriété stockées dans le registre que les applications lisent et écrivent. Ils sont associés à l’objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou à l’objet [**IWiaItem2**](-wia-iwiaitem2.md) . Les propriétés des appareils représentent des informations sur l’appareil, telles que l’état de la connexion et l’heure de l’appareil Chaque propriété d’appareil est associée à une chaîne de propriété d’appareil.

Les constantes de propriété d’appareil répertoriées ici sont communes à la plupart ou à la totalité des périphériques matériels WIA.

Le préfixe « WIA \_ DPA \_ » indique une propriété d’appareil pour tous les appareils et est la Convention d’affectation de noms utilisée dans C/C++. À des fins de script, ces constantes utilisent le préfixe « Device » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.



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
<td ><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td >État actuel de la connexion pour l’appareil. Le minipilote crée et gère cette propriété.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> La propriété peut avoir les valeurs possibles suivantes.<br/> 
<table>
<thead>
<tr class="header">
<th>Connecter Statu</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>L’appareil n’est pas connecté.</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>L’appareil est connecté et opérationnel.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td ><p>Heure actuelle de l’horloge stockée sur l’appareil. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Cette propriété est prise en charge uniquement par les appareils qui ont une horloge interne. Si l’horloge de l’appareil peut être définie, cette propriété est en lecture/écriture ; dans le cas contraire, il est en lecture seule.</p>
<p>Les appareils WIA signalent l’heure dans une structure <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SystemTime</a> .</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td ><p>Version du microprogramme de l’appareil. Cette valeur doit être une valeur de chaîne, telle que &quot; 1.0.4 &quot; ou &quot; 1.0 ABC &quot; . Le minipilote crée et gère cette propriété. Si le minipilote WIA ne fournit pas de ressource de version, le service WIA fournit la valeur &quot; 0.0.0.0 &quot; comme valeur par défaut. Une application lit cette propriété pour déterminer la version de la DLL du minipilote WIA.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
