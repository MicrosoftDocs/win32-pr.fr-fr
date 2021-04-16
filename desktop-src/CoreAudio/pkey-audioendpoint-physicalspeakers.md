---
description: 'En savoir plus sur : PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524079"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>\_AudioEndpoint \_ PhysicalSpeakers

La **propriété \_ \_ PhysicalSpeakers AudioEndpoint** spécifie le masque de configuration de canal pour l’appareil de point de terminaison audio. Le masque indique la configuration physique d’un ensemble de haut-parleurs et spécifie l’attribution de canaux aux orateurs. Pour plus d’informations sur les masques de configuration de canal, consultez les rubriques suivantes :

1.  Description de la propriété de \_ configuration de canal audio KSPROPERTY \_ \_ dans la documentation de Windows DDK.
2.  Le livre blanc intitulé « prise en charge du pilote audio pour les configurations du locuteur Home Cinema » sur le site Web [des technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.

Le membre **uintVal** de la structure **PROPVARIANT** contient un masque de configuration de canal qui est converti en type **uint**.

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

 

 




