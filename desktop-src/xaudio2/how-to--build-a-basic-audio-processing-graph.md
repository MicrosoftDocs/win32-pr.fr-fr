---
description: La configuration minimale requise pour permettre à XAudio2 de lire des données audio est un graphique de traitement audio, qui est construit à partir d’une seule voix de mastérisation et d’une seule voix source.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Procédure : créer un graphique de traitement audio de base'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bab39c878b37a6f89ef7598f6fa6b6eb1a997654373122fe3c3980bf12f160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082957"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>Procédure : créer un graphique de traitement audio de base

La configuration minimale requise pour permettre à XAudio2 de lire des données audio est un graphique de traitement audio, qui est construit à partir d’une seule voix de mastérisation et d’une seule voix source.

## <a name="to-build-a-basic-audio-processing-graph"></a>Pour générer un graphique de traitement audio de base

1.  Initialisez le moteur XAudio2 en suivant les étapes décrites dans [How to : Initialize XAudio2](how-to--initialize-xaudio2.md).
2.  Remplissez une structure de [**\_ mémoire tampon**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEX** et XAUDIO2 en suivant les étapes décrites dans [Comment : charger des fichiers de données audio dans XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
3.  Créez une voix source à l’aide de la fonction [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

    Lorsque vous spécifiez NULL pour l’argument pSendList de [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), la sortie de la voix source passe à la voix de mastérisation créée à l’étape 1.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Une fois cette étape terminée, il existe un simple graphique audio qui se compose de la voix source, de la voix de mastérisation et du périphérique audio. Les étapes restantes de cette rubrique de procédure vous montrent comment démarrer le flux de données audio dans le graphique.

    Graphique audio simple

    ![graphique audio simple.](images/xaudio2-audio-graph.png)

4.  Utilisez la fonction [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) pour envoyer une [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) à la voix source.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Utilisez la fonction [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) pour démarrer la voix source.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Graphiques audio](audio-graphs.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> </dl>

 

 
