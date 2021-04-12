---
description: La \_ propriété AudioEndpoint de la \_ propriété de type FormFactor spécifie le facteur de forme du périphérique de point de terminaison audio. Le facteur de forme indique les attributs physiques du périphérique de point de terminaison audio manipulé par l’utilisateur.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483681"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




