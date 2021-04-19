---
description: API DeviceTopology
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: API DeviceTopology
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 472c02cd59ca0cadd922cbe398a768c97cfab73a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106538369"
---
# <a name="devicetopology-api"></a>API DeviceTopology

Reportez-vous à l' [exemple de capture de voix haute qualité Microsoft DMO](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

L’API DeviceTopology fournit aux applications clientes la possibilité de traverser les topologies de matériel fonctionnelle des appareils de rendu et de capture audio. Via les interfaces et les méthodes de l’API DeviceTopology, les clients peuvent découvrir les sous-unités fonctionnelles (par exemple, le contrôle du volume) qui se trouvent le long des chemins de données qui mènent à et à partir des [périphériques de point de terminaison audio](audio-endpoint-devices.md). Les clients peuvent traverser les topologies internes des périphériques de carte audio et des périphériques de point de terminaison audio, et effectuer un pas à pas détaillé sur les connexions qui lient un appareil à un autre. Pour plus d’informations, consultez [topologies d’appareils](device-topologies.md).

Le fichier d’en-tête Devicetopology. h définit les interfaces dans l’API DeviceTopology.

Pour accéder aux interfaces de l’API DeviceTopology, un client obtient d’abord une référence à l’interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) pour un périphérique de point de terminaison audio en procédant comme suit :

1.  En utilisant l’une des techniques décrites dans l' [**interface IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice), obtenez une référence à l’interface **IMMDevice** pour un périphérique de point de terminaison audio.
2.  Appelez la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) avec l' *IID* de paramètre défini sur **REFIID** IID \_ IDeviceTopology.

Le client peut obtenir des références aux autres interfaces dans l’API DeviceTopology en appelant les méthodes dans l’interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) .

L’API DeviceTopology implémente les interfaces suivantes.



| Interface                                                  | Description                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Permet d’accéder à un contrôle d’obtention automatique de matériel (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Fournit l’accès à un contrôle de niveau de basses matériel.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Fournit l’accès à un contrôle de configuration de canal matériel.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Fournit l’accès à un contrôle de multiplexeur matériel (sélecteur d’entrée).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Fournit l’accès à un contrôle de compensation « intensité sonore ».                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Permet d’accéder à un contrôle de niveau de milieu matériel.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Permet d’accéder à un contrôle matériel muet.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Fournit l’accès à un contrôle de démultiplexeur matériel (sélecteur de sortie).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Permet d’accéder à un contrôle de pointe matériel.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Permet d’accéder à un contrôle matériel au niveau des aigus.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Fournit l’accès à un contrôle de volume matériel.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Représente un point de connexion entre des composants.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Représente une interface de contrôle sur une partie (sous-unité ou connecteur).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Représente une propriété spécifique à l’appareil d’un connecteur ou d’une sous-unité.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Permet d’accéder à la topologie d’un périphérique audio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Fournit des informations sur les formats de données audio pris en charge par une connexion d’e/s configurée par logiciel (généralement un canal DMA) entre le périphérique audio et la mémoire système.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Fournit des informations sur les connecteurs ou connecteurs internes qui fournissent une connexion physique entre un appareil sur une carte audio et un périphérique de point de terminaison externe ou interne (par exemple, un microphone ou un lecteur de CD). |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Représente une partie (connecteur ou sous-unité) d’une topologie d’appareil.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Représente une liste de parties (connecteurs et sous-unités).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Représente une interface de contrôle de sous-unité générique qui fournit un contrôle par canal sur le niveau du volume, en décibels, d’un flux audio ou d’une bande de fréquence dans un flux audio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Représente une sous-unité matérielle (par exemple, un contrôle au niveau du volume) qui se trouve dans le chemin d’accès aux données entre un client et un périphérique de point de terminaison audio.                                                                             |



 

Les clients d’API DeviceTopology qui requièrent la notification des événements de modification de contrôle dans les connecteurs et sous-unités doivent implémenter l’interface suivante.



| Interface                                            | Description                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Fournit des notifications lorsque l’état d’un composant (connecteur ou sous-unité) change. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Topologies d’appareils](device-topologies.md)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 
