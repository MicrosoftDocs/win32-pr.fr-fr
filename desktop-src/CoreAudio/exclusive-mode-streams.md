---
description: Exclusive-Mode Flux
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode Flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50bc9b17dbb508d04bd4665b48dfaa8f1373cc1e167b892f7ac791b3d9a0d0b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104409"
---
# <a name="exclusive-mode-streams"></a>Exclusive-Mode Flux

Comme expliqué précédemment, si une application ouvre un flux en mode exclusif, l’application utilise exclusivement l’appareil de point de terminaison audio qui lit ou enregistre le flux. En revanche, plusieurs applications peuvent partager un périphérique de point de terminaison audio en ouvrant des flux en mode partagé sur l’appareil.

L’accès en mode exclusif à un périphérique audio peut bloquer les sons importants du système, empêcher l’interopérabilité avec d’autres applications et dégrader l’expérience utilisateur. Pour atténuer ces problèmes, une application avec un flux en mode exclusif abandonne généralement le contrôle du périphérique audio lorsque l’application n’est pas le processus de premier plan ou n’est pas active en continu.

La latence du flux est le délai inhérent au chemin de données qui connecte la mémoire tampon de point de terminaison d’une application à un périphérique de point de terminaison audio. Pour un flux de rendu, la latence est le délai maximal entre le moment où une application écrit un échantillon dans une mémoire tampon de point de terminaison et le moment où l’échantillon est audible à travers les intervenants. Pour un flux de capture, la latence est le délai maximal entre le moment où un son entre dans le microphone et le moment où une application peut lire l’exemple pour ce son à partir du tampon de point de terminaison.

Les applications qui utilisent des flux en mode exclusif le font souvent, car elles nécessitent des latences faibles dans les chemins d’accès aux données entre les périphériques de point de terminaison audio et les threads d’application qui accèdent aux mémoires tampons de point de terminaison. En règle générale, ces threads s’exécutent en priorité relativement élevée et se planifient pour s’exécuter à intervalles réguliers qui sont proches ou identiques à l’intervalle périodique qui sépare les passages successifs de traitement par le matériel audio. Pendant chaque passe, le matériel audio traite les nouvelles données dans les mémoires tampons de point de terminaison.

Pour obtenir les plus petites latences de flux, une application peut nécessiter un matériel audio spécial et un système informatique légèrement chargé. La conduite du matériel audio au-delà de ses limites de synchronisation ou du chargement du système avec des tâches haute priorité concurrentes peut provoquer un problème dans un flux audio à faible latence. Par exemple, pour un flux de rendu, un problème peut se produire si l’écriture de l’application échoue dans une mémoire tampon de point de terminaison avant que le matériel audio ne lise la mémoire tampon, ou si le matériel ne parvient pas à lire le tampon avant que la mémoire tampon ne soit planifiée. En règle générale, une application destinée à être exécutée sur une grande variété de matériel audio et dans un large éventail de systèmes doit être suffisamment longue pour éviter des problèmes dans tous les environnements cibles.

Windows Vista offre plusieurs fonctionnalités pour prendre en charge les applications qui nécessitent des flux audio à faible latence. Comme indiqué dans les [composants audio en mode utilisateur](user-mode-audio-components.md), les applications qui effectuent des opérations critiques peuvent appeler les fonctions du service Planificateur de classes multimédias (MMCSS) pour augmenter la priorité des threads sans refuser les ressources du processeur aux applications de faible priorité. En outre, la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) prend en charge un \_ indicateur de EventCallback suivante STREAMFLAGS AUDCLNT \_ qui permet au thread de maintenance de mémoire tampon d’une application de planifier son exécution lorsqu’une nouvelle mémoire tampon est disponible à partir du périphérique audio. En utilisant ces fonctionnalités, un thread d’application peut réduire l’incertitude quant au moment de son exécution, ce qui réduit le risque de problèmes dans un flux audio à faible latence.

Les pilotes pour les cartes audio plus anciennes sont susceptibles d’utiliser l’interface DDI WaveCyclic ou WavePci, tandis que les pilotes pour les cartes audio plus récentes sont plus susceptibles de prendre en charge l’interface DDI WaveRT. Pour les applications en mode exclusif, les pilotes WaveRT peuvent offrir de meilleures performances que les pilotes WaveCyclic ou WavePci, mais les pilotes WaveRT requièrent des capacités matérielles supplémentaires. Ces fonctionnalités incluent la possibilité de partager des mémoires tampons matérielles directement avec les applications. Avec le partage direct, aucune intervention du système n’est requise pour transférer des données entre une application en mode exclusif et le matériel audio. En revanche, les pilotes WaveCyclic et WavePci conviennent aux cartes audio plus anciennes et moins compatibles. Ces adaptateurs s’appuient sur des logiciels système pour transporter des blocs de données (attachés à des paquets de demande d’e/s système ou des IRP) entre les mémoires tampons d’application et les mémoires tampons matérielles. En outre, les périphériques audio USB s’appuient sur des logiciels système pour transporter des données entre les mémoires tampons d’application et les mémoires tampons matérielles. Pour améliorer les performances des applications en mode exclusif qui se connectent aux périphériques audio qui reposent sur le système pour le transport de données, WASAPI augmente automatiquement la priorité des threads système qui transfèrent les données entre les applications et le matériel. WASAPI utilise MMCSS pour augmenter la priorité des threads. dans Windows Vista, si un thread système gère le transport de données pour un flux de lecture audio en mode exclusif avec un format PCM et une période d’appareil inférieure à 10 millisecondes, WASAPI affecte le nom de tâche MMCSS « Pro audio » au thread. Si la période d’appareil du flux est supérieure ou égale à 10 millisecondes, WASAPI assigne le nom de tâche MMCSS « audio » au thread. pour plus d’informations sur les DDIs WaveCyclic, WavePci et WaveRT, consultez la documentation Windows DDK. Pour plus d’informations sur la sélection d’une période d’appareil appropriée, consultez [**IAudioClient :: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).

