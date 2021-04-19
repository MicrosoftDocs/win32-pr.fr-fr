---
description: La configuration minimale requise pour permettre à XAudio2 de lire des données audio est un graphique de traitement audio, qui est construit à partir d’une seule voix de mastérisation et d’une seule voix source.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Procédure : créer un graphique de traitement audio de base'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520603"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="c5585-103">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="c5585-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="c5585-104">La configuration minimale requise pour permettre à XAudio2 de lire des données audio est un graphique de traitement audio, qui est construit à partir d’une seule voix de mastérisation et d’une seule voix source.</span><span class="sxs-lookup"><span data-stu-id="c5585-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="c5585-105">Pour générer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="c5585-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="c5585-106">Initialisez le moteur XAudio2 en suivant les étapes décrites dans [How to : Initialize XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="c5585-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="c5585-107">Remplissez une structure de [**\_ mémoire tampon**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEX** et XAUDIO2 en suivant les étapes décrites dans [Comment : charger des fichiers de données audio dans XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="c5585-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="c5585-108">Créez une voix source à l’aide de la fonction [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .</span><span class="sxs-lookup"><span data-stu-id="c5585-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="c5585-109">Lorsque vous spécifiez NULL pour l’argument pSendList de [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), la sortie de la voix source passe à la voix de mastérisation créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="c5585-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="c5585-110">Une fois cette étape terminée, il existe un simple graphique audio qui se compose de la voix source, de la voix de mastérisation et du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="c5585-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="c5585-111">Les étapes restantes de cette rubrique de procédure vous montrent comment démarrer le flux de données audio dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="c5585-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="c5585-112">Graphique audio simple</span><span class="sxs-lookup"><span data-stu-id="c5585-112">A simple audio graph</span></span>

    ![graphique audio simple.](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="c5585-114">Utilisez la fonction [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) pour envoyer une [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) à la voix source.</span><span class="sxs-lookup"><span data-stu-id="c5585-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="c5585-115">Utilisez la fonction [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) pour démarrer la voix source.</span><span class="sxs-lookup"><span data-stu-id="c5585-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c5585-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5585-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5585-117">Graphiques audio</span><span class="sxs-lookup"><span data-stu-id="c5585-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="c5585-118">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="c5585-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
