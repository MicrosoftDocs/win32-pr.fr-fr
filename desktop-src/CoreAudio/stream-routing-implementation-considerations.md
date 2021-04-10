---
description: Dans Windows 7, les API de plateforme de haut niveau qui utilisent des API audio de base, telles que Media Foundation, DirectSound et les API Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison audio par défaut.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Considérations relatives à l’implémentation du routage de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27dc1f7e3fe56d6b421ca59f528ab1a65d2261a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950671"
---
# <a name="stream-routing-implementation-considerations"></a>Considérations relatives à l’implémentation du routage de flux

Dans Windows 7, les API de plateforme de haut niveau qui utilisent des API audio de base, telles que Media Foundation, DirectSound et les API Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison audio par défaut. Les applications multimédias qui utilisent ces API utilisent le comportement de routage de flux sans aucune modification de la source. Les clients WASAPI directs peuvent utiliser les notifications envoyées par les composants audio principaux et implémenter la fonctionnalité de routage de flux.

Les clients WASAPI directs (applications multimédias qui utilisent WASAPI directement) reçoivent de nouvelles notifications de session audio et de périphérique envoyées par les principaux composants audio. Le comportement de la fonctionnalité de routage de flux est défini par la manière dont l’application gère ces notifications.

L’API MMDevice et la session audio envoient des notifications sur les modifications de l’état des appareils et les modifications de session des clients WASAPI sous la forme de rappels. Pour recevoir ces notifications, le client doit inscrire son implémentation de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) et [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Pour plus d’informations, consultez [notifications pertinentes pour le routage de flux](relevant-device-notifications-for-stream-routing.md).

Dans le scénario de casque USB décrit dans [routage de flux](stream-routing.md), une application lit un flux audio et utilise MMDEVICEAPI et WASAPI pour afficher le flux sur le périphérique de rendu par défaut, l' **intervenant**. Lorsque l’appareil par défaut est modifié, l’application reçoit une notification [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) . L’application reçoit également des notifications [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) indiquant que l’utilisateur a supprimé l’appareil de point de terminaison audio ou que le format de flux de données a changé pour l’appareil auquel la session audio est connectée. Lors de la réception des notifications, l’application arrête la diffusion en continu vers le point de terminaison de l’orateur et ouvre à nouveau le flux de rendu sur le point de terminaison par défaut actuel, le casque.

![diagramme de workflow pour les notifications d’appareil.](images/stream-routing.gif)

En réponse à ces notifications, le client peut rouvrir le flux sur le nouvel appareil par défaut dans le nouveau format sélectionné par l’utilisateur.

## <a name="stream-managment"></a>Gestion de flux

La liste suivante résume les étapes qu’un client WASAPI doit effectuer pour fournir la fonctionnalité de basculement de flux.

1.  Attendez la notification [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) appropriée. Si l’appareil est l’appareil par défaut, la notification [**IMMNotificationClient :: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) est reçue.
2.  Si un nouvel appareil est disponible, obtenir une référence au point de terminaison du nouvel appareil. Appelez [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour le nouvel appareil par défaut. Si le nouvel appareil n’est pas le périphérique par défaut, vous pouvez récupérer l’appareil en appelant [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Pour plus d’informations, consultez [obtention du point de terminaison de l’appareil pour le routage de flux](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Attendez que [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) avec la valeur Reason.
    > [!Note]  
    > Étant donné que toutes ces opérations sont asynchrone, l’ordre dans lequel l’application reçoit les notifications de modification d’appareil et de déconnexion de session ne peut pas être prédit. L’application doit implémenter la gestion des notifications pour recevoir ces notifications dans n’importe quel ordre. Toutefois, en général, l’application reçoit la valeur **AudioSessionDisconnect** avant la notification de modification d’appareil par défaut.

     

4.  Évaluez la valeur de raison et déterminez si le flux doit être transféré vers un autre point de terminaison audio ou si le flux doit être réinitialisé avec un nouveau format.
5.  Arrêter la diffusion en continu vers l’ancien appareil par défaut si la raison indique que le flux doit être redirigé vers le nouvel appareil par défaut.
6.  Effectuez des calculs de mappage de position.
7.  Ouvrez le flux sur le nouvel appareil et transférez toutes les informations d’État.
8.  Reprendre la diffusion sur le nouvel appareil par défaut.
9.  Gérer le départ de l’ancien appareil par défaut.

Pour que l’opération de basculement de flux apparaisse transparente, elle doit être effectuée aussi rapidement que possible. Cela dépend des performances des composants impliqués dans la réinitialisation du flux sur le nouvel appareil.

## <a name="position-mapping-considerations"></a>Considérations relatives au mappage de position

Lorsque l’application obtient des notifications [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) et [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) , elle peut acheminer les flux existants vers le nouvel appareil par défaut. Lorsqu’un flux audio existant est interrompu et ouvert sur le nouvel appareil, le rendu sur le nouvel appareil doit commencer à la position à laquelle le flux a été arrêté sur l’ancien appareil. Pour ce faire, l’application doit disposer de la dernière position de l’appareil connu, afin de calculer la position de départ sur le nouvel appareil. Par exemple, cette position peut être utilisée comme décalage Delta pour le mappage de position suivant. Lorsque le flux démarre le rendu, la nouvelle position de l’appareil peut être remappée à la position de l’appareil mis en cache.

Les étapes suivantes résument le processus de transition de flux continu.

1.  Met en cache la dernière position d’appareil du flux sur l’ancien appareil.
2.  Arrêtez le flux sur l’ancien appareil.
3.  Effectuez des calculs de remappage pour accéder à la nouvelle position.
4.  Commencez le rendu du flux sur le nouvel appareil.
5.  Libérer l’ancien flux.

Pendant la transition, l’application doit s’assurer que l’horloge n’est pas désynchronisée, ce qui provoque des flux audio et vidéo hors synchronisation. Cela peut se produire si les exemples de vidéos continuent de s’afficher pendant que le flux audio est routé vers le nouvel appareil. L’application doit mettre en cache la position de l’horloge pour le calcul de remappage et vérifier que les exemples de vidéos ne sont pas rendus tant que le flux audio n’est pas rouvert sur le nouvel appareil, de sorte que lorsque le clip reprend le rendu, les flux audio et vidéo sont synchronisés. Dans certains cas, lorsque l’heure de présentation du rendu des images vidéo est basée sur l’horloge audio, il suffit d’arrêter le flux audio jusqu’à ce que le basculement de flux soit terminé et qu’aucune autre implémentation de mappage de position pour le flux vidéo ne soit nécessaire pour la synchronisation vidéo audio.

Si le rendu est en cours, [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) retourne une erreur, car l’ancien appareil est perdu, l’application n’a pas besoin d’arrêter l’ancien flux, car l’opération de diffusion en continu est déjà terminée. Pour plus d’informations sur la gestion de cette erreur, consultez [récupération à partir d’une erreur de Invalid-Device](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API MMDevice](mmdevice-api.md)
</dt> <dt>

[À propos de WASAPI](wasapi.md)
</dt> <dt>

[Routage de flux](stream-routing.md)
</dt> </dl>

 

 



