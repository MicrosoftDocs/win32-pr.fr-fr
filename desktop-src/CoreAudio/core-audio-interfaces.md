---
description: 'Cette référence de programmation pour le kit de développement logiciel (SDK) audio principal comprend les interfaces suivantes :'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Interfaces audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eed875bad93bed1625a175bd74b849f139a0140
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110018"
---
# <a name="core-audio-interfaces"></a>Interfaces audio principales

Cette référence de programmation pour le kit de développement logiciel (SDK) audio principal comprend les interfaces suivantes :

## <a name="mmdevice-api"></a>API MMDevice

L’API Windows Multimedia Device (MMDevice) permet aux clients audio de découvrir des [périphériques de point de terminaison audio](audio-endpoint-devices.md), de déterminer leurs fonctionnalités et de créer des instances de pilote pour ces appareils. Le fichier d’en-tête MMDeviceAPI. h définit les interfaces dans l’API MMDevice. Pour plus d’informations, consultez [à propos de l’API MMDevice](mmdevice-api.md).

Le tableau suivant répertorie les interfaces MMDevice disponibles avec le kit de développement logiciel (SDK) audio principal pour Windows Vista.



| Interface                                              | Description                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Représente un périphérique audio.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Représente une collection de périphériques audio.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Fournit des méthodes pour énumérer des périphériques audio.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Représente un périphérique de point de terminaison audio.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fournit des notifications lorsqu’un périphérique de point de terminaison audio est ajouté ou supprimé, lorsque l’État ou les propriétés d’un appareil change ou lorsqu’un changement du rôle par défaut est affecté à un appareil. |



 

## <a name="wasapi"></a>WASAPI

L’API de session audio Windows (WASAPI) permet aux applications clientes de gérer le flux de données audio entre l’application et un [périphérique de point de terminaison audio](audio-endpoint-devices.md). Les fichiers d’en-tête Audioclient. h et Audiopolicy. h définissent les interfaces WASAPI. Pour plus d’informations, consultez [à propos de WASAPI](wasapi.md).

Le tableau suivant répertorie les interfaces WASAPI disponibles avec le kit de développement logiciel (SDK) audio principal pour Windows Vista et versions ultérieures.



| Interface                                                                                    | Description                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Représente une opération asynchrone activant une interface [WASAPI](wasapi.md) et fournit une méthode pour récupérer les résultats de l’activation.<br/> S’applique à partir de Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Fournit un rappel pour indiquer que l’activation d’une interface [WASAPI](wasapi.md) est terminée.<br/> S’applique à partir de Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Permet à un client de lire des données d’entrée à partir d’une mémoire tampon de point de terminaison de capture.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Permet à un client de créer et d’initialiser un flux audio entre une application audio et le moteur audio ou la mémoire tampon matérielle d’un périphérique de point de terminaison audio.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Permet à un client de surveiller le débit de données d’un flux et la position actuelle dans le flux.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Permet à un client d’obtenir la position actuelle de l’appareil.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Permet à un client de définir le taux d’échantillonnage d’un flux.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Permet à un client d’écrire des données de sortie dans une mémoire tampon de point de terminaison de rendu.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Permet à un client de configurer les paramètres de contrôle pour une session audio et de surveiller les événements de la session.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Permet à un client d’obtenir des informations sur la session audio.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Permet à un client d’accéder aux contrôles de session et aux contrôles de volume pour les sessions audio à processus croisé et spécifiques au processus.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Gère tous les sous-mixages, y compris l’énumération et la notification des sous-combinaisons. Il assure également la prise en charge des notifications.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Permet à un client d’énumérer des sessions audio.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Permet à un client de contrôler et de surveiller les niveaux de volume de tous les canaux dans un flux audio.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Permet à un client de contrôler les niveaux de volume de tous les canaux de la session audio à laquelle le flux appartient.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Permet à un client de contrôler le niveau de volume principal d’une session audio.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Fournit des notifications d’événements liés à la session, tels que les modifications apportées au niveau du volume, au nom complet et à l’état de session.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Envoie des notifications lorsque des modifications de session se produisent. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Envoie des notifications concernant les modifications du système en attente.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>API DeviceTopology

