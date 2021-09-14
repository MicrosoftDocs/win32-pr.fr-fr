---
description: Une application multimédia qui souhaite fournir une expérience d’un canard personnalisé doit écouter les notifications d’événements lorsqu’un flux de communication est ouvert ou fermé dans le système.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obtention d’événements de canard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114937"
---
# <a name="getting-ducking-events"></a>Obtention d’événements de canard

Une application multimédia qui souhaite fournir une expérience d’un canard personnalisé doit écouter les notifications d’événements lorsqu’un flux de communication est ouvert ou fermé dans le système. l’implémentation personnalisée peut être fournie à l’aide de MediaFoundation, DirectShow ou DirectSound, qui utilisent les api Audio de base. Un client direct WASAPI peut également remplacer la gestion par défaut s’il sait à quel moment la session de communication démarre et se termine.

Pour fournir une implémentation personnalisée, une application multimédia doit recevoir des notifications du système lorsqu’une application de communication démarre ou termine un flux de communication. L’application multimédia doit implémenter l’interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) et inscrire l’implémentation auprès du système audio. Une fois l’inscription réussie, l’application multimédia reçoit des notifications d’événements sous la forme de rappels via les méthodes de l’interface. Pour plus d’informations, consultez [considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md).

Pour envoyer des notifications de canard, le système audio doit savoir quelle session audio est à l’écoute des événements de l’événement. Chaque session audio est identifiée de manière unique avec un GUID (identificateur d’instance de session). Le gestionnaire de sessions permet à une application d’obtenir des informations sur la session, telles que le titre de la session audio, l’état du rendu et l’identificateur de l’instance de session. L’identificateur peut être récupéré à l’aide de l’interface de contrôle de stratégie, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).

Les étapes suivantes résument le processus d’obtention de l’identificateur d’instance de session de l’application multimédia :

1.  Instanciez l’énumérateur d’appareil et utilisez-le pour obtenir une référence au point de terminaison de l’appareil que l’application multimédia utilise pour restituer le flux de non-communication.
2.  Activez le gestionnaire de sessions à partir du point de terminaison de l’appareil et récupérez une référence à l’interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) du gestionnaire de sessions.
3.  En utilisant le pointeur [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , vous pouvez obtenir une référence à l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) du gestionnaire de sessions.
4.  Interrogez le [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) à partir de l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Appelez [**IAudioSessionControl2 :: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) et récupérez une chaîne qui contient l’identificateur de session pour la session audio en cours.

Pour obtenir des notifications sur les flux de communication, l’application multimédia appelle [**IAudioSessionManager2 :: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). L’application multimédia fournit son identificateur d’instance de session au système audio et un pointeur vers l’implémentation de [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . L’application peut désormais recevoir une notification d’événement lorsqu’un flux est ouvert sur le périphérique de communication. Pour ne plus recevoir de notification, l’application multimédia doit appeler [**IAudioSessionManager2 :: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

Le code suivant montre comment une application peut s’inscrire pour recevoir des notifications de canard. La classe CMediaPlayer est définie dans [considérations d’implémentation pour l’application de notifications](handling-audio-ducking-events-from-communication-devices.md). L’exemple [DuckingMediaPlayer](duckingmediaplayer.md) implémente cette fonctionnalité.


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’un appareil de communication](using-the-communication-device.md)
</dt> <dt>

[Expérience de l’utilisation des canards par défaut](stream-attenuation.md)
</dt> <dt>

[Désactivation de l’expérience de l’utilisation des canards par défaut](disabling-the-ducking-experience.md)
</dt> <dt>

[Fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



