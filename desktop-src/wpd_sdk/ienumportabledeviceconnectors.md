---
description: prend en charge l’énumération des interfaces IPortableDeviceConnector, représentant les appareils MTP/Bluetooth qui ont été jumelés avec le PC.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interface IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 024d9a813cb20a511c1c23a414625aa78416c530521777ab2c1abaab1c4b4bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652752"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Interface IEnumPortableDeviceConnectors

l’interface **IEnumPortableDeviceConnectors** prend en charge l’énumération des interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , représentant les appareils MTP/Bluetooth qui ont été appariés avec le PC. Notez que cela permet de récupérer tous les appareils précédemment couplés, y compris ceux qui sont associés mais déconnectés. Pour déterminer si un appareil est toujours connecté, interrogez la propriété **DEVPKEY \_ MTPBTH \_ IsConnected** de cet appareil.

## <a name="members"></a>Membres

L’interface **IEnumPortableDeviceConnectors** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumPortableDeviceConnectors** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumPortableDeviceConnectors** possède ces méthodes.



| Méthode                                               | Description                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumportabledeviceconnectors-clone.md) | Crée une copie de l’interface **IEnumPortableDeviceConnectors** actuelle.<br/>                                                       |
| [**Suivant**](ienumportabledeviceconnectors-next.md)   | Récupère le suivant d’un ou plusieurs objets [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) dans la séquence d’énumération.<br/> |
| [**Initialisation**](ienumportabledeviceconnectors-reset.md) | Réinitialise la séquence d'énumération au début.<br/>                                                                                |
| [**Saut**](ienumportabledeviceconnectors-skip.md)   | Ignore le nombre spécifié d’appareils dans la séquence d’énumération.<br/>                                                               |



 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

