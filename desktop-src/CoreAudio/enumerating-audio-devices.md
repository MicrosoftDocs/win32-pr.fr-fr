---
description: Énumération des périphériques audio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Énumération des périphériques audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707b9a88181c83344757c711af1c0199c19ebc16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033707"
---
# <a name="enumerating-audio-devices"></a>Énumération des périphériques audio

La première tâche d’une application audio client consiste à trouver un périphérique audio approprié à utiliser. L' [API MMDevice](mmdevice-api.md) permet aux clients de découvrir les [périphériques de point de terminaison audio](audio-endpoint-devices.md) dans le système et de déterminer les appareils qui conviennent à l’application. Cette API permet aux clients de récupérer les regroupements des appareils de point de terminaison disponibles et d’obtenir les fonctionnalités de chaque appareil. Le fichier d’en-tête MMDeviceAPI. h définit les interfaces dans l’API MMDevice.

Une carte audio peut contenir plusieurs appareils, par exemple, un périphérique de rendu d’onde et un périphérique de capture d’onde. Il s’agit des périphériques d’adaptateur plutôt que des appareils de point de terminaison. Comme mentionné précédemment, les périphériques d’adaptateur sont inscrits par le gestionnaire de Plug-and-Play, contrairement aux appareils de point de terminaison qui sont inscrits par le gestionnaire des points de terminaison. Chaque périphérique d’adaptateur prend généralement en charge un ou plusieurs périphériques de point de terminaison. Un périphérique de point de terminaison de rendu (par exemple, un casque) peut recevoir un flux de données audio à partir d’une application cliente, et un périphérique de point de terminaison de capture (par exemple, un microphone) peut envoyer un flux audio à une application cliente.

Avant d’énumérer les appareils de point de terminaison dans le système, le client doit d’abord appeler la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Windows pour créer un énumérateur d’appareil. Un énumérateur d’appareil est un objet avec une interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Pour plus d’informations sur **CoCreateInstance**, consultez la documentation SDK Windows.

Le client appelle la méthode [**IMMDeviceEnumerator :: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) pour créer une collection d’objets de point de terminaison. Chaque objet de point de terminaison représente un périphérique de point de terminaison audio dans le système. Dans cet appel, le client spécifie si la collection doit contenir tous les périphériques de rendu du système, tous les périphériques de capture, ou les deux.

Une collection d’appareils est un objet avec une interface [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . Chaque élément d’une collection de périphériques est un objet de point de terminaison avec au moins les deux interfaces suivantes :

-   Interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . Un client obtient une référence à l’interface **IMMDevice** d’un objet de point de terminaison dans une collection de périphériques en appelant la méthode [**IMMDeviceCollection :: Item**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item) .
-   Interface [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) . Un client obtient une référence à l’interface **IMMEndpoint** d’un objet de point de terminaison en appelant la méthode [**IMMDevice :: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

Après avoir récupéré une collection d’appareils de point de terminaison, le client peut interroger les propriétés des différents appareils dans le regroupement afin de déterminer leur aptitude à l’emploi. Pour obtenir un exemple de code qui montre comment énumérer les appareils de point de terminaison et interroger leurs propriétés, consultez Propriétés de l' [appareil](device-properties.md).

Après avoir sélectionné un appareil approprié, le client peut appeler la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour activer les interfaces spécifiques à l’appareil dans [WASAPI](wasapi.md), l' [API DeviceTopology](devicetopology-api.md)et l' [API EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> </dl>

 

 
