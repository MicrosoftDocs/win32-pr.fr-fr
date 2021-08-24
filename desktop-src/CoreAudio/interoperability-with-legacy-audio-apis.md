---
description: Interopérabilité avec les API audio héritées
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interopérabilité avec les API audio héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f894c20785ebd49e50765ad67ba19056f5439bd5ab8c8fc7e0bcfbdd05fe04ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875429"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interopérabilité avec les API audio héritées

de nombreuses applications existantes utilisent des api audio héritées telles que DirectSound, DirectShow et les fonctions multimédias Windows. avec uniquement des modifications mineures, ces applications peuvent être augmentées pour utiliser les [rôles d’appareil](device-roles.md), les contrôles de volume de [session](session-volume-controls.md)et d’autres fonctionnalités des api audio de base dans Windows Vista.

Comme indiqué dans les [composants audio en mode utilisateur](user-mode-audio-components.md), les API audio principales servent de base sur laquelle sont créées les API audio de niveau supérieur. dans Windows Vista, les périphériques audio auxquels les applications accèdent via des api audio héritées telles que DirectSound et les fonctions Windows media **waveOutXxx** et **waveInXxx** sont, en fait, des [appareils de point de terminaison audio](audio-endpoint-devices.md) qui sont implémentés par les api audio de base. En raison des limitations inhérentes aux interfaces des API audio héritées, une application peut accéder à certaines des fonctionnalités des appareils de point de terminaison audio via ces interfaces. Les sections suivantes décrivent les techniques permettant d’améliorer les applications existantes en accédant aux fonctionnalités supplémentaires des appareils de point de terminaison audio directement via les API audio de base. Ces améliorations requièrent généralement uniquement des modifications mineures apportées au code d’application existant.

Les sections suivantes décrivent comment incorporer des fonctionnalités des API audio de base dans des applications existantes qui utilisent des API audio héritées :

-   [Rôles d’appareil pour les applications DirectSound](device-roles-for-directsound-applications.md)
-   [rôles d’appareil pour les Applications DirectShow](device-roles-for-directshow-applications.md)
-   [rôles d’appareil pour les Applications multimédias héritées Windows](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md)
-   [Sons de notification pour les applications audio héritées](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rôles d’appareil](device-roles.md)
</dt> </dl>

 

 



