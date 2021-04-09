---
description: La \_ propriété hyperAudioEndpoint \_ FullRangeSpeakers spécifie le masque de configuration de canal pour les haut-parleurs complets connectés à l’appareil de point de terminaison audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111326"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>\_AudioEndpoint \_ FullRangeSpeakers

La **propriété \_ hyperAudioEndpoint \_ FullRangeSpeakers** spécifie le masque de configuration de canal pour les haut-parleurs complets connectés à l’appareil de point de terminaison audio. Le masque indique la configuration physique des haut-parleurs complets et spécifie l’affectation des canaux à ces intervenants.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.

Le membre **uintVal** de la structure **PROPVARIANT** contient un masque de configuration de canal qui est converti en type **uint**.

Un orateur complet est en train de jouer des sons sur la plage complète, de graves à aigus. En règle générale, les haut-parleurs sont de gamme complète, mais les plus petits sont beaucoup moins aptes à jouer des basses. Dans Windows Vista, le moteur audio utilise cette propriété pour gérer les niveaux de basses dans le flux de sortie audio joué par l’appareil de point de terminaison audio.

Le masque de configuration de canal pour cette propriété est au même format que le masque de configuration de canal pour la propriété [**\_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) . Pour plus d’informations sur les masques de configuration de canal, consultez les rubriques suivantes :

-   Description de la propriété de \_ configuration de canal audio KSPROPERTY \_ \_ dans la documentation de Windows DDK.
-   Le livre blanc intitulé « prise en charge du pilote audio pour les configurations du locuteur Home Cinema » sur le site Web [des technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Le système obtient le masque de configuration de canal pour la \_ propriété AudioEndpoint \_ FullRangeSpeakers de l’utilisateur. L’utilisateur entre ces informations par le biais du panneau de configuration multimédia de Windows, Mmsys.cpl. Pour plus d’informations sur Mmsys.cpl, consultez la documentation de Windows DDK.

Le masque de configuration de canal pour la \_ \_ propriété AudioEndpoint FullRangeSpeakers d’un appareil de point de terminaison audio est un sous-ensemble du masque de configuration de canal pour la \_ \_ propriété PhysicalSpeakers AudioEndpoint du même appareil.

Par exemple, si un périphérique de point de terminaison audio pilote un ensemble de haut-parleurs de son surround 5,1, le masque de configuration de canal pour la \_ \_ propriété AudioEndpoint PHYSICALSPEAKERS est KSAUDIO \_ Speaker \_ 5POINT1. Ce masque indique la présence de haut-parleurs de l’avant-plan, du front-droit, du front-Center, du côté gauche et du côté droit, ainsi qu’un caisson de basses. Si les haut-parleurs de l’avant-plan et de l’avant-plan sont suffisamment grands pour produire des basses, mais que les haut-parleurs plus petits et les haut-parleurs latéraux ne le sont pas, le masque de configuration de canal pour la \_ \_ propriété AudioEndpoint FULLRANGESPEAKERS est KSAUDIO \_ Speaker \_ , qui indique uniquement les haut-parleurs avant gauche et avant. Les masques de configuration de canaux KSAUDIO \_ Speaker \_ 5POINT1 et KSAUDIO \_ Speaker \_ Stereo sont définis dans le fichier d’en-tête Ksmedia. h.

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
</dt> <dt>

[**\_Propriété AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




