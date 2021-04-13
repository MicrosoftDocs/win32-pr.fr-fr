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
# <a name="rendering-a-stream"></a><span data-ttu-id="54903-103">Rendu d’un flux</span><span class="sxs-lookup"><span data-stu-id="54903-103">Rendering a Stream</span></span>

<span data-ttu-id="54903-104">Le client appelle les méthodes dans l’interface [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) pour écrire des données de rendu dans une mémoire tampon de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="54903-104">The client calls the methods in the [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) interface to write rendering data to an endpoint buffer.</span></span> <span data-ttu-id="54903-105">Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</span><span class="sxs-lookup"><span data-stu-id="54903-105">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span> <span data-ttu-id="54903-106">Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="54903-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span> <span data-ttu-id="54903-107">Pour demander une mémoire tampon de point de terminaison d’une taille particulière, le client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="54903-107">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="54903-108">Pour connaître la taille de la mémoire tampon allouée, qui peut être différente de la taille demandée, le client appelle la méthode [**IAudioClient :: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="54903-108">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="54903-109">Pour déplacer un flux de données de rendu via la mémoire tampon du point de terminaison, le client appelle également la méthode [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) et la méthode [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="54903-109">To move a stream of rendering data through the endpoint buffer, the client alternately calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method and the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method.</span></span> <span data-ttu-id="54903-110">Le client accède aux données dans la mémoire tampon du point de terminaison sous la forme d’une série de paquets de données.</span><span class="sxs-lookup"><span data-stu-id="54903-110">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="54903-111">L’appel **GetBuffer** récupère le paquet suivant afin que le client puisse le remplir avec des données de rendu.</span><span class="sxs-lookup"><span data-stu-id="54903-111">The **GetBuffer** call retrieves the next packet so that the client can fill it with rendering data.</span></span> <span data-ttu-id="54903-112">Une fois les données écrites dans le paquet, le client appelle **ReleaseBuffer** pour ajouter le paquet terminé à la file d’attente de rendu.</span><span class="sxs-lookup"><span data-stu-id="54903-112">After writing the data to the packet, the client calls **ReleaseBuffer** to add the completed packet to the rendering queue.</span></span>

