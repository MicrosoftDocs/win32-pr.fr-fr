---
description: La \_ propriété AudioEndpoint de la \_ propriété de type FormFactor spécifie le facteur de forme du périphérique de point de terminaison audio. Le facteur de forme indique les attributs physiques du périphérique de point de terminaison audio manipulé par l’utilisateur.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76b53b91a03cda5e8484878f62c3c7a205e422f53ed647d29cca6435e0f14f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018337"
---
# <a name="pkey_audioendpoint_formfactor"></a>\_AudioEndpoint \_ FormFactor

La **propriété \_ AudioEndpoint \_** de la propriété de type FormFactor spécifie le facteur de forme du périphérique de point de terminaison audio. Le facteur de forme indique les attributs physiques du périphérique de point de terminaison audio manipulé par l’utilisateur.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.

Le membre **uintVal** de la structure **PROPVARIANT** contient une valeur d’énumération qui est castée en type uint. Elle est définie sur l’une des valeurs d’énumération [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) suivantes :

-   RemoteNetworkDevice
-   Haut-parleurs
-   LineLevel
-   Un casque
-   Microphone
-   Casque
-   Téléphone
-   UnknownDigitalPassthrough
-   SPDIF
-   HDMI
-   UnknownFormFactor

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




