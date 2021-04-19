---
description: L’objet DeviceInfo permet d’accéder aux propriétés d’un périphérique matériel WIA (Windows Image Acquisition).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Objet DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525066"
---
# <a name="deviceinfo-object"></a>Objet DeviceInfo

L’objet **DeviceInfo** permet d’accéder aux propriétés d’un périphérique matériel WIA (Windows Image Acquisition). En outre, par le biais de sa méthode de [**création**](-wia-iwiadeviceinfo-create.md) , permet à l’application ou au script de se connecter à l’appareil et d’obtenir un objet d' [**élément**](-wia-item.md) qui représente l’appareil. Utilisez la méthode [**Devices**](-wia-iwia-devices.md) pour obtenir une collection d’objets **DeviceInfo** .

## <a name="members"></a>Membres

L’objet **DeviceInfo** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **DeviceInfo** a ces méthodes.



| Méthode                                                 | Description                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Créés**](-wia-iwiadeviceinfo-create.md)           | La méthode [**Create**](-wia-iwiadeviceinfo-create.md) de l’objet **DeviceInfo** établit une connexion au périphérique WIA spécifié par l’objet **DeviceInfo** et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | La méthode [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) de l’objet **DEVICEINFO** utilise l’ID d’une propriété d’appareil pour retourner sa valeur.<br/>                                                                                               |



 

### <a name="properties"></a>Propriétés

L’objet **DeviceInfo** a ces propriétés.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriété</th>
<th style="text-align: left;">Type d’accès</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-id.md"><strong>Identifi</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Récupère l’ID du périphérique matériel WIA. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Fabricant</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Récupère le nom du fabricant de cet appareil matériel.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-name.md"><strong>Nom</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Nom du périphérique matériel WIA tel qu’il apparaît dans l’interface utilisateur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Récupère le port auquel le périphérique matériel WIA est connecté.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-type.md"><strong>Entrer</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Récupère le type d’appareil matériel WIA. Les valeurs possibles sont les suivantes : <br/>
<ul>
<li>DigitalCamera</li>
<li>Scanneur</li>
<li>StreamingVideo</li>
<li>Default</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Récupère l’ID de classe de l’interface utilisateur fournie par le fabricant pour cet appareil matériel WIA. La valeur est une représentation sous forme de chaîne d’un GUID. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




