---
description: Gestion de flux
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Gestion de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110934"
---
# <a name="stream-management"></a>Gestion de flux

Après avoir énuméré les [périphériques de point de terminaison audio](audio-endpoint-devices.md) dans le système et identifié un appareil de rendu ou de capture approprié, la tâche suivante pour une application cliente audio consiste à ouvrir une connexion avec l’appareil de point de terminaison et à gérer le flux de données audio sur cette connexion. [WASAPI](wasapi.md) permet aux clients de créer et de gérer des flux audio.

WASAPI implémente plusieurs interfaces pour fournir des services de gestion de flux aux clients audio. L’interface principale est [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient). Un client obtient l’interface **IAudioClient** pour un périphérique de point de terminaison audio en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (avec l' *IID* de paramètre défini sur **REFIID** IID \_ IAudioClient) sur l’objet de point de terminaison.

Le client appelle les méthodes dans l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) pour effectuer les opérations suivantes :

-   Découvrez les formats audio pris en charge par l’appareil de point de terminaison.
-   Obtient la taille de la mémoire tampon du point de terminaison.
-   Obtient le format et la latence du flux.
-   Démarrer, arrêter et réinitialiser le flux qui transite par l’appareil de point de terminaison.
-   Accédez à des services audio supplémentaires.

Pour créer un flux, un client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Par le biais de cette méthode, le client spécifie le format de données du flux, la taille de la mémoire tampon du point de terminaison et si le flux fonctionne en mode partagé ou exclusif.

Les autres méthodes de l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) se répartissent en deux groupes :

-   Méthodes qui peuvent être appelées uniquement après que le flux a été ouvert par [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Méthodes qui peuvent être appelées à tout moment avant ou après l’appel [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .

Les méthodes suivantes peuvent être appelées uniquement après l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):

-   [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**IAudioClient::GetStreamLatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**IAudioClient :: Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**IAudioClient :: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**IAudioClient :: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

Les méthodes suivantes peuvent être appelées avant ou après l’appel de [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :

-   [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Pour accéder aux services du client audio supplémentaires, le client appelle la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . Par le biais de cette méthode, le client peut obtenir des références aux interfaces suivantes :

-   [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Écrit des données de rendu dans une mémoire tampon de point de terminaison de rendu audio.

-   [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Lit les données capturées à partir d’une mémoire tampon de point de terminaison de capture audio.

-   [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Communique avec le gestionnaire de sessions audio pour configurer et gérer la session audio associée au flux.

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Contrôle le niveau de volume de la session audio associée au flux.

-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Contrôle les niveaux de volume des canaux individuels dans la session audio associée au flux.

-   [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Analyse la vitesse et la position du flux de données de flux.

En outre, les clients WASAPI qui requièrent la notification des événements liés à la session doivent implémenter l’interface suivante :

-   [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Pour recevoir des notifications d’événements, le client passe un pointeur vers son interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) à la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) en tant que paramètre d’appel.

Enfin, un client peut utiliser une API de niveau supérieur pour créer un flux audio, mais il doit également avoir accès aux contrôles de session et aux contrôles de volume pour la session qui contient le flux. En général, une API de niveau supérieur ne fournit pas cet accès. Le client peut obtenir les contrôles pour une session particulière par le biais de l’interface [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) . Cette interface permet au client d’obtenir les interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) et [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) pour une session sans demander au client d’utiliser l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) pour créer un flux et assigner le flux à la session. Un client obtient l’interface **IAudioSessionManager** pour un périphérique de point de terminaison audio en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (avec l' *IID* de paramètre défini sur **REFIID** IID \_ IAudioSessionManager) sur l’objet de point de terminaison.

Les interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)et [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) sont définies dans le fichier d’en-tête Audiopolicy. h. Toutes les autres interfaces WASAPI sont définies dans le fichier d’en-tête Audioclient. h.

Les sections suivantes décrivent comment utiliser WASAPI pour gérer des flux audio :

-   [À propos de WASAPI](wasapi.md)
-   [Rendu d’un flux](rendering-a-stream.md)
-   [Capture d’un flux](capturing-a-stream.md)
-   [Enregistrement de bouclage](loopback-recording.md)
-   [Flux en mode exclusif](exclusive-mode-streams.md)
-   [Récupération à partir d’une erreur Invalid-Device](recovering-from-an-invalid-device-error.md)
-   [Utilisation d’un appareil de communication](using-the-communication-device.md)
-   [Routage de flux](stream-routing.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 



