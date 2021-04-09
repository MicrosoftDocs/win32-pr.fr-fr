---
description: Un utilisateur peut désactiver l’expérience de l’ingestion par défaut fournie par le système à l’aide des options disponibles sous l’onglet Communications du panneau de configuration multimédia de Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Désactivation de l’expérience de l’utilisation des canards par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111551"
---
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="e7d56-103">Désactivation de l’expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="e7d56-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="e7d56-104">Un utilisateur peut désactiver l’expérience de l’ingestion [par défaut](stream-attenuation.md) fournie par le système à l’aide des options disponibles sous l’onglet **communications** du panneau de configuration multimédia de Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="e7d56-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="e7d56-105">Lorsque l’application d’un canard est appliquée, un effet de fondu et d’atténuation est utilisé pour une période de 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="e7d56-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="e7d56-106">Il se peut qu’une application de jeu ne souhaite pas que le flux de communication interfère avec l’audio du jeu.</span><span class="sxs-lookup"><span data-stu-id="e7d56-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="e7d56-107">Certaines applications multimédias peuvent constater que l’expérience de lecture est transférerez quand la musique est de nouveau en fondu.</span><span class="sxs-lookup"><span data-stu-id="e7d56-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="e7d56-108">Ces types d’applications peuvent choisir de ne pas participer à l’expérience de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7d56-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="e7d56-109">Par programme, un client direct WASAPI peut s’abonner à l’aide du gestionnaire de sessions pour la session audio qui fournit le contrôle du volume pour les flux de non-communication.</span><span class="sxs-lookup"><span data-stu-id="e7d56-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="e7d56-110">Notez que même si un client ne s’en rend pas compte, il reçoit toujours les notifications du système.</span><span class="sxs-lookup"><span data-stu-id="e7d56-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="e7d56-111">Pour désactiver l’ingestion, le client doit obtenir une référence à l’interface [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) du gestionnaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="e7d56-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="e7d56-112">Pour désactiver l’expérience utilisateur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e7d56-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="e7d56-113">Instanciez l’énumérateur d’appareil et utilisez-le pour obtenir une référence au point de terminaison de l’appareil que l’application multimédia utilise pour restituer le flux de non-communication.</span><span class="sxs-lookup"><span data-stu-id="e7d56-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="e7d56-114">Activez le gestionnaire de sessions à partir du point de terminaison de l’appareil et récupérez une référence à l’interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) du gestionnaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="e7d56-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="e7d56-115">En utilisant le pointeur [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , vous pouvez obtenir une référence à l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) du gestionnaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="e7d56-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="e7d56-116">Interrogez le [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) à partir de l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="e7d56-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="e7d56-117">Appelez [**IAudioSessionControl2 :: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) et transmettez **true** ou **false** pour spécifier la préférence d’un canard.</span><span class="sxs-lookup"><span data-stu-id="e7d56-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="e7d56-118">La préférence spécifiée peut être modifiée dynamiquement pendant la session.</span><span class="sxs-lookup"><span data-stu-id="e7d56-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="e7d56-119">Notez que la modification de l’annulation n’entre pas en vigueur tant que le flux n’a pas été arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="e7d56-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="e7d56-120">Le code suivant montre comment une application peut spécifier ses préférences en matière de canard.</span><span class="sxs-lookup"><span data-stu-id="e7d56-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="e7d56-121">L’appelant de la fonction doit passer **true** ou **false** dans le paramètre DuckingOptOutChecked.</span><span class="sxs-lookup"><span data-stu-id="e7d56-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="e7d56-122">Selon la valeur passée, l’un des canards est activé ou désactivé par le biais de [**IAudioSessionControl2 :: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span><span class="sxs-lookup"><span data-stu-id="e7d56-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e7d56-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7d56-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d56-124">Utilisation d’un appareil de communication</span><span class="sxs-lookup"><span data-stu-id="e7d56-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="e7d56-125">Expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="e7d56-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="e7d56-126">Fournir un comportement de canard personnalisé</span><span class="sxs-lookup"><span data-stu-id="e7d56-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="e7d56-127">Considérations relatives à l’implémentation pour l’installation de notifications</span><span class="sxs-lookup"><span data-stu-id="e7d56-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="e7d56-128">Obtention d’événements de canard</span><span class="sxs-lookup"><span data-stu-id="e7d56-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



