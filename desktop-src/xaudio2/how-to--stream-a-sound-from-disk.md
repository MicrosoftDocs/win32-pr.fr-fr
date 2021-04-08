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
# <a name="how-to-stream-a-sound-from-disk"></a>Procédure : diffuser un son en continu à partir du disque

> [!Note]  
> Ce contenu s’applique uniquement aux applications de bureau et nécessite une révision pour fonctionner dans une application Windows Store. Reportez-vous à la documentation de **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)et **GetOverlappedResultEx**. Consultez l’exemple StreamEffect Windows 8 dans la [Galerie d’exemples SDK Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).

 

Vous pouvez diffuser des données audio dans XAudio2 en créant un thread distinct et effectuer des lectures de mémoire tampon des données audio dans le thread de streaming, puis utiliser des rappels pour contrôler ce thread.

-   [Exécution des lectures de mémoire tampon dans le thread de streaming](#performing-buffer-reads-in-the-streaming-thread)
-   [Création de la classe de rappel](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Exécution des lectures de mémoire tampon dans le thread de streaming

Pour effectuer des lectures de mémoire tampon dans le thread de streaming, procédez comme suit :

1.  Créez un tableau de mémoires tampons de lecture.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Initialise une structure OVERLAPPED.

    La structure est utilisée pour vérifier à quel moment une lecture de disque asynchrone est terminée.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Appelez la fonction [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) sur la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) qui lit le streaming audio.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Boucle lorsque la position de lecture actuelle ne reçoit pas la fin du fichier audio.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    Dans la boucle, procédez comme suit :

    1.  Lecture d’un segment de données à partir du disque dans la mémoire tampon de lecture actuelle.

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

        

    2.  Utilisez la fonction **GetOverlappedResult** pour attendre l’événement qui signale que la lecture est terminée.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Attendez que le nombre de mémoires tampons en file d’attente sur la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) soit inférieur au nombre de tampons de lecture.

        L’état de la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) est vérifié à l’aide de la fonction [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Envoyez la mémoire tampon de lecture actuelle à la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) à l’aide de la fonction [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .

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

        

    5.  Définit l’index de la mémoire tampon de lecture en cours sur la mémoire tampon suivante.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  Une fois la boucle terminée, attendez la fin de la lecture des tampons mis en file d’attente restants.

    Lorsque les mémoires tampons restantes sont terminées, le son s’arrête et le thread peut se fermer ou être réutilisé pour diffuser un autre son.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Création de la classe de rappel

Pour créer la classe de rappel, créez une classe qui hérite de l’interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .

La classe doit définir un événement dans sa méthode [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) . Cela permet au thread de streaming de se mettre en veille jusqu’à ce que l’événement indique qu’XAudio2 a fini de lire à partir d’une mémoire tampon audio. Pour plus d’informations sur l’utilisation de rappels avec XAudio2, consultez [Comment : utiliser des rappels vocaux source](how-to--use-source-voice-callbacks.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Diffusion en continu de données audio](streaming-audio-data.md)
</dt> <dt>

[Rappels XAudio2](callbacks.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procédure : utiliser des rappels de voix source](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
