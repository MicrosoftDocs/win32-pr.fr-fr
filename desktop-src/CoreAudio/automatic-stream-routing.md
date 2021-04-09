---
description: Cet article explique comment mettre à jour une implémentation de WASAPI pour tirer parti du routage de flux automatique.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Routage de flux automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950835"
---
# <a name="automatic-stream-routing"></a>Routage de flux automatique

Cet article explique comment mettre à jour une implémentation de WASAPI pour tirer parti du routage de flux automatique.

À compter de Windows 7, chaque fois que le périphérique audio par défaut change, le flux de lecture audio d’une application est transféré en toute transparence du périphérique audio par défaut précédent vers le nouveau périphérique audio par défaut. Ce transfert se produit automatiquement sans code d’application supplémentaire. Toutefois, avant Windows 10, version 1607, les applications qui utilisaient l’API de session audio Windows (WASAPI) de bas niveau ne pouvaient pas participer à cette fonctionnalité de routage de flux automatisé. Les applications utilisant WASAPI devaient implémenter leur propre forme de routage de flux en ajoutant du code supplémentaire pour détecter l’arrivée et la suppression des périphériques audio et basculer le flux vers ces appareils, le cas échéant. Les applications qui utilisent des WASAPI qui n’implémentent pas leur propre mécanisme de routage de flux sur l’arrivée ou la suppression d’un appareil a risqué de fournir une expérience utilisateur moins que idéale.

Depuis la version 1607 de Windows 10, les applications qui utilisent WASAPI peuvent tirer parti du routage de flux automatique. Si votre application utilise WASAPI, il est vivement recommandé de mettre à jour votre application pour tirer parti de cette nouvelle fonctionnalité en procédant comme suit :

1.  Windows 10, version 1607, définit deux nouveaux GUID qui peuvent être utilisés pour activer un rendu audio ou une interface de capture avec routage de flux automatique, le [ \_ \_ rendu audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids) et la [ \_ \_ capture audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids). Obtenir une représentation sous forme de chaîne de ces GUID en appelant [**échec stringfromiid**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid). L’exemple suivant illustre cet appel pour le GUID de rendu audio.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Activez le point de terminaison audio en passant la chaîne d’identificateur à la fonction WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) . L’exemple suivant passe dans l’identificateur de rendu audio obtenu à l’étape 1 :

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Libérez la mémoire allouée pour conserver l’identificateur de point de terminaison :

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Une fois que vous avez modifié votre application pour activer l’interface audio de la manière décrite ci-dessus, elle participera à la fonctionnalité de routage de flux automatique.

Pour illustrer le routage automatique du flux, utilisez un ordinateur portable ou une tablette équipée de haut-parleurs internes pour lire les données audio. Vous devez entendre la lecture audio via les intervenants internes de l’appareil. Pendant la lecture audio, connectez une paire de casque. Vous devez maintenant entendre la lecture audio dans le casque. Ensuite, débranchez le casque et l’audio doivent automatiquement être redirigés vers les haut-parleurs internes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Routage de flux](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
