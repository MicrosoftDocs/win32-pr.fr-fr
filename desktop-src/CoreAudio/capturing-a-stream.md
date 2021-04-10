---
description: Capture d’un flux
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Capture d’un flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861213"
---
# <a name="capturing-a-stream"></a>Capture d’un flux

Le client appelle les méthodes dans l’interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) pour lire les données capturées à partir d’une mémoire tampon de point de terminaison. Le client partage la mémoire tampon du point de terminaison avec le moteur audio en mode partagé et avec le périphérique audio en mode exclusif. Pour demander une mémoire tampon de point de terminaison d’une taille particulière, le client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Pour connaître la taille de la mémoire tampon allouée, qui peut être différente de la taille demandée, le client appelle la méthode [**IAudioClient :: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Pour déplacer un flux de données capturées via la mémoire tampon du point de terminaison, le client appelle alternativement la méthode [**IAudioCaptureClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) et la méthode [**IAudioCaptureClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) . Le client accède aux données dans la mémoire tampon du point de terminaison sous la forme d’une série de paquets de données. L’appel **GetBuffer** récupère le paquet suivant de données capturées à partir de la mémoire tampon. Après avoir lu les données du paquet, le client appelle **ReleaseBuffer** pour libérer le paquet et le rendre disponible pour d’autres données capturées.

La taille du paquet peut varier d’un appel [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) à l’autre. Avant d’appeler **GetBuffer**, le client a la possibilité d’appeler la méthode [**IAudioCaptureClient :: GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) pour récupérer à l’avance la taille du paquet suivant. En outre, le client peut appeler la méthode [**IAudioClient :: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) pour connaître la quantité totale de données capturées disponibles dans la mémoire tampon. À tout moment, la taille du paquet est toujours inférieure ou égale à la quantité totale de données capturées dans la mémoire tampon.

Pendant chaque passe de traitement, le client a la possibilité de traiter les données capturées de l’une des manières suivantes :

-   Le client appelle également [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) et [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), en lisant un paquet avec chaque paire d’appels, jusqu’à ce que **GetBuffer** retourne AUDCNT \_ S \_ BUFFEREMPTY, ce qui indique que la mémoire tampon est vide.
-   Le client appelle [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) avant chaque paire d’appels à [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) et [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) jusqu’à ce que **GetNextPacketSize** signale une taille de paquet de 0, indiquant que la mémoire tampon est vide.

Les deux techniques produisent des résultats équivalents.

L’exemple de code suivant montre comment enregistrer un flux audio à partir du périphérique de capture par défaut :


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
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
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
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

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



Dans l’exemple précédent, la fonction RecordAudioStream accepte un seul paramètre, `pMySink` , qui est un pointeur vers un objet qui appartient à une classe définie par le client, MyAudioSink, avec deux fonctions, CopyData et SetFormat. L’exemple de code n’inclut pas l’implémentation de MyAudioSink, car :

-   Aucun des membres de la classe ne communique directement avec l’une des méthodes des interfaces dans WASAPI.
-   La classe peut être implémentée de plusieurs façons, selon les besoins du client. (Par exemple, il peut écrire les données de capture dans un fichier WAV.)

Toutefois, les informations sur le fonctionnement des deux méthodes sont utiles pour comprendre l’exemple.

La fonction CopyData copie un nombre spécifié de trames audio à partir d’un emplacement de mémoire tampon spécifié. La fonction RecordAudioStream utilise la fonction CopyData pour lire et enregistrer les données audio à partir de la mémoire tampon partagée. La fonction SetFormat spécifie le format de la fonction CopyData à utiliser pour les données.

Tant que l’objet MyAudioSink nécessite des données supplémentaires, la fonction CopyData génère la valeur **false** à l’aide de son troisième paramètre, qui, dans l’exemple de code précédent, est un pointeur vers la variable `bDone` . Lorsque l’objet MyAudioSink contient toutes les données requises, la fonction CopyData affecte la `bDone` **valeur true**, ce qui amène le programme à quitter la boucle dans la fonction RecordAudioStream.

La fonction RecordAudioStream alloue une mémoire tampon partagée qui a une durée d’une seconde. (La mémoire tampon allouée peut avoir une durée légèrement plus longue.) Dans la boucle principale, l’appel à la fonction [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) de Windows entraîne l’attente d’une demi-seconde par le programme. Au début de chaque appel de mise en **veille** , la mémoire tampon partagée est vide ou presque vide. Au moment du retour de l’appel de **veille** , la mémoire tampon partagée est à moitié remplie avec les données de capture.

À la suite de l’appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , le flux reste ouvert jusqu’à ce que le client libère toutes ses références à l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) et à toutes les références aux interfaces de service obtenues par le client par le biais de la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . L’appel de [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) finale ferme le flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> </dl>

 

 
