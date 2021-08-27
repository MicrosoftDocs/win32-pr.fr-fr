---
description: Cette référence de programmation pour le kit de développement logiciel (SDK) audio principal comprend les propriétés suivantes.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Propriétés audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2d6513798a03cbcd9092e24b37900b5eb686d5fd0c434480a933af50c02fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058999"
---
# <a name="core-audio-properties"></a>Propriétés audio principales

Cette référence de programmation pour le kit de développement logiciel (SDK) audio principal comprend les propriétés suivantes.

## <a name="audio-endpoint-properties"></a>Propriétés du point de terminaison audio

Le kit de développement logiciel (SDK) audio principal comprend plusieurs propriétés des [appareils de point de terminaison audio](audio-endpoint-devices.md). Pour plus d’informations, consultez [Propriétés du point de terminaison audio](audio-endpoint-properties.md).

les propriétés suivantes sont définies dans Mmdeviceapi. h dans Windows Vista et versions ultérieures.



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
| [**\_AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio. <br/>                                                                                    |



 

## <a name="device-properties"></a>Propriétés de l’appareil

Le kit de développement logiciel (SDK) audio de base comprend plusieurs propriétés d' [appareils de point de terminaison audio](audio-endpoint-devices.md). Pour plus d’informations, consultez Propriétés de l' [appareil](device-properties.md).

les propriétés suivantes sont définies dans Functiondiscoverykeys \_ devpkey. h dans Windows Vista et versions ultérieures.



| Propriété                                                                         | Description                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Deviceinterface \_ FriendlyName FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nom convivial de la carte audio à laquelle l’appareil de point de terminaison est attaché (par exemple, « carte audio XYZ »).                                                                               |
| [**Périphérique de l' \_ appareil \_**](pkey-device-devicedesc.md)                       | Description de l’appareil du point de terminaison (par exemple, « Speakers »).                                                                                                                          |
| [**Périphérique de l' \_ appareil \_**](pkey-device-friendlyname.md)                   | Nom convivial de l’appareil de point de terminaison (par exemple, « Speakers (carte audio XYZ) »).                                                                                                           |
| **\_ContainerId d’appareil \_**                                                    | Stocke l’identificateur de conteneur du périphérique PnP qui implémente le point de terminaison audio. pour plus d’informations sur cette propriété, consultez « référence des propriétés de l’appareil » dans la documentation WDK de Windows. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de référence de programmation](programming-reference.md)
</dt> </dl>

 

 




