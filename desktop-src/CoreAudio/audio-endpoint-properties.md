---
description: Propriétés du point de terminaison audio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Propriétés du point de terminaison audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf76ef70afaed98ed04ad2ee56e83c38c14ffde1bb6e4d43b557d25769afb2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828500"
---
# <a name="audio-endpoint-properties"></a>Propriétés du point de terminaison audio

le fichier d’en-tête Mmdeviceapi. h définit plusieurs propriétés des [appareils de point de terminaison audio](audio-endpoint-devices.md) dans Windows Vista et versions ultérieures. le service audio Windows définit les valeurs de ces propriétés. Les clients peuvent lire ces propriétés, mais ne doivent pas les définir. Les valeurs de propriété sont stockées en tant que structures **PROPVARIANT** .

La méthode recommandée pour lire les propriétés d’un périphérique d’entrée audio consiste à utiliser les API du [**Windows. Espace de noms Devices. Enumeration**](/uwp/api/Windows.Devices.Enumeration) . ces api sont prises en charge pour les applications de bureau Windows store et. Pour les applications de bureau existantes qui lisent les propriétés des appareils à l’aide de l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , consultez Propriétés de l' [appareil](device-properties.md). **IMMDevice** n’est pas pris en charge pour les applications Windows store.

Pour obtenir des exemples de code qui montrent comment accéder aux propriétés d’un périphérique de point de terminaison audio, consultez les rubriques suivantes :

-   [Événements de l’appareil](device-events.md)
-   [Rôles d’appareil pour les applications DirectSound](device-roles-for-directsound-applications.md)

pour plus d’informations sur **PROPVARIANT**, consultez la documentation SDK Windows.

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

 

