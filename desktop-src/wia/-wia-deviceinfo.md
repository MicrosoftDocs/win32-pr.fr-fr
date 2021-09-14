---
description: l’objet DeviceInfo permet d’accéder aux propriétés d’un périphérique matériel WIA (Windows Image Acquisition).
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
ms.openlocfilehash: 69b34a97483a8a6ce231890454148c7948f63e4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231084"
---
# <a name="deviceinfo-object"></a>Objet DeviceInfo

l’objet **DeviceInfo** permet d’accéder aux propriétés d’un périphérique matériel WIA (Windows Image Acquisition). En outre, par le biais de sa méthode de [**création**](-wia-iwiadeviceinfo-create.md) , permet à l’application ou au script de se connecter à l’appareil et d’obtenir un objet d' [**élément**](-wia-item.md) qui représente l’appareil. Utilisez la méthode [**Devices**](-wia-iwia-devices.md) pour obtenir une collection d’objets **DeviceInfo** .

## <a name="members"></a>Membres

L’objet **DeviceInfo** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **DeviceInfo** a ces méthodes.



| Méthode                                                 | Description                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Créer**](-wia-iwiadeviceinfo-create.md)           | La méthode [**Create**](-wia-iwiadeviceinfo-create.md) de l’objet **DeviceInfo** établit une connexion au périphérique WIA spécifié par l’objet **DeviceInfo** et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | La méthode [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) de l’objet **DEVICEINFO** utilise l’ID d’une propriété d’appareil pour retourner sa valeur.<br/>                                                                                               |



 

### <a name="properties"></a>Propriétés

L’objet **DeviceInfo** a ces propriétés.




| Propriété | Type d’accès | Description | 
|----------|-------------|-------------|
| <a href="-wia-iwiadeviceinfo-id.md"><strong>Identifi</strong></a><br /> | Lecture seule<br /> | Récupère l’ID du périphérique matériel WIA. <br /> | 
| <a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Fabricant</strong></a><br /> | Lecture seule<br /> | Récupère le nom du fabricant de cet appareil matériel.<br /> | 
| <a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a><br /> | Lecture seule<br /> | Nom du périphérique matériel WIA tel qu’il apparaît dans l’interface utilisateur.<br /> | 
| <a href="-wia-iwiadeviceinfo-port.md"><strong>Importer</strong></a><br /> | Lecture seule<br /> | Récupère le port auquel le périphérique matériel WIA est connecté.<br /> | 
| <a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a><br /> | Lecture seule<br /> | Récupère le type d’appareil matériel WIA. Les valeurs possibles sont les suivantes : <br /><ul><li>DigitalCamera</li><li>Scanneur</li><li>StreamingVideo</li><li>Valeur par défaut</li></ul> | 
| <a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br /> | Lecture seule<br /> | Récupère l’ID de classe de l’interface utilisateur fournie par le fabricant pour cet appareil matériel WIA. La valeur est une représentation sous forme de chaîne d’un GUID. <br /> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




