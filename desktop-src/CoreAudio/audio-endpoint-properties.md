---
description: Propriétés du point de terminaison audio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Propriétés du point de terminaison audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201012"
---
# <a name="audio-endpoint-properties"></a>Propriétés du point de terminaison audio

Le fichier d’en-tête MMDeviceAPI. h définit plusieurs propriétés des [appareils de point de terminaison audio](audio-endpoint-devices.md) dans Windows Vista et versions ultérieures. Le service audio Windows définit les valeurs de ces propriétés. Les clients peuvent lire ces propriétés, mais ne doivent pas les définir. Les valeurs de propriété sont stockées en tant que structures **PROPVARIANT** .

La méthode recommandée pour lire les propriétés d’un périphérique d’entrée audio consiste à utiliser les API de l’espace de noms [**Windows. Devices. Enumeration**](/uwp/api/Windows.Devices.Enumeration) . Ces API sont prises en charge pour les applications du Windows Store et les applications de bureau. Pour les applications de bureau existantes qui lisent les propriétés des appareils à l’aide de l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , consultez Propriétés de l' [appareil](device-properties.md). **IMMDevice** n’est pas pris en charge pour les applications du Windows Store.

Pour obtenir des exemples de code qui montrent comment accéder aux propriétés d’un périphérique de point de terminaison audio, consultez les rubriques suivantes :

-   [Événements de l’appareil](device-events.md)
-   [Rôles d’appareil pour les applications DirectSound](device-roles-for-directsound-applications.md)

Pour plus d’informations sur **PROPVARIANT**, consultez la documentation SDK Windows.

Les propriétés suivantes sont spécifiques aux périphériques de point de terminaison audio.



| Propriété                                                                                                            | Description                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Association de AudioEndpoint de la \_ \_**](pkey-audioendpoint-association.md)                                          | Associe une catégorie de code confidentiel (KS) de diffusion en continu de noyau à un périphérique de point de terminaison audio.                                                                                |
| [**\_AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio.                                              |
| [**AudioEndpoint de la \_ \_ SysFx de désactivation \_**](pkey-audioendpoint-disable-sysfx.md)                                     | Indique si les effets système sont activés dans le flux en mode partagé qui circule vers ou à partir de l’appareil de point de terminaison audio.                                       |
| [**\_AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indique les attributs physiques du périphérique de point de terminaison audio.                                                                                               |
| [**\_AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Spécifie le masque de configuration de canal pour les haut-parleurs complets connectés à l’appareil de point de terminaison audio.                                         |
| [**GUID de AudioEndpoint de la \_ \_**](pkey-audioendpoint-guid.md)                                                        | Fournit l’identificateur d’appareil DirectSound qui correspond à l’appareil de point de terminaison audio.                                                                     |
| [**\_AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Définit la configuration du haut-parleur physique pour l’appareil de point de terminaison audio.                                                                                     |
| [**\_AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Spécifie le format du périphérique, qui est le format que le moteur audio utilise pour le flux en mode partagé qui circule vers ou depuis l’appareil de point de terminaison audio.       |
| [**\_AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Spécifie le format par défaut de l’appareil utilisé pour le rendu ou la capture d’un flux. Les valeurs sont remplies par le fabricant d’ordinateurs OEM dans un fichier. inf. <br/> |
| [**Le AudioEndpoint de la- \_ \_ prend en charge le \_ \_ mode EventDriven**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indique si le point de terminaison prend en charge le mode piloté par les événements. Les valeurs sont remplies par le fabricant d’ordinateurs OEM dans un fichier. inf.<br/>                                |



 

Les API audio de base prennent en charge des propriétés supplémentaires qui ne s’appliquent pas exclusivement aux périphériques de point de terminaison audio. Pour plus d’informations sur ces propriétés supplémentaires, consultez Propriétés de l' [appareil](device-properties.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

