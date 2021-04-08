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
# <a name="how-to-use-source-voice-callbacks"></a>Procédure : utiliser des rappels de voix source

Lorsque vous créez une voix source, vous pouvez lui transmettre une structure qui définit des rappels pour certains événements audio. Vous pouvez utiliser ces rappels pour effectuer des actions ou signaler un autre code.

1.  Créez une classe qui hérite de l’interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) . Toutes les fonctions membres de **IXAudio2VoiceCallback** sont purement virtuelles et doivent être définies. La seule fonction intéressante dans cet exemple est [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend). Par conséquent, les autres fonctions sont des stubs. La fonction **OnStreamEnd** déclenche un événement qui indique que la diffusion du son est terminée.

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

    

2.  Créez une [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) avec [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) à l’aide d’une instance de la classe de rappel créée précédemment comme paramètre pCallback.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  Après avoir démarré la voix, utilisez la méthode [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) pour attendre que l’événement soit déclenché.

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rappels](callbacks.md)
</dt> <dt>

[Rappels XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procédure : diffuser un son en continu à partir du disque](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