<span data-ttu-id="54903-113">Pour une mémoire tampon de rendu, la valeur de remplissage qui est signalée par la méthode [**IAudioClient :: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) représente la quantité de données de rendu mises en file d’attente dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="54903-113">For a rendering buffer, the padding value that is reported by the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method represents the amount of rendering data that is queued up to play in the buffer.</span></span> <span data-ttu-id="54903-114">Une application de rendu peut utiliser la valeur de remplissage pour déterminer la quantité de données qu’elle peut écrire en toute sécurité dans la mémoire tampon sans risque de remplacer les données écrites précédemment, que le moteur audio n’a pas encore lues dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="54903-114">A rendering application can use the padding value to determine how much new data it can safely write to the buffer without the risk of overwriting previously written data that the audio engine has not yet read from the buffer.</span></span> <span data-ttu-id="54903-115">L’espace disponible est simplement la taille de la mémoire tampon moins la taille de remplissage.</span><span class="sxs-lookup"><span data-stu-id="54903-115">The available space is simply the buffer size minus the padding size.</span></span> <span data-ttu-id="54903-116">Le client peut demander une taille de paquet qui représente tout ou partie de cet espace disponible lors de son prochain appel [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="54903-116">The client can request a packet size that represents some or all of this available space in its next [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) call.</span></span>

<span data-ttu-id="54903-117">La taille d’un paquet est exprimée en *trames audio*.</span><span class="sxs-lookup"><span data-stu-id="54903-117">The size of a packet is expressed in *audio frames*.</span></span> <span data-ttu-id="54903-118">Une trame audio dans un flux PCM est un ensemble d’exemples (l’ensemble contient un échantillon pour chaque canal du flux) qui joue ou qui sont enregistrés en même temps (le battement de l’horloge).</span><span class="sxs-lookup"><span data-stu-id="54903-118">An audio frame in a PCM stream is a set of samples (the set contains one sample for each channel in the stream) that play or are recorded at the same time (clock tick).</span></span> <span data-ttu-id="54903-119">Par conséquent, la taille d’une trame audio correspond à la taille de l’échantillon multipliée par le nombre de canaux dans le flux.</span><span class="sxs-lookup"><span data-stu-id="54903-119">Thus, the size of an audio frame is the sample size multiplied by the number of channels in the stream.</span></span> <span data-ttu-id="54903-120">Par exemple, la taille de trame d’un flux stéréo (2 canaux) avec des échantillons de 16 bits est de quatre octets.</span><span class="sxs-lookup"><span data-stu-id="54903-120">For example, the frame size for a stereo (2-channel) stream with 16-bit samples is four bytes.</span></span>

<span data-ttu-id="54903-121">L’exemple de code suivant montre comment lire un flux audio sur le périphérique de rendu par défaut :</span><span class="sxs-lookup"><span data-stu-id="54903-121">The following code example shows how to play an audio stream on the default rendering device:</span></span>


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



<span data-ttu-id="54903-122">Dans l’exemple précédent, la fonction PlayAudioStream accepte un seul paramètre, `pMySource` , qui est un pointeur vers un objet qui appartient à une classe définie par le client, MyAudioSource, avec deux fonctions membres, LoadData et SetFormat.</span><span class="sxs-lookup"><span data-stu-id="54903-122">In the preceding example, the PlayAudioStream function takes a single parameter, `pMySource`, which is a pointer to an object that belongs to a client-defined class, MyAudioSource, with two member functions, LoadData and SetFormat.</span></span> <span data-ttu-id="54903-123">L’exemple de code n’inclut pas l’implémentation de MyAudioSource, car :</span><span class="sxs-lookup"><span data-stu-id="54903-123">The example code does not include the implementation of MyAudioSource because:</span></span>

-   <span data-ttu-id="54903-124">Aucun des membres de la classe ne communique directement avec l’une des méthodes des interfaces dans WASAPI.</span><span class="sxs-lookup"><span data-stu-id="54903-124">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="54903-125">La classe peut être implémentée de plusieurs façons, selon les besoins du client.</span><span class="sxs-lookup"><span data-stu-id="54903-125">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="54903-126">(Par exemple, il peut lire les données de rendu à partir d’un fichier WAV et effectuer une conversion à la volée dans le format de flux.)</span><span class="sxs-lookup"><span data-stu-id="54903-126">(For example, it might read the rendering data from a WAV file and perform on-the-fly conversion to the stream format.)</span></span>

<span data-ttu-id="54903-127">Toutefois, certaines informations sur le fonctionnement des deux fonctions sont utiles pour comprendre l’exemple.</span><span class="sxs-lookup"><span data-stu-id="54903-127">However, some information about the operation of the two functions is useful for understanding the example.</span></span>

<span data-ttu-id="54903-128">La fonction LoadData écrit un nombre spécifié de trames audio (premier paramètre) à un emplacement de mémoire tampon spécifié (deuxième paramètre).</span><span class="sxs-lookup"><span data-stu-id="54903-128">The LoadData function writes a specified number of audio frames (first parameter) to a specified buffer location (second parameter).</span></span> <span data-ttu-id="54903-129">(La taille d’une image audio est le nombre de canaux du flux multiplié par la taille de l’échantillon.) La fonction PlayAudioStream utilise LoadData pour remplir des parties de la mémoire tampon partagée avec des données audio.</span><span class="sxs-lookup"><span data-stu-id="54903-129">(The size of an audio frame is the number of channels in the stream multiplied by the sample size.) The PlayAudioStream function uses LoadData to fill portions of the shared buffer with audio data.</span></span> <span data-ttu-id="54903-130">La fonction SetFormat spécifie le format de la fonction LoadData à utiliser pour les données.</span><span class="sxs-lookup"><span data-stu-id="54903-130">The SetFormat function specifies the format for the LoadData function to use for the data.</span></span> <span data-ttu-id="54903-131">Si la fonction LoadData est en mesure d’écrire au moins un frame dans l’emplacement de mémoire tampon spécifié, mais qu’elle n’a plus de données avant d’avoir écrit le nombre spécifié de frames, elle écrit le silence dans les frames restants.</span><span class="sxs-lookup"><span data-stu-id="54903-131">If the LoadData function is able to write at least one frame to the specified buffer location but runs out of data before it has written the specified number of frames, then it writes silence to the remaining frames.</span></span>

<span data-ttu-id="54903-132">Tant que LoadData parvient à écrire au moins une trame de données réelles (pas de silence) à l’emplacement de mémoire tampon spécifié, il sort de 0 à son troisième paramètre, qui, dans l’exemple de code précédent, est un pointeur de sortie vers la `flags` variable.</span><span class="sxs-lookup"><span data-stu-id="54903-132">As long as LoadData succeeds in writing at least one frame of real data (not silence) to the specified buffer location, it outputs 0 through its third parameter, which, in the preceding code example, is an output pointer to the `flags` variable.</span></span> <span data-ttu-id="54903-133">Lorsque LoadData est en dehors des données et ne peut pas écrire un seul Frame dans l’emplacement de mémoire tampon spécifié, il n’écrit rien dans la mémoire tampon (pas même le silence) et écrit la valeur AUDCLNT \_ BUFFERFLAGS \_ Silent dans la `flags` variable.</span><span class="sxs-lookup"><span data-stu-id="54903-133">When LoadData is out of data and cannot write even a single frame to the specified buffer location, it writes nothing to the buffer (not even silence), and it writes the value AUDCLNT\_BUFFERFLAGS\_SILENT to the `flags` variable.</span></span> <span data-ttu-id="54903-134">La `flags` variable transmet cette valeur à la méthode [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , qui répond en remplissant le nombre spécifié de frames dans la mémoire tampon avec un silence.</span><span class="sxs-lookup"><span data-stu-id="54903-134">The `flags` variable conveys this value to the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method, which responds by filling the specified number of frames in the buffer with silence.</span></span>

<span data-ttu-id="54903-135">Dans son appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , la fonction PlayAudioStream dans l’exemple précédent demande une mémoire tampon partagée qui a une durée d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="54903-135">In its call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the PlayAudioStream function in the preceding example requests a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="54903-136">(La mémoire tampon allouée peut avoir une durée légèrement plus longue.) Dans ses appels initiaux aux méthodes [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) et [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , la fonction remplit l’intégralité de la mémoire tampon avant d’appeler la méthode [**IAudioClient :: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) pour commencer la diffusion de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="54903-136">(The allocated buffer might have a slightly longer duration.) In its initial calls to the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) and [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) methods, the function fills the entire buffer before calling the [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) method to begin playing the buffer.</span></span>

<span data-ttu-id="54903-137">Dans la boucle principale, la fonction remplit de façon itérative la moitié de la mémoire tampon à intervalles de demi-seconde.</span><span class="sxs-lookup"><span data-stu-id="54903-137">Within the main loop, the function iteratively fills half of the buffer at half-second intervals.</span></span> <span data-ttu-id="54903-138">Juste avant chaque appel à la fonction [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) de Windows dans la boucle principale, la mémoire tampon est pleine ou presque saturée.</span><span class="sxs-lookup"><span data-stu-id="54903-138">Just before each call to the Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function in the main loop, the buffer is full or nearly full.</span></span> <span data-ttu-id="54903-139">Lorsque l’appel de mise en **veille** retourne, la mémoire tampon est à moitié pleine.</span><span class="sxs-lookup"><span data-stu-id="54903-139">When the **Sleep** call returns, the buffer is about half full.</span></span> <span data-ttu-id="54903-140">La boucle se termine après l’appel final à la fonction LoadData affecte `flags` à la variable la valeur AUDCLNT \_ BUFFERFLAGS \_ Silent.</span><span class="sxs-lookup"><span data-stu-id="54903-140">The loop ends after the final call to the LoadData function sets the `flags` variable to the value AUDCLNT\_BUFFERFLAGS\_SILENT.</span></span> <span data-ttu-id="54903-141">À ce stade, la mémoire tampon contient au moins une trame de données réelles et peut contenir jusqu’à une demi-seconde de données réelles.</span><span class="sxs-lookup"><span data-stu-id="54903-141">At that point, the buffer contains at least one frame of real data, and it might contain as much as a half second of real data.</span></span> <span data-ttu-id="54903-142">Le reste de la mémoire tampon contient le silence.</span><span class="sxs-lookup"><span data-stu-id="54903-142">The remainder of the buffer contains silence.</span></span> <span data-ttu-id="54903-143">L’appel de mise en **veille** qui suit la boucle fournit suffisamment de temps (une demi-seconde) pour lire toutes les données restantes.</span><span class="sxs-lookup"><span data-stu-id="54903-143">The **Sleep** call that follows the loop provides sufficient time (a half second) to play all of the remaining data.</span></span> <span data-ttu-id="54903-144">Le silence qui suit les données empêche les sons indésirables avant que l’appel à la méthode [**IAudioClient :: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) arrête le flux audio.</span><span class="sxs-lookup"><span data-stu-id="54903-144">The silence that follows the data prevents unwanted sounds before the call to the [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) method stops the audio stream.</span></span> <span data-ttu-id="54903-145">Pour plus d’informations sur la mise en **veille**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="54903-145">For more information about **Sleep**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="54903-146">À la suite de l’appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , le flux reste ouvert jusqu’à ce que le client libère toutes ses références à l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) et à toutes les références aux interfaces de service obtenues par le client par le biais de la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="54903-146">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="54903-147">L’appel de [**version**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) finale ferme le flux.</span><span class="sxs-lookup"><span data-stu-id="54903-147">The final [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

<span data-ttu-id="54903-148">La fonction PlayAudioStream de l’exemple de code précédent appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un énumérateur pour les périphériques de point de terminaison audio dans le système.</span><span class="sxs-lookup"><span data-stu-id="54903-148">The PlayAudioStream function in the preceding code example calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="54903-149">À moins que le programme appelant n’ait appelé auparavant la fonction **CoCreateInstance** ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com, l’appel **CoCreateInstance** échoue.</span><span class="sxs-lookup"><span data-stu-id="54903-149">Unless the calling program previously called either the **CoCreateInstance** or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="54903-150">Pour plus d’informations sur **CoCreateInstance**, **CoCreateInstance** et **CoInitializeEx**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="54903-150">For more information about **CoCreateInstance**, **CoCreateInstance**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54903-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54903-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54903-152">Gestion de flux</span><span class="sxs-lookup"><span data-stu-id="54903-152">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
