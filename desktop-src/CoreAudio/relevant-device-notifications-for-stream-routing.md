---
description: En savoir plus sur les notifications pour le routage de flux. Les API implémentent le routage de flux en gérant le basculement de flux vers un nouveau point de terminaison audio par défaut.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notifications appropriées pour le routage de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0660735590853161395b1cf771ba17bbb72e48e072b2f9daa11a0841c9a5c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109459"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notifications appropriées pour le routage de flux

dans Windows 7, les api de plateforme de haut niveau qui utilisent des api Audio de base, telles que les api Media Foundation, DirectSound et Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison Audio par défaut. Les applications multimédias qui utilisent ces API utilisent le comportement de routage de flux sans aucune modification de la source. Les clients WASAPI directs peuvent utiliser les notifications envoyées par les composants audio principaux et implémenter la fonctionnalité de routage de flux.

Pour implémenter la fonctionnalité de routage de flux, un client doit écouter deux types d’événements : les notifications de modification de l’appareil et les notifications de déconnexion de la session. Dans l’implémentation fournie par les API de haut niveau, ces événements sont envoyés pour les points de terminaison de périphérique par défaut créés en appelant [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Pour plus d’informations, consultez [obtention du point de terminaison de l’appareil pour le routage de flux](getting-the-default-device-endpoint-for-stream-routing.md).

Le composant audio principal MMDeviceAPI fournit des rappels de notification lors de l’ajout, de la suppression ou de la modification de périphériques audio. Les modifications de format et de session audio sont signalées en tant qu’événements via WASAPI.

## <a name="device-change-notifications"></a>Notifications de modification d’appareil

MMDeviceAPI déclenche des événements lors de l’ajout, de la suppression ou de la modification de périphériques audio. Si le client doit fournir la fonctionnalité de routage de flux, il doit implémenter l’interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) et inscrire son implémentation auprès de MMDeviceAPI.

Pour recevoir des notifications de changement d’appareil, le client doit effectuer les tâches suivantes :

-   Implémentez l’interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) pour gérer les notifications de modification d’appareil envoyées par MMDeviceAPI.
-   Enregistrez l’implémentation de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) avec MMDeviceAPI en appelant la méthode [**IMMDeviceEnumerator :: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .

Une fois que l’implémentation de ces interfaces du client est inscrite, le client reçoit des notifications sous la forme de rappels via les méthodes de ces interfaces. Les méthodes [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) sont appelées par MMDeviceAPI lorsqu’elles déclenchent des événements au niveau du point de terminaison (modifications d’état de point de terminaison, nouvelles arrivées de point de terminaison, suppressions de point de terminaison, modifications de point de terminaison par défaut et modifications de propriété de point

Si le client souhaite fournir le routage de flux pour l’appareil par défaut, le client doit implémenter le comportement de changement d’appareil lorsqu’il reçoit la notification via le rappel [**IMMNotificationClient :: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) .

## <a name="audio-session-change-notifications"></a>Notifications de modification de session audio

Les modifications apportées aux sessions audio et aux formats sont signalées comme des événements de session audio via WASAPI. Un client WASAPI implémente l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) et enregistre l’implémentation avec WASAPI.

Pour recevoir des notifications de changement de session audio, le client doit effectuer les tâches suivantes :

-   Implémentez l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) pour gérer les notifications de modification de format envoyées par WASAPI.
-   Enregistrez l’implémentation de [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) avec WASAPI en appelant la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) .

Les méthodes [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) sont appelées par WASAPI lorsque des modifications de session audio se produisent. Ces événements sont déclenchés lorsque le nom complet de la session, le chemin d’accès de l’icône, le volume, le paramètre de regroupement ou l’état change.

Pour implémenter la fonctionnalité de routage de flux, le client doit attendre la notification de déconnexion de session. Lorsqu’une session audio est déconnectée ou que le format d’un appareil est modifié, WASAPI envoie les notifications du client sous la forme de rappels via [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Avec la notification de déconnexion, WASAPI envoie également une valeur qui indique la raison pour laquelle la session a été déconnectée. Cela peut se produire pour plusieurs raisons, par exemple lorsque l’appareil a été supprimé, que le serveur s’est arrêté, et ainsi de suite. Pour obtenir la liste complète des raisons, consultez l’énumération **AudioSessionDisconnectReason** définie dans AudioPolicy. h. Si l’appareil par défaut change, le client doit attendre les notifications (si elles n’ont pas déjà été reçues) qui sont accompagnées d’une valeur **DisconnectReasonDeviceRemoval** . En réponse à ces notifications, le client peut rouvrir le flux sur le nouvel appareil par défaut.

Étant donné que toutes ces opérations sont asynchrone, l’ordre dans lequel l’application reçoit les notifications ne peut pas être prédit. Toutefois, en général, l’application reçoit la valeur **AudioSessionDisconnect** avant la notification de modification d’appareil par défaut.

### <a name="format-change-notifications"></a>Mettre en forme les notifications de modification

Les modifications de format audio se produisent lorsque le format du flux de données change. Cela peut se produire lorsque l’utilisateur sélectionne un nouveau format dans le panneau de configuration du **son** , ou le nouvel appareil par défaut prend en charge un nouveau format (par exemple, HDMI ou certaines interfaces audio professionnelles avec un réglage manuel de l’échantillonnage). Pour notifier le client de ces types de modifications de format, WASAPI envoie une notification de session par l’implémentation inscrite de [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) avec une raison de déconnexion de **DisconnectReasonFormatChanged**. Le client peut gérer la notification en réouvrant le flux dans le nouveau format.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API MMDevice](mmdevice-api.md)
</dt> <dt>

[À propos de WASAPI](wasapi.md)
</dt> <dt>

[Routage de flux](stream-routing.md)
</dt> </dl>

 

 



