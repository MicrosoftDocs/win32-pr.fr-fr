---
description: Rôles d’appareil
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Rôles d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110786"
---
# <a name="device-roles"></a>Rôles d’appareil

Si un système contient au moins deux appareils de point de terminaison de rendu audio, un appareil peut être idéal pour la lecture d’un seul type de contenu audio, et un autre pour la lecture d’un autre type de contenu. Par exemple, si un système a deux périphériques de rendu, l’utilisateur peut choisir de lire la musique sur un appareil et de lire les sons de notification du système.

De même, si un système contient au moins deux périphériques de point de terminaison de capture audio, un périphérique peut être le mieux adapté à la capture d’un type de contenu audio, et un autre périphérique peut être idéal pour capturer un autre type de contenu. Par exemple, si un système a deux périphériques de capture, l’utilisateur peut choisir d’enregistrer la musique en direct sur un appareil et d’utiliser l’autre appareil pour les commandes vocales.

Les appareils peuvent avoir trois rôles : console, communications et multimédia. le tableau suivant décrit les rôles d’appareil identifiés par les trois constantes (eConsole, eCommunications et eMultimedia) dans l’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .



| ERole constante)  | Rôle de l’appareil                              | Exemples de rendu             | Exemples de capture                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | Interaction avec l’ordinateur            | Jeux et notifications système | Commandes vocales                     |
| eCommunications | Communications vocales avec une autre personne | Conversation et VoIP                  | Conversation et VoIP                      |
| eMultimedia     | Lecture ou enregistrement de contenu audio       | Musique et films               | Narration et enregistrement de musique en direct |



 

Il se peut qu’un appareil de rendu ou de capture particulier soit affecté d’un ou de plusieurs rôles dans le tableau précédent. À tout moment, chaque rôle de la table est affecté à un seul périphérique de rendu (et un seul) et à un seul périphérique de capture. Autrement dit, l’affectation de rôles aux périphériques de rendu est indépendante de l’attribution de rôles aux périphériques de capture.

Une application peut choisir de lire tous ses flux de sortie via un seul appareil de point de terminaison de rendu et d’enregistrer tous ses flux d’entrée à partir d’un seul appareil de point de terminaison de capture. Une application peut également choisir de lire certains de ses flux de sortie via un appareil de rendu et de lire d’autres flux de sortie via un autre appareil de rendu. De même, il peut choisir d’enregistrer certains de ses flux d’entrée via un appareil de capture et d’enregistrer d’autres flux d’entrée via un autre appareil de capture. Dans tous les cas, l’application peut attribuer chaque flux à l’appareil dont le rôle est le plus approprié pour ce flux.

Par exemple, une application VoIP peut affecter le flux de sortie qui contient la notification de sonnerie à l’appareil de point de terminaison de rendu avec le rôle eConsole.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> <dt>

[Utilisation des rôles d’appareil](device-roles-in-windows-vista.md)
</dt> <dt>

[Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