L’API DeviceTopology fournit aux applications clientes la possibilité de traverser les topologies de matériel fonctionnelle des appareils de rendu et de capture audio. Le fichier d’en-tête Devicetopology. h définit les interfaces dans l’API DeviceTopology. Pour plus d’informations, consultez [topologies d’appareils](device-topologies.md) et [**API DeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology).

Le tableau suivant répertorie les interfaces DeviceTopology disponibles avec le kit de développement logiciel (SDK) audio principal pour Windows Vista et versions ultérieures.



| Interface                                                           | Description                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Permet d’accéder à un contrôle d’obtention automatique de matériel (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Fournit l’accès à un contrôle de niveau de basses matériel.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Fournit l’accès à un contrôle de configuration de canal matériel.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Fournit l’accès à un contrôle de multiplexeur matériel (sélecteur d’entrée).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Fournit l’accès à un contrôle de compensation « intensité sonore ».                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Permet d’accéder à un contrôle de niveau de milieu matériel.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Permet d’accéder à un contrôle matériel muet.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Fournit l’accès à un contrôle de démultiplexeur matériel (sélecteur de sortie).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Permet d’accéder à un contrôle de pointe matériel.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Permet d’accéder à un contrôle matériel au niveau des aigus.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Fournit l’accès à un contrôle de volume matériel.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Représente un point de connexion entre des composants.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Représente une interface de contrôle sur une partie (sous-unité ou connecteur).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Représente une propriété spécifique à l’appareil d’un connecteur ou d’une sous-unité.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Permet d’accéder à la topologie d’un périphérique audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Fournit des informations sur les formats de données audio pris en charge par une connexion d’e/s configurée par logiciel (généralement un canal DMA) entre le périphérique audio et la mémoire système.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Fournit des informations sur les connecteurs ou connecteurs internes qui fournissent une connexion physique entre un appareil sur une carte audio et un périphérique de point de terminaison externe ou interne (par exemple, un microphone ou un lecteur de CD). |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Fournit un accès pratique à la propriété **\_ \_ Description2 Jack KSPROPERTY** d’un connecteur à un appareil de point de terminaison.<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Fournit des informations sur le récepteur Jack si le Jack est pris en charge par le matériel.<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Représente une partie (connecteur ou sous-unité) d’une topologie d’appareil.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Représente une liste de parties (connecteurs et sous-unités).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Représente une interface de contrôle de sous-unité générique qui fournit un contrôle par canal sur le niveau du volume, en décibels, d’un flux audio ou d’une bande de fréquence dans un flux audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Représente une sous-unité matérielle (par exemple, un contrôle au niveau du volume) qui se trouve dans le chemin d’accès aux données entre un client et un périphérique de point de terminaison audio.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Fournit des notifications lorsque l’état d’un composant (connecteur ou sous-unité) change.                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>API EndpointVolume

L’API EndpointVolume permet aux clients spécialisés de contrôler et de surveiller les niveaux de volume des [appareils de point de terminaison audio](audio-endpoint-devices.md). Le fichier d’en-tête Endpointvolume. h définit les interfaces dans l’API EndpointVolume. Pour plus d’informations, consultez [**API EndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

Le tableau suivant répertorie les interfaces EndpointVolume disponibles avec le kit de développement logiciel (SDK) audio principal pour Windows Vista.



| **Interface**                                                        | **Description**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Représente les contrôles de volume du flux audio vers ou à partir d’un périphérique de point de terminaison audio.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Fournit des contrôles de volume sur le flux audio vers ou à partir d’un point de terminaison d’appareil.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Représente un compteur de pic sur le flux audio vers ou à partir d’un périphérique de point de terminaison audio.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fournit des notifications lorsque le niveau de volume ou l’État muet d’un périphérique de point de terminaison audio change. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de référence de programmation](programming-reference.md)
</dt> </dl>

 

