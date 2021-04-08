---
description: Lorsque vous créez une voix source, vous pouvez lui transmettre une structure qui définit des rappels pour certains événements audio. Vous pouvez utiliser ces rappels pour effectuer des actions ou signaler un autre code.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 'Procédure : utiliser des rappels de voix source'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752421"
---
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="bbf5e-104">Procédure : utiliser des rappels de voix source</span><span class="sxs-lookup"><span data-stu-id="bbf5e-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="bbf5e-105">Lorsque vous créez une voix source, vous pouvez lui transmettre une structure qui définit des rappels pour certains événements audio.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="bbf5e-106">Vous pouvez utiliser ces rappels pour effectuer des actions ou signaler un autre code.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="bbf5e-107">Créez une classe qui hérite de l’interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="bbf5e-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="bbf5e-108">Toutes les fonctions membres de **IXAudio2VoiceCallback** sont purement virtuelles et doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="bbf5e-109">La seule fonction intéressante dans cet exemple est [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span><span class="sxs-lookup"><span data-stu-id="bbf5e-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="bbf5e-110">Par conséquent, les autres fonctions sont des stubs.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="bbf5e-111">La fonction **OnStreamEnd** déclenche un événement qui indique que la diffusion du son est terminée.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  <span data-ttu-id="bbf5e-112">Créez une [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) avec [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) à l’aide d’une instance de la classe de rappel créée précédemment comme paramètre pCallback.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="bbf5e-113">Après avoir démarré la voix, utilisez la méthode [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) pour attendre que l’événement soit déclenché.</span><span class="sxs-lookup"><span data-stu-id="bbf5e-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="bbf5e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbf5e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf5e-115">Rappels</span><span class="sxs-lookup"><span data-stu-id="bbf5e-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="bbf5e-116">Rappels XAudio2</span><span class="sxs-lookup"><span data-stu-id="bbf5e-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="bbf5e-117">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="bbf5e-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="bbf5e-118">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="bbf5e-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="bbf5e-119">Procédure : diffuser un son en continu à partir du disque</span><span class="sxs-lookup"><span data-stu-id="bbf5e-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
