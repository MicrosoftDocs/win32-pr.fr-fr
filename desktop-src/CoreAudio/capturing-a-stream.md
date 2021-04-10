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
# <a name="capturing-a-stream"></a><span data-ttu-id="9a770-103">Capture d’un flux</span><span class="sxs-lookup"><span data-stu-id="9a770-103">Capturing a Stream</span></span>

<span data-ttu-id="9a770-104">Le client appelle les méthodes dans l’interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) pour lire les données capturées à partir d’une mémoire tampon de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9a770-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="9a770-105">Le client partage la mémoire tampon du point de terminaison avec le moteur audio en mode partagé et avec le périphérique audio en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="9a770-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="9a770-106">Pour demander une mémoire tampon de point de terminaison d’une taille particulière, le client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="9a770-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="9a770-107">Pour connaître la taille de la mémoire tampon allouée, qui peut être différente de la taille demandée, le client appelle la méthode [**IAudioClient :: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="9a770-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="9a770-108">Pour déplacer un flux de données capturées via la mémoire tampon du point de terminaison, le client appelle alternativement la méthode [**IAudioCaptureClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) et la méthode [**IAudioCaptureClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="9a770-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="9a770-109">Le client accède aux données dans la mémoire tampon du point de terminaison sous la forme d’une série de paquets de données.</span><span class="sxs-lookup"><span data-stu-id="9a770-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="9a770-110">L’appel **GetBuffer** récupère le paquet suivant de données capturées à partir de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9a770-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="9a770-111">Après avoir lu les données du paquet, le client appelle **ReleaseBuffer** pour libérer le paquet et le rendre disponible pour d’autres données capturées.</span><span class="sxs-lookup"><span data-stu-id="9a770-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="9a770-112">La taille du paquet peut varier d’un appel [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) à l’autre.</span><span class="sxs-lookup"><span data-stu-id="9a770-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="9a770-113">Avant d’appeler **GetBuffer**, le client a la possibilité d’appeler la méthode [**IAudioCaptureClient :: GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) pour récupérer à l’avance la taille du paquet suivant.</span><span class="sxs-lookup"><span data-stu-id="9a770-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="9a770-114">En outre, le client peut appeler la méthode [**IAudioClient :: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) pour connaître la quantité totale de données capturées disponibles dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9a770-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="9a770-115">À tout moment, la taille du paquet est toujours inférieure ou égale à la quantité totale de données capturées dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9a770-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="9a770-116">Pendant chaque passe de traitement, le client a la possibilité de traiter les données capturées de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a770-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="9a770-117">Le client appelle également [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) et [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), en lisant un paquet avec chaque paire d’appels, jusqu’à ce que **GetBuffer** retourne AUDCNT \_ S \_ BUFFEREMPTY, ce qui indique que la mémoire tampon est vide.</span><span class="sxs-lookup"><span data-stu-id="9a770-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="9a770-118">Le client appelle [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) avant chaque paire d’appels à [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) et [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) jusqu’à ce que **GetNextPacketSize** signale une taille de paquet de 0, indiquant que la mémoire tampon est vide.</span><span class="sxs-lookup"><span data-stu-id="9a770-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="9a770-119">Les deux techniques produisent des résultats équivalents.</span><span class="sxs-lookup"><span data-stu-id="9a770-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="9a770-120">L’exemple de code suivant montre comment enregistrer un flux audio à partir du périphérique de capture par défaut :</span><span class="sxs-lookup"><span data-stu-id="9a770-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


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



<span data-ttu-id="9a770-121">Dans l’exemple précédent, la fonction RecordAudioStream accepte un seul paramètre, `pMySink` , qui est un pointeur vers un objet qui appartient à une classe définie par le client, MyAudioSink, avec deux fonctions, CopyData et SetFormat.</span><span class="sxs-lookup"><span data-stu-id="9a770-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="9a770-122">L’exemple de code n’inclut pas l’implémentation de MyAudioSink, car :</span><span class="sxs-lookup"><span data-stu-id="9a770-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="9a770-123">Aucun des membres de la classe ne communique directement avec l’une des méthodes des interfaces dans WASAPI.</span><span class="sxs-lookup"><span data-stu-id="9a770-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="9a770-124">La classe peut être implémentée de plusieurs façons, selon les besoins du client.</span><span class="sxs-lookup"><span data-stu-id="9a770-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="9a770-125">(Par exemple, il peut écrire les données de capture dans un fichier WAV.)</span><span class="sxs-lookup"><span data-stu-id="9a770-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="9a770-126">Toutefois, les informations sur le fonctionnement des deux méthodes sont utiles pour comprendre l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9a770-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="9a770-127">La fonction CopyData copie un nombre spécifié de trames audio à partir d’un emplacement de mémoire tampon spécifié.</span><span class="sxs-lookup"><span data-stu-id="9a770-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="9a770-128">La fonction RecordAudioStream utilise la fonction CopyData pour lire et enregistrer les données audio à partir de la mémoire tampon partagée.</span><span class="sxs-lookup"><span data-stu-id="9a770-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="9a770-129">La fonction SetFormat spécifie le format de la fonction CopyData à utiliser pour les données.</span><span class="sxs-lookup"><span data-stu-id="9a770-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="9a770-130">Tant que l’objet MyAudioSink nécessite des données supplémentaires, la fonction CopyData génère la valeur **false** à l’aide de son troisième paramètre, qui, dans l’exemple de code précédent, est un pointeur vers la variable `bDone` .</span><span class="sxs-lookup"><span data-stu-id="9a770-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="9a770-131">Lorsque l’objet MyAudioSink contient toutes les données requises, la fonction CopyData affecte la `bDone` **valeur true**, ce qui amène le programme à quitter la boucle dans la fonction RecordAudioStream.</span><span class="sxs-lookup"><span data-stu-id="9a770-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="9a770-132">La fonction RecordAudioStream alloue une mémoire tampon partagée qui a une durée d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="9a770-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="9a770-133">(La mémoire tampon allouée peut avoir une durée légèrement plus longue.) Dans la boucle principale, l’appel à la fonction [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) de Windows entraîne l’attente d’une demi-seconde par le programme.</span><span class="sxs-lookup"><span data-stu-id="9a770-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="9a770-134">Au début de chaque appel de mise en **veille** , la mémoire tampon partagée est vide ou presque vide.</span><span class="sxs-lookup"><span data-stu-id="9a770-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="9a770-135">Au moment du retour de l’appel de **veille** , la mémoire tampon partagée est à moitié remplie avec les données de capture.</span><span class="sxs-lookup"><span data-stu-id="9a770-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="9a770-136">À la suite de l’appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , le flux reste ouvert jusqu’à ce que le client libère toutes ses références à l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) et à toutes les références aux interfaces de service obtenues par le client par le biais de la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="9a770-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="9a770-137">L’appel de [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) finale ferme le flux.</span><span class="sxs-lookup"><span data-stu-id="9a770-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a770-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a770-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a770-139">Gestion de flux</span><span class="sxs-lookup"><span data-stu-id="9a770-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