Comme décrit dans la section [contrôles de volume de session](session-volume-controls.md), [WASAPI](wasapi.md) fournit les interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)et [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) pour contrôler les niveaux de volume des flux audio en mode partagé. Toutefois, les contrôles dans ces interfaces n’ont aucun effet sur les flux en mode exclusif. Au lieu de cela, les applications qui gèrent des flux en mode exclusif utilisent généralement l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) dans l' [API EndpointVolume](endpointvolume-api.md) pour contrôler les niveaux de volume de ces flux. Pour plus d’informations sur cette interface, consultez [contrôles du volume du point de terminaison](endpoint-volume-controls.md).

Pour chaque périphérique de lecture et périphérique de capture dans le système, l’utilisateur peut contrôler si l’appareil peut être utilisé en mode exclusif. Si l’utilisateur désactive l’utilisation en mode exclusif de l’appareil, l’appareil peut être utilisé pour lire ou enregistrer uniquement des flux en mode partagé.

Si l’utilisateur active l’utilisation en mode exclusif de l’appareil, l’utilisateur peut également contrôler si une demande d’utilisation de l’appareil en mode exclusif par une application est préoccupée par l’utilisation de l’appareil par des applications qui peuvent actuellement exécuter ou enregistrer des flux en mode partagé via l’appareil. Si la préemption est activée, une demande par une application pour prendre le contrôle exclusif de l’appareil réussit si l’appareil n’est pas en cours d’utilisation ou si l’appareil est utilisé en mode partagé, mais la demande échoue si une autre application a déjà le contrôle exclusif de l’appareil. Si la préemption est désactivée, une demande d’une application qui prend le contrôle exclusif de l’appareil réussit si l’appareil n’est pas en cours d’utilisation, mais la demande échoue si l’appareil est déjà utilisé en mode partagé ou en mode exclusif.

dans Windows Vista, les paramètres par défaut d’un périphérique de point de terminaison audio sont les suivants :

-   L’appareil peut être utilisé pour lire ou enregistrer des flux en mode exclusif.
-   Une demande d’utilisation d’un appareil pour lire ou enregistrer un flux en mode exclusif prévaut sur tout flux en mode partagé en cours de lecture ou d’enregistrement via l’appareil.

**Pour modifier les paramètres du mode exclusif d’un appareil de lecture ou d’enregistrement**

1.  Cliquez avec le bouton droit sur l’icône de haut-parleur dans la zone de notification, située sur le côté droit de la barre des tâches, puis sélectionnez **périphériques de lecture** ou **périphériques d’enregistrement**. (vous pouvez également exécuter le Windows panneau de configuration multimédia, Mmsys.cpl à partir d’une fenêtre d’invite de commandes. Pour plus d’informations, consultez la section Notes dans les [ \_ \_ constantes](device-state-xxx-constants.md)de l’état de l’appareil xxx.)
2.  Une fois la fenêtre **audio** affichée, sélectionnez **lecture** ou **enregistrement**. Sélectionnez ensuite une entrée dans la liste des noms d’appareils, puis cliquez sur **Propriétés**.
3.  Une fois que la fenêtre **Propriétés** s’affiche, cliquez sur **avancé**.
4.  Pour permettre aux applications d’utiliser l’appareil en mode exclusif, cochez la case **autoriser les applications à prendre le contrôle exclusif de cet appareil**. Pour désactiver l’utilisation en mode exclusif de l’appareil, désactivez la case à cocher.
5.  Si l’utilisation du mode exclusif de l’appareil est activée, vous pouvez spécifier si une demande de contrôle exclusif de l’appareil est réussie si l’appareil est en train de visionner ou d’enregistrer des flux en mode partagé. Pour attribuer la priorité aux applications en mode exclusif sur les applications en mode partagé, cochez la case **nommer les applications en mode exclusif priorité**. Pour refuser la priorité des applications en mode exclusif sur les applications en mode partagé, désactivez la case à cocher.

L’exemple de code suivant montre comment lire un flux audio à faible latence sur un périphérique de rendu audio configuré pour une utilisation en mode exclusif :


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;
    DWORD taskIndex = 0;
    
    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



