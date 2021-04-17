---
description: Cette rubrique décrit les étapes minimales requises pour lire des données audio précédemment chargées dans XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Procédure : lire un son avec XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526883"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>Procédure : lire un son avec XAudio2

Cette rubrique décrit les étapes minimales requises pour lire des données audio précédemment chargées dans XAudio2. Après l’initialisation de XAudio2 (voir [Comment : initialiser XAudio2](how-to--initialize-xaudio2.md)) et charger les données audio (voir procédure [: chargement des fichiers de données audio dans XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), vous pouvez lire un son en créant une voix source et en lui transmettant des données audio.

## <a name="to-play-a-sound"></a>Pour émettre un signal sonore

1.  Initialisez le moteur XAudio2 en suivant les étapes décrites dans [How to : Initialize XAudio2](how-to--initialize-xaudio2.md).
2.  Remplissez une structure de [**\_ mémoire tampon**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) et XAUDIO2 en suivant les étapes décrites dans [Comment : charger des fichiers de données audio dans XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
    > [!Note]  
    > Selon le format des données audio, vous devrez peut-être utiliser une plus grande structure de données contenant une structure [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) à la place d’un **WAVEFORMATEX**. Pour plus d’informations, consultez la page de référence de **WAVEFORMATEX** .

     

3.  Créez une voix source en appelant la méthode [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) sur une instance du moteur XAudio2. Le format de la voix est spécifié par les valeurs définies dans une structure [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Soumettez [**une \_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) à la voix source à l’aide de la fonction [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Les exemples de données audio auxquels les points de la *mémoire tampon* sont toujours « détenus » par l’application et qui doivent rester alloués et accessibles jusqu’à ce que le son s’arrête.

     

5.  Utilisez la fonction [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) pour démarrer la voix source. Dans la mesure où toutes les voix XAudio2 envoient leur sortie à la voix de mastérisation par défaut, l’audio de la voix source rend automatiquement le périphérique audio sélectionné lors de l’initialisation. Dans un graphique audio plus complexe, la voix source doit spécifier la voix à laquelle sa sortie doit être envoyée.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Notes pour les applications du Windows Store

Nous vous recommandons d’utiliser un [pointeur intelligent](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) pour gérer la durée de vie des objets XAUDIO2 de façon sécurisée. Pour les applications du Windows Store, vous pouvez utiliser le modèle de pointeur intelligent [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) à partir de la bibliothèque de modèles C++ Windows Runtime (WRL).


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> Assurez-vous que tous les pointeurs intelligents vers les objets XAUDIO2 sont entièrement libérés avant de libérer l’objet [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[XAudio2 Prise en main](getting-started.md)
</dt> <dt>

[Procédure : initialiser XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Procédure : charger des fichiers de données audio dans XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
