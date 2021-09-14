---
description: API EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114949"
---
# <a name="endpointvolume-api"></a>API EndpointVolume

L’API EndpointVolume permet aux clients spécialisés de contrôler et de surveiller les niveaux de volume des [appareils de point de terminaison audio](audio-endpoint-devices.md). Un client obtient des références aux interfaces dans l’API EndpointVolume en obtenant l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) d’un périphérique de point de terminaison audio et en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .

Le fichier d’en-tête Endpointvolume. h définit les interfaces dans l’API EndpointVolume.

Les applications audio qui utilisent l' [API MMDevice](mmdevice-api.md) et [WASAPI](wasapi.md) utilisent généralement l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) pour contrôler les niveaux de volume pour chaque session. Seuls deux types d’applications audio requièrent l’utilisation de l’API EndpointVolume. Ces types d’applications sont les suivants :

-   les Applications qui gèrent les niveaux de volume principal des appareils de point de terminaison audio, similaires à celles du Windows programme de contrôle de volume, Sndvol.exe.
-   Professional les applications audio (« pro audio ») qui requièrent un accès en mode exclusif aux appareils de point de terminaison audio.

l’utilisation inappropriée de l’API EndpointVolume peut interférer avec Windows stratégie audio et perturber les paramètres de volume système de l’utilisateur.

Si un périphérique de point de terminaison audio implémente des contrôles de volume matériel et de sourdine, l’API EndpointVolume utilise ces contrôles pour gérer le volume de l’appareil. Dans le cas contraire, l’API EndpointVolume implémente les contrôles dans le logiciel, de manière transparente pour le client.

Si un appareil a des contrôles volume matériel et muet, les modifications apportées aux paramètres volume et muet de l’appareil via l’API EndpointVolume affectent le niveau de volume en mode partagé et en mode exclusif. Si un appareil ne dispose pas de contrôles de volume matériel et de contrôle muet, les modifications apportées au volume logiciel et les contrôles muet via l’API EndpointVolume affectent le niveau de volume en mode partagé, mais pas en mode exclusif. En mode exclusif, le client et l’appareil échangent directement des données audio, en ignorant les contrôles logiciels.

Pour les applications qui doivent gérer le volume matériel et les contrôles de sourdine, l’API EndpointVolume offre deux avantages potentiels par rapport à l' [API DeviceTopology](devicetopology-api.md).

Tout d’abord, un certain nombre de périphériques de carte audio n’ont pas de contrôle de volume matériel. Si un appareil ne dispose pas d’un contrôle de volume matériel, l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de l’API EndpointVolume implémente automatiquement un contrôle de volume logiciel sur le flux de ce périphérique. Pour un client de l’API EndpointVolume, le résultat est le même que le contrôle du volume soit implémenté dans le matériel par l’appareil ou dans le logiciel par l’interface de l’API EndpointVolume.

Deuxièmement, même si l’appareil de l’adaptateur implémente des contrôles de volume matériel, une application qui utilise l’API DeviceTopology pour implémenter un algorithme de parcours topologique peut ne pas trouver le contrôle qu’elle recherche. En règle générale, une telle application est conçue pour traverser la topologie matérielle d’un périphérique particulier ou un ensemble d’appareils associés. L’application risque d’échouer si elle tente de traverser la topologie d’un appareil pour laquelle elle n’a pas été spécifiquement conçue ou testée.

Seules les applications spécialisées qui doivent accéder à des fonctions matérielles autres que les contrôles volume et muet requièrent l’utilisation de l’API DeviceTopology. Pour les applications qui requièrent uniquement le contrôle du niveau de volume d’un flux en mode exclusif, l’API EndpointVolume est plus simple à utiliser et fonctionne de manière fiable avec un plus grand nombre de périphériques matériels audio.

Pour obtenir des exemples de code qui utilisent les interfaces dans l’API EndpointVolume, consultez les rubriques suivantes :

-   [Contrôles du volume du point de terminaison](endpoint-volume-controls.md)
-   [Compteurs de pic](peak-meters.md)

pour voir un exemple qui utilise l’API EndpointVolume, consultez [EndpointVolume](endpointvolume.md) dans la SDK Windows.

L’API EndpointVolume implémente les interfaces suivantes.



| Interface                                                | Description                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Représente les contrôles de volume du flux audio vers ou à partir d’un périphérique de point de terminaison audio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Représente un compteur de pic sur le flux audio vers ou à partir d’un périphérique de point de terminaison audio.        |



 

En outre, les clients de l’API EndpointVolume qui requièrent la notification du volume et les modifications en sourdine des appareils de point de terminaison audio doivent implémenter l’interface suivante.



| Interface                                                            | Description                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fournit des notifications lorsque le niveau de volume ou l’État muet d’un périphérique de point de terminaison audio change. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles de volume](volume-controls.md)
</dt> <dt>

[**Interface IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 



