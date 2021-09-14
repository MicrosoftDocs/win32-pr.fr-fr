---
description: un utilisateur peut désactiver l’expérience de l’ingestion par défaut fournie par le système à l’aide des options disponibles sous l’onglet Communications de l’Windows panneau de configuration multimédia, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Désactivation de l’expérience de l’utilisation des canards par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114977"
---
# <a name="disabling-the-default-ducking-experience"></a>Désactivation de l’expérience de l’utilisation des canards par défaut

un utilisateur peut désactiver l’expérience de l’ingestion [par défaut](stream-attenuation.md) fournie par le système à l’aide des options disponibles sous l’onglet **Communications** de l’Windows panneau de configuration multimédia, Mmsys.cpl.

Lorsque l’application d’un canard est appliquée, un effet de fondu et d’atténuation est utilisé pour une période de 1 seconde. Il se peut qu’une application de jeu ne souhaite pas que le flux de communication interfère avec l’audio du jeu. Certaines applications multimédias peuvent constater que l’expérience de lecture est transférerez quand la musique est de nouveau en fondu. Ces types d’applications peuvent choisir de ne pas participer à l’expérience de l’utilisateur.

Par programme, un client direct WASAPI peut s’abonner à l’aide du gestionnaire de sessions pour la session audio qui fournit le contrôle du volume pour les flux de non-communication. Notez que même si un client ne s’en rend pas compte, il reçoit toujours les notifications du système.

Pour désactiver l’ingestion, le client doit obtenir une référence à l’interface [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) du gestionnaire de sessions. Pour désactiver l’expérience utilisateur, procédez comme suit :

1.  Instanciez l’énumérateur d’appareil et utilisez-le pour obtenir une référence au point de terminaison de l’appareil que l’application multimédia utilise pour restituer le flux de non-communication.
2.  Activez le gestionnaire de sessions à partir du point de terminaison de l’appareil et récupérez une référence à l’interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) du gestionnaire de sessions.
3.  En utilisant le pointeur [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , vous pouvez obtenir une référence à l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) du gestionnaire de sessions.
4.  Interrogez le [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) à partir de l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Appelez [**IAudioSessionControl2 :: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) et transmettez **true** ou **false** pour spécifier la préférence d’un canard. La préférence spécifiée peut être modifiée dynamiquement pendant la session. Notez que la modification de l’annulation n’entre pas en vigueur tant que le flux n’a pas été arrêté et redémarré.

Le code suivant montre comment une application peut spécifier ses préférences en matière de canard. L’appelant de la fonction doit passer **true** ou **false** dans le paramètre DuckingOptOutChecked. Selon la valeur passée, l’un des canards est activé ou désactivé par le biais de [**IAudioSessionControl2 :: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
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

[Fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtention d’événements de canard](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



