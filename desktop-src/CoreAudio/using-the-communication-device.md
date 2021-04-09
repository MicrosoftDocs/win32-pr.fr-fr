---
description: Dans Windows 7, le panneau de configuration Windows multimédia, Mmsys.cpl, fournit un nouvel onglet communications.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Utilisation d’un appareil de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861290"
---
# <a name="using-a-communication-device"></a>Utilisation d’un appareil de communication

Dans Windows 7, le panneau de configuration Windows multimédia, Mmsys.cpl, fournit un nouvel onglet **communications** . Cet onglet contient des options qui permettent à un utilisateur de définir des options qui définissent la façon dont le système gère un *périphérique de communication*. Un appareil de communication est principalement utilisé pour le placement ou la réception d’appels téléphoniques sur l’ordinateur. Pour un ordinateur qui n’a qu’un seul périphérique de rendu (conférencier) et un périphérique de capture (microphone), ces périphériques audio jouent également le rôle d’appareils de communication par défaut. Lorsqu’un utilisateur se connecte à un nouvel appareil, tel qu’un casque USB, le système effectue une détection automatique des rôles d’appareil en recherchant les paramètres de configuration qui sont renseignés par l’OEM. Si le système détermine qu’un périphérique est le mieux adapté à des fins de communication, le système affecte le rôle **eCommunications** à l’appareil. Pour ces appareils, le Mmsys.cpl Windows 7 fournit l’option **appareil de communication par défaut** qui permet à un utilisateur de sélectionner un appareil de communication pour le rendu audio (onglet **lecture** ) et la capture audio (onglet **enregistrement** ). Le système effectue une détection automatique des rôles, mais ne définit pas un appareil particulier à utiliser pour les communications. Cette opération doit être effectuée par l’utilisateur. Le nouveau rôle **eCommunications** permet à une application de faire la distinction entre un appareil qui est choisi par l’utilisateur pour gérer les appels téléphoniques et un appareil à utiliser comme périphérique multimédia (lecture musicale). Par exemple, si l’utilisateur a un casque et un conférencier connectés à l’ordinateur, le système affecte le rôle **eConsole** au haut-parleur et le rôle **eCommunications** au casque. Une fois que l’utilisateur a sélectionné le casque à utiliser comme périphérique de communication, pour développer une application de communication, vous pouvez cibler le casque en particulier pour le rendu d’un flux audio. Une application l’utilisateur ne peut pas modifier le rôle d’appareil affecté par le système. Pour plus d’informations sur les rôles d’appareil, consultez [rôles d’appareil](device-roles.md).

Les applications de communication, telles que les applications de communication unifiée et VoIP, placent et reçoivent des appels téléphoniques par le biais d’un ordinateur. Par exemple, une application VoIP peut affecter un flux qui contient la notification de sonnerie au point de terminaison d’un ensemble d’appareils de communication pour le rendu des flux audio. En outre, l’application peut ouvrir les flux d’entrée et de sortie vocaux sur les appareils de point de terminaison de capture et de rendu qui sont définis en tant qu’appareils de communication.

Pour intégrer les fonctionnalités de communication à vos applications, vous pouvez utiliser :

-   [API MMDevice](mmdevice-api.md): pour obtenir une référence au point de terminaison de l’appareil de communication.
-   [WASAPI](wasapi.md): pour afficher et capturer des flux audio via l’appareil de communication. Le système d’exploitation considère le flux ouvert sur un appareil de communication comme un *flux de communication*.

L’application de communication énumère les appareils et assure la gestion des flux de données pour un flux de communication (rendu ou capture) de la même manière qu’il gère un flux de données de non-communication à l’aide des API audio principales.

L’une des fonctionnalités que vous pouvez intégrer dans votre application de communication *est l'* entourage ou l' *atténuation du flux*. Ce comportement définit ce qui doit se produire avec d’autres sons lorsqu’un flux de communication est ouvert, par exemple lors de la réception d’un appel téléphonique sur le périphérique de communication. Le système peut désactiver ou baisser le volume audio du flux de données de non-communication en fonction du choix de l’utilisateur. Le système audio génère des événements de canard lorsqu’un flux de communication est ouvert ou fermé pour les flux de rendu ou de capture. Par défaut, le système d’exploitation fournit une expérience de l’utilisation de l’interface utilisateur par défaut. Une application multimédia peut remplacer le comportement par défaut et gérer ces événements pour fournir une expérience de canard personnalisée.

Les sections suivantes décrivent comment utiliser les API audio de base pour fournir une expérience de canard personnalisée.

-   [Expérience de l’utilisation des canards par défaut](stream-attenuation.md)
-   [Désactivation de l’expérience de l’utilisation des canards par défaut](disabling-the-ducking-experience.md)
-   [Fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md)
-   [Considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md)
-   [Obtention d’événements de canard](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Obtention d’une référence au point de terminaison de l’appareil de communication

Pour utiliser l’appareil de communication, un client direct WASAPI doit énumérer les appareils à l’aide de l’énumérateur d’appareil. Obtenir une référence au point de terminaison de l’appareil de communication par défaut en appelant [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Dans cet appel, l’application doit spécifier **eCommunications** dans le paramètre *role* pour limiter l’énumération des appareils aux périphériques de communication. Une fois que vous avez obtenu une référence au point de terminaison de périphérique pour l’appareil, vous pouvez activer les services dont la portée est définie pour le point de terminaison en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Par exemple, vous pouvez transmettre l’identificateur de service **\_ IAudioClient IID** pour activer un objet client audio et l’utiliser pour la gestion du flux de données, l’identificateur **IID \_ IAudioEndpointVolume** pour accéder aux contrôles de volume du point de terminaison de périphérique de communication, ou l’identificateur d' **IID \_ IAudioSessionManager** pour activer le gestionnaire de session qui vous permet d’interagir avec le moteur de stratégie du point de terminaison. Pour plus d’informations sur les opérations de flux, consultez [gestion des flux](stream-management.md).

À l’aide de la référence [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , vous pouvez également accéder à la Banque de propriétés pour le point de terminaison de l’appareil. Ces valeurs de propriété, telles que le nom convivial de l’appareil et le nom du fabricant, sont remplies par l’OEM et permettent à une application de déterminer les caractéristiques d’un appareil de communication. Pour plus d’informations, consultez Propriétés de l' [appareil](device-properties.md).

L’exemple de code suivant obtient une référence au point de terminaison de l’appareil de communication par défaut pour le rendu d’un flux audio.


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> </dl>

 

 



