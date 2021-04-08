---
description: Cette rubrique vous montre comment modifier le volume d’une voix au niveau global, à chaque canal de sortie, ou entre chaque canal d’une voix et une autre voix dans son sendlist.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Comment : modifier le volume vocal'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757695"
---
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="4930e-103">Comment : modifier le volume vocal</span><span class="sxs-lookup"><span data-stu-id="4930e-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="4930e-104">Cette rubrique vous montre comment modifier le volume d’une voix au niveau global, à chaque canal de sortie, ou entre chaque canal d’une voix et une autre voix dans son [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="4930e-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="4930e-105">Pour définir un niveau de volume global pour l’entrée de la voix</span><span class="sxs-lookup"><span data-stu-id="4930e-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="4930e-106">Utilisez la fonction [**setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .</span><span class="sxs-lookup"><span data-stu-id="4930e-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="4930e-107">Pour définir le volume des canaux de sortie de la voix</span><span class="sxs-lookup"><span data-stu-id="4930e-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="4930e-108">Créez un tableau de nombres à virgule flottante qui contiennent les volumes souhaités de tous les canaux de sortie de la voix.</span><span class="sxs-lookup"><span data-stu-id="4930e-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="4930e-109">Le tableau aura une entrée pour chaque canal de la voix.</span><span class="sxs-lookup"><span data-stu-id="4930e-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="4930e-110">Utilisez la fonction [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) pour définir le volume des canaux de sortie.</span><span class="sxs-lookup"><span data-stu-id="4930e-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="4930e-111">Pour définir le volume des connexions</span><span class="sxs-lookup"><span data-stu-id="4930e-111">To set the volume of connections</span></span>

<span data-ttu-id="4930e-112">Définissez le volume de connexion entre la voix et une voix dans son [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="4930e-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="4930e-113">Créez un tableau de nombres à virgule flottante qui définit une matrice de sortie si la voix envoie à une autre voix.</span><span class="sxs-lookup"><span data-stu-id="4930e-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="4930e-114">Le tableau doit avoir un nombre d’entrées égal aux canaux vocaux source × canaux vocaux de destination.</span><span class="sxs-lookup"><span data-stu-id="4930e-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="4930e-115">Dans cet exemple, le mappage provient d’une voix avec un canal vers une voix avec deux canaux.</span><span class="sxs-lookup"><span data-stu-id="4930e-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="4930e-116">Utilisez la fonction [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) pour définir la matrice de sortie.</span><span class="sxs-lookup"><span data-stu-id="4930e-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4930e-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4930e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4930e-118">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="4930e-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="4930e-119">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="4930e-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="4930e-120">Contrôle du volume et du tangage XAudio2</span><span class="sxs-lookup"><span data-stu-id="4930e-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
