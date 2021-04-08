---
description: À propos de l’API MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: À propos de l’API MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748780"
---
# <a name="about-mmdevice-api"></a>À propos de l’API MMDevice

L’API Windows Multimedia Device (MMDevice) permet aux clients audio de découvrir des [périphériques de point de terminaison audio](audio-endpoint-devices.md), de déterminer leurs fonctionnalités et de créer des instances de pilote pour ces appareils.

Le fichier d’en-tête MMDeviceAPI. h définit les interfaces dans l’API MMDevice.

L’API MMDevice est constituée de plusieurs interfaces. La première est l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Pour accéder aux interfaces dans l’API MMDevice, un client obtient une référence à l’interface **IMMDeviceEnumerator** d’un objet d’énumérateur d’appareil en appelant la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , comme indiqué dans le fragment de code suivant :


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



Dans le fragment de code précédent, CLSID \_ MMDeviceEnumerator et IID \_ IMMDeviceEnumerator sont les valeurs GUID jointes en tant qu’attributs à l’objet de classe **MMDeviceEnumerator** et à l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . L’appel [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passe ces valeurs par référence. `hr`La variable est de type **HRESULT** et `pEnumerator` la variable est un pointeur vers l’interface **IMMDeviceEnumerator** d’un objet d’énumérateur d’appareil. **IMMDeviceEnumerator** fournit des méthodes pour énumérer les appareils de point de terminaison audio. Pour plus d’informations sur l’opérateur **\_ \_ uuidof** , la fonction **CoCreateInstance** et les \_ constantes CLSCTX *xxx* , consultez la documentation SDK Windows.

Par le biais de l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , le client peut obtenir des références aux autres interfaces dans l’API MMDevice. L’API MMDevice implémente les interfaces suivantes.



| Interface                                          | Description                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Représente un périphérique audio.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Représente une collection de périphériques audio.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Fournit des méthodes pour énumérer des périphériques audio. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Représente un périphérique de point de terminaison audio.            |



 

En outre, les clients de l’API MMDevice qui requièrent la notification des modifications d’État dans les appareils de point de terminaison audio doivent implémenter l’interface suivante.



| Interface                                              | Description                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fournit des notifications lorsqu’un périphérique de point de terminaison audio est ajouté ou supprimé, lorsque l’État ou les propriétés d’un appareil change ou lorsqu’un changement du rôle par défaut est affecté à un appareil. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 
