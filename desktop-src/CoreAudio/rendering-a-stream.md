---
description: Rendu d’un flux
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Rendu d’un flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483480"
---
# <a name="rendering-a-stream"></a>Rendu d’un flux

Le client appelle les méthodes dans l’interface [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) pour écrire des données de rendu dans une mémoire tampon de point de terminaison. Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio. Pour demander une mémoire tampon de point de terminaison d’une taille particulière, le client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Pour connaître la taille de la mémoire tampon allouée, qui peut être différente de la taille demandée, le client appelle la méthode [**IAudioClient :: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Pour déplacer un flux de données de rendu via la mémoire tampon du point de terminaison, le client appelle également la méthode [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) et la méthode [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) . Le client accède aux données dans la mémoire tampon du point de terminaison sous la forme d’une série de paquets de données. L’appel **GetBuffer** récupère le paquet suivant afin que le client puisse le remplir avec des données de rendu. Une fois les données écrites dans le paquet, le client appelle **ReleaseBuffer** pour ajouter le paquet terminé à la file d’attente de rendu.

Pour une mémoire tampon de rendu, la valeur de remplissage qui est signalée par la méthode [**IAudioClient :: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) représente la quantité de données de rendu mises en file d’attente dans la mémoire tampon. Une application de rendu peut utiliser la valeur de remplissage pour déterminer la quantité de données qu’elle peut écrire en toute sécurité dans la mémoire tampon sans risque de remplacer les données écrites précédemment, que le moteur audio n’a pas encore lues dans la mémoire tampon. L’espace disponible est simplement la taille de la mémoire tampon moins la taille de remplissage. Le client peut demander une taille de paquet qui représente tout ou partie de cet espace disponible lors de son prochain appel [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .

La taille d’un paquet est exprimée en *trames audio*. Une trame audio dans un flux PCM est un ensemble d’exemples (l’ensemble contient un échantillon pour chaque canal du flux) qui joue ou qui sont enregistrés en même temps (le battement de l’horloge). Par conséquent, la taille d’une trame audio correspond à la taille de l’échantillon multipliée par le nombre de canaux dans le flux. Par exemple, la taille de trame d’un flux stéréo (2 canaux) avec des échantillons de 16 bits est de quatre octets.

L’exemple de code suivant montre comment lire un flux audio sur le périphérique de rendu par défaut :


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
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

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
    BYTE *pData;
    DWORD flags = 0;

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

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



Dans l’exemple précédent, la fonction PlayAudioStream accepte un seul paramètre, `pMySource` , qui est un pointeur vers un objet qui appartient à une classe définie par le client, MyAudioSource, avec deux fonctions membres, LoadData et SetFormat. L’exemple de code n’inclut pas l’implémentation de MyAudioSource, car :

-   Aucun des membres de la classe ne communique directement avec l’une des méthodes des interfaces dans WASAPI.
-   La classe peut être implémentée de plusieurs façons, selon les besoins du client. (Par exemple, il peut lire les données de rendu à partir d’un fichier WAV et effectuer une conversion à la volée dans le format de flux.)

Toutefois, certaines informations sur le fonctionnement des deux fonctions sont utiles pour comprendre l’exemple.

La fonction LoadData écrit un nombre spécifié de trames audio (premier paramètre) à un emplacement de mémoire tampon spécifié (deuxième paramètre). (La taille d’une image audio est le nombre de canaux du flux multiplié par la taille de l’échantillon.) La fonction PlayAudioStream utilise LoadData pour remplir des parties de la mémoire tampon partagée avec des données audio. La fonction SetFormat spécifie le format de la fonction LoadData à utiliser pour les données. Si la fonction LoadData est en mesure d’écrire au moins un frame dans l’emplacement de mémoire tampon spécifié, mais qu’elle n’a plus de données avant d’avoir écrit le nombre spécifié de frames, elle écrit le silence dans les frames restants.

Tant que LoadData parvient à écrire au moins une trame de données réelles (pas de silence) à l’emplacement de mémoire tampon spécifié, il sort de 0 à son troisième paramètre, qui, dans l’exemple de code précédent, est un pointeur de sortie vers la `flags` variable. Lorsque LoadData est en dehors des données et ne peut pas écrire un seul Frame dans l’emplacement de mémoire tampon spécifié, il n’écrit rien dans la mémoire tampon (pas même le silence) et écrit la valeur AUDCLNT \_ BUFFERFLAGS \_ Silent dans la `flags` variable. La `flags` variable transmet cette valeur à la méthode [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , qui répond en remplissant le nombre spécifié de frames dans la mémoire tampon avec un silence.

Dans son appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , la fonction PlayAudioStream dans l’exemple précédent demande une mémoire tampon partagée qui a une durée d’une seconde. (La mémoire tampon allouée peut avoir une durée légèrement plus longue.) Dans ses appels initiaux aux méthodes [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) et [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , la fonction remplit l’intégralité de la mémoire tampon avant d’appeler la méthode [**IAudioClient :: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) pour commencer la diffusion de la mémoire tampon.

Dans la boucle principale, la fonction remplit de façon itérative la moitié de la mémoire tampon à intervalles de demi-seconde. Juste avant chaque appel à la fonction [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) de Windows dans la boucle principale, la mémoire tampon est pleine ou presque saturée. Lorsque l’appel de mise en **veille** retourne, la mémoire tampon est à moitié pleine. La boucle se termine après l’appel final à la fonction LoadData affecte `flags` à la variable la valeur AUDCLNT \_ BUFFERFLAGS \_ Silent. À ce stade, la mémoire tampon contient au moins une trame de données réelles et peut contenir jusqu’à une demi-seconde de données réelles. Le reste de la mémoire tampon contient le silence. L’appel de mise en **veille** qui suit la boucle fournit suffisamment de temps (une demi-seconde) pour lire toutes les données restantes. Le silence qui suit les données empêche les sons indésirables avant que l’appel à la méthode [**IAudioClient :: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) arrête le flux audio. Pour plus d’informations sur la mise en **veille**, consultez la documentation SDK Windows.

À la suite de l’appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , le flux reste ouvert jusqu’à ce que le client libère toutes ses références à l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) et à toutes les références aux interfaces de service obtenues par le client par le biais de la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . L’appel de [**version**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) finale ferme le flux.

La fonction PlayAudioStream de l’exemple de code précédent appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un énumérateur pour les périphériques de point de terminaison audio dans le système. À moins que le programme appelant n’ait appelé auparavant la fonction **CoCreateInstance** ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com, l’appel **CoCreateInstance** échoue. Pour plus d’informations sur **CoCreateInstance**, **CoCreateInstance** et **CoInitializeEx**, consultez la documentation SDK Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> </dl>

 

 
