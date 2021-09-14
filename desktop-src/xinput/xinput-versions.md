---
title: Versions de XInput
description: XInput est une API multiplateforme qui a été fournie pour une utilisation sur Xbox et Windows.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d3624b8ea12872058ed1d874aa242a5806aec2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225465"
---
# <a name="xinput-versions"></a>Versions de XInput

XInput est une API multiplateforme qui a été fournie pour une utilisation sur Xbox et Windows. Sur Xbox, XInput est une bibliothèque statique qui est compilée dans l’exécutable principal du jeu. sur Windows, XInput est fourni sous la forme d’une DLL installée dans les dossiers système du système d’exploitation.

Il existe actuellement trois versions actuelles de la DLL XInput. choisissez la version appropriée de XInput en fonction des fonctionnalités de XInput que vous utilisez et des versions de Windows que vous avez l’intention de prendre en charge.

- XInput 1,4 : XInput 1,4 est fourni avec Windows 10. Utilisez cette version pour créer des applications UWP.
- XInput 9.1.0 : XInput 9.1.0 est fourni avec Windows Vista, Windows 7 et Windows 8. utilisez cette version si votre application de bureau est destinée à s’exécuter sur ces versions de Windows et que vous utilisez les fonctionnalités de base de XInput.
- XInput 1,3 : XInput 1,3 est fourni en tant que composant redistribuable dans le kit de développement logiciel (SDK) DirectX avec prise en charge de Windows Vista, Windows 7 et Windows 8. utilisez cette version si votre application de bureau est destinée à s’exécuter sur ces versions de Windows et que vous avez besoin de fonctionnalités qui ne sont pas prises en charge par XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1,4

XInput 1,4 est livré aujourd’hui en tant que composant système dans Windows 8 en tant que XINPUT1 \_4.DLL. Elle est disponible dans la « boîte de réception » et ne nécessite pas de redistribution avec une application. le kit de développement logiciel (SDK) Windows contient l’en-tête et la bibliothèque d’importation pour la liaison statique avec XINPUT1 \_4.DLL. pour télécharger le kit de développement logiciel (SDK) Windows 8, consultez [téléchargements pour le développement d’applications de bureau](https://developer.microsoft.com/windows/downloads/).

XInput 1,4 offre les principaux avantages suivants par rapport aux autres versions de XInput :

-   il s’agit de la seule version qui peut être utilisée dans les applications C++/DirectX Windows store.
-   La nouvelle fonction [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) fournit une chaîne d’ID de périphérique audio que vous pouvez utiliser pour ouvrir une voix ou un périphérique audio de mastérisation XAudio2 pour un casque attaché à un contrôleur courant Xbox. La fonction [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) n’est pas disponible dans cette version.
-   Fournit des fonctionnalités d’appareil améliorées, notamment XINPUT \_ Cap \_ Wireless, XInput \_ Cap \_ FFB \_ pris en charge, XInput \_ Cap \_ \_ pris en charge et XInput \_ Caps \_ aucun \_ indicateur de navigation et une création de rapports plus précise de la \_ voix XInput Caps \_ \_ prise en charge. Ces indicateurs sont combinés dans le membre **Flags** de la structure de [**\_ fonctionnalités XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) . La fonction [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) retourne **les \_ fonctionnalités XInput**.

### <a name="xinput-910"></a>XInput 9.1.0

comme XInput 1,4, XInput 9.1.0 est aujourd’hui un composant système dans Windows 10, Windows 8. x, Windows 7 et Windows Vista en tant que XINPUT9 \_ 1 \_0.DLL. Il est principalement géré pour assurer la compatibilité descendante avec les applications existantes. Avec un jeu de fonctions réduit, nous vous recommandons d’utiliser XInput 1,4, si possible. toutefois, il est pratique d’utiliser pour les applications qui doivent s’exécuter sur des versions de niveau inférieure de Windows mais n’ont pas besoin des fonctionnalités audio supplémentaires fournies par XInput 1,4 ou XInput 1,3.

l’SDK Windows contient l’en-tête et la bibliothèque d’importation pour une liaison statique par rapport à XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 présente ces inconvénients par rapport aux autres versions de XInput :

-   Pour des raisons de compatibilité descendante, [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) dans cette version de XInput retourne des informations de fonctionnalité fixes. Quel que soit l’appareil du contrôleur commun Xbox attaché, **XInputGetCapabilities** dans XInput 9.1.0 signalera toujours un sous-type d’appareil de boîtier. Elle ne retourne pas le \_ bit de \_ fonction sans fil XInput Cap, même si un appareil sans fil est connecté.
-   Vous ne pouvez pas déterminer le casque pour un ID d’utilisateur donné. la fonction [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) n’est pas disponible et la fonction [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) ne retourne aucun résultat sur Windows 8. x ou Windows 10.
-   Les fonctions [**XInputEnable**](/windows/desktop/api/XInput/nf-xinput-xinputenable), [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)et [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) ne sont pas disponibles.

### <a name="xinput-13"></a>XInput 1,3

Certaines versions précédentes de XInput ont été fournies en tant que dll redistribuables dans le kit de développement logiciel (SDK) DirectX. La première version redistribuable de XInput, XInput 1,1, est fournie dans la version d’avril 2006 du SDK DirectX. La dernière version à envoyer dans le kit de développement logiciel (SDK) DirectX était XInput 1,3, disponible dans la version de juin 2010 du SDK DirectX hérité. *Le kit de développement logiciel (SDK) DirectX n’est plus disponible sur les téléchargements Microsoft*.

vous pouvez utiliser XInput 1,3 pour les applications qui prennent en charge des versions de niveau inférieure de Windows et qui requièrent des fonctionnalités non fournies par XInput 9.1.0 (autrement dit, le rapport de sous-type correct, la prise en charge audio, la prise en charge explicite des rapports de batterie, etc.).
