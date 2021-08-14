---
description: 'pour Windows 7, Windows appareils mobiles prend en charge les attributs suivants pour les événements d’un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetEventAttributes.'
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
ms.openlocfilehash: 9ee6fe335d5e3906a923dfe5c470142cdf36fb1e521c3498963e478369a9b251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193290"
---
# <a name="event-attributes-portabledeviceh"></a>Attributs d’événement (PortableDevice. h)

pour Windows 7, Windows appareils mobiles prend en charge les attributs suivants pour les événements d’un service d’appareil. Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




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

 

 




