---
description: Contrôles de volume
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: Contrôles de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10697a38410a60af912ceb77b13ae8584d47c8fa5e8ac49fedc81d14e05305f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088199"
---
# <a name="volume-controls"></a>Contrôles de volume

Les clients qui gèrent des flux en mode partagé utilisent généralement les interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) et [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) dans [WASAPI](wasapi.md) pour contrôler et surveiller les niveaux de volume de flux. Grâce aux méthodes de l’interface **ISimpleAudioVolume** , le client peut récupérer et définir les niveaux de volume des [sessions audio](audio-sessions.md) auxquelles appartiennent les flux en mode partagé. Si sndvol ou une autre application modifie le niveau du volume de session, le client peut recevoir la notification de la modification via l’interface **IAudioSessionEvents** .

Les clients qui gèrent des flux en mode exclusif utilisent généralement les interfaces [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) et [**IAUDIOENDPOINTVOLUMECALLBACK**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) dans l' [API EndpointVolume](endpointvolume-api.md) pour contrôler et surveiller les niveaux de volume de flux. Grâce aux méthodes de l’interface **IAudioEndpointVolume** , le client peut récupérer et définir le niveau de volume d’un [périphérique de point de terminaison audio](audio-endpoint-devices.md). Si sndvol ou une autre application modifie le niveau de volume de l’appareil de point de terminaison, le client peut recevoir la notification de la modification par le biais de l’interface **IAudioEndpointVolumeCallback** .

Comme expliqué dans [sessions audio](audio-sessions.md), sndvol est le programme de contrôle du volume système. Il affiche des contrôles de volume pour les appareils de point de terminaison de rendu audio dans le système. (Actuellement, il n’affiche pas les contrôles de volume pour les appareils de point de terminaison de capture audio.) Pour afficher les contrôles de volume pour un appareil particulier, cliquez sur **périphérique** dans la barre de menus et sélectionnez un nom de périphérique dans la liste des appareils disponibles.

La fenêtre sndvol sépare les contrôles de volume d’un appareil en deux groupes. La zone de groupe sur le côté gauche de la fenêtre est intitulée **appareil**. La zone **appareil** contient un contrôle de volume unique contrôlé par l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Les modifications apportées par l’utilisateur à ce contrôle de volume peuvent être surveillées par le biais de l’interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .

La zone de groupe sur le côté droit de la fenêtre sndvol s’intitule **applications**. La zone **applications** contient les contrôles de volume des applications qui partagent actuellement l’appareil. Pour les applications qui utilisent l’appareil en mode partagé, les contrôles du volume représentent les niveaux de volume contrôlés par l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Les modifications apportées par l’utilisateur à ces contrôles de volume peuvent être surveillées par le biais de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .

Bien qu’une application en mode partagé puisse utiliser son interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) pour surveiller les modifications apportées par l’utilisateur au contrôle de volume de l’application dans la zone **applications** de la fenêtre sndvol, l’application ne peut pas surveiller les modifications apportées aux contrôles de volume d’autres applications non liées. De même, une application peut modifier les niveaux de volume de ses sessions audio par le biais de l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) , mais elle ne peut pas modifier les niveaux de volume des sessions qui appartiennent à d’autres applications non liées.

Toutefois, au moins deux applications (ou instances de la même application) associées peuvent partager le même contrôle de volume dans la zone **applications** de la fenêtre sndvol en affectant leurs flux audio à la même session inter-processus ou en associant leurs sessions respectives au même paramètre de regroupement. Pour plus d’informations, consultez [sessions audio](audio-sessions.md) et [paramètres de regroupement](grouping-parameters.md).

WASAPI fournit deux interfaces supplémentaires, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) et [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume), pour contrôler les niveaux de volume des flux en mode partagé. Ces interfaces sont principalement utilisées par des clients spécialisés qui requièrent le contrôle des niveaux de volume des canaux individuels dans une session ou des flux individuels dans une session.

L' [API DeviceTopology](devicetopology-api.md) permet aux clients d’accéder aux contrôles de volume dans les topologies des adaptateurs audio. Toutefois, les clients qui gèrent des flux en mode exclusif utilisent généralement l’API EndpointVolume au lieu de l’API DeviceTopology pour contrôler les niveaux de volume de flux. L’API EndpointVolume simplifie le contrôle du volume d’un appareil de point de terminaison de deux manières. Premièrement, si un périphérique de point de terminaison implémente un contrôle de volume matériel, l’API DeviceTopology nécessite que le client parcoure la topologie de l’appareil lors de la recherche du contrôle matériel. En revanche, l’API EndpointVolume détecte automatiquement le contrôle du volume matériel pour le client. Deuxièmement, si l’appareil de point de terminaison n’implémente pas de contrôle de volume matériel, un client DeviceTopology doit implémenter un contrôle de volume dans le logiciel. En revanche, l’API EndpointVolume remplace automatiquement un contrôle de volume logiciel pour le contrôle matériel manquant.

Les sections suivantes décrivent les contrôles de volume pour les sessions audio et les périphériques de point de terminaison audio :

-   [Contrôles du volume de session](session-volume-controls.md)
-   [Contrôles du volume du point de terminaison](endpoint-volume-controls.md)
-   [API EndpointVolume](endpointvolume-api.md)
-   [Contrôles de volume à cônes audio](audio-tapered-volume-controls.md)
-   [Compteurs de pic](peak-meters.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 



