---
description: 'Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les événements d’un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetEventAttributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Attributs d’événement (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532492"
---
# <a name="event-attributes-portabledeviceh"></a>Attributs d’événement (PortableDevice. h)

Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les événements d’un service d’appareil. Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




| Attribut                             | VarType         | Description                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_nom d' \_ attribut d’événement wpd \_**       | **\_LPWStr VT**  | Chaîne qui spécifie le nom convivial du script de l’événement. Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '. |
| **\_Options des \_ attributs d’événement wpd \_**    | **VT \_ inconnu** | [**IPortableDeviceValues**](iportabledevicevalues.md) qui contient les options d’événement.                               |
| **\_paramètres d' \_ attribut d’événement wpd \_** | **VT \_ inconnu** | [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui contient les paramètres d’événement.              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs**](properties-and-attributes.md)
</dt> </dl>

 

 




