---
description: À propos de WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: À propos de WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114710"
---
# <a name="about-wasapi"></a>À propos de WASAPI

l’API de Session audio Windows (WASAPI) permet aux applications clientes de gérer le flux de données audio entre l’application et un [périphérique de point de terminaison audio](audio-endpoint-devices.md).

Les fichiers d’en-tête Audioclient. h et Audiopolicy. h définissent les interfaces WASAPI.

Chaque flux audio est membre d’une [session audio](audio-sessions.md). Grâce à l’abstraction de session, un client WASAPI peut identifier un flux audio en tant que membre d’un groupe de flux audio associés. Le système peut gérer tous les flux de la session en tant qu’unité unique.

Le moteur audio est le [composant audio en mode utilisateur](user-mode-audio-components.md) par le biais duquel les applications partagent l’accès à un périphérique de point de terminaison audio. Le moteur audio transporte des données audio entre une mémoire tampon de point de terminaison et un périphérique de point de terminaison. Pour lire un flux audio via un périphérique de point de terminaison de rendu, une application écrit périodiquement des données audio dans une mémoire tampon de point de terminaison de rendu. Le moteur audio mélange les flux de données des différentes applications. Pour enregistrer un flux audio à partir d’un périphérique de point de terminaison de capture, une application lit régulièrement les données audio à partir d’une mémoire tampon de point de terminaison de capture.

WASAPI se compose de plusieurs interfaces. La première est l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) . Pour accéder aux interfaces WASAPI, un client obtient d’abord une référence à l’interface **IAudioClient** d’un périphérique de point de terminaison audio en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) avec l' *IID* de paramètre défini sur **REFIID** IID \_ IAudioClient. Le client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) pour initialiser un flux sur un appareil de point de terminaison. Après l’initialisation d’un flux, le client peut obtenir des références aux autres interfaces WASAPI en appelant la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .

La plupart des méthodes de WASAPI renvoient le code d’erreur AUDCLNT \_ E \_ Device \_ invalidé si le périphérique de point de terminaison audio utilisé par une application cliente n’est plus valide. Souvent, l’application peut récupérer à partir de cette erreur. Pour plus d’informations, consultez [récupération à partir d’une erreur de Invalid-Device](recovering-from-an-invalid-device-error.md).

WASAPI implémente les interfaces suivantes.



| Interface                                            | Description                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Permet à un client de lire des données d’entrée à partir d’une mémoire tampon de point de terminaison de capture.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Permet à un client de créer et d’initialiser un flux audio entre une application audio et le moteur audio ou la mémoire tampon matérielle d’un périphérique de point de terminaison audio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Permet à un client de surveiller le débit de données d’un flux et la position actuelle dans le flux.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Permet à un client d’écrire des données de sortie dans une mémoire tampon de point de terminaison de rendu.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Permet à un client de configurer les paramètres de contrôle pour une session audio et de surveiller les événements de la session.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Permet à un client d’accéder aux contrôles de session et aux contrôles de volume pour les sessions audio à processus croisé et spécifiques au processus.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Permet à un client de contrôler et de surveiller les niveaux de volume de tous les canaux dans un flux audio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Permet à un client de contrôler les niveaux de volume de tous les canaux de la session audio à laquelle le flux appartient.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Permet à un client de contrôler le niveau de volume principal d’une session audio.                                                                                        |



 

Les clients WASAPI qui requièrent une notification des événements liés à la session doivent implémenter l’interface suivante.



| Interface                                          | Description                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Fournit des notifications d’événements liés à la session, tels que les modifications apportées au niveau du volume, au nom complet et à l’état de session. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 



