---
description: Vous pouvez diffuser des données audio dans XAudio2 en créant un thread distinct et effectuer des lectures de mémoire tampon des données audio dans le thread de streaming, puis utiliser des rappels pour contrôler ce thread.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 'Procédure : diffuser un son en continu à partir du disque'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757689"
---
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="84ae7-103">Procédure : diffuser un son en continu à partir du disque</span><span class="sxs-lookup"><span data-stu-id="84ae7-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="84ae7-104">Ce contenu s’applique uniquement aux applications de bureau et nécessite une révision pour fonctionner dans une application Windows Store.</span><span class="sxs-lookup"><span data-stu-id="84ae7-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="84ae7-105">Reportez-vous à la documentation de **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)et **GetOverlappedResultEx**.</span><span class="sxs-lookup"><span data-stu-id="84ae7-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="84ae7-106">Consultez l’exemple StreamEffect Windows 8 dans la [Galerie d’exemples SDK Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="84ae7-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="84ae7-107">Vous pouvez diffuser des données audio dans XAudio2 en créant un thread distinct et effectuer des lectures de mémoire tampon des données audio dans le thread de streaming, puis utiliser des rappels pour contrôler ce thread.</span><span class="sxs-lookup"><span data-stu-id="84ae7-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="84ae7-108">Exécution des lectures de mémoire tampon dans le thread de streaming</span><span class="sxs-lookup"><span data-stu-id="84ae7-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="84ae7-109">Création de la classe de rappel</span><span class="sxs-lookup"><span data-stu-id="84ae7-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="84ae7-110">Exécution des lectures de mémoire tampon dans le thread de streaming</span><span class="sxs-lookup"><span data-stu-id="84ae7-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="84ae7-111">Pour effectuer des lectures de mémoire tampon dans le thread de streaming, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="84ae7-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="84ae7-112">Créez un tableau de mémoires tampons de lecture.</span><span class="sxs-lookup"><span data-stu-id="84ae7-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="84ae7-113">Initialise une structure OVERLAPPED.</span><span class="sxs-lookup"><span data-stu-id="84ae7-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="84ae7-114">La structure est utilisée pour vérifier à quel moment une lecture de disque asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="84ae7-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="84ae7-115">Appelez la fonction [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) sur la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) qui lit le streaming audio.</span><span class="sxs-lookup"><span data-stu-id="84ae7-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="84ae7-116">Boucle lorsque la position de lecture actuelle ne reçoit pas la fin du fichier audio.</span><span class="sxs-lookup"><span data-stu-id="84ae7-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="84ae7-117">Dans la boucle, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="84ae7-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="84ae7-118">Lecture d’un segment de données à partir du disque dans la mémoire tampon de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="84ae7-118">Read a chunk of data from the disk into the current read buffer.</span></span>

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  <span data-ttu-id="84ae7-119">Utilisez la fonction **GetOverlappedResult** pour attendre l’événement qui signale que la lecture est terminée.</span><span class="sxs-lookup"><span data-stu-id="84ae7-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="84ae7-120">Attendez que le nombre de mémoires tampons en file d’attente sur la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) soit inférieur au nombre de tampons de lecture.</span><span class="sxs-lookup"><span data-stu-id="84ae7-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="84ae7-121">L’état de la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) est vérifié à l’aide de la fonction [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .</span><span class="sxs-lookup"><span data-stu-id="84ae7-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="84ae7-122">Envoyez la mémoire tampon de lecture actuelle à la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) à l’aide de la fonction [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .</span><span class="sxs-lookup"><span data-stu-id="84ae7-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  <span data-ttu-id="84ae7-123">Définit l’index de la mémoire tampon de lecture en cours sur la mémoire tampon suivante.</span><span class="sxs-lookup"><span data-stu-id="84ae7-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="84ae7-124">Une fois la boucle terminée, attendez la fin de la lecture des tampons mis en file d’attente restants.</span><span class="sxs-lookup"><span data-stu-id="84ae7-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="84ae7-125">Lorsque les mémoires tampons restantes sont terminées, le son s’arrête et le thread peut se fermer ou être réutilisé pour diffuser un autre son.</span><span class="sxs-lookup"><span data-stu-id="84ae7-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="84ae7-126">Création de la classe de rappel</span><span class="sxs-lookup"><span data-stu-id="84ae7-126">Creating the callback class</span></span>

<span data-ttu-id="84ae7-127">Pour créer la classe de rappel, créez une classe qui hérite de l’interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="84ae7-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="84ae7-128">La classe doit définir un événement dans sa méthode [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) .</span><span class="sxs-lookup"><span data-stu-id="84ae7-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="84ae7-129">Cela permet au thread de streaming de se mettre en veille jusqu’à ce que l’événement indique qu’XAudio2 a fini de lire à partir d’une mémoire tampon audio.</span><span class="sxs-lookup"><span data-stu-id="84ae7-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="84ae7-130">Pour plus d’informations sur l’utilisation de rappels avec XAudio2, consultez [Comment : utiliser des rappels vocaux source](how-to--use-source-voice-callbacks.md).</span><span class="sxs-lookup"><span data-stu-id="84ae7-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a><span data-ttu-id="84ae7-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84ae7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84ae7-132">Diffusion en continu de données audio</span><span class="sxs-lookup"><span data-stu-id="84ae7-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="84ae7-133">Rappels XAudio2</span><span class="sxs-lookup"><span data-stu-id="84ae7-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="84ae7-134">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="84ae7-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="84ae7-135">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="84ae7-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="84ae7-136">Procédure : utiliser des rappels de voix source</span><span class="sxs-lookup"><span data-stu-id="84ae7-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
