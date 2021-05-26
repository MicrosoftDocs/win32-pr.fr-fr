---
description: Fichiers d’en-tête et composants système
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Fichiers d’en-tête et composants système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424289"
---
# <a name="header-files-and-system-components"></a>Fichiers d’en-tête et composants système

Le tableau suivant répertorie les fichiers d’en-tête qui contiennent les définitions d’interface des quatre principaux composants audio.



| Composant audio principal                         | Fichier d’en-tête                  |
|----------------------------------------------|------------------------------|
| [API MMDevice](mmdevice-api.md)             | MMDeviceAPI. h                |
| [WASAPI](wasapi.md)                         | Audioclient. h, Audiopolicy. h |
| [API DeviceTopology](devicetopology-api.md) | Devicetopology. h             |
| [API EndpointVolume](endpointvolume-api.md) | Endpointvolume. h             |



 

Un autre fichier d’en-tête, Audiosessiontypes. h, définit les constantes utilisées par WASAPI. Ces fichiers d’en-tête se trouvent dans le répertoire% MSSdk% \\ include, où% MSSdk% est le répertoire racine de l’installation SDK Windows sur votre ordinateur.

Chaque API du tableau précédent se compose d’un ensemble d’interfaces COM associées. Étant donné que certains aspects de la diffusion audio dépendent de la faible latence et de la synchronisation précise, les implémentations des API MMDevice, WASAPI, DeviceTopology et EndpointVolume n’utilisent pas l’infrastructure Microsoft .NET ou l’environnement d’exécution managé.

Les API audio de base sont implémentées dans les composants système en mode utilisateur Audioses.dll et Mmdevapi.dll. Les applications clientes n’accèdent pas directement aux points d’entrée de ces dll. Au lieu de cela, les clients appellent la fonction **CoCreateInstance** ou **CoCreateInstanceEx** pour obtenir l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) de l’objet de classe MMDeviceEnumerator. Cet objet énumère les [périphériques de point de terminaison audio](audio-endpoint-devices.md) dans le système. L’interface **IMMDeviceEnumerator** fait partie de l’API MMDevice. À partir de cette interface, les clients peuvent obtenir directement ou indirectement les autres interfaces de l’API MMDevice, y compris l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . **IMMDevice** représente un périphérique de point de terminaison audio particulier. Par le biais de **IMMDevice**, les clients peuvent obtenir directement ou indirectement les interfaces spécifiques à l’appareil dans WASAPI, l’API DeviceTopology et l’API EndpointVolume. Pour plus d’informations sur **CoCreateInstance** et **CoCreateInstanceEx**, consultez la documentation SDK Windows. Pour plus d’informations sur l’accès aux interfaces dans les API audio de base, consultez [énumération des périphériques audio](enumerating-audio-devices.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des API audio Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



