---
description: Récupération à partir d’une erreur Invalid-Device
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Récupération à partir d’une erreur Invalid-Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca20c32be46367f53a14ce26c39f980e3649b652
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111306"
---
# <a name="recovering-from-an-invalid-device-error"></a>Récupération à partir d’une erreur Invalid-Device

La plupart des méthodes de WASAPI renvoient le code d’erreur AUDCLNT \_ E \_ Device \_ invalidé si l’appareil de point de terminaison audio utilisé par l’application cliente n’est pas valide. Ce code d’erreur indique que l’appareil de point de terminaison a été débranché, ou que le matériel audio ou les ressources matérielles associées ont été reconfigurés, désactivés, supprimés ou rendus indisponibles pour utilisation. Souvent, l’application peut récupérer à partir de cette erreur.

>[!NOTE]
> Pour plus d’informations sur la récupération à partir d’erreurs d’appareil non valides lors de l’utilisation d’API audio spatiales (ISAC), consultez [récupération d’une erreur de Invalid-Device (son spatial)](recovering-from-an-invalid-device-error-spatial-sound.md)

La stratégie qu’une application doit utiliser pour récupérer à partir d’une \_ erreur d’invalidation de l’appareil AUDCLNT E dépend de \_ \_ laquelle des techniques suivantes sont utilisées par l’application pour sélectionner un périphérique de point de terminaison audio :

-   Sélectionnez toujours l’appareil de rendu ou de capture audio par défaut.
-   Sélectionnez un périphérique de point de terminaison audio spécifique.

Dans ce dernier cas, soit l’application sélectionne automatiquement un appareil spécifique en fonction des exigences internes, soit elle permet à l’utilisateur de sélectionner explicitement un appareil dans une liste d’appareils disponibles.

Une application qui utilise l’appareil par défaut peut tenter de récupérer à partir d’une \_ erreur d’invalidation de l’appareil AUDCLNT E \_ \_ , comme suit :

1.  Libérez l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) et toutes les autres interfaces WASAPI acquises sur l’appareil.
2.  Appelez la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour récupérer le périphérique audio par défaut actuel.
3.  Essayez d’activer [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) sur le périphérique audio par défaut.

En suivant les étapes précédentes, l’application a tendance à répondre de manière appropriée, quelle que soit la cause de l' \_ \_ erreur d’invalidation de l’appareil AUDCLNT E \_ . Si la reconfiguration de l’appareil par défaut a provoqué l’erreur (par exemple, si l’utilisateur a modifié le format de flux utilisé par l’appareil), ces étapes, si elles ont échoué, permettent à l’application de continuer à utiliser le même appareil. Si l’utilisateur a désactivé ou supprimé l’appareil que l’application utilisait et qu’un autre périphérique est disponible pour assumer le rôle de périphérique par défaut, l’application peut continuer à utiliser le nouvel appareil par défaut. Dans les deux cas, l’application s’adapte automatiquement sans nécessiter l’intervention de l’utilisateur.

Une application qui sélectionne un appareil spécifique peut tenter de récupérer à partir de l' \_ erreur d’invalidation de l’appareil AUDCLNT E \_ \_ comme suit :

1.  Libérez l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) et toutes les autres interfaces WASAPI acquises sur l’appareil.
2.  Tentative d’activation d’une interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) sur le même appareil.
3.  Si l’étape 2 échoue, l’application peut, en option, inviter l’utilisateur à sélectionner un autre appareil.

L’étape 2 peut être effectuée si l’appareil utilisé par l’application a été reconfiguré mais qu’il n’a pas été désactivé ou supprimé. En cas de réussite, l’étape 2 permet à l’application de continuer à utiliser automatiquement le même appareil sans nécessiter l’intervention de l’utilisateur. L’étape 3 est appropriée si l’application permet à l’utilisateur de sélectionner explicitement un autre périphérique une fois que l’utilisateur a désactivé ou supprimé l’appareil précédemment utilisé.

Une application peut déterminer plus précisément la cause d’une erreur d’appareil non valide en s’inscrivant pour recevoir une notification lorsqu’une session perd sa connexion à un appareil. Pour activer cette notification, l’application implémente une interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) et appelle la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) pour inscrire l’interface. Quand une erreur d’appareil non valide provoque la déconnexion de la session, WASAPI appelle la méthode [**IAudioSessionEvents :: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dans l’interface inscrite. À l’aide de cette méthode, WASAPI informe l’application de la raison de la déconnexion. Dans Windows Vista, l’appel **OnSessionDisconnected** identifie les raisons suivantes :

-   L’utilisateur a supprimé l’appareil de point de terminaison audio.
-   Le service audio Windows s’est arrêté.
-   Le format de flux préféré a changé pour l’appareil auquel la session audio est connectée.
-   L’utilisateur a fermé la session Windows Terminal Services (WTS) dans laquelle la session audio s’exécutait. Pour plus d’informations sur les sessions WTS, consultez la documentation SDK Windows.
-   La session WTS dans laquelle la session audio s’exécutait a été déconnectée.
-   La session audio (en mode partagé) a été déconnectée pour rendre l’appareil de point de terminaison audio disponible pour une connexion en mode exclusif.

En réponse à l’événement de déconnexion, WASAPI ferme tous les flux qui appartiennent à la session. Si une application tente par la suite d’accéder à un flux fermé par le biais d’une méthode WASAPI comme [**IAudioClient :: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding), la méthode échoue et retourne le code d’erreur AUDCLNT E l’appareil n’est pas \_ \_ \_ valide.

La réception de notifications par l’intermédiaire de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) présente un avantage supplémentaire : les notifications arrivent de manière asynchrone. Ainsi, même lorsque le flux de communication n’est pas en cours d’exécution, l’application recevra quand même des notifications en temps utile des erreurs de périphérique non valides qui peuvent empêcher l’exécution du flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> </dl>

 

 



