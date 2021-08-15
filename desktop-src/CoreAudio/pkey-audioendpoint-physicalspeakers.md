---
description: 'En savoir plus sur : PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358623626274a0ab3a0898e9e912e4f5f990c14d00dd6f6ef57bb4050297403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406415"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>\_AudioEndpoint \_ PhysicalSpeakers

La **propriété \_ \_ PhysicalSpeakers AudioEndpoint** spécifie le masque de configuration de canal pour l’appareil de point de terminaison audio. Le masque indique la configuration physique d’un ensemble de haut-parleurs et spécifie l’attribution de canaux aux orateurs. Pour plus d’informations sur les masques de configuration de canal, consultez les rubriques suivantes :

1.  description de la propriété de \_ configuration de canal AUDIO KSPROPERTY \_ \_ dans la documentation Windows DDK.
2.  le livre blanc intitulé « prise en charge du pilote audio pour les configurations de haut-parleur Home cinema » est intitulé « [Technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) site web ».

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.

Le membre **uintVal** de la structure **PROPVARIANT** contient un masque de configuration de canal qui est converti en type **uint**.

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

 

 




