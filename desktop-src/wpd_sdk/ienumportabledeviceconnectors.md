---
description: Prend en charge l’énumération des interfaces IPortableDeviceConnector, représentant les appareils MTP/Bluetooth qui ont été couplés avec le PC.
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
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202909"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Interface IEnumPortableDeviceConnectors

L’interface **IEnumPortableDeviceConnectors** prend en charge l’énumération des interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , représentant les appareils MTP/Bluetooth qui ont été couplés avec le PC. Notez que cela permet de récupérer tous les appareils précédemment couplés, y compris ceux qui sont associés mais déconnectés. Pour déterminer si un appareil est toujours connecté, interrogez la propriété **DEVPKEY \_ MTPBTH \_ IsConnected** de cet appareil.

## <a name="members"></a>Membres

L’interface **IEnumPortableDeviceConnectors** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumPortableDeviceConnectors** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumPortableDeviceConnectors** possède ces méthodes.



| Méthode                                               | Description                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumportabledeviceconnectors-clone.md) | Crée une copie de l’interface **IEnumPortableDeviceConnectors** actuelle.<br/>                                                       |
| [**Suivant**](ienumportabledeviceconnectors-next.md)   | Récupère le suivant d’un ou plusieurs objets [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) dans la séquence d’énumération.<br/> |
| [**Réinitialiser**](ienumportabledeviceconnectors-reset.md) | Réinitialise la séquence d'énumération au début.<br/>                                                                                |
| [**Saut**](ienumportabledeviceconnectors-skip.md)   | Ignore le nombre spécifié d’appareils dans la séquence d’énumération.<br/>                                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

