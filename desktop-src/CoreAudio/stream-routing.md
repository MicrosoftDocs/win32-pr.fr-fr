---
description: Le routage de flux est la capacité d’une application multimédia à basculer les flux entre les appareils avec une interruption minimale de la lecture ou de la session de capture.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Routage de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e76944954c969ce458175585076d23ce015ea573a86e3f89dbbcd296aff444
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018227"
---
# <a name="stream-routing"></a>Routage de flux

Le *routage de flux* est la capacité d’une application multimédia à basculer les flux entre les appareils avec une interruption minimale de la lecture ou de la session de capture.

Un ordinateur peut avoir plusieurs périphériques de rendu et de capture. Le système répertorie ces périphériques dans le panneau de configuration **sons** . Dans cette liste, un utilisateur peut définir un appareil comme périphérique par défaut pour chaque rôle : lecture, enregistrement ou quatre rôles de communication (rendu de la console, capture de la console, rendu de communication ou capture de communication). La liste des appareils peut être modifiée de manière dynamique, car certains de ces appareils peuvent être temporairement disponibles, par exemple un casque USB. Lorsque plusieurs appareils sont disponibles, l’utilisateur peut modifier la valeur par défaut sur un autre appareil. L’utilisateur peut également modifier le format d’un appareil (taux d’échantillonnage, bits par échantillon, etc.) sous l’onglet **avancé** des propriétés de l’appareil.

Imaginez un scénario dans lequel un utilisateur sélectionne les **intervenants** comme appareil par défaut pour le rendu des flux audio. L’utilisateur connecte ensuite un casque USB, sélectionne le casque comme nouvel appareil par défaut et modifie le taux d’échantillonnage de l’appareil de 44,1 kHz à 48 kHz. L’utilisateur souhaite lire le flux audio sur le casque à la nouvelle fréquence d’échantillonnage avec une interruption minimale de la session de streaming.

Dans ce scénario, l’application multimédia doit gérer deux cas :

-   Le flux doit être transféré vers le nouvel appareil par défaut avec une interruption minimale de la lecture.
-   Le nouvel appareil doit reprendre la lecture dans le nouveau format (c’est-à-dire que l’utilisateur peut modifier plus que le taux d’échantillonnage).

dans Windows Vista, pour prendre en charge ce scénario, l’application multimédia devait fournir l’implémentation du routage de flux. L’application était responsable de l’arrêt des flux existants et du redémarrage des flux sur le nouvel appareil. Si l’utilisateur a modifié l’appareil par défaut ou son format Mix modifié, toutes les sessions associées ont été fermées et l’application devait gérer la récupération.

dans Windows 7, une application peut transférer en toute transparence un flux à partir d’un périphérique par défaut existant vers un nouveau point de terminaison audio par défaut. Les ensembles d’API audio de haut niveau, tels que Media Foundation, DirectSound et les API WAVE, implémentent la fonctionnalité de routage de flux. Les applications multimédias qui utilisent ces ensembles d’API pour lire ou capturer un flux à partir de l’appareil par défaut utilisent l’implémentation par défaut et n’ont pas besoin de modifier l’application. Toutefois, si votre application multimédia utilise MMDeviceAPI ou WASAPI directement, l’application doit fournir l’implémentation du routage du flux.

> [!Note]  
> MMDeviceAPI et WASAPI sont des composants d’API audio essentiels qu’une application peut utiliser pour afficher ou capturer un flux sur un appareil. Le MMDeviceAPI Découvre le nouvel appareil de point de terminaison audio et WASAPI gère le flux de données audio entre une application multimédia et l’appareil de point de terminaison audio.

 

Pour implémenter la fonctionnalité de routage de flux, l’application doit écouter les notifications envoyées par MMDeviceAPI et WASAPI lorsque :

-   L’appareil par défaut est modifié par l’utilisateur.
-   L’appareil par défaut existant est supprimé et un nouveau périphérique par défaut est ajouté.
-   Le format de l’appareil a été modifié.

En gérant ces notifications, une application peut effectuer les opérations de gestion de flux nécessaires lors du transfert du flux vers le nouvel appareil par défaut. En outre, l’application peut afficher ou capturer des flux existants en utilisant le nouveau format spécifié par l’utilisateur pendant qu’une session de rendu est active.

Cette section contient les rubriques suivantes :

-   [Obtention du point de terminaison de l’appareil pour le routage du flux](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Notifications appropriées pour le routage de flux](relevant-device-notifications-for-stream-routing.md)
-   [Considérations relatives à l’implémentation du routage de flux](stream-routing-implementation-considerations.md)

les exemples suivants, inclus dans le SDK Windows, montrent comment une application peut gérer les notifications de routage de flux.

-   [RenderSharedTimerDriven](rendersharedtimerdriven.md)
-   [RenderSharedEventDriven](rendersharedeventdriven.md)
-   [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)
-   [RenderExclusiveEventDriven](renderexclusiveeventdriven.md)
-   [CaptureSharedTimerDriven](capturesharedtimerdriven.md)
-   [CaptureSharedEventDriven](capturesharedeventdriven.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> <dt>

[À propos de l’API MMDevice](mmdevice-api.md)
</dt> <dt>

[À propos de WASAPI](wasapi.md)
</dt> </dl>

 

 