Dans l’exemple de code précédent, la fonction PlayExclusiveStream s’exécute dans le thread d’application qui sert les tampons de point de terminaison pendant la diffusion d’un flux de rendu. La fonction accepte un seul paramètre, pMySource, qui est un pointeur vers un objet qui appartient à une classe définie par le client, MyAudioSource. Cette classe a deux fonctions membres, LoadData et SetFormat, qui sont appelées dans l’exemple de code. MyAudioSource est décrit dans [rendu d’un flux](rendering-a-stream.md).

La fonction PlayExclusiveStream appelle une fonction d’assistance, GetStreamFormat, qui négocie avec le périphérique de rendu par défaut pour déterminer si l’appareil prend en charge un format de flux en mode exclusif pouvant être utilisé par l’application. Le code de la fonction GetStreamFormat n’apparaît pas dans l’exemple de code ; Cela est dû au fait que les détails de son implémentation dépendent entièrement des exigences de l’application. Toutefois, le fonctionnement de la fonction GetStreamFormat peut être décrit simplement : elle appelle la méthode [**IAudioClient :: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) une ou plusieurs fois pour déterminer si l’appareil prend en charge un format approprié. Les exigences de l’application déterminent les formats que GetStreamFormat présente à la méthode **IsFormatSupported** et l’ordre dans lequel elle les présente. Pour plus d’informations sur **IsFormatSupported**, consultez [formats de périphérique](device-formats.md).

Après l’appel de GetStreamFormat, la fonction PlayExclusiveStream appelle la méthode [**IAudioClient :: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) pour obtenir la période de périphérique minimale prise en charge par le matériel audio. Ensuite, la fonction appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) pour demander une durée de mémoire tampon égale à la période minimale. Si l’appel est effectué, la méthode **Initialize** alloue deux tampons de point de terminaison, chacun d’entre eux ayant une durée égale à la période minimale. Plus tard, lorsque le flux audio commence à s’exécuter, l’application et le matériel audio partagent les deux mémoires tampons de la manière « ping-pong », c’est-à-dire que l’application écrit dans une mémoire tampon, le matériel lit à partir de l’autre mémoire tampon.

Avant de démarrer le flux, la fonction PlayExclusiveStream effectue les opérations suivantes :

-   Crée et inscrit le descripteur d’événement par le biais duquel il recevra des notifications lorsque les mémoires tampons seront prêtes à être remplies.
-   Remplit la première mémoire tampon avec des données de la source audio pour réduire le délai à partir duquel le flux commence à s’exécuter lorsque le son initial est audible.
-   Appelle la fonction **AvSetMmThreadCharacteristics** pour demander que MMCSS augmente la priorité du thread dans lequel PlayExclusiveStream s’exécute. (Lorsque l’exécution du flux s’arrête, l’appel de la fonction **AvRevertMmThreadCharacteristics** restaure la priorité du thread d’origine.)

pour plus d’informations sur **AvSetMmThreadCharacteristics** et **AvRevertMmThreadCharacteristics**, consultez la documentation SDK Windows.

Pendant que le flux est en cours d’exécution, chaque itération de la boucle **while** dans l’exemple de code précédent remplit une mémoire tampon de point de terminaison. Entre les itérations, l’appel de fonction **WaitForSingleObject** attend que le handle d’événement soit signalé. Lorsque le descripteur est signalé, le corps de la boucle effectue les opérations suivantes :

1.  Appelle la méthode [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) pour accéder à la mémoire tampon suivante.
2.  Remplit la mémoire tampon.
3.  Appelle la méthode [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) pour libérer la mémoire tampon.

pour plus d’informations sur **WaitForSingleObject**, consultez la documentation SDK Windows.

Si la carte audio est contrôlée par un pilote WaveRT, la signalisation du descripteur d’événement est liée aux notifications de transfert DMA du matériel audio. Pour un périphérique audio USB ou pour un périphérique audio contrôlé par un pilote WaveCyclic ou WavePci, la signalisation du descripteur d’événement est liée à la saisie semi-automatique des IRP qui transfèrent les données de la mémoire tampon d’application vers la mémoire tampon matérielle.

L’exemple de code précédent pousse le matériel audio et le système informatique à leurs limites de performances. Tout d’abord, pour réduire la latence du flux, l’application planifie son thread de maintenance de mémoire tampon afin d’utiliser la période de périphérique minimale prise en charge par le matériel audio. deuxièmement, pour vous assurer que le thread s’exécute de manière fiable dans chaque période de l’appareil, l’appel de fonction **AvSetMmThreadCharacteristics** définit le paramètre TaskName sur « Pro Audio », qui est, dans Windows Vista, le nom de tâche par défaut avec la priorité la plus élevée. Déterminez si les exigences de synchronisation de votre application peuvent être assouplies sans compromettre son utilité. Par exemple, l’application peut planifier son thread de maintenance de mémoire tampon pour utiliser une période plus longue que la valeur minimale. Un délai plus long peut permettre d’utiliser en toute sécurité une priorité de thread inférieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> </dl>

 

 



